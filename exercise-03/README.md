# Exercise 03 - Backoffice Framework Extension 
## Expected Duration - 30 Minutes

For this exercise we are going create a new Backoffice extension and a widget


## Create & Install the Backoffice extension

We now want to create a new extenstion

1. Run `ant extgen`, choose `ybackoffice` as template, name `mybackoffice`, package `org.officeco`
2. Accept all default options (including `sample widget`)
3. Browse the folders, you will notice a new extension called `mybackoffice` in the folder `custom`
4. We now have to add our new addon to `config/localextensions.xml`
5. Add the following block to the file

```xml
 <!-- Your new extension -->
 <extension name="mybackoffice"/>  
```
6. Remove `ybackoffice` template from `localextensions.xml`
7. Run `ant clean all`
8. You should now see your new backoffice extenstion in list of available cockpits
9. Look at the sample widget, modify and experiement


## Create a new widget

We now want to create a new widget

10. In `mybackoffice/backoffice/resources/widgets` directory create a new folder called `mychat`
    
## Widget Definition
1.  Create a file `definition.xml`
2.  Add the the following contents

```
<?xml version="1.0" encoding="UTF-8" standalone="yes" ?>
 
<widget-definition id="org.myextension.widgets.mychat" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://www.hybris.com/schema/cockpitng/widget-definition.xsd">
	<name>My Chat</name>
	<description>My chat widget.</description>

	<sockets>
		<input type="java.lang.String" id="incomingMsg"/>
		<output type="java.lang.String" id="outgoingMsg"/>
	</sockets>
	
	<keywords>
		<keyword>Chat</keyword>
	</keywords>
	
</widget-definition>

``` 

## Widget View 
13. Create a ZUL view file called `mychat.zul`
14. Add button, text box etc. 

```
<?xml version="1.0" encoding="UTF-8" standalone="yes" ?>

<widget xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://www.zkoss.org/2005/zul">
	<div>
		<textbox id="msgInput"/>
		<button id="sendBtn" label="Send"/>
	</div>
	<div>
		<label id="lastMsgLabel" value="No message."></label>
	</div>
</widget>
```

## Controller
13. In the `mybackoffice/backoffice/src/org/mybackoffice` directory, create a controller with the following package name: `org.officeco.widgets.mychat`. It should extend the DefaultWidgetController. Call it MyChatController


```
public class MyChatController extends DefaultWidgetController
{
	private Label lastMsgLabel;
	private Textbox msgInput;

	@ViewEvent(componentID = "sendBtn", eventName = Events.ON_CLICK)
	public void sendMsg()
	{
		sendOutput("outgoingMsg", msgInput.getText());

	}

	@SocketEvent(socketId = "incomingMsg")
	public void updateTranscript(final String msg)
	{
		lastMsgLabel.setValue(msg);
	}
}
```

14. Add the controller class to the widget definition

```
<!-- ... -->
   <controller class="org.officeco.widgets.mychat.MyChatController"/>
<!-- ... -->
</widget-definition>
```
15. Run `ant clean all`

# Add widget to the application
16. Using the Application Orchestrator mode, add two copies of your newly created chat widget inside a layout that allows multiple widgets.


