---
description: Шаг 1. Создание транзакционного компонента
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: Шаг 1. Создание транзакционного компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350932"
---
# <a name="step-1-creating-a-transactional-component"></a><span data-ttu-id="6d7bf-103">Шаг 1. Создание транзакционного компонента</span><span class="sxs-lookup"><span data-stu-id="6d7bf-103">Step 1: Creating a Transactional Component</span></span>

## <a name="objectives"></a><span data-ttu-id="6d7bf-104">Задачи</span><span class="sxs-lookup"><span data-stu-id="6d7bf-104">Objectives</span></span>

<span data-ttu-id="6d7bf-105">На этом шаге вы узнаете следующее:</span><span class="sxs-lookup"><span data-stu-id="6d7bf-105">In this step, you will learn the following:</span></span>

-   <span data-ttu-id="6d7bf-106">Написание транзакционного компонента в Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6d7bf-106">How to write a transactional component in Microsoft Visual Basic</span></span>
-   <span data-ttu-id="6d7bf-107">Параметры по умолчанию для служб COM+</span><span class="sxs-lookup"><span data-stu-id="6d7bf-107">What the default settings for COM+ services are</span></span>
-   <span data-ttu-id="6d7bf-108">Настройка служб COM+</span><span class="sxs-lookup"><span data-stu-id="6d7bf-108">How to configure COM+ services</span></span>

## <a name="description"></a><span data-ttu-id="6d7bf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6d7bf-109">Description</span></span>

<span data-ttu-id="6d7bf-110">Компонент Упдатеаусораддресс, создаваемый в этом разделе, обновляет адрес существующего автора в базе данных Pubs.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-110">The UpdateAuthorAddress component, the component to be created in this section, updates the address of an existing author in the Pubs database.</span></span> <span data-ttu-id="6d7bf-111">База данных Pubs — это образец базы данных, который поставляется с Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-111">The Pubs database is a sample database that ships with Microsoft SQL Server.</span></span> <span data-ttu-id="6d7bf-112">Он содержит сведения о публикации, такие как имена авторов, адреса и названия книг.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-112">It contains publishing information such as author names, addresses, and book titles.</span></span>

> [!Note]  
> <span data-ttu-id="6d7bf-113">Pubs — это хранилище данных, используемое в рамках этого учебника.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-113">Pubs is the data store that is used throughout this primer.</span></span>

 

<span data-ttu-id="6d7bf-114">Так как Упдатеаусораддресс обновляет хранилище данных, рекомендуется включить работу в транзакцию, как показано на следующем рисунке, чтобы при вызове компонента клиент COM+ автоматически запустил транзакцию и прикрепляет базу данных (Resource Manager) к этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-114">Because UpdateAuthorAddress updates a data store, it is advisable to include the work in a transaction, as shown in the following illustration, so that when a client calls the component, COM+ automatically starts a transaction and enlists the database (resource manager) in that transaction.</span></span> <span data-ttu-id="6d7bf-115">(Подробные сведения о транзакциях в COM+ см. в разделе [транзакции COM+](com--transactions.md).)</span><span class="sxs-lookup"><span data-stu-id="6d7bf-115">(For detailed information about transactions in COM+, see [COM+ Transactions](com--transactions.md).)</span></span>

![Схема, показывающая транзакцию COM+ с Упдатеаусораддресс.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

<span data-ttu-id="6d7bf-117">Чтобы сделать Упдатеаусораддресс транзакционным компонентом, необходимо выполнить следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-117">To make UpdateAuthorAddress a transactional component, the following steps are required:</span></span>

1.  <span data-ttu-id="6d7bf-118">Компонент должен быть написан.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-118">The component must be written.</span></span> <span data-ttu-id="6d7bf-119">Для дополнительной защиты добавляется подподпрограмма, проверяющая, что COM+ создал объект в транзакции.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-119">For extra protection, a subroutine is added, verifying that COM+ created the object in a transaction.</span></span> <span data-ttu-id="6d7bf-120">Кроме того, основная обработка ошибок включена в компонент, чтобы упростить восстановление после ошибок.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-120">Also, basic error handling is included in the component to simplify error recovery.</span></span> <span data-ttu-id="6d7bf-121">Проверка транзакций и обработка ошибок повышают надежность компонента.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-121">Transaction verification and error handling enhance the reliability of the component.</span></span> <span data-ttu-id="6d7bf-122">(См. шаг 1. пример кода для получения полного перечня компонента Упдатеаусораддресс.)</span><span class="sxs-lookup"><span data-stu-id="6d7bf-122">(See Step 1 Sample Code for a complete listing of the UpdateAuthorAddress component.)</span></span>
2.  <span data-ttu-id="6d7bf-123">После добавления компонента в приложение COM+ и установки приложения атрибут transaction должен иметь значение **Required**, что гарантирует, что com+ создает каждый объект упдатеаусораддресс в транзакции.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-123">After adding the component to a COM+ application and installing the application, the transaction attribute must be set to **Required**, which guarantees that COM+ creates each UpdateAuthorAddress object in a transaction.</span></span> <span data-ttu-id="6d7bf-124">Инструкции по заданию атрибута транзакции для компонента см. в разделе [Задание атрибута транзакции](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="6d7bf-124">For instructions on how to set the transaction attribute for a component, see [Setting the Transaction Attribute](setting-the-transaction-attribute.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="6d7bf-125">Установка атрибута транзакции для компонента определяет, как COM+ создает каждый объект в отношении транзакций.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-125">Setting the transaction attribute on a component defines how COM+ creates each object with regard to transactions.</span></span> <span data-ttu-id="6d7bf-126">Значения атрибутов транзакций **пропускаются**, **не поддерживаются**, **поддерживаются**, **обязательны** и **требуют новых**.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-126">Transaction attribute values are **Ignored**, **Not Supported**, **Supported**, **Required**, and **Requires New**.</span></span> <span data-ttu-id="6d7bf-127">**Требуемое** значение не является одним из значений атрибута по умолчанию компонента.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-127">The **Required** value is not one of a component's default attribute values.</span></span>

     

<span data-ttu-id="6d7bf-128">COM+ привязывает службу транзакций с JIT-активацией и параллелизмом.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-128">COM+ binds the transaction service with just-in-time (JIT) activation and concurrency.</span></span> <span data-ttu-id="6d7bf-129">Когда компонент объявляется транзакционным, COM+ также обеспечивает принудительную JIT-активацию и защиту параллелизма (синхронизацию).</span><span class="sxs-lookup"><span data-stu-id="6d7bf-129">When you declare a component to be transactional, COM+ also enforces JIT activation and concurrency protection (synchronization).</span></span>

## <a name="sample-code"></a><span data-ttu-id="6d7bf-130">Пример кода</span><span class="sxs-lookup"><span data-stu-id="6d7bf-130">Sample code</span></span>

<span data-ttu-id="6d7bf-131">Компонент Упдатеаусораддресс открывает подключение к базе данных pubs, позволяя пользователю изменять имя автора, адрес или состояние контракта.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-131">The UpdateAuthorAddress component opens a connection to the Pubs database, allowing the user to modify an author's name, address, or contract status.</span></span> <span data-ttu-id="6d7bf-132">Он также вызывает второй компонент, который рассматривается в разделе [Шаг 2. расширение транзакции для нескольких компонентов](step-2--extending-a-transaction-across-multiple-components.md).</span><span class="sxs-lookup"><span data-stu-id="6d7bf-132">It also calls a second component, which is discussed in [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md).</span></span>

<span data-ttu-id="6d7bf-133">Чтобы использовать следующий код в проекте Microsoft Visual Basic, откройте новый проект ActiveX.dll и добавьте ссылки на библиотеку Microsoft объекты данных ActiveX и библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-133">To use the following code in a Microsoft Visual Basic project, open a new ActiveX.dll project and add references to the Microsoft ActiveX Data Objects Library and the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="6d7bf-134">Пример кода в этом учебнике предназначен для целей иллюстрации и может не быть самым эффективным для фактического промежуточного хранения и рабочей среды.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-134">The sample code in this primer is for purposes of illustration and may not be the most efficient for actual staging and production.</span></span>

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a><span data-ttu-id="6d7bf-135">Сводка</span><span class="sxs-lookup"><span data-stu-id="6d7bf-135">Summary</span></span>

-   <span data-ttu-id="6d7bf-136">COM+ назначает значения атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-136">COM+ assigns default attribute values.</span></span> <span data-ttu-id="6d7bf-137">Большинство атрибутов службы можно изменить.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-137">You can reconfigure most service attributes.</span></span>
-   <span data-ttu-id="6d7bf-138">Установка атрибута транзакции компонента в значение **Required** гарантирует, что COM+ должен создать каждый экземпляр этого компонента в транзакции, но не обязательно запускает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-138">Setting a component's transaction attribute to **Required** guarantees that COM+ must create each instance of that component in a transaction but doesn't necessarily start a new transaction.</span></span>
-   <span data-ttu-id="6d7bf-139">Проверка наличия транзакции подтверждает, что значение атрибута транзакции компонента не было случайно сброшено на нетранзакционное значение, например **Ignore** или **not supported**.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-139">Verifying the presence of a transaction confirms that the component's transaction attribute value wasn't inadvertently reset to a non-transactional value, such as **Ignore** or **Not Supported**.</span></span>
-   <span data-ttu-id="6d7bf-140">Обработка ошибок делает компонент более надежным и проще в устранении неполадок.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-140">Handling errors makes your component more reliable and easier to troubleshoot.</span></span>
-   <span data-ttu-id="6d7bf-141">COM+ принудительно реализует [JIT-активацию](com--just-in-time-activation.md) и службы [защиты параллелизма](com--synchronization.md) для транзакционных компонентов.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-141">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [concurrency protection](com--synchronization.md) services for transactional components.</span></span>
-   <span data-ttu-id="6d7bf-142">Закрытие подключения к базе данных по завершении с ним позволяет другому компоненту в той же транзакции повторно использовать подключение из пула подключений.</span><span class="sxs-lookup"><span data-stu-id="6d7bf-142">Closing the database connection when you are done with it allows another component in the same transaction to reuse the connection from the connection pool.</span></span> <span data-ttu-id="6d7bf-143">(Объединение соединений не следует путать с [пулом объектов](com--object-pooling.md).)</span><span class="sxs-lookup"><span data-stu-id="6d7bf-143">(Connection pooling should not be confused with [object pooling](com--object-pooling.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d7bf-144">См. также</span><span class="sxs-lookup"><span data-stu-id="6d7bf-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d7bf-145">Шаг 2. расширение транзакции для нескольких компонентов</span><span class="sxs-lookup"><span data-stu-id="6d7bf-145">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="6d7bf-146">Шаг 3. повторное использование компонентов</span><span class="sxs-lookup"><span data-stu-id="6d7bf-146">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="6d7bf-147">JIT-активация COM+</span><span class="sxs-lookup"><span data-stu-id="6d7bf-147">COM+ Just-in-Time Activation</span></span>](com--just-in-time-activation.md)
</dt> <dt>

[<span data-ttu-id="6d7bf-148">Синхронизация COM+</span><span class="sxs-lookup"><span data-stu-id="6d7bf-148">COM+ Synchronization</span></span>](com--synchronization.md)
</dt> <dt>

[<span data-ttu-id="6d7bf-149">Настройка транзакций</span><span class="sxs-lookup"><span data-stu-id="6d7bf-149">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="6d7bf-150">Создание приложений COM+</span><span class="sxs-lookup"><span data-stu-id="6d7bf-150">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="6d7bf-151">Установка атрибута Transaction</span><span class="sxs-lookup"><span data-stu-id="6d7bf-151">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



