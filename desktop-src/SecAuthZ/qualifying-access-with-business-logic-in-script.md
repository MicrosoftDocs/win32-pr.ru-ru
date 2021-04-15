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
ms.openlocfilehash: 65ee69e0572c0f480cded2930ea81ac6da710b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662573"
---
# <a name="qualifying-access-with-business-logic-in-script"></a><span data-ttu-id="22982-103">Уточнение доступа с помощью бизнес-логики в скрипте</span><span class="sxs-lookup"><span data-stu-id="22982-103">Qualifying Access with Business Logic in Script</span></span>

<span data-ttu-id="22982-104">Используйте сценарии бизнес-правил для предоставления логики времени выполнения для проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="22982-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="22982-105">Дополнительные сведения о бизнес-правилах см. в разделе [бизнес-правила](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="22982-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="22982-106">Чтобы назначить бизнес-правило задаче, сначала установите свойство [**бизрулелангуаже**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) объекта [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) , представляющего задачу.</span><span class="sxs-lookup"><span data-stu-id="22982-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="22982-107">Скрипт должен быть написан с помощью языка программирования Visual Basic Scripting Edition (VBScript) или программного обеспечения для разработки на JScript.</span><span class="sxs-lookup"><span data-stu-id="22982-107">The script must be written using the Visual Basic Scripting Edition (VBScript) programming language or JScript development software.</span></span> <span data-ttu-id="22982-108">После указания языка скрипта задайте для свойства [**бизруле**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) объекта **иазтаск** строковое представление скрипта.</span><span class="sxs-lookup"><span data-stu-id="22982-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="22982-109">При проверке доступа для операции, содержащейся в задаче, имеющей связанное бизнес-правило, приложение должно создать два массива того же размера, которые будут переданы в качестве параметров *варпараметернамес* и *варпараметервалуес* метода [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) объекта [**иазклиентконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) .</span><span class="sxs-lookup"><span data-stu-id="22982-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method of an [**IAzClientContext**](/windows/desktop/api/Azroles/nn-azroles-iazclientcontext) object.</span></span> <span data-ttu-id="22982-110">Сведения о создании контекста клиента см. в разделе [Установка контекста клиента в скрипте](establishing-a-client-context-in-script.md).</span><span class="sxs-lookup"><span data-stu-id="22982-110">For information about creating a client context, see [Establishing a Client Context in Script](establishing-a-client-context-in-script.md).</span></span>

<span data-ttu-id="22982-111">Метод [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) создает объект [**азбизрулеконтекст**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) , который передается в скрипт бизнес-правила.</span><span class="sxs-lookup"><span data-stu-id="22982-111">The [**AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="22982-112">Затем скрипт задает свойство [**бусинессрулересулт**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) объекта **азбизрулеконтекст** .</span><span class="sxs-lookup"><span data-stu-id="22982-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="22982-113">Значение **true** указывает, что доступ предоставляется, а значение **false** указывает на то, что доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="22982-113">A value of **True** indicates that access is granted, and a value of **False** indicates that access is denied.</span></span>

<span data-ttu-id="22982-114">Не удается назначить скрипт бизнес-правил объекту [**иазтаск**](/windows/desktop/api/Azroles/nn-azroles-iaztask) , содержащемуся в делегированном объекте [**иазскопе**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="22982-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="22982-115">В следующем примере показано, как использовать сценарий бизнес-правила для проверки доступа клиента к операции.</span><span class="sxs-lookup"><span data-stu-id="22982-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="22982-116">В этом примере предполагается, что существует хранилище политик XML с именем MyStore.xml в корневом каталоге диска C и что это хранилище содержит приложение с именем "расходы", задачу с именем "Отправить расходы" и операцию с именем Усеформконтрол.</span><span class="sxs-lookup"><span data-stu-id="22982-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, and that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl.</span></span>


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



 

 



