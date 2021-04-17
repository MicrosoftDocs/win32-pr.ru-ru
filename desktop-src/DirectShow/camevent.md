---
description: Класс Камевент является оболочкой для событий ручного сброса и автоматического сброса.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Класс Камевент (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665432"
---
# <a name="camevent-class"></a><span data-ttu-id="fae3a-103">Класс Камевент</span><span class="sxs-lookup"><span data-stu-id="fae3a-103">CAMEvent class</span></span>

![Иерархия классов камевент](images/util06.png)

<span data-ttu-id="fae3a-105">Класс **камевент** является оболочкой для событий ручного сброса и автоматического сброса.</span><span class="sxs-lookup"><span data-stu-id="fae3a-105">The **CAMEvent** class is a wrapper for manual-reset and auto-reset events.</span></span>

<span data-ttu-id="fae3a-106">Этот класс предоставляет удобный способ управления событиями вместо вызова таких функций, как [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)и [**ресетевент**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span><span class="sxs-lookup"><span data-stu-id="fae3a-106">This class provides a convenient way to manage events, rather than calling functions such as [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), and [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span></span>



| <span data-ttu-id="fae3a-107">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="fae3a-107">Protected Member Variables</span></span>                          | <span data-ttu-id="fae3a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fae3a-108">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="fae3a-109">**m \_ Хевент**</span><span class="sxs-lookup"><span data-stu-id="fae3a-109">**m\_hEvent**</span></span>](camevent-m-hevent.md)              | <span data-ttu-id="fae3a-110">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="fae3a-110">Event handle.</span></span>                                                   |
| <span data-ttu-id="fae3a-111">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="fae3a-111">Public Methods</span></span>                                      | <span data-ttu-id="fae3a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fae3a-112">Description</span></span>                                                     |
| [<span data-ttu-id="fae3a-113">**камевент**</span><span class="sxs-lookup"><span data-stu-id="fae3a-113">**CAMEvent**</span></span>](camevent-camevent.md)               | <span data-ttu-id="fae3a-114">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="fae3a-114">Constructor method.</span></span>                                             |
| [<span data-ttu-id="fae3a-115">**~ Камевент**</span><span class="sxs-lookup"><span data-stu-id="fae3a-115">**~CAMEvent**</span></span>](camevent--camevent.md)             | <span data-ttu-id="fae3a-116">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="fae3a-116">Destructor method.</span></span>                                              |
| [<span data-ttu-id="fae3a-117">**службы "Функции Azure"**</span><span class="sxs-lookup"><span data-stu-id="fae3a-117">**Check**</span></span>](camevent-check.md)                     | <span data-ttu-id="fae3a-118">Проверяет, задано ли событие, без блокировки.</span><span class="sxs-lookup"><span data-stu-id="fae3a-118">Checks whether the event is set, without blocking.</span></span>              |
| [<span data-ttu-id="fae3a-119">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="fae3a-119">**Reset**</span></span>](camevent-reset.md)                     | <span data-ttu-id="fae3a-120">Задает несигнальное состояние события.</span><span class="sxs-lookup"><span data-stu-id="fae3a-120">Sets the state of the event to nonsignaled.</span></span>                     |
| [<span data-ttu-id="fae3a-121">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="fae3a-121">**Set**</span></span>](camevent-set.md)                         | <span data-ttu-id="fae3a-122">Сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="fae3a-122">Signals the event.</span></span>                                              |
| [<span data-ttu-id="fae3a-123">**Ожидание**</span><span class="sxs-lookup"><span data-stu-id="fae3a-123">**Wait**</span></span>](camevent-wait.md)                       | <span data-ttu-id="fae3a-124">Блокируется до получения сигнала о событии или до истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="fae3a-124">Blocks until the event is signaled, or until a time-out occurs.</span></span> |
| <span data-ttu-id="fae3a-125">Операторы</span><span class="sxs-lookup"><span data-stu-id="fae3a-125">Operators</span></span>                                           | <span data-ttu-id="fae3a-126">Описание:</span><span class="sxs-lookup"><span data-stu-id="fae3a-126">Description</span></span>                                                     |
| [<span data-ttu-id="fae3a-127">**МАРКЕР оператора**</span><span class="sxs-lookup"><span data-stu-id="fae3a-127">**operator HANDLE**</span></span>](camevent-operator-handle.md) | <span data-ttu-id="fae3a-128">Получает маркер события.</span><span class="sxs-lookup"><span data-stu-id="fae3a-128">Retrieves the event handle.</span></span>                                     |



 

## <a name="requirements"></a><span data-ttu-id="fae3a-129">Требования</span><span class="sxs-lookup"><span data-stu-id="fae3a-129">Requirements</span></span>



| <span data-ttu-id="fae3a-130">Требование</span><span class="sxs-lookup"><span data-stu-id="fae3a-130">Requirement</span></span> | <span data-ttu-id="fae3a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fae3a-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae3a-132">Header</span><span class="sxs-lookup"><span data-stu-id="fae3a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="fae3a-133"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fae3a-133"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fae3a-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fae3a-134">Library</span></span><br/> | <dl> <span data-ttu-id="fae3a-135"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fae3a-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

