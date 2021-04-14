---
description: Шаг 3. повторное использование компонентов
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: Шаг 3. повторное использование компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561618"
---
# <a name="step-3-reusing-components"></a><span data-ttu-id="7d47a-103">Шаг 3. повторное использование компонентов</span><span class="sxs-lookup"><span data-stu-id="7d47a-103">Step 3: Reusing Components</span></span>

## <a name="objectives"></a><span data-ttu-id="7d47a-104">Задачи</span><span class="sxs-lookup"><span data-stu-id="7d47a-104">Objectives</span></span>

<span data-ttu-id="7d47a-105">На этом шаге вы узнаете о следующих возможностях:</span><span class="sxs-lookup"><span data-stu-id="7d47a-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="7d47a-106">Многократно используемые компоненты.</span><span class="sxs-lookup"><span data-stu-id="7d47a-106">Reusable components.</span></span>
-   <span data-ttu-id="7d47a-107">Планирование повторного использования.</span><span class="sxs-lookup"><span data-stu-id="7d47a-107">How to plan for reusability.</span></span>

## <a name="description"></a><span data-ttu-id="7d47a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7d47a-108">Description</span></span>

<span data-ttu-id="7d47a-109">Две предыдущие части этого учебника по службам COM+, [Шаг 1. Создание транзакционного компонента](step-1--creating-a-transactional-component.md) и [Шаг 2. расширение транзакции для нескольких компонентов](step-2--extending-a-transaction-across-multiple-components.md) показывает, как написать один компонент, вызывающий второй компонент для выполнения некоторой работы, обновляя сведения об авторе в Microsoft SQL Server базе данных Pubs; Вся работа защищена одной транзакцией.</span><span class="sxs-lookup"><span data-stu-id="7d47a-109">Two previous parts of this COM+ services primer, [Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) and [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md) show how to write one component that calls a second component to assist in completing some work, updating author information in the Microsoft SQL Server Pubs database; all work is protected by a single transaction.</span></span> <span data-ttu-id="7d47a-110">Примеры компонентов зависят от работы по обновлению данных автора и проверке адреса автора, а также от COM+, обеспечивающего обработку транзакций, [JIT-активацию](com--just-in-time-activation.md)и [защиту параллелизма](com--synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="7d47a-110">The sample components focused on the work of updating an author's data and verifying the author's address, and COM+ provided transaction processing, [JIT activation](com--just-in-time-activation.md), and [concurrency protection](com--synchronization.md).</span></span>

<span data-ttu-id="7d47a-111">На этом шаге демонстрируется повторное использование компонентов, созданных в шагах 1 и 2, и рассматривается структура этих компонентов.</span><span class="sxs-lookup"><span data-stu-id="7d47a-111">This step demonstrates how to reuse the components created in steps 1 and 2 and looks at what this means to the design of those components.</span></span> <span data-ttu-id="7d47a-112">Как показано на следующем рисунке, это означает создание нового компонента, `AddNewAuthor` который добавляет новых авторов в базу данных путем вызова `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="7d47a-112">As shown in the following illustration, this means creating a new component, `AddNewAuthor`, that adds new authors to the database by calling `UpdateAuthorAddress`.</span></span>

![Схема, показывающая последовательность при повторном использовании компонентов.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

<span data-ttu-id="7d47a-114">В дополнение к повторному использованию существующих функций компонента `AddNewAuthor` вызывается другой новый компонент с именем `ValidateAuthorName` .</span><span class="sxs-lookup"><span data-stu-id="7d47a-114">In addition to reusing existing component functionality, `AddNewAuthor` calls another new component called `ValidateAuthorName`.</span></span> <span data-ttu-id="7d47a-115">Как показано на предыдущем рисунке, `ValidateAuthorName` является нетранзакционным.</span><span class="sxs-lookup"><span data-stu-id="7d47a-115">As the preceding illustration shows, `ValidateAuthorName` is non-transactional.</span></span> <span data-ttu-id="7d47a-116">Значение атрибута транзакции для этого компонента оставлено по умолчанию (**не поддерживается**), чтобы исключить свою работу из транзакции.</span><span class="sxs-lookup"><span data-stu-id="7d47a-116">The transaction attribute value for this component is left at its default setting (**Not Supported**) to exclude its work from the transaction.</span></span> <span data-ttu-id="7d47a-117">Как показано в примере кода Step 3, `ValidateAuthorName` выполняет запросы только для чтения к базе данных, и сбой этой дополнительной задачи не должен иметь возможности прерывать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7d47a-117">As shown in the step 3 sample code, `ValidateAuthorName` performs read-only queries on the database, and the failure of this minor task should not have the potential to abort the transaction.</span></span> <span data-ttu-id="7d47a-118">Однако значение атрибута транзакции `AddNewAuthor` для компонента задается как **Обязательное**.</span><span class="sxs-lookup"><span data-stu-id="7d47a-118">However, the transaction attribute value of the `AddNewAuthor` component is set to **Required**.</span></span>

<span data-ttu-id="7d47a-119">`AddNewAuthor`Компоненты, `UpdateAuthorAddress` и `ValidateAuthorAddress` проголосуют за транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7d47a-119">The `AddNewAuthor`, `UpdateAuthorAddress`, and `ValidateAuthorAddress` components all vote in the transaction.</span></span> <span data-ttu-id="7d47a-120">В этой транзакции `AddNewAuthor` это корневой объект.</span><span class="sxs-lookup"><span data-stu-id="7d47a-120">In this transaction, `AddNewAuthor` is the root object.</span></span> <span data-ttu-id="7d47a-121">COM+ всегда делает первый объект, созданный в транзакции, корневым объектом.</span><span class="sxs-lookup"><span data-stu-id="7d47a-121">COM+ always makes the first object created in the transaction the root object.</span></span>

<span data-ttu-id="7d47a-122">В этом примере повторное использование `UpdateAuthorAddress` компонента — это просто — com + автоматически доставляет ожидаемые службы.</span><span class="sxs-lookup"><span data-stu-id="7d47a-122">In this example, reusing the `UpdateAuthorAddress` component is easy—COM+ automatically delivers the expected services.</span></span> <span data-ttu-id="7d47a-123">Однако результаты будут отличаться, если значение атрибута транзакции `UpdateAuthorAddress` для компонента изначально задается вместо **обязательно**. </span><span class="sxs-lookup"><span data-stu-id="7d47a-123">However, the results would be different if the transaction attribute value of the `UpdateAuthorAddress` component were initially set to **Requires New** instead of **Required**.</span></span> <span data-ttu-id="7d47a-124">На поверхности эти параметры выглядят одинаково. Обе гарантируют транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7d47a-124">On the surface, both settings appear similar; both guarantee a transaction.</span></span> <span data-ttu-id="7d47a-125">**, Однако**, обязательно запускает новую транзакцию, а при **необходимости** запускает новую транзакцию только в том случае, если вызывающий объект не является транзакционным.</span><span class="sxs-lookup"><span data-stu-id="7d47a-125">**Requires New**, however, always starts a new transaction, while **Required** starts a new transaction only when the object's caller is non-transactional.</span></span> <span data-ttu-id="7d47a-126">Вы видите, насколько важно `UpdateAuthorAddress` тщательно и продуманная Настройка.</span><span class="sxs-lookup"><span data-stu-id="7d47a-126">You can see from this how important it was to configure `UpdateAuthorAddress` carefully and thoughtfully.</span></span> <span data-ttu-id="7d47a-127">В противном случае COM+ мог интерпретировать запрос на обслуживание по-другому, создавая две несвязанные транзакции, как показано на следующем рисунке, а не на одном.</span><span class="sxs-lookup"><span data-stu-id="7d47a-127">Otherwise, COM+ might have interpreted the service request differently, generating two unrelated transactions, as shown in the following illustration, instead of one.</span></span>

![Схема, показывающая последовательность при повторном использовании компонентов с "требуется создать".](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> <span data-ttu-id="7d47a-129">При повторном использовании компонентов убедитесь, что службы настроены для поддержки желаемого результата.</span><span class="sxs-lookup"><span data-stu-id="7d47a-129">When you reuse components, make sure the services are configured to support your desired outcome.</span></span>

 

## <a name="sample-code"></a><span data-ttu-id="7d47a-130">Пример кода</span><span class="sxs-lookup"><span data-stu-id="7d47a-130">Sample code</span></span>

<span data-ttu-id="7d47a-131">Компонент Аддневаусор выполняет пакетное Добавление новых авторов, позволяя объекту оставаться активным до тех пор, пока клиент не освободит ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="7d47a-131">The AddNewAuthor component performs batch additions of new authors by allowing the object to remain active until the client releases its reference to the object.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



<span data-ttu-id="7d47a-132">`ValidateAuthorName`Компонент проверяет имена авторов перед `AddNewAuthor` добавлением имени в базу данных.</span><span class="sxs-lookup"><span data-stu-id="7d47a-132">The `ValidateAuthorName` component validates author names before `AddNewAuthor` adds the name to the database.</span></span> <span data-ttu-id="7d47a-133">Этот компонент выдает ошибку обратно вызывающему объекту в случае возникновения непредвиденных событий.</span><span class="sxs-lookup"><span data-stu-id="7d47a-133">This component throws an error back to its caller if something unexpected happens.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a><span data-ttu-id="7d47a-134">Сводка</span><span class="sxs-lookup"><span data-stu-id="7d47a-134">Summary</span></span>

-   <span data-ttu-id="7d47a-135">Иногда не нужно, чтобы компонент проголосовать за транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7d47a-135">There are times when you don't want a component to vote in the transaction.</span></span>
-   <span data-ttu-id="7d47a-136">COM+ не применяет принудительную активацию или защиту параллелизма для нетранзакционных компонентов.</span><span class="sxs-lookup"><span data-stu-id="7d47a-136">COM+ does not enforce JIT activation or concurrency protection on non-transactional components.</span></span> <span data-ttu-id="7d47a-137">Эти службы можно настроить отдельно.</span><span class="sxs-lookup"><span data-stu-id="7d47a-137">You may configure these services separately.</span></span>
-   <span data-ttu-id="7d47a-138">Конфигурация вызывающего компонента влияет на то, как COM+ интерпретирует запросы на обслуживание вызванного компонента.</span><span class="sxs-lookup"><span data-stu-id="7d47a-138">A calling component's configuration affects how COM+ interprets the service requests of the called component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d47a-139">См. также</span><span class="sxs-lookup"><span data-stu-id="7d47a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d47a-140">Шаг 1. Создание транзакционного компонента</span><span class="sxs-lookup"><span data-stu-id="7d47a-140">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="7d47a-141">Шаг 2. расширение транзакции для нескольких компонентов</span><span class="sxs-lookup"><span data-stu-id="7d47a-141">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="7d47a-142">Настройка транзакций</span><span class="sxs-lookup"><span data-stu-id="7d47a-142">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="7d47a-143">Проектирование для масштабируемости</span><span class="sxs-lookup"><span data-stu-id="7d47a-143">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> </dl>

 

 



