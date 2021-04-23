---
description: Класс Кбаседиспатч является базовым классом для реализации интерфейса IDispatch в фильтре DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Класс Кбаседиспатч (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657300"
---
# <a name="cbasedispatch-class"></a><span data-ttu-id="f6631-103">Класс Кбаседиспатч</span><span class="sxs-lookup"><span data-stu-id="f6631-103">CBaseDispatch class</span></span>

![Иерархия классов кбаседиспатч](images/cutil01.png)

<span data-ttu-id="f6631-105">Класс **кбаседиспатч** является базовым классом для реализации интерфейса **IDispatch** в фильтре DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f6631-105">The **CBaseDispatch** class is a base class for implementing the **IDispatch** interface in a DirectShow filter.</span></span>

<span data-ttu-id="f6631-106">Этот класс ограничен для поддержки интерфейсов, совместимых со службой автоматизации, экспортируемых библиотекой типов DirectShow Куартзтипелиб.</span><span class="sxs-lookup"><span data-stu-id="f6631-106">This class is limited to supporting the Automation-compatible interfaces exported by the DirectShow type library, QuartzTypeLib.</span></span> <span data-ttu-id="f6631-107">Например, классы [**кмедиаконтрол**](cmediacontrol.md) и [**кмедиапоситион**](cmediaposition.md) используют **Кбаседиспатч** для реализации [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition)соответственно.</span><span class="sxs-lookup"><span data-stu-id="f6631-107">For example, the [**CMediaControl**](cmediacontrol.md) and [**CMediaPosition**](cmediaposition.md) classes use **CBaseDispatch** to implement [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectively.</span></span> <span data-ttu-id="f6631-108">В связи с этим ограничением, вероятно, нет причин использовать **кбаседиспатч** непосредственно в собственных фильтрах.</span><span class="sxs-lookup"><span data-stu-id="f6631-108">Because of this limitation, there is probably no reason to use **CBaseDispatch** directly in your own filters.</span></span>

<span data-ttu-id="f6631-109">Чтобы использовать этот класс, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f6631-109">To use this class, do the following:</span></span>

-   <span data-ttu-id="f6631-110">Объявите новый класс, поддерживающий **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="f6631-110">Declare a new class that supports **IDispatch**.</span></span>
-   <span data-ttu-id="f6631-111">Присвойте новому классу закрытую переменную-член типа **кбаседиспатч**.</span><span class="sxs-lookup"><span data-stu-id="f6631-111">Give your new class a private member variable of type **CBaseDispatch**.</span></span>
-   <span data-ttu-id="f6631-112">Реализуйте методы **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="f6631-112">Implement the **IDispatch** methods.</span></span>
-   <span data-ttu-id="f6631-113">В методах **IDispatch** вызовите методы **кбаседиспатч** .</span><span class="sxs-lookup"><span data-stu-id="f6631-113">In your **IDispatch** methods, call the **CBaseDispatch** methods.</span></span>

<span data-ttu-id="f6631-114">Дополнительные сведения см. в исходном коде любого из примеров классов, объявленных в Ктлутил. h.</span><span class="sxs-lookup"><span data-stu-id="f6631-114">For more details, refer to the source code for any of the sample classes declared in Ctlutil.h.</span></span>



| <span data-ttu-id="f6631-115">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="f6631-115">Public Methods</span></span>                                             | <span data-ttu-id="f6631-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f6631-116">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6631-117">**кбаседиспатч**</span><span class="sxs-lookup"><span data-stu-id="f6631-117">**CBaseDispatch**</span></span>](cbasedispatch-cbasedispatch.md)       | <span data-ttu-id="f6631-118">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="f6631-118">Constructor method.</span></span>                                                                                                 |
| [<span data-ttu-id="f6631-119">**~ Кбаседиспатч**</span><span class="sxs-lookup"><span data-stu-id="f6631-119">**~CBaseDispatch**</span></span>](cbasedispatch--cbasedispatch.md)     | <span data-ttu-id="f6631-120">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="f6631-120">Destructor method.</span></span>                                                                                                  |
| [<span data-ttu-id="f6631-121">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="f6631-121">**GetIDsOfNames**</span></span>](cbasedispatch-getidsofnames.md)       | <span data-ttu-id="f6631-122">Сопоставляет набор имен с соответствующим набором идентификаторов DISPID.</span><span class="sxs-lookup"><span data-stu-id="f6631-122">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="f6631-123">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="f6631-123">**GetTypeInfo**</span></span>](cbasedispatch-gettypeinfo.md)           | <span data-ttu-id="f6631-124">Извлекает сведения о типе для объекта, который затем можно использовать для получения сведений о типе для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f6631-124">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="f6631-125">**жеттипеинфокаунт**</span><span class="sxs-lookup"><span data-stu-id="f6631-125">**GetTypeInfoCount**</span></span>](cbasedispatch-gettypeinfocount.md) | <span data-ttu-id="f6631-126">Возвращает число интерфейсов сведений о типе, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="f6631-126">Retrieves the number of type information interfaces the object provides.</span></span>                                            |



 

## <a name="requirements"></a><span data-ttu-id="f6631-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f6631-127">Requirements</span></span>



| <span data-ttu-id="f6631-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f6631-128">Requirement</span></span> | <span data-ttu-id="f6631-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f6631-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6631-130">Header</span><span class="sxs-lookup"><span data-stu-id="f6631-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f6631-131"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6631-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6631-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f6631-132">Library</span></span><br/> | <dl> <span data-ttu-id="f6631-133"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f6631-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6631-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6631-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6631-135">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="f6631-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




