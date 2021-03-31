---
description: Операции администрирования COM+ в транзакциях
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Операции администрирования COM+ в транзакциях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21612ffec1b9f082dc6a91861882a71f18fb07be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807972"
---
# <a name="com-administration-operations-within-transactions"></a><span data-ttu-id="0f10b-103">Операции администрирования COM+ в транзакциях</span><span class="sxs-lookup"><span data-stu-id="0f10b-103">COM+ Administration Operations Within Transactions</span></span>

<span data-ttu-id="0f10b-104">База данных регистрации COM+ (Регдб) — это транзакционный диспетчер ресурсов, который может участвовать в транзакциях COM+.</span><span class="sxs-lookup"><span data-stu-id="0f10b-104">The COM+ registration database (RegDB) is a transacted resource manager that can participate in COM+ transactions.</span></span> <span data-ttu-id="0f10b-105">Это позволяет выполнять операции администрирования в рамках транзакции и зафиксировать или прерывать все изменения конфигурации как атомарную операцию даже на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="0f10b-105">This enables you to perform administration operations within a transaction and have all configuration changes committed or aborted as an atomic operation, even across multiple computers.</span></span> <span data-ttu-id="0f10b-106">В некоторых обстоятельствах это может быть очень полезно, несмотря на то, что необходимо учитывать изоляцию и блокировку, а выполнение задач администрирования в рамках транзакций влечет за собой незначительные изменения в стандартной модели программирования администрирования.</span><span class="sxs-lookup"><span data-stu-id="0f10b-106">In some circumstances, it can be very beneficial to do this, although there is isolation and blocking behavior that you should take into account, and performing administration tasks within transactions does involve slight changes to the normal administration programming model.</span></span>

## <a name="benefits-of-doing-administration-operations-within-transactions"></a><span data-ttu-id="0f10b-107">Преимущества выполнения административных операций в транзакциях</span><span class="sxs-lookup"><span data-stu-id="0f10b-107">Benefits of Doing Administration Operations Within Transactions</span></span>

-   <span data-ttu-id="0f10b-108">**Согласованность данных —** Операции администрирования, выполняемые внутри транзакции, фиксируются или прерываются в целом, хотя существуют некоторые нетранзакционные ресурсы каталога COM+, для которых это может быть не так.</span><span class="sxs-lookup"><span data-stu-id="0f10b-108">**Consistency of data—** Administration operations performed within a transaction are committed or aborted as a whole, although there are some non-transactional COM+ catalog resources for which this may not be the case.</span></span> <span data-ttu-id="0f10b-109">(См. раздел нетранзакционные ресурсы каталога COM+ ниже.)</span><span class="sxs-lookup"><span data-stu-id="0f10b-109">(See Non-Transactional COM+ Catalog Resources below.)</span></span>
-   <span data-ttu-id="0f10b-110">**Согласованное развертывание на нескольких компьютерах —** При развертывании приложений COM+ на нескольких серверах можно гарантировать, что все серверы будут оставаться одинаковыми конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="0f10b-110">**Consistent deployment across multiple machines—** If you are deploying COM+ applications across multiple servers, you can guarantee that all servers are left with identical configurations.</span></span>
-   <span data-ttu-id="0f10b-111">**Масштабирование и производительность —** При выполнении нескольких операций в рамках транзакции все операции записи в Регдб выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="0f10b-111">**Scaling and performance—** When you do multiple operations within a transaction, all writes to RegDB are performed at once.</span></span> <span data-ttu-id="0f10b-112">Постоянные операции записи в Регдб являются относительно дорогостоящей операцией. Если вы вносите много операций записи в Регдб, вы можете добиться значительного выигрыша в производительности сразу, а не каждый раз, когда вызывается метод [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span><span class="sxs-lookup"><span data-stu-id="0f10b-112">Persisted writes to RegDB are a relatively expensive operation; if you are making many writes to RegDB, you can get a big performance benefit from doing them all at once instead of every time you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span></span>

## <a name="isolation-behavior-of-regdb"></a><span data-ttu-id="0f10b-113">Режим изоляции Регдб</span><span class="sxs-lookup"><span data-stu-id="0f10b-113">Isolation Behavior of RegDB</span></span>

<span data-ttu-id="0f10b-114">Чтобы обеспечить правильную согласованность данных и сериализуемые транзакции, Регдб обеспечивает определенную блокировку и изоляцию при выполнении операций администрирования в рамках транзакций.</span><span class="sxs-lookup"><span data-stu-id="0f10b-114">To ensure proper data consistency and serializable transactions, RegDB enforces particular blocking and isolation behavior when administration operations are being performed within transactions.</span></span>

<span data-ttu-id="0f10b-115">Всякий раз, когда компонент, выполняющий работу в рамках транзакции, вызывает любой метод, который вызовет запись в каталог COM+ (например, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)или [**инсталлкомпонент**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)), в коде сервера каталога COM+ выполняется блокировка записи, которая блокирует любые другие модули записи, пока текущая транзакция не зафиксируется или не завершится.</span><span class="sxs-lookup"><span data-stu-id="0f10b-115">Whenever a component that is doing work within a transaction calls any method that will cause a write to the COM+ catalog—such as [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication), or [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)—a writer lock is taken on COM+ catalog server code that will block any other writers from coming in until the current transaction commits or aborts.</span></span> <span data-ttu-id="0f10b-116">То есть модули записи могут поступать только в том случае, если они имеют правильные сходство транзакций и участвуют в текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="0f10b-116">That is, writers can come in only if they have the correct transaction affinity and are participating in the current transaction.</span></span>

<span data-ttu-id="0f10b-117">Читатели не блокируются.</span><span class="sxs-lookup"><span data-stu-id="0f10b-117">Readers are not blocked.</span></span> <span data-ttu-id="0f10b-118">Однако данные, которые видят читатели, не отображают промежуточные изменения, внесенные в транзакцию до фактической фиксации транзакции.</span><span class="sxs-lookup"><span data-stu-id="0f10b-118">However, the data that readers see does not reflect any interim changes made within the transaction until that transaction actually commits.</span></span> <span data-ttu-id="0f10b-119">Все компоненты, участвующие в этой транзакции, видят промежуточные состояния данных при чтении данных, но все компоненты за пределами транзакции видят эти изменения только после завершения транзакции.</span><span class="sxs-lookup"><span data-stu-id="0f10b-119">Any components participating in that transaction sees interim data states when they read data, but all components outside the transaction see those changes only after the transaction has completed.</span></span>

## <a name="savechanges-behavior"></a><span data-ttu-id="0f10b-120">Поведение метода SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0f10b-120">SaveChanges Behavior</span></span>

<span data-ttu-id="0f10b-121">Чтобы добиться описанного выше поведения изоляции, Регдб эффективно предоставляет кэш, обрабатываемый компонентами внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="0f10b-121">To achieve the isolation behavior described above, RegDB effectively provides a cache that is acted on by components within the transaction.</span></span> <span data-ttu-id="0f10b-122">Это изменяет поведение метода [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="0f10b-122">This changes the behavior of the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method.</span></span>

<span data-ttu-id="0f10b-123">Как правило, без транзакции все ожидающие изменения записываются в каталог при вызове метода [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), а **SaveChanges** не возвращается до тех пор, пока не будут завершены все операции записи.</span><span class="sxs-lookup"><span data-stu-id="0f10b-123">Normally, without the presence of a transaction, any pending changes are written to the catalog when you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), and **SaveChanges** doesn't return until all writes are completed.</span></span> <span data-ttu-id="0f10b-124">Это гарантирует, что если вызов **SaveChanges** вернется успешно, можно вызвать [**стартаппликатион**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) и активировать приложение с новыми данными.</span><span class="sxs-lookup"><span data-stu-id="0f10b-124">This guarantees that if a call to **SaveChanges** returns successfully, you can call [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) and it will activate the application with fresh data.</span></span>

<span data-ttu-id="0f10b-125">Однако в рамках транзакции функция [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) влияет только на кэш, а не на сам регдб, а **SaveChanges** немедленно возвращает информацию о том, что все изменения были транзакционно зафиксированы в регдб.</span><span class="sxs-lookup"><span data-stu-id="0f10b-125">However, within a transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affects only the cache, not the RegDB itself, and **SaveChanges** returns immediately whether all changes have been transactionally committed to RegDB.</span></span> <span data-ttu-id="0f10b-126">Нет никакой гарантии, что [**стартаппликатион**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) использует новые данные после возвращения метода **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="0f10b-126">There is no guarantee that [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) is using fresh data subsequent to **SaveChanges** returning.</span></span> <span data-ttu-id="0f10b-127">Если необходимо вызвать **стартаппликатион** в этом контексте, рекомендуется подождать некоторое время, прежде чем делать это.</span><span class="sxs-lookup"><span data-stu-id="0f10b-127">If you need to call **StartApplication** in this context, it is advisable to wait for some period of time before doing so.</span></span>

## <a name="transaction-time-out-period"></a><span data-ttu-id="0f10b-128">Период Time-Out транзакции</span><span class="sxs-lookup"><span data-stu-id="0f10b-128">Transaction Time-Out Period</span></span>

<span data-ttu-id="0f10b-129">Если вы выполняете множество административных операций в рамках транзакции, это может быть долго выполняющаяся транзакция.</span><span class="sxs-lookup"><span data-stu-id="0f10b-129">If you are doing numerous administration operations within a transaction, it may be a long running transaction.</span></span> <span data-ttu-id="0f10b-130">В этом случае значение времени ожидания транзакции может быть проблемой.</span><span class="sxs-lookup"><span data-stu-id="0f10b-130">In this case, the transaction time-out value can be an issue.</span></span> <span data-ttu-id="0f10b-131">Это определяется либо значением времени ожидания транзакции, заданным для компонента, запускающего транзакцию, либо параметром времени ожидания на уровне компьютера, на котором работает этот компонент.</span><span class="sxs-lookup"><span data-stu-id="0f10b-131">This is determined either by the transaction time-out value set for the component initiating the transaction or by the machine-wide time-out setting for the machine where that component is running.</span></span> <span data-ttu-id="0f10b-132">При выполнении множества операций в рамках транзакции рекомендуется установить для соответствующего времени ожидания транзакции достаточно длинное значение и при необходимости восстановить первоначальный параметр по завершении.</span><span class="sxs-lookup"><span data-stu-id="0f10b-132">If you are doing numerous operations within a transaction, it is advisable to set the appropriate transaction time-out period to a sufficiently long value and, if necessary, to restore the original setting when you are finished.</span></span>

## <a name="non-transactional-com-catalog-resources"></a><span data-ttu-id="0f10b-133">Нетранзакционные ресурсы каталога COM+</span><span class="sxs-lookup"><span data-stu-id="0f10b-133">Non-Transactional COM+ Catalog Resources</span></span>

<span data-ttu-id="0f10b-134">Реестр, файловая система и установщик Windows (MSI) являются ресурсами каталога COM+, которые не являются транзакционными.</span><span class="sxs-lookup"><span data-stu-id="0f10b-134">The registry, the file system, and Windows Installer (MSI) are COM+ catalog resources that are not transactional.</span></span>

> [!Note]  
> <span data-ttu-id="0f10b-135">Если возникает ошибка, которая прерывает транзакцию, изменения этих ресурсов могут быть не отменены.</span><span class="sxs-lookup"><span data-stu-id="0f10b-135">If there is an error that aborts a transaction, changes to these resources may not be rolled back.</span></span>

 

<span data-ttu-id="0f10b-136">Если при установке существующего приложения COM+ из MSI-файла возникла ошибка, приложение не отображается в оснастке "службы компонентов", но может появиться в окне "Установка и удаление программ". в этом случае его необходимо удалить вручную.</span><span class="sxs-lookup"><span data-stu-id="0f10b-136">If there is an error while installing an existing COM+ application from an .msi file, the application doesn't appear in the Component Services snap-in but it might appear in Add/Remove programs, in which case you need to manually remove it.</span></span>

## <a name="recovering-in-the-event-of-system-hangs"></a><span data-ttu-id="0f10b-137">Восстановление в случае зависания системы</span><span class="sxs-lookup"><span data-stu-id="0f10b-137">Recovering in the Event of System Hangs</span></span>

<span data-ttu-id="0f10b-138">Если компонент, выполняющий операции администрирования в рамках транзакции, должен зависнуть в то время, когда он удерживает блокировку записи в коде сервера каталога, он блокирует внесение любых изменений в каталог всем остальным.</span><span class="sxs-lookup"><span data-stu-id="0f10b-138">If a component doing administration operations within a transaction were to hang while it holds a writer lock on the catalog server code, it would block everyone else from making any changes to the catalog.</span></span> <span data-ttu-id="0f10b-139">В этом случае можно снять блокировку каталога, завершив и перезапустив Системное приложение.</span><span class="sxs-lookup"><span data-stu-id="0f10b-139">Should this happen, you can clear the lock on the catalog by shutting down and restarting the System application.</span></span>

## <a name="scripting-with-a-transactioncontext-object"></a><span data-ttu-id="0f10b-140">Создание сценариев с помощью объекта Трансактионконтекст</span><span class="sxs-lookup"><span data-stu-id="0f10b-140">Scripting with a TransactionContext Object</span></span>

<span data-ttu-id="0f10b-141">Простым способом администрирования операций в транзакциях является использование объекта [**трансактионконтекст**](transactioncontext.md) для управления транзакцией.</span><span class="sxs-lookup"><span data-stu-id="0f10b-141">A simple way to do administration operations within transactions is to use a [**TransactionContext**](transactioncontext.md) object to control the transaction.</span></span> <span data-ttu-id="0f10b-142">Например, следующий сценарий Visual Basic демонстрирует, как добавить в приложение два новых приложения, чтобы одновременно не создавалось оба приложения или ни одно из них:</span><span class="sxs-lookup"><span data-stu-id="0f10b-142">For example, the following Visual Basic script demonstrates how to transactionally add two new applications so that either both applications or neither application is created:</span></span>


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a><span data-ttu-id="0f10b-143">См. также</span><span class="sxs-lookup"><span data-stu-id="0f10b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f10b-144">Обработка ошибок администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="0f10b-144">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="0f10b-145">Вводный пример с использованием каталога администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="0f10b-145">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="0f10b-146">Общие сведения об объектах Комадмин</span><span class="sxs-lookup"><span data-stu-id="0f10b-146">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="0f10b-147">Получение коллекций в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="0f10b-147">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="0f10b-148">Установка свойств и сохранение изменений в каталоге COM+</span><span class="sxs-lookup"><span data-stu-id="0f10b-148">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



