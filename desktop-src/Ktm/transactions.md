---
description: Транзакция — это объект, определяющий логическую единицу работы.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Транзакции (диспетчер транзакций ядра)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673597"
---
# <a name="transactions"></a><span data-ttu-id="df3d6-103">Transactions</span><span class="sxs-lookup"><span data-stu-id="df3d6-103">Transactions</span></span>

<span data-ttu-id="df3d6-104">Транзакция — это объект, определяющий логическую единицу работы.</span><span class="sxs-lookup"><span data-stu-id="df3d6-104">A transaction is an object that defines a logical unit of work.</span></span> <span data-ttu-id="df3d6-105">Транзакция выполняется до тех пор, пока существует обработчик, ссылающийся на эту транзакцию, и считается активным, если транзакция еще не была зафиксирована или не была выполнена ее откат.</span><span class="sxs-lookup"><span data-stu-id="df3d6-105">The transaction is alive as long as there is a handle referencing the transaction and it is considered active if the transaction has not yet been committed or rolled back.</span></span> <span data-ttu-id="df3d6-106">Если транзакция создана и все ее дескрипторы были закрыты до выполнения фиксации или отката, то будет выполнен откат транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-106">If a transaction is created and all handles to it have been closed before a commit or rollback occurs, the transaction will be rolled back.</span></span>

<span data-ttu-id="df3d6-107">Рассмотрим случай транзакционного клиента пользовательского режима, который создает транзакцию для определения области ее операций, а затем выполняет обновления в одном или нескольких диспетчерах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df3d6-107">Consider the case of a user-mode transactional client that creates a transaction to scope its operations, then performs updates on one or more resource managers.</span></span> <span data-ttu-id="df3d6-108">Происходят следующие события.</span><span class="sxs-lookup"><span data-stu-id="df3d6-108">The following occurs:</span></span>

1.  <span data-ttu-id="df3d6-109">Клиент вызывает функцию [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) для создания транзакции и получает в качестве возвращаемого значения маркер этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-109">The client calls the [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) function to create the transaction and receives a handle to that transaction as the return value.</span></span>

    <span data-ttu-id="df3d6-110">Транзакция может быть открыта или унаследована любым количеством процессов. Поэтому каждый процесс участвует в транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-110">The transaction can be opened or inherited by any number of processes; each process is thus involved in the transaction.</span></span> <span data-ttu-id="df3d6-111">Сбой любого из этих процессов приведет к прерыванию транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-111">The failure of any of these processes will cause the transaction to abort.</span></span>

    <span data-ttu-id="df3d6-112">Эта транзакция еще не может быть постоянной.</span><span class="sxs-lookup"><span data-stu-id="df3d6-112">This transaction may not yet be persistent.</span></span> <span data-ttu-id="df3d6-113">Только транзакции, которые достигли подготовленного состояния, должны быть восстановлены между сбоями системы, если в транзакции используется ведение журнала с предполагаемым преобразованием.</span><span class="sxs-lookup"><span data-stu-id="df3d6-113">Only transactions that have reached the prepared state must be recovered across system failures if the transaction uses presumed-abort logging.</span></span>

2.  <span data-ttu-id="df3d6-114">Клиент должен явно передать транзакцию в Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="df3d6-114">The client must pass a transaction to the resource manager explicitly.</span></span>
3.  <span data-ttu-id="df3d6-115">Клиент выполняет все свои транзакционные операции с одним или несколькими службами RMs, такими как транзакционные файловые системы.</span><span class="sxs-lookup"><span data-stu-id="df3d6-115">The client performs all its transactional operations with one or more RMs, such as transacted file systems.</span></span>
4.  <span data-ttu-id="df3d6-116">Клиент вызывает функцию [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .</span><span class="sxs-lookup"><span data-stu-id="df3d6-116">The client calls the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function.</span></span>
5.  <span data-ttu-id="df3d6-117">Диспетчер ресурсов получает уведомления от KTM для подготовки и фиксации своих данных.</span><span class="sxs-lookup"><span data-stu-id="df3d6-117">The resource manager receives notifications from KTM to prepare and commit its data.</span></span>

## <a name="transactions-and-threads"></a><span data-ttu-id="df3d6-118">Транзакции и потоки</span><span class="sxs-lookup"><span data-stu-id="df3d6-118">Transactions and Threads</span></span>

<span data-ttu-id="df3d6-119">Транзакции не совпадают с потоками.</span><span class="sxs-lookup"><span data-stu-id="df3d6-119">Transactions are not the same as threads.</span></span> <span data-ttu-id="df3d6-120">Несколько потоков или процессов могут быть частью одной транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-120">Multiple threads or processes can be a part of a single transaction.</span></span> <span data-ttu-id="df3d6-121">И наоборот, поток может быть частью нескольких разных транзакций в разное время.</span><span class="sxs-lookup"><span data-stu-id="df3d6-121">Conversely, a thread can be a part of several different transactions at different times.</span></span>

## <a name="transaction-functions"></a><span data-ttu-id="df3d6-122">Функции транзакций</span><span class="sxs-lookup"><span data-stu-id="df3d6-122">Transaction Functions</span></span>

<span data-ttu-id="df3d6-123">В транзакциях используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-123">The following functions are used with transactions.</span></span>



| <span data-ttu-id="df3d6-124">Функция</span><span class="sxs-lookup"><span data-stu-id="df3d6-124">Function</span></span>                                                            | <span data-ttu-id="df3d6-125">Описание</span><span class="sxs-lookup"><span data-stu-id="df3d6-125">Description</span></span>                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df3d6-126">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="df3d6-126">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | <span data-ttu-id="df3d6-127">Запрашивает фиксацию указанной транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-127">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="df3d6-128">**коммиттрансактионасинк**</span><span class="sxs-lookup"><span data-stu-id="df3d6-128">**CommitTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | <span data-ttu-id="df3d6-129">Запрашивает фиксацию указанной транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-129">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="df3d6-130">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="df3d6-130">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | <span data-ttu-id="df3d6-131">Создает новый объект Transaction.</span><span class="sxs-lookup"><span data-stu-id="df3d6-131">Creates a new transaction object.</span></span>                                                             |
| [<span data-ttu-id="df3d6-132">**жеттрансактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="df3d6-132">**GetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | <span data-ttu-id="df3d6-133">Возвращает запрошенные сведения об указанной транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-133">Returns the requested information about the specified transaction.</span></span>                            |
| [<span data-ttu-id="df3d6-134">**опентрансактион**</span><span class="sxs-lookup"><span data-stu-id="df3d6-134">**OpenTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | <span data-ttu-id="df3d6-135">Открывает существующую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="df3d6-135">Opens an existing transaction.</span></span>                                                                |
| [<span data-ttu-id="df3d6-136">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="df3d6-136">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | <span data-ttu-id="df3d6-137">Запросы, для которых была произведена откат указанной транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-137">Requests that the specified transaction be rolled back.</span></span>                                       |
| [<span data-ttu-id="df3d6-138">**роллбакктрансактионасинк**</span><span class="sxs-lookup"><span data-stu-id="df3d6-138">**RollbackTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | <span data-ttu-id="df3d6-139">Запросы, для которых была произведена откат указанной транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-139">Requests that the specified transaction be rolled back.</span></span> <span data-ttu-id="df3d6-140">Эта функция возвращает асинхронно.</span><span class="sxs-lookup"><span data-stu-id="df3d6-140">This function returns asynchronously.</span></span> |
| [<span data-ttu-id="df3d6-141">**сеттрансактионинформатион**</span><span class="sxs-lookup"><span data-stu-id="df3d6-141">**SetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | <span data-ttu-id="df3d6-142">Задает сведения о транзакции для указанной транзакции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-142">Sets the transaction information for the specified transaction.</span></span>                               |



 

 

 



