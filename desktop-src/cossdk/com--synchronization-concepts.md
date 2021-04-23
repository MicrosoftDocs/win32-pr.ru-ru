---
description: Как правило, синхронизация не требуется, если имеется однопотоковое подразделение (STA), так как подразделение обеспечивает синхронизацию.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Основные понятия синхронизации COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807810"
---
# <a name="com-synchronization-concepts"></a><span data-ttu-id="553e3-103">Основные понятия синхронизации COM+</span><span class="sxs-lookup"><span data-stu-id="553e3-103">COM+ Synchronization Concepts</span></span>

<span data-ttu-id="553e3-104">Как правило, синхронизация не требуется, если имеется однопотоковое подразделение (STA), так как подразделение обеспечивает синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="553e3-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="553e3-105">Синхронизация важна при наличии многопоточного апартамента (MTA) и объекта с произвольным потоком.</span><span class="sxs-lookup"><span data-stu-id="553e3-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="553e3-106">В прошлом объекты, работающие в свободной потоке, вынуждены обрабатывали блокировку.</span><span class="sxs-lookup"><span data-stu-id="553e3-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="553e3-107">Можно исключить необходимость использования блокировки, задав атрибут синхронизации для компонента.</span><span class="sxs-lookup"><span data-stu-id="553e3-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="553e3-108">Синхронизация имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="553e3-108">Synchronization has the following properties:</span></span>

-   <span data-ttu-id="553e3-109">Позволяет одному вызывающему объекту вводить компонент за раз.</span><span class="sxs-lookup"><span data-stu-id="553e3-109">Allows one caller to enter the component at a time.</span></span>
-   <span data-ttu-id="553e3-110">Запрещает поток в процессе или на компьютере.</span><span class="sxs-lookup"><span data-stu-id="553e3-110">Prohibits flow across process or across computer.</span></span>
-   <span data-ttu-id="553e3-111">Перетекает из компонента в компонент внутри процесса.</span><span class="sxs-lookup"><span data-stu-id="553e3-111">Flows from component to component within a process.</span></span>
-   <span data-ttu-id="553e3-112">Разрешает повторное вход из того же вызывающего.</span><span class="sxs-lookup"><span data-stu-id="553e3-112">Allows reentrancy from the same caller.</span></span>

<span data-ttu-id="553e3-113">В отличие от подразделения, действия охватывают контексты от нескольких процессов и узлов.</span><span class="sxs-lookup"><span data-stu-id="553e3-113">Unlike apartments, activities span contexts from multiple processes and hosts.</span></span> <span data-ttu-id="553e3-114">Синхронизация определяет, какое действие будет содержать объект.</span><span class="sxs-lookup"><span data-stu-id="553e3-114">Synchronization determines which activity will contain an object.</span></span> <span data-ttu-id="553e3-115">Объекты могут находиться в любом из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="553e3-115">Objects can reside in any of the following activities:</span></span>

-   <span data-ttu-id="553e3-116">Действие создателя</span><span class="sxs-lookup"><span data-stu-id="553e3-116">Creator's activity</span></span>
-   <span data-ttu-id="553e3-117">Новое действие</span><span class="sxs-lookup"><span data-stu-id="553e3-117">New activity</span></span>
-   <span data-ttu-id="553e3-118">Нет действий</span><span class="sxs-lookup"><span data-stu-id="553e3-118">No activity</span></span>

<span data-ttu-id="553e3-119">COM+ обеспечивает параллелизм с помощью ряда блокировок для каждого действия.</span><span class="sxs-lookup"><span data-stu-id="553e3-119">COM+ ensures concurrency by a series of locks for each activity.</span></span> <span data-ttu-id="553e3-120">Если вызывающий объект пытается ввести синхронизированный компонент COM+, который уже используется другим вызывающим объектом, вызов блокируется до тех пор, пока блокировка не будет снята.</span><span class="sxs-lookup"><span data-stu-id="553e3-120">If a caller tries to enter a COM+ synchronized component that is already being used by another caller, the call is blocked until the lock is released.</span></span> <span data-ttu-id="553e3-121">Это поведение блокировки не будет истекает и его нельзя настроить для истечения времени ожидания. Если блокировка не используется, блокировка запрашивается и обрабатывается вызов.</span><span class="sxs-lookup"><span data-stu-id="553e3-121">This blocking behavior will not time out and cannot be configured to time out. If the lock is not in use, the lock is acquired and the call is processed.</span></span> <span data-ttu-id="553e3-122">После завершения этого процесса блокировка освобождается для следующего вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="553e3-122">After completing, the lock is released for the next caller.</span></span> <span data-ttu-id="553e3-123">Чтобы предотвратить взаимоблокировку, COM+ управляет доступом ко всем объектам в действиях во вложенном ряде вызовов, связанных по сети.</span><span class="sxs-lookup"><span data-stu-id="553e3-123">To prevent deadlock, COM+ manages access to all objects across activities by a nested series of calls chained throughout the network.</span></span>

<span data-ttu-id="553e3-124">COM+ предоставляет следующие параметры синхронизации:</span><span class="sxs-lookup"><span data-stu-id="553e3-124">COM+ provides the following synchronization settings:</span></span>

-   <span data-ttu-id="553e3-125">Выключено</span><span class="sxs-lookup"><span data-stu-id="553e3-125">Disabled</span></span>
-   <span data-ttu-id="553e3-126">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="553e3-126">Not Supported</span></span>
-   <span data-ttu-id="553e3-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="553e3-127">Supported</span></span>
-   <span data-ttu-id="553e3-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="553e3-128">Required</span></span>
-   <span data-ttu-id="553e3-129">RequiresNew</span><span class="sxs-lookup"><span data-stu-id="553e3-129">Requires New</span></span>

> [!Note]  
> <span data-ttu-id="553e3-130">Некоторые параметры синхронизации работают совместно с другими параметрами компонента COM+.</span><span class="sxs-lookup"><span data-stu-id="553e3-130">Some synchronization settings work in conjunction with other COM+ component settings.</span></span> <span data-ttu-id="553e3-131">Например, если включена служба [JIT-активации COM+](com--just-in-time-activation.md) , требуется синхронизация.</span><span class="sxs-lookup"><span data-stu-id="553e3-131">For example, synchronization is required if the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service is enabled.</span></span> <span data-ttu-id="553e3-132">При включении транзакций JIT-компилятор является обязательным. Таким образом, для [обработки транзакций](com--transactions.md) com+ также требуется синхронизация.</span><span class="sxs-lookup"><span data-stu-id="553e3-132">JIT is required if you enable transactions; therefore, COM+ [transaction processing](com--transactions.md) requires synchronization as well.</span></span> <span data-ttu-id="553e3-133">Таким образом, классы с параметром JIT = true также должны иметь параметр синхронизации = Required или Synchronization = RequiresNew.</span><span class="sxs-lookup"><span data-stu-id="553e3-133">So, classes with the setting of JIT=True must also have the setting of either Synchronization=Required or Synchronization=RequiresNew.</span></span>

 

<span data-ttu-id="553e3-134">Инструкции по настройке параметров синхронизации с помощью средства администрирования "службы компонентов" см. в разделе [Установка атрибута синхронизации](setting-the-synchronization-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="553e3-134">For instructions about setting synchronization options by using the Component Services administrative tool, see [Setting the Synchronization Attribute](setting-the-synchronization-attribute.md).</span></span>

<span data-ttu-id="553e3-135">Дополнительные сведения об использовании библиотеки администрирования COM+ для настройки параметров синхронизации см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="553e3-135">To obtain more information on using the COM+ Administration Library to set synchronization options, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="553e3-136">См. также</span><span class="sxs-lookup"><span data-stu-id="553e3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="553e3-137">Задачи синхронизации COM+</span><span class="sxs-lookup"><span data-stu-id="553e3-137">COM+ Synchronization Tasks</span></span>](com--synchronization-tasks.md)
</dt> </dl>

 

 



