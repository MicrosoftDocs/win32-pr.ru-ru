---
description: Класс Кмедиапоситион обрабатывает методы IDispatch сдвоенного интерфейса Имедиапоситион.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Класс Кмедиапоситион (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675204"
---
# <a name="cmediaposition-class"></a><span data-ttu-id="cde10-103">Класс Кмедиапоситион</span><span class="sxs-lookup"><span data-stu-id="cde10-103">CMediaPosition class</span></span>

![Иерархия классов кмедиапоситион](images/cutil14.png)

<span data-ttu-id="cde10-105">Класс **кмедиапоситион** обрабатывает методы **IDispatch** сдвоенного интерфейса [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="cde10-105">The **CMediaPosition** class handles the **IDispatch** methods of the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) dual interface.</span></span>

<span data-ttu-id="cde10-106">Этот класс наследует интерфейс [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) , но не реализует его.</span><span class="sxs-lookup"><span data-stu-id="cde10-106">This class inherits the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface but does not implement it.</span></span> <span data-ttu-id="cde10-107">Реализует **IDispatch** через класс [**кбаседиспатч**](cbasedispatch.md) и библиотеку типов DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cde10-107">It implements **IDispatch** through the [**CBaseDispatch**](cbasedispatch.md) class and the DirectShow type library.</span></span> <span data-ttu-id="cde10-108">Не используйте этот класс напрямую.</span><span class="sxs-lookup"><span data-stu-id="cde10-108">Do not use this class directly.</span></span> <span data-ttu-id="cde10-109">Вместо этого используйте один из следующих классов:</span><span class="sxs-lookup"><span data-stu-id="cde10-109">Instead, use one of the following classes:</span></span>

-   <span data-ttu-id="cde10-110">Фильтры источников: используйте базовый класс [**ксаурцесикинг**](csourceseeking.md) для реализации поиска.</span><span class="sxs-lookup"><span data-stu-id="cde10-110">Source filters: Use the [**CSourceSeeking**](csourceseeking.md) base class to implement seeking.</span></span>
-   <span data-ttu-id="cde10-111">Фильтры преобразования. Используйте класс [**кпоспасссру**](cpospassthru.md) для передачи команд поиска в восходящий поток.</span><span class="sxs-lookup"><span data-stu-id="cde10-111">Transform filters: Use the [**CPosPassThru**](cpospassthru.md) class to pass seeking commands upstream.</span></span>
-   <span data-ttu-id="cde10-112">Модули подготовки отчетов: Используйте класс [**крендерерпоспасссру**](crendererpospassthru.md) для передачи команд для поиска в восходящий поток.</span><span class="sxs-lookup"><span data-stu-id="cde10-112">Renderers: Use the [**CRendererPosPassThru**](crendererpospassthru.md) class to pass seeking commands upstream.</span></span>



| <span data-ttu-id="cde10-113">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="cde10-113">Public Methods</span></span>                                              | <span data-ttu-id="cde10-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cde10-114">Description</span></span>                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cde10-115">**кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="cde10-115">**CMediaPosition**</span></span>](cmediaposition-cmediaposition.md)     | <span data-ttu-id="cde10-116">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="cde10-116">Constructor method.</span></span>                                                                                                 |
| <span data-ttu-id="cde10-117">Методы IDispatch</span><span class="sxs-lookup"><span data-stu-id="cde10-117">IDispatch Methods</span></span>                                           | <span data-ttu-id="cde10-118">Описание</span><span class="sxs-lookup"><span data-stu-id="cde10-118">Description</span></span>                                                                                                         |
| [<span data-ttu-id="cde10-119">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="cde10-119">**GetIDsOfNames**</span></span>](cmediaposition-getidsofnames.md)       | <span data-ttu-id="cde10-120">Сопоставляет набор имен с соответствующим набором идентификаторов DISPID.</span><span class="sxs-lookup"><span data-stu-id="cde10-120">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="cde10-121">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="cde10-121">**GetTypeInfo**</span></span>](cmediaposition-gettypeinfo.md)           | <span data-ttu-id="cde10-122">Извлекает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cde10-122">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="cde10-123">**жеттипеинфокаунт**</span><span class="sxs-lookup"><span data-stu-id="cde10-123">**GetTypeInfoCount**</span></span>](cmediaposition-gettypeinfocount.md) | <span data-ttu-id="cde10-124">Возвращает число интерфейсов сведений о типе, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="cde10-124">Retrieves the number of type information interfaces the object provides.</span></span>                                            |
| [<span data-ttu-id="cde10-125">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="cde10-125">**Invoke**</span></span>](cmediaposition-invoke.md)                     | <span data-ttu-id="cde10-126">Предоставляет доступ к свойствам и методам, предоставляемым объектом.</span><span class="sxs-lookup"><span data-stu-id="cde10-126">Provides access to properties and methods exposed by the object.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="cde10-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cde10-127">Requirements</span></span>



| <span data-ttu-id="cde10-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cde10-128">Requirement</span></span> | <span data-ttu-id="cde10-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cde10-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cde10-130">Header</span><span class="sxs-lookup"><span data-stu-id="cde10-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cde10-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cde10-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cde10-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cde10-132">Library</span></span><br/> | <dl> <span data-ttu-id="cde10-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="cde10-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cde10-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cde10-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde10-135">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="cde10-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




