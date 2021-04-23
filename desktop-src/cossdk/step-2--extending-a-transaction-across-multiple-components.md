---
description: Шаг 2. расширение транзакции для нескольких компонентов
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: Шаг 2. расширение транзакции для нескольких компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350935"
---
# <a name="step-2-extending-a-transaction-across-components"></a><span data-ttu-id="0ef79-103">Шаг 2. расширение транзакции между компонентами</span><span class="sxs-lookup"><span data-stu-id="0ef79-103">Step 2: Extending a Transaction Across Components</span></span>

## <a name="objectives"></a><span data-ttu-id="0ef79-104">Задачи</span><span class="sxs-lookup"><span data-stu-id="0ef79-104">Objectives</span></span>

<span data-ttu-id="0ef79-105">На этом шаге вы узнаете о следующих возможностях:</span><span class="sxs-lookup"><span data-stu-id="0ef79-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="0ef79-106">Поток транзакций</span><span class="sxs-lookup"><span data-stu-id="0ef79-106">Transaction flow</span></span>
-   <span data-ttu-id="0ef79-107">Голосование нескольких объектов в транзакции</span><span class="sxs-lookup"><span data-stu-id="0ef79-107">How multiple objects vote in a transaction</span></span>

## <a name="description"></a><span data-ttu-id="0ef79-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0ef79-108">Description</span></span>

<span data-ttu-id="0ef79-109">[Шаг 1. Создание транзакционного компонента](step-1--creating-a-transactional-component.md) показывает, как написать простой транзакционный компонент, который обновляет сведения об авторе в базе данных Microsoft SQL Server Pubs.</span><span class="sxs-lookup"><span data-stu-id="0ef79-109">[Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) shows how to write a simple transactional component that updates author information in the Microsoft SQL Server Pubs database.</span></span> <span data-ttu-id="0ef79-110">Шаг 2 показывает, что происходит при расширении транзакции по нескольким компонентам.</span><span class="sxs-lookup"><span data-stu-id="0ef79-110">Step 2 shows what happens when a transaction is extended across multiple components.</span></span>

<span data-ttu-id="0ef79-111">В соответствии с моделью программирования COM+ `UpdateAuthorAddress` вызывает другой компонент в процессе выполнения своей работы.</span><span class="sxs-lookup"><span data-stu-id="0ef79-111">In keeping with the COM+ programming model, `UpdateAuthorAddress` calls another component in the course of completing its work.</span></span> <span data-ttu-id="0ef79-112">Второй компонент, `ValidateAuthorAddress` , проверяет адрес автора и возвращает результаты вызывающему объекту, `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="0ef79-112">The second component, `ValidateAuthorAddress`, validates the author's address and returns the results to its caller, `UpdateAuthorAddress`.</span></span>

<span data-ttu-id="0ef79-113">В отличие от вызывающего объекта, `ValidateAuthorAddress` транзакция не требует транзакции, но она по-прежнему может участвовать в ее транзакции вызывающего.</span><span class="sxs-lookup"><span data-stu-id="0ef79-113">Unlike its caller, `ValidateAuthorAddress` does not require a transaction, but it can still participate in its caller's transaction.</span></span> <span data-ttu-id="0ef79-114">На этом шаге для его атрибута транзакции задано значение **Supported**, как показано на следующем рисунке, который расширяет существующую транзакцию до нового объекта.</span><span class="sxs-lookup"><span data-stu-id="0ef79-114">In this step, its transaction attribute value is set to **Supported**, as shown in the following illustration, which extends the existing transaction to the new object.</span></span>

![Схема, показывающая расширение существующей транзакции до нового объекта.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

<span data-ttu-id="0ef79-116">**Поддерживаемое** значение атрибута расширяет (или проходит) существующую транзакцию только в том случае, если вызывающий объект является транзакционным.</span><span class="sxs-lookup"><span data-stu-id="0ef79-116">The **Supported** attribute value extends (or flows) an existing transaction only when the caller is transactional.</span></span> <span data-ttu-id="0ef79-117">При `UpdateAuthorAddress` вызовах `ValidateAuthorAddress` com+ сначала проверяет контекст вызывающего объекта, чтобы определить, является ли он транзакционным.</span><span class="sxs-lookup"><span data-stu-id="0ef79-117">When `UpdateAuthorAddress` calls `ValidateAuthorAddress`, COM+ first looks at the caller's context to see whether it is transactional.</span></span> <span data-ttu-id="0ef79-118">Затем COM+ просматривает атрибуты службы, заданные в параметре, `ValidateAuthorAddress` и присваивает новому объекту тот же идентификатор транзакции, который назначен вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="0ef79-118">COM+ then looks at the service attributes that are set on `ValidateAuthorAddress` and assigns the new object the same transaction identifier that is assigned to the caller object.</span></span> <span data-ttu-id="0ef79-119">Чтобы лучше понять этот процесс, см. раздел [Активация контекста](context-activation.md).</span><span class="sxs-lookup"><span data-stu-id="0ef79-119">To better understand this process, see [Context Activation](context-activation.md).</span></span>

<span data-ttu-id="0ef79-120">Так как они используют один и тот же идентификатор транзакции, оба объекта должны успешно завершить свою работу, или COM+ отменяет транзакцию (отменяя любые изменения, внесенные в базу данных Pubs).</span><span class="sxs-lookup"><span data-stu-id="0ef79-120">Because they share the same transaction identifier, both objects must complete their work successfully or COM+ aborts the transaction (undoing any changes made to the Pubs database).</span></span>

<span data-ttu-id="0ef79-121">Все объекты, участвующие в голосовании транзакции, для фиксации или прерывания транзакции.</span><span class="sxs-lookup"><span data-stu-id="0ef79-121">All objects participating in a transaction vote to either commit or abort the transaction.</span></span> <span data-ttu-id="0ef79-122">Голосование происходит явно при включении в код инструкций голосования, как показано в следующем примере кода, который создает `UpdateAuthorAddress` компонент:</span><span class="sxs-lookup"><span data-stu-id="0ef79-122">Voting occurs explicitly when you include voting instructions in your code, as shown in the following extraction from the Step 1 Sample Code, which creates the `UpdateAuthorAddress` component:</span></span>


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



<span data-ttu-id="0ef79-123">Голосование также происходит неявно, как это делается в `ValidateAuthorAddress` компоненте.</span><span class="sxs-lookup"><span data-stu-id="0ef79-123">Voting also occurs implicitly, as is done in the `ValidateAuthorAddress` component.</span></span> <span data-ttu-id="0ef79-124">Если в объекте не объявлено иначе, COM+ предполагает, что объект завершил свою работу успешно, но не готов к деактивации.</span><span class="sxs-lookup"><span data-stu-id="0ef79-124">Unless the object declares otherwise, COM+ assumes an object has completed its work successfully but that it is not ready to be deactivated.</span></span> <span data-ttu-id="0ef79-125">COM+ делает следующее допущение:</span><span class="sxs-lookup"><span data-stu-id="0ef79-125">COM+ makes the following assumption:</span></span>


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



<span data-ttu-id="0ef79-126">При `ValidateAuthorAddress` возврате вызывающему объекту COM+ читает свой голос в качестве фиксации.</span><span class="sxs-lookup"><span data-stu-id="0ef79-126">When `ValidateAuthorAddress` returns to its caller, COM+ reads its vote as a commit.</span></span> <span data-ttu-id="0ef79-127">COM+ не учитывает голоса до тех пор, пока не будет отключен корневой объект, который является первым объектом в транзакции в данном случае, `UpdateAuthorAddress` объектом.</span><span class="sxs-lookup"><span data-stu-id="0ef79-127">COM+ doesn't count the votes until it deactivates the root object, which is the first object in the transaction in this case, the `UpdateAuthorAddress` object.</span></span>

## <a name="sample-code"></a><span data-ttu-id="0ef79-128">Пример кода</span><span class="sxs-lookup"><span data-stu-id="0ef79-128">Sample code</span></span>

<span data-ttu-id="0ef79-129">`ValidateAuthorAddress`Компонент выполняет простую проверку адреса автора.</span><span class="sxs-lookup"><span data-stu-id="0ef79-129">The `ValidateAuthorAddress` component makes a simple check of the author's address.</span></span> <span data-ttu-id="0ef79-130">Так как не продается `UpdateAuthorAddress` явно, com+ использует параметры голосования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ef79-130">Because `UpdateAuthorAddress` does not vote explicitly, COM+ uses the default vote settings.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a><span data-ttu-id="0ef79-131">Сводка</span><span class="sxs-lookup"><span data-stu-id="0ef79-131">Summary</span></span>

-   <span data-ttu-id="0ef79-132">Установка значения " **поддерживается** " для атрибута транзакции компонента может привести к созданию нового объекта в транзакции вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="0ef79-132">Setting a component's transaction attribute to **Supported** can result in the new object being created in the calling object's transaction.</span></span> <span data-ttu-id="0ef79-133">COM+ просматривает контекст вызывающего объекта, чтобы определить состояние транзакций для нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0ef79-133">COM+ looks at the caller's context to determine the transactional status of the new object.</span></span> <span data-ttu-id="0ef79-134">Если вызывающий объект является транзакционным, COM+ передает транзакцию в новый объект.</span><span class="sxs-lookup"><span data-stu-id="0ef79-134">If the caller is transactional, COM+ flows the transaction to the new object.</span></span>
-   <span data-ttu-id="0ef79-135">Все объекты, участвующие в одной транзакции, совместно используют общий идентификатор транзакции, который COM+ считывает из контекста объекта.</span><span class="sxs-lookup"><span data-stu-id="0ef79-135">All objects participating in the same transaction share a common transaction identifier, which COM+ reads from the object's context.</span></span>
-   <span data-ttu-id="0ef79-136">Каждый объект в транзакции подвигается независимо от других объектов.</span><span class="sxs-lookup"><span data-stu-id="0ef79-136">Each object in a transaction votes independently of other objects.</span></span> <span data-ttu-id="0ef79-137">COM+ подсчитывает голоса при деактивации корневого объекта.</span><span class="sxs-lookup"><span data-stu-id="0ef79-137">COM+ counts the votes when the root object is deactivated.</span></span>
-   <span data-ttu-id="0ef79-138">Можно переключить голосование транзакций объекта между фиксацией и прервать до тех пор, пока COM+ не активирует объект или пока COM+ не активирует корневой объект и не завершит транзакцию.</span><span class="sxs-lookup"><span data-stu-id="0ef79-138">You can toggle an object's transaction vote between commit and abort until COM+ deactivates the object or until COM+ deactivates the root object and ends the transaction.</span></span> <span data-ttu-id="0ef79-139">Учитывается только последний параметр голосования.</span><span class="sxs-lookup"><span data-stu-id="0ef79-139">Only the last vote setting counts.</span></span> <span data-ttu-id="0ef79-140">Интерфейсы [**иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) и [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) предоставляют методы и, которые создают аналогичные результаты голосования, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0ef79-140">The [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) and [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interfaces provide methods and that produce similar voting results as shown in the following table.</span></span> <span data-ttu-id="0ef79-141">Для прямого голосования в транзакции можно использовать любой из этих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0ef79-141">You can use either interface to vote explicitly in a transaction.</span></span> 

    | <span data-ttu-id="0ef79-142">Комбинированные методы [**иконтекстстате**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="0ef79-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) combination methods</span></span>                                                                                                                                                      | <span data-ttu-id="0ef79-143">Эквивалентный метод [**иобжектконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="0ef79-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) equivalent method</span></span>       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="0ef79-144">[**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **ткскоммит**</span><span class="sxs-lookup"><span data-stu-id="0ef79-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="0ef79-145">[**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="0ef79-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>  | [<span data-ttu-id="0ef79-146">**сеткомплете**</span><span class="sxs-lookup"><span data-stu-id="0ef79-146">**SetComplete**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | <span data-ttu-id="0ef79-147">[**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **ткскоммит**</span><span class="sxs-lookup"><span data-stu-id="0ef79-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="0ef79-148">[**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="0ef79-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/> | [<span data-ttu-id="0ef79-149">**енаблекоммит**</span><span class="sxs-lookup"><span data-stu-id="0ef79-149">**EnableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | <span data-ttu-id="0ef79-150">[**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **тксаборт**</span><span class="sxs-lookup"><span data-stu-id="0ef79-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="0ef79-151">[**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="0ef79-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>   | [<span data-ttu-id="0ef79-152">**SetAbort**</span><span class="sxs-lookup"><span data-stu-id="0ef79-152">**SetAbort**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | <span data-ttu-id="0ef79-153">[**Сетмитрансактионвоте**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *тксвоте*  =  **тксаборт**</span><span class="sxs-lookup"><span data-stu-id="0ef79-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="0ef79-154">[**Сетдеактиватеонретурн**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *бдеактивате*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="0ef79-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/>  | [<span data-ttu-id="0ef79-155">**дисаблекоммит**</span><span class="sxs-lookup"><span data-stu-id="0ef79-155">**DisableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   <span data-ttu-id="0ef79-156">COM+ устанавливает голосование объекта в эквивалент [**енаблекоммит**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) , если только голоса компонента не были явно указаны.</span><span class="sxs-lookup"><span data-stu-id="0ef79-156">COM+ sets an object's vote to the equivalent of [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) unless the component votes explicitly.</span></span>
-   <span data-ttu-id="0ef79-157">Явное голосование может сократить общую длительность транзакции и освободить ресурсоемкие блокировки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ef79-157">Voting explicitly can reduce the overall duration of the transaction and release expensive resource locks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ef79-158">См. также</span><span class="sxs-lookup"><span data-stu-id="0ef79-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ef79-159">Шаг 1. Создание транзакционного компонента</span><span class="sxs-lookup"><span data-stu-id="0ef79-159">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="0ef79-160">Шаг 3. повторное использование компонентов</span><span class="sxs-lookup"><span data-stu-id="0ef79-160">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="0ef79-161">Активация контекста</span><span class="sxs-lookup"><span data-stu-id="0ef79-161">Context Activation</span></span>](context-activation.md)
</dt> <dt>

[<span data-ttu-id="0ef79-162">Управление автоматическими транзакциями в COM+</span><span class="sxs-lookup"><span data-stu-id="0ef79-162">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




