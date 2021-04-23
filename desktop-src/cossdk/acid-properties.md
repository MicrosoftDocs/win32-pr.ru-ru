---
description: С помощью последовательностей обработки транзакций аббревиатура ACID означает атомарную, непротиворечивую, изолированную и устойчивую.
ms.assetid: 857d145c-710d-4097-8ed6-df11e8d52228
title: Свойства ACID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2e725cae75b4aa80d25f2959d474e8baa05f70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141386"
---
# <a name="acid-properties"></a><span data-ttu-id="48302-103">Свойства ACID</span><span class="sxs-lookup"><span data-stu-id="48302-103">ACID Properties</span></span>

<span data-ttu-id="48302-104">С помощью последовательностей обработки транзакций аббревиатура ACID означает атомарную, непротиворечивую, изолированную и устойчивую.</span><span class="sxs-lookup"><span data-stu-id="48302-104">Coined by transaction processing pioneers, the acronym ACID stands for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="48302-105">Чтобы обеспечить предсказуемое поведение, всем транзакциям должны быть предоставлены эти базовые свойства, что позволяет получить роль критически важных транзакций как все или ни одно.</span><span class="sxs-lookup"><span data-stu-id="48302-105">To ensure predictable behavior, all transactions must possess these basic properties, reinforcing the role of mission-critical transactions as all-or-none propositions.</span></span>

<span data-ttu-id="48302-106">Следующий список содержит определение и описание каждого свойства ACID:</span><span class="sxs-lookup"><span data-stu-id="48302-106">The following list contains a definition and a description of each ACID property:</span></span>

<dl> <dt>

<span data-ttu-id="48302-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>At</span><span class="sxs-lookup"><span data-stu-id="48302-107"><span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atomic</span></span>
</dt> <dd>

<span data-ttu-id="48302-108">Транзакция должна выполняться только один раз и должна быть атомарной — либо вся работа выполняется, либо ни одна из них не является.</span><span class="sxs-lookup"><span data-stu-id="48302-108">A transaction must execute exactly once and must be atomic—either all of the work is done or none of it is.</span></span> <span data-ttu-id="48302-109">Операции в рамках транзакции обычно имеют общую цель и являются взаимозависимыми.</span><span class="sxs-lookup"><span data-stu-id="48302-109">Operations within a transaction usually share a common intent and are interdependent.</span></span> <span data-ttu-id="48302-110">Выполняя только подмножество этих операций, система может нарушить общую цель транзакции.</span><span class="sxs-lookup"><span data-stu-id="48302-110">By performing only a subset of these operations, the system could compromise the overall intent of the transaction.</span></span> <span data-ttu-id="48302-111">Атомарность устраняет вероятность обработки только подмножества операций.</span><span class="sxs-lookup"><span data-stu-id="48302-111">Atomicity eliminates the chance of processing only a subset of operations.</span></span>

</dd> <dt>

<span data-ttu-id="48302-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Стабильны</span><span class="sxs-lookup"><span data-stu-id="48302-112"><span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistent</span></span>
</dt> <dd>

<span data-ttu-id="48302-113">Транзакция должна сохранить согласованность данных, преобразуя одно согласованное состояние данных в другое согласованное состояние данных.</span><span class="sxs-lookup"><span data-stu-id="48302-113">A transaction must preserve the consistency of data, transforming one consistent state of data into another consistent state of data.</span></span> <span data-ttu-id="48302-114">Большая часть ответственности за поддержание согласованности относится к разработчику приложения.</span><span class="sxs-lookup"><span data-stu-id="48302-114">Much of the responsibility for maintaining consistency falls to the application developer.</span></span>

</dd> <dt>

<span data-ttu-id="48302-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Изолирован</span><span class="sxs-lookup"><span data-stu-id="48302-115"><span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>Isolated</span></span>
</dt> <dd>

<span data-ttu-id="48302-116">Транзакция должна быть единицей изоляции, что означает, что параллельные транзакции должны вести себя так, будто каждая из них была единственной транзакцией, запущенной в системе.</span><span class="sxs-lookup"><span data-stu-id="48302-116">A transaction must be a unit of isolation, which means that concurrent transactions should behave as if each were the only transaction running in the system.</span></span> <span data-ttu-id="48302-117">Так как высокий уровень изоляции может ограничивать количество параллельных транзакций, некоторые приложения уменьшают уровень изоляции в Exchange для повышения пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="48302-117">Because a high degree of isolation can limit the number of concurrent transactions, some applications reduce the isolation level in exchange for better throughput.</span></span> <span data-ttu-id="48302-118">Дополнительные сведения см. в разделе [Настройка уровней изоляции транзакций](configuring-transaction-isolation-levels.md) .</span><span class="sxs-lookup"><span data-stu-id="48302-118">See [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="48302-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Надежно</span><span class="sxs-lookup"><span data-stu-id="48302-119"><span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable</span></span>
</dt> <dd>

<span data-ttu-id="48302-120">Транзакция должна быть восстановлена и, следовательно, должна иметь устойчивость.</span><span class="sxs-lookup"><span data-stu-id="48302-120">A transaction must be recoverable and therefore must have durability.</span></span> <span data-ttu-id="48302-121">Если транзакция фиксируется, система гарантирует, что ее обновления могут сохраняться даже в случае сбоя компьютера сразу после фиксации.</span><span class="sxs-lookup"><span data-stu-id="48302-121">If a transaction commits, the system guarantees that its updates can persist even if the computer crashes immediately after the commit.</span></span> <span data-ttu-id="48302-122">Специализированное ведение журнала позволяет процедуре перезапуска системы выполнять незавершенные операции, требуемые транзакцией, делая ее устойчивой.</span><span class="sxs-lookup"><span data-stu-id="48302-122">Specialized logging allows the system's restart procedure to complete unfinished operations required by the transaction, making the transaction durable.</span></span>

</dd> </dl>

 

 



