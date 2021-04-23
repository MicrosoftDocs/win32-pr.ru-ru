---
description: Класс Кбасемедиафилтер реализует интерфейс Имедиафилтер.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Класс Кбасемедиафилтер (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665409"
---
# <a name="cbasemediafilter-class"></a><span data-ttu-id="d10cb-103">Класс Кбасемедиафилтер</span><span class="sxs-lookup"><span data-stu-id="d10cb-103">CBaseMediaFilter class</span></span>

![кбасемедиафилтер](images/filter05.png)

<span data-ttu-id="d10cb-105">`CBaseMediaFilter`Класс реализует интерфейс [**имедиафилтер**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) .</span><span class="sxs-lookup"><span data-stu-id="d10cb-105">The `CBaseMediaFilter` class implements the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface.</span></span> <span data-ttu-id="d10cb-106">Используйте этот класс для распространителей подключаемых модулей или других объектов, которым требуется поддержка **имедиафилтер** без поддержки интерфейса [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="d10cb-106">Use this class for plug-in distributors or other objects that need to support **IMediaFilter** without supporting the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="d10cb-107">Не используйте этот класс для фильтров.</span><span class="sxs-lookup"><span data-stu-id="d10cb-107">Do not use this class for filters.</span></span> <span data-ttu-id="d10cb-108">Вместо этого используйте класс [**кбасефилтер**](cbasefilter.md) или базовый класс, производный от **кбасефилтер**.</span><span class="sxs-lookup"><span data-stu-id="d10cb-108">Instead, use the [**CBaseFilter**](cbasefilter.md) class, or a base class derived from **CBaseFilter**.</span></span>



| <span data-ttu-id="d10cb-109">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="d10cb-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="d10cb-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d10cb-110">Description</span></span>                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d10cb-111">**\_штат m**</span><span class="sxs-lookup"><span data-stu-id="d10cb-111">**m\_State**</span></span>](cbasemediafilter-m-state.md)                     | <span data-ttu-id="d10cb-112">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d10cb-112">Current state of the object.</span></span>                                 |
| [<span data-ttu-id="d10cb-113">**m \_ пклокк**</span><span class="sxs-lookup"><span data-stu-id="d10cb-113">**m\_pClock**</span></span>](cbasemediafilter-m-pclock.md)                   | <span data-ttu-id="d10cb-114">Указатель на время обращения к объекту.</span><span class="sxs-lookup"><span data-stu-id="d10cb-114">Pointer to the object's reference clock.</span></span>                     |
| [<span data-ttu-id="d10cb-115">**m \_ тстарт**</span><span class="sxs-lookup"><span data-stu-id="d10cb-115">**m\_tStart**</span></span>](cbasemediafilter-m-tstart.md)                   | <span data-ttu-id="d10cb-116">Справочное время, соответствующее времени потока 0.</span><span class="sxs-lookup"><span data-stu-id="d10cb-116">Reference time that corresponds to stream time 0.</span></span>            |
| [<span data-ttu-id="d10cb-117">**m \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="d10cb-117">**m\_clsid**</span></span>](cbasemediafilter-m-clsid.md)                     | <span data-ttu-id="d10cb-118">Идентификатор класса (CLSID) объекта.</span><span class="sxs-lookup"><span data-stu-id="d10cb-118">Class identifier (CLSID) of the object.</span></span>                      |
| [<span data-ttu-id="d10cb-119">**m \_ плокк**</span><span class="sxs-lookup"><span data-stu-id="d10cb-119">**m\_pLock**</span></span>](cbasemediafilter-m-plock.md)                     | <span data-ttu-id="d10cb-120">Указатель на критическую секцию.</span><span class="sxs-lookup"><span data-stu-id="d10cb-120">Pointer to a critical section.</span></span>                               |
| <span data-ttu-id="d10cb-121">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="d10cb-121">Public Methods</span></span>                                                   | <span data-ttu-id="d10cb-122">Описание</span><span class="sxs-lookup"><span data-stu-id="d10cb-122">Description</span></span>                                                  |
| [<span data-ttu-id="d10cb-123">**кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="d10cb-123">**CBaseMediaFilter**</span></span>](cbasemediafilter-cbasemediafilter.md)    | <span data-ttu-id="d10cb-124">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="d10cb-124">Constructor method.</span></span>                                          |
| [<span data-ttu-id="d10cb-125">**~ Кбасемедиафилтер**</span><span class="sxs-lookup"><span data-stu-id="d10cb-125">**~ CBaseMediaFilter**</span></span>](cbasemediafilter--cbasemediafilter.md) | <span data-ttu-id="d10cb-126">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="d10cb-126">Destructor method.</span></span> <span data-ttu-id="d10cb-127">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="d10cb-127">Virtual.</span></span>                                  |
| [<span data-ttu-id="d10cb-128">**стреамтиме**</span><span class="sxs-lookup"><span data-stu-id="d10cb-128">**StreamTime**</span></span>](cbasemediafilter-streamtime.md)                | <span data-ttu-id="d10cb-129">Извлекает текущее время потока.</span><span class="sxs-lookup"><span data-stu-id="d10cb-129">Retrieves the current stream time.</span></span> <span data-ttu-id="d10cb-130">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="d10cb-130">Virtual.</span></span>                  |
| [<span data-ttu-id="d10cb-131">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="d10cb-131">**IsActive**</span></span>](cbasemediafilter-isactive.md)                    | <span data-ttu-id="d10cb-132">Определяет, является ли объект активным (запущен или приостановлен).</span><span class="sxs-lookup"><span data-stu-id="d10cb-132">Determines whether the object is active (running or paused).</span></span> |
| <span data-ttu-id="d10cb-133">Методы IPersist</span><span class="sxs-lookup"><span data-stu-id="d10cb-133">IPersist Methods</span></span>                                                 | <span data-ttu-id="d10cb-134">Описание</span><span class="sxs-lookup"><span data-stu-id="d10cb-134">Description</span></span>                                                  |
| [<span data-ttu-id="d10cb-135">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="d10cb-135">**GetClassID**</span></span>](cbasemediafilter-getclassid.md)                | <span data-ttu-id="d10cb-136">Получает идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="d10cb-136">Retrieves the class identifier.</span></span>                              |
| <span data-ttu-id="d10cb-137">Методы Имедиафилтер</span><span class="sxs-lookup"><span data-stu-id="d10cb-137">IMediaFilter Methods</span></span>                                             | <span data-ttu-id="d10cb-138">Описание</span><span class="sxs-lookup"><span data-stu-id="d10cb-138">Description</span></span>                                                  |
| [<span data-ttu-id="d10cb-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="d10cb-139">**GetState**</span></span>](cbasemediafilter-getstate.md)                    | <span data-ttu-id="d10cb-140">Получает состояние объекта (запущен, остановлен или приостановлен).</span><span class="sxs-lookup"><span data-stu-id="d10cb-140">Retrieves the object's state (running, stopped, or paused).</span></span>  |
| [<span data-ttu-id="d10cb-141">**сетсинксаурце**</span><span class="sxs-lookup"><span data-stu-id="d10cb-141">**SetSyncSource**</span></span>](cbasemediafilter-setsyncsource.md)          | <span data-ttu-id="d10cb-142">Задает время ссылки для объекта.</span><span class="sxs-lookup"><span data-stu-id="d10cb-142">Sets a reference clock for the object.</span></span>                       |
| [<span data-ttu-id="d10cb-143">**жетсинксаурце**</span><span class="sxs-lookup"><span data-stu-id="d10cb-143">**GetSyncSource**</span></span>](cbasemediafilter-getsyncsource.md)          | <span data-ttu-id="d10cb-144">Извлекает ссылочное время, которое использует объект.</span><span class="sxs-lookup"><span data-stu-id="d10cb-144">Retrieves the reference clock that the object is using.</span></span>      |
| [<span data-ttu-id="d10cb-145">**Stop**</span><span class="sxs-lookup"><span data-stu-id="d10cb-145">**Stop**</span></span>](cbasemediafilter-stop.md)                            | <span data-ttu-id="d10cb-146">Останавливает объект.</span><span class="sxs-lookup"><span data-stu-id="d10cb-146">Stops the object.</span></span>                                            |
| [<span data-ttu-id="d10cb-147">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="d10cb-147">**Pause**</span></span>](cbasemediafilter-pause.md)                          | <span data-ttu-id="d10cb-148">Приостанавливает работу объекта.</span><span class="sxs-lookup"><span data-stu-id="d10cb-148">Pauses the object.</span></span>                                           |
| [<span data-ttu-id="d10cb-149">**Выполнить**</span><span class="sxs-lookup"><span data-stu-id="d10cb-149">**Run**</span></span>](cbasemediafilter-run.md)                              | <span data-ttu-id="d10cb-150">Запускает объект.</span><span class="sxs-lookup"><span data-stu-id="d10cb-150">Runs the object.</span></span>                                             |



 

## <a name="requirements"></a><span data-ttu-id="d10cb-151">Требования</span><span class="sxs-lookup"><span data-stu-id="d10cb-151">Requirements</span></span>



| <span data-ttu-id="d10cb-152">Требование</span><span class="sxs-lookup"><span data-stu-id="d10cb-152">Requirement</span></span> | <span data-ttu-id="d10cb-153">Значение</span><span class="sxs-lookup"><span data-stu-id="d10cb-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10cb-154">Header</span><span class="sxs-lookup"><span data-stu-id="d10cb-154">Header</span></span><br/>  | <dl> <span data-ttu-id="d10cb-155"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d10cb-155"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d10cb-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d10cb-156">Library</span></span><br/> | <dl> <span data-ttu-id="d10cb-157"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d10cb-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




