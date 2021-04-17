---
description: Класс Крендерерпоспасссру обрабатывает команды Seek для фильтров модуля подготовки отчетов, передавая их в следующий фильтр.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Класс Крендерерпоспасссру (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665467"
---
# <a name="crendererpospassthru-class"></a><span data-ttu-id="e9485-103">Класс Крендерерпоспасссру</span><span class="sxs-lookup"><span data-stu-id="e9485-103">CRendererPosPassThru class</span></span>

![Иерархия классов крендерерпоспасссру](images/cutil14.png)

<span data-ttu-id="e9485-105">`CRendererPosPassThru`Класс обрабатывает команды Seek для фильтров модуля подготовки отчетов, передавая их в следующий фильтр.</span><span class="sxs-lookup"><span data-stu-id="e9485-105">The `CRendererPosPassThru` class handles seek commands for renderer filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="e9485-106">Этот класс является производным от класса [**кпоспасссру**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="e9485-106">This class derives from the [**CPosPassThru**](cpospassthru.md) class.</span></span> <span data-ttu-id="e9485-107">Он добавляет поддержку кэширования меток времени из примеров по мере их поступления.</span><span class="sxs-lookup"><span data-stu-id="e9485-107">It adds support for caching the time stamps from samples as they arrive.</span></span> <span data-ttu-id="e9485-108">Используйте этот класс так же, как класс **кпоспасссру** .</span><span class="sxs-lookup"><span data-stu-id="e9485-108">Use this class in the same way as the **CPosPassThru** class.</span></span> <span data-ttu-id="e9485-109">Дополнительные сведения см. в документации по **кпоспасссру** .</span><span class="sxs-lookup"><span data-stu-id="e9485-109">Refer to the **CPosPassThru** documentation for details.</span></span>

<span data-ttu-id="e9485-110">Фильтр модуля подготовки отчетов должен обновить `CRendererPosPassThru` кэшированные временные метки объекта следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e9485-110">The renderer filter must update the `CRendererPosPassThru` object's cached time stamps, as follows:</span></span>

-   <span data-ttu-id="e9485-111">Для каждого образца, полученного фильтром, вызовите метод [**крендерерпоспасссру:: регистермедиатиме**](crendererpospassthru-registermediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="e9485-111">For each sample the filter receives, call the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method.</span></span>
-   <span data-ttu-id="e9485-112">Когда фильтр останавливается или получает вызов **ендфлуш** , вызовите метод [**Крендерерпоспасссру:: ресетмедиатиме**](crendererpospassthru-resetmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="e9485-112">When the filter is stopped or receives an **EndFlush** call, call the [**CRendererPosPassThru::ResetMediaTime**](crendererpospassthru-resetmediatime.md) method.</span></span>
-   <span data-ttu-id="e9485-113">Когда фильтр получает уведомление об окончании потока, вызовите метод [**крендерерпоспасссру:: EOS**](crendererpospassthru-eos.md) .</span><span class="sxs-lookup"><span data-stu-id="e9485-113">When the filter receives an end-of-stream notification, call the [**CRendererPosPassThru::EOS**](crendererpospassthru-eos.md) method.</span></span>

<span data-ttu-id="e9485-114">Пример использования этого класса см. в исходном коде [**кбасерендерер**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="e9485-114">For an example of how to use this class, refer to the [**CBaseRenderer**](cbaserenderer.md) source code.</span></span>



| <span data-ttu-id="e9485-115">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="e9485-115">Public Methods</span></span>                                                            | <span data-ttu-id="e9485-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e9485-116">Description</span></span>                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="e9485-117">**крендерерпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="e9485-117">**CRendererPosPassThru**</span></span>](crendererpospassthru-crendererpospassthru.md) | <span data-ttu-id="e9485-118">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="e9485-118">Constructor method.</span></span>                                                 |
| [<span data-ttu-id="e9485-119">**жетмедиатиме**</span><span class="sxs-lookup"><span data-stu-id="e9485-119">**GetMediaTime**</span></span>](crendererpospassthru-getmediatime.md)                 | <span data-ttu-id="e9485-120">Извлекает метки времени для текущего образца.</span><span class="sxs-lookup"><span data-stu-id="e9485-120">Retrieves the time stamps on the current sample.</span></span>                    |
| [<span data-ttu-id="e9485-121">**регистермедиатиме**</span><span class="sxs-lookup"><span data-stu-id="e9485-121">**RegisterMediaTime**</span></span>](crendererpospassthru-registermediatime.md)       | <span data-ttu-id="e9485-122">Кэширует метки времени из текущего образца.</span><span class="sxs-lookup"><span data-stu-id="e9485-122">Caches the time stamps from the current sample.</span></span>                     |
| [<span data-ttu-id="e9485-123">**ресетмедиатиме**</span><span class="sxs-lookup"><span data-stu-id="e9485-123">**ResetMediaTime**</span></span>](crendererpospassthru-resetmediatime.md)             | <span data-ttu-id="e9485-124">Сбрасывает кэшированные отметки времени в ноль.</span><span class="sxs-lookup"><span data-stu-id="e9485-124">Resets the cached time stamps to zero.</span></span>                              |
| [<span data-ttu-id="e9485-125">**EOS**</span><span class="sxs-lookup"><span data-stu-id="e9485-125">**EOS**</span></span>](crendererpospassthru-eos.md)                                   | <span data-ttu-id="e9485-126">Обновляет кэшированные метки времени после уведомления о завершении потока.</span><span class="sxs-lookup"><span data-stu-id="e9485-126">Updates the cached time stamps after an end-of-stream notification.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e9485-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e9485-127">Requirements</span></span>



| <span data-ttu-id="e9485-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e9485-128">Requirement</span></span> | <span data-ttu-id="e9485-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e9485-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9485-130">Header</span><span class="sxs-lookup"><span data-stu-id="e9485-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e9485-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9485-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9485-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e9485-132">Library</span></span><br/> | <dl> <span data-ttu-id="e9485-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e9485-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




