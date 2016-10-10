---
title: "Receive Activity Designer"
ms.custom: na
ms.date: 10/02/2016
ms.prod: .net-framework-4.6
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: f58d3c70-944d-4bb4-90a7-e68c103caddc
caps.latest.revision: 8
manager: erikre
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# Receive Activity Designer
The **Receive** activity designer is used to create and configure a <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity. A <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity is an activity that receives a message that can be either a built-in type such as <xref:System.ServiceModel.Channels.Message?qualifyHint=False>, <xref:System.IO.Stream?qualifyHint=False> or <xref:System.Xml.Linq.XElement?qualifyHint=False>, or an application-defined data contract, message contract, or XML class that can be serialized.  
  
## The Receive Activity  
 The <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity can receive a single item or multiple items depending on the type of receive content used. A <xref:System.ServiceModel.Activities.SendReply?qualifyHint=False> activity can be bound to a <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity that receives a message as part of a request/response message exchange pattern on the service.  
  
### Using the Receive Activity Designer  
 The **Receive** activity designer can be found in the **Messaging** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab on the Workflow Designer (Alternatively, select **Toolbar** from the **View** menu or CTRL+ALT+X.)  
  
 The **Receive** activity designer can be dragged from the **Toolbox** and dropped on to the Workflow Designer surface wherever activities are usually placed. This creates a <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity with a default <xref:System.Activities.Activity.DisplayName?qualifyHint=False> of Receive. The <xref:System.Activities.Activity.DisplayName?qualifyHint=False> can be edited in the header of the **Receive** activity designer or in the **DisplayName** box of the property grid.  
  
 To create a <xref:System.ServiceModel.Activities.SendReply?qualifyHint=False> activity and bind it to the selected <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity, right-click the **Receive** activity designer, click the **Create SendReply** item in the context menu and the **SendReplyToReceive** designer appears below the **Receive** designer. The <xref:System.ServiceModel.Activities.SendReply?qualifyHint=False> activity is an activity that sends the reply message as part of a request/response message exchange pattern on the service. It can be configured with the **SendReplyToReceive** designer.  
  
 Alternatively, the **ReceiveAndSendReply** template designer in the **Messaging** category of the **Toolbox** can be used to create a pair of pre-configured <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> and <xref:System.ServiceModel.Activities.SendReply?qualifyHint=False> activity. For more information about the use of the **ReceiveAndSendReply** and **SendReplyToReceive** template, see the [ReceiveAndSendReply](../WF_Design/ReceiveAndSendReply-Template-Designer.md) topic.  
  
### The Receive Activity Properties  
 The following table shows the <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> properties and describes how they are used in the designer. These properties can be edited in properties grid or on the Workflow Designer surface. The only required property is the <xref:System.ServiceModel.Activities.Receive.OperationName?qualifyHint=False> property.  
  
|Property Name|Required|Usage|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName?qualifyHint=False>|False|Specifies the friendly name of the <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity. The default value is Receive.<br /><br /> Although the use of a non-default value for the friendly <xref:System.Activities.Activity.DisplayName?qualifyHint=False> is not strictly required, it is a best practice to use such a value.|  
|<xref:System.ServiceModel.Activities.Receive.OperationName?qualifyHint=False>|True|Specifies the name of the service operation implemented by this <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity. This property is used to construct the default value for the **Action** property if the **Action** property is not explicitly set.|  
|<xref:System.ServiceModel.Activities.Receive.ServiceContractName?qualifyHint=False>|False|Specifies the name of the service contract. This property is used to group service operations into individual service contracts. All <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activities that have the same <xref:System.ServiceModel.Activities.Receive.ServiceContractName?qualifyHint=False> are grouped into the same service contract (WSDL Port Type). The default value is the fully-qualified CLR name of the top level (root) activity.|  
|<xref:System.ServiceModel.Activities.Receive.Content?qualifyHint=False>|False|Specifies the message or parameter content to receive. It can be either a <xref:System.ServiceModel.Activities.ReceiveMessageContent?qualifyHint=False> activity or a <xref:System.ServiceModel.Activities.ReceiveParametersContent?qualifyHint=False> activity. Edit this property by clicking the ellipse button beside the **Content** field in property grid or clicking the **Define…** button beside the **Content** label on the **Receive** activity designer surface. Both display the **Content Definition** dialog. For more information about how to use this box, see the [Content Definition Dialog Box](../WF_Design/Content-Definition-Dialog-Box.md) topic.|  
|<xref:System.ServiceModel.Activities.Receive.CorrelatesOn?qualifyHint=False>|False|Specifies the correlations between <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activities in service operations of a workflow with a <xref:System.ServiceModel.MessageQuerySet?qualifyHint=False> object. Click the ellipsis button next to the <xref:System.ServiceModel.Activities.Receive.CorrelatesOn?qualifyHint=False> property in the properties grid to open the **CorrelatesOn Definition** dialog box. For more information about the use of this dialog box, see the [Content Definition Dialog Box](../WF_Design/Content-Definition-Dialog-Box.md) topic.|  
|<xref:System.ServiceModel.Activities.Receive.CorrelatesWith?qualifyHint=False>|False|Specifies the <xref:System.ServiceModel.Activities.CorrelationHandle?qualifyHint=False> used to route the message to the appropriate workflow instance.<br /><br /> Click the ellipsis button next to the <xref:System.ServiceModel.Activities.Receive.CorrelatesWith?qualifyHint=False> property in the properties grid to open the **Expression Editor** dialog box. For more information about the use of this dialog box, see the [How to: Use the Expression Editor](../WF_Design/How-to--Use-the-Expression-Editor.md) topic.|  
|<xref:System.ServiceModel.Activities.Receive.CorrelationInitializers?qualifyHint=False>|False|Specifies the collection of <xref:System.ServiceModel.Activities.CorrelationInitializer?qualifyHint=False> objects that initialize multiple <xref:System.ServiceModel.Activities.CorrelationHandle?qualifyHint=False> objects that configure this <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity within the workflow. Click the ellipsis button next to the <xref:System.ServiceModel.Activities.Receive.CorrelationInitializers?qualifyHint=False> property in the properties grid to open the **Add Correlation Initializers** dialog box. For more information about using this box, see the [Add CorrelationInitializers Dialog Box](../WF_Design/Add-CorrelationInitializers-Dialog-Box.md) topic.|  
|<xref:System.ServiceModel.Activities.Receive.CanCreateInstance?qualifyHint=False>|False|Specifies a value that determines whether a new workflow instance is created to process the message if the message does not correlate to an existing workflow instance. If the value is set to **true**, a new workflow instance is created to process the message when the message is not correlated with an existing workflow instance.|  
|<xref:System.ServiceModel.Activities.Receive.KnownTypes?qualifyHint=False>|False|Specifies a collection of known types for the service operation implemented by this <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity. This property should be used in conjunction with the <xref:System.ServiceModel.Activities.Receive.SerializerOption?qualifyHint=False> property set to <xref:System.Runtime.Serialization.DataContractSerializer?qualifyHint=False>. It is ignored if <xref:System.Xml.Serialization.XmlSerializer?qualifyHint=False> is used.<br /><br /> Click the ellipse button beside the **KnownTypes** field in property grid to display the **Type Collection Editor** dialog box with which you can add relevant types. For more information about using this box, see the [Type Collection Editor Dialog Box](../WF_Design/Type-Collection-Editor-Dialog-Box.md) topic.|  
|<xref:System.ServiceModel.Activities.Receive.ProtectionLevel?qualifyHint=False>|False|Specifies the <xref:System.Net.Security.ProtectionLevel?qualifyHint=False> for the message.<br /><br /> 1.  <xref:System.Net.Security.ProtectionLevel?qualifyHint=False> means authentication only.<br />2.  <xref:System.Net.Security.ProtectionLevel?qualifyHint=False> means sign data to help ensure the integrity of transmitted data.<br />3.  <xref:System.Net.Security.ProtectionLevel?qualifyHint=False> means encrypt and sign data to help ensure the confidentiality and integrity of transmitted data.|  
|<xref:System.ServiceModel.Activities.Receive.SerializerOption?qualifyHint=False>|False|Specifies the type of serializer to use for the service operation implemented by the <xref:System.ServiceModel.Activities.Receive?qualifyHint=False> activity. The default value is <xref:System.Runtime.Serialization.DataContractSerializer?qualifyHint=False>, which serializes and deserializes an instance of a type into an XML stream or document that uses a supplied data contract. The <xref:System.Xml.Serialization.XmlSerializer?qualifyHint=False> can also be used if more control is required over the XML.|  
|<xref:System.ServiceModel.Activities.Receive.Action?qualifyHint=False>|False|Specifies the action header of the message. If it is not explicitly set, its value defaults to: https://tempuri.org/{service contract namespace}/{service contract name}/{operation name}.|  
  
## See Also  
 [InitializeCorrelation](../WF_Design/InitializeCorrelation-Activity-Designer.md)   
 [CorrelationScope](../WF_Design/CorrelationScope-Activity-Designer.md)   
 [ReceiveAndSendReply](../WF_Design/ReceiveAndSendReply-Template-Designer.md)   
 [Send](../WF_Design/Send-Activity-Designer.md)   
 [SendAndReceiveReply](../WF_Design/SendAndReceiveReply-Template-Designer.md)   
 [TransactedReceiveScope](../WF_Design/TransactedReceiveScope-Activity-Designer.md)