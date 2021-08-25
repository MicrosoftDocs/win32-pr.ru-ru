---
description: Использование сценариев бизнес-правил в скрипте для обеспечения логики времени выполнения для проверки доступа.
ms.assetid: 10c28ecb-3f36-45a8-b037-7038e8927b6b
title: Уточнение доступа с помощью бизнес-логики в скрипте
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b77ff1d6d520780d30efab5619c3e9bc3c896ad88315fba56e3a19e05d3ae97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907554"
---
# <a name="qualifying-access-with-business-logic-in-script"></a>Уточнение доступа с помощью бизнес-логики в скрипте

Используйте сценарии бизнес-правил для предоставления логики времени выполнения для проверки доступа. Дополнительные сведения о бизнес-правилах см. в разделе [бизнес-правила](business-rules.md).

Чтобы назначить бизнес-правило задаче, сначала установите свойство [**бизрулелангуаже**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) объекта [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) , представляющего задачу. скрипт должен быть написан с помощью языка программирования Visual Basic scripting Edition (VBScript) или JScript программного обеспечения разработки. После указания языка скрипта задайте для свойства [**бизруле**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) объекта **иазтаск** строковое представление скрипта.

При проверке доступа для операции, содержащейся в задаче, имеющей связанное бизнес-правило, приложение должно создать два массива того же размера, которые будут переданы в качестве параметров *варпараметернамес* и *варпараметервалуес* метода [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) . Сведения о создании контекста клиента см. в разделе [Установка контекста клиента в скрипте](establishing-a-client-context-in-script.md).

Метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) создает объект [**азбизрулеконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) , который передается в скрипт бизнес-правила. Затем скрипт задает свойство [**бусинессрулересулт**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) объекта **азбизрулеконтекст** . Значение **true** указывает, что доступ предоставляется, а значение **false** указывает на то, что доступ запрещен.

Не удается назначить скрипт бизнес-правил объекту [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) , содержащемуся в делегированном объекте [**иазскопе**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .

В следующем примере показано, как использовать сценарий бизнес-правила для проверки доступа клиента к операции. В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C и что это хранилище содержит приложение с именем "расходы", задачу с именем "Отправить расходы" и операцию с именем Усеформконтрол.


```VB
<%@ Language=VBScript %>
<%
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 0, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp = AzManStore.OpenApplication("Expense")

'  Create a client context.
Dim clientName
clientName = Request.ServerVariables("LOGON_USER")
Dim clientContext
Set clientContext = _
    expenseApp.InitializeClientContextFromName(clientName)

'  Create a business rule for the Submit Expense task.

'  Open the Submit Expense task.
Dim submitTask
Set submitTask = expenseApp.OpenTask("Submit Expense")

'  Set the business rule language to VBScript.
submitTask.BizRuleLanguage = "VBScript"

'  Create a string with the business rule code.
Dim newline
newline = chr(13)
Dim bizRuleString
bizRuleString = "Dim Amount" + newline _
         +"AzBizRuleContext.BusinessRuleResult = FALSE" + newline _
         +"Amount = AzBizRuleContext.GetParameter(""ExpAmount"")" _
   +newline _
   +"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"

'  Assign the business rule to the Submit Expense task.
submitTask.BizRule = bizRuleString
                
'  Save the task information to the store.
submitTask.Submit

'  Open the operation to check.
Dim formOperation
Set formOperation = expenseApp.OpenOperation("UseFormControl")

'  Get the ID of the operation.
Dim operationID
operationID = formOperation.OperationID

'  Set up arrays for operations and results.
Dim Operations(1)
Operations(0) = operationID
Dim Results

'  Set up business rule parameters.
Dim bizNames(1)
Dim bizValues(1)
bizNames(0) = "ExpAmount"
bizValues(0) = 100

'  Check access.
Results = clientContext.AccessCheck _
    ("UseFormControl", Empty, Operations, bizNames, bizValues)
 
%>
```



 

 



