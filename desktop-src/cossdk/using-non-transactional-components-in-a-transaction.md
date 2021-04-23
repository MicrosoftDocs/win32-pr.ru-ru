---
description: Использование нетранзакционных компонентов в транзакции
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Использование нетранзакционных компонентов в транзакции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807894"
---
# <a name="using-non-transactional-components-in-a-transaction"></a><span data-ttu-id="8e0d0-103">Использование нетранзакционных компонентов в транзакции</span><span class="sxs-lookup"><span data-stu-id="8e0d0-103">Using Non-Transactional Components in a Transaction</span></span>

<span data-ttu-id="8e0d0-104">Часто бывает полезно поместить нетранзакционные компоненты в транзакцию, чтобы воспользоваться преимуществами [свойств ACID](acid-properties.md) транзакций.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-104">It is often useful to place non-transactional components into a transaction to take advantage of the [ACID properties](acid-properties.md) of transactions.</span></span> <span data-ttu-id="8e0d0-105">Например, при наличии нетранзакционных устаревших компонентов, используемых для обновления паролей в сети, эти компоненты можно поместить в транзакцию, чтобы обеспечить согласованность обновлений паролей по сети.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-105">For example, if you have non-transactional legacy components that you use to update passwords on a network, you can place those components in a transaction to ensure that password updates are consistent across the network.</span></span>

<span data-ttu-id="8e0d0-106">*Объект контекста транзакции* — это универсальный объект, позволяющий нетранзакционным клиентам объединять работу нескольких COM-объектов в одну транзакцию без необходимости разработки нового компонента специально для этой цели.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-106">The *transaction context object* is a generic object that allows non-transactional clients to combine the work of multiple COM objects into a single transaction, without requiring you to develop a new component specifically for that purpose.</span></span> <span data-ttu-id="8e0d0-107">В отличие от автоматической транзакции, объект контекста транзакции требует, чтобы его клиент явно зафиксировал или прервал транзакцию.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-107">In contrast to an automatic transaction, the transaction context object requires its client to explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="8e0d0-108">По умолчанию атрибут Transaction объекта контекста транзакции имеет значение Required.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-108">By default, the transaction attribute value of the transaction context object is set to Required.</span></span> <span data-ttu-id="8e0d0-109">COM+ прерывает транзакцию, если клиент освобождает объект контекста транзакции без явного выполнения вызова Commit или Abort.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-109">COM+ aborts the transaction if the client releases the transaction context object without explicitly issuing a commit or abort call.</span></span>

<span data-ttu-id="8e0d0-110">В следующем примере Visual Basic показано, как нетранзакционный клиент может составить работу, выполняемую более чем одним объектом, в одну транзакцию:</span><span class="sxs-lookup"><span data-stu-id="8e0d0-110">The following Visual Basic example shows how a non-transactional client can compose the work done by more than one object into a single transaction:</span></span>


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a><span data-ttu-id="8e0d0-111">Ограничения объекта контекста транзакции</span><span class="sxs-lookup"><span data-stu-id="8e0d0-111">Limitations of the Transaction Context Object</span></span>

<span data-ttu-id="8e0d0-112">Ниже приведены некоторые важные ограничения объекта контекста транзакции.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-112">Following are some important limitations of the transaction context object:</span></span>

-   <span data-ttu-id="8e0d0-113">При использовании объекта контекста транзакции логика приложения, объединяющая работу нескольких объектов в одну транзакцию, связана с определенной нетранзакционной реализацией клиента, и некоторые преимущества использования COM-компонентов теряются.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-113">When using a transaction context object, the application logic that combines the work of multiple objects into a single transaction is tied to a specific non-transactional client implementation and some advantages of using COM components are lost.</span></span> <span data-ttu-id="8e0d0-114">Эти потерянные преимущества включают следующие.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-114">These lost advantages include the following:</span></span>
    -   <span data-ttu-id="8e0d0-115">Возможность повторного использования логики приложения в рамках еще больших транзакций</span><span class="sxs-lookup"><span data-stu-id="8e0d0-115">Ability to reuse the application logic as part of an even larger transaction</span></span>
    -   <span data-ttu-id="8e0d0-116">Ликвидация декларативной безопасности</span><span class="sxs-lookup"><span data-stu-id="8e0d0-116">Imposition of declarative security</span></span>
    -   <span data-ttu-id="8e0d0-117">Гибкость запуска логики удаленно от клиента</span><span class="sxs-lookup"><span data-stu-id="8e0d0-117">Flexibility to run the logic remotely from the client</span></span>
-   <span data-ttu-id="8e0d0-118">Объект контекста транзакции выполняется в процессе с нетранзакционным клиентом, что означает, что COM+ должен быть доступен на нетранзакционном клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-118">The transaction context object runs in-process with the non-transactional client, which means that COM+ must be available on the non-transactional client computer.</span></span> <span data-ttu-id="8e0d0-119">Это может не быть проблемой, например, когда объект контекста транзакции используется на странице Active Server страниц (ASP), которая работает на том же сервере, что и COM+.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-119">This might not be a problem, for example, when the transaction context object is used from an Active Server Pages (ASP) page that is running on the same server as COM+.</span></span>
-   <span data-ttu-id="8e0d0-120">При создании объекта контекста транзакции контекст для нетранзакционного клиента не получается.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-120">You do not get a context for the non-transactional client when you create a transaction context object.</span></span> <span data-ttu-id="8e0d0-121">Транзакционные операции можно выполнять только косвенно через COM-объекты, созданные с помощью объекта контекста транзакции.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-121">Transactional work can only be done indirectly, through COM objects created by using the transaction context object.</span></span> <span data-ttu-id="8e0d0-122">В частности, нетранзакционный клиент не может использовать распределителя ресурсов COM+ (например, ODBC) и включать работу в транзакцию.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-122">In particular, the non-transactional client cannot use COM+ resource dispensers (such as ODBC) and have the work included in the transaction.</span></span> <span data-ttu-id="8e0d0-123">Например, разработчики могут ознакомиться со следующим синтаксисом для транзакционной работы в системах реляционных баз данных:</span><span class="sxs-lookup"><span data-stu-id="8e0d0-123">For example, developers may be familiar with the following syntax for doing transactional work on relational database systems:</span></span>

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    <span data-ttu-id="8e0d0-124">Использование объекта контекста транзакции аналогичным образом не дает желаемого результата:</span><span class="sxs-lookup"><span data-stu-id="8e0d0-124">Using the transaction context object in a similar way does not yield the desired result:</span></span>

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    <span data-ttu-id="8e0d0-125">Вызов DoWork в этом примере не прикреплен к транзакции.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-125">The call to DoWork in this example is not enlisted in a transaction.</span></span> <span data-ttu-id="8e0d0-126">Вместо этого необходимо создать COM-компонент, который вызывает DoWork, создать экземпляр объекта этого компонента с помощью объекта контекста транзакции, а затем вызвать этот объект из нетранзакционного клиента, чтобы работа была частью транзакции, управляемой клиентом.</span><span class="sxs-lookup"><span data-stu-id="8e0d0-126">Instead, you must build a COM component that calls DoWork, create an object instance of that component using the transaction context object, and then call that object from the non-transactional client for the work to be part of the client-controlled transaction.</span></span>

 

 



