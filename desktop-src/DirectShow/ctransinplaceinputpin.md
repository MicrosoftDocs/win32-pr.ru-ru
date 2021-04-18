---
description: Класс Ктрансинплацеинпутпин реализует входной ПИН-код, используемый классом Ктрансинплацефилтер.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Класс Ктрансинплацеинпутпин (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675156"
---
# <a name="ctransinplaceinputpin-class"></a><span data-ttu-id="d3ad8-103">Класс Ктрансинплацеинпутпин</span><span class="sxs-lookup"><span data-stu-id="d3ad8-103">CTransInPlaceInputPin class</span></span>

![Иерархия классов ктрансинплацеинпутпин](images/tsip01.png)

<span data-ttu-id="d3ad8-105">`CTransInPlaceInputPin`Класс реализует входной ПИН-код, используемый классом [**ктрансинплацефилтер**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ad8-105">The `CTransInPlaceInputPin` class implements an input pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="d3ad8-106">Как правило, наследование от этого класса не требуется.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="d3ad8-107">В этом случае необходимо переопределить метод [**ктрансинплацефилтер:: жетпин**](ctransinplacefilter-getpin.md) фильтра, чтобы создать экземпляры производного класса.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="d3ad8-108">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="d3ad8-108">Protected Member Variables</span></span>                                                          | <span data-ttu-id="d3ad8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d3ad8-109">Description</span></span>                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="d3ad8-110">**m \_ бреадонли**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-110">**m\_bReadOnly**</span></span>](ctransinplaceinputpin-m-breadonly.md)                           | <span data-ttu-id="d3ad8-111">Флаг, указывающий, доступен ли входной поток только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-111">Flag that specifies whether the input stream is read-only.</span></span> |
| [<span data-ttu-id="d3ad8-112">**m \_ птипфилтер**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-112">**m\_pTIPFilter**</span></span>](ctransinplaceinputpin-m-ptipfilter.md)                         | <span data-ttu-id="d3ad8-113">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-113">Pointer to the filter that created this pin.</span></span>               |
| <span data-ttu-id="d3ad8-114">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="d3ad8-114">Public Methods</span></span>                                                                      | <span data-ttu-id="d3ad8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d3ad8-115">Description</span></span>                                                |
| [<span data-ttu-id="d3ad8-116">**ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-116">**CTransInPlaceInputPin**</span></span>](ctransinplaceinputpin-ctransinplaceinputpin.md)        | <span data-ttu-id="d3ad8-117">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-117">Constructor method.</span></span>                                        |
| [<span data-ttu-id="d3ad8-118">**чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-118">**CheckMediaType**</span></span>](ctransinplaceinputpin-checkmediatype.md)                      | <span data-ttu-id="d3ad8-119">Определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-119">Determines if the pin accepts a specific media type.</span></span>       |
| [<span data-ttu-id="d3ad8-120">**пикаллокатор**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-120">**PeekAllocator**</span></span>](ctransinplaceinputpin-peekallocator.md)                        | <span data-ttu-id="d3ad8-121">Получает указатель на распределитель контакта.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-121">Retrieves a pointer to the pin's allocator.</span></span>                |
| [<span data-ttu-id="d3ad8-122">**Доступно**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-122">**ReadOnly**</span></span>](ctransinplaceinputpin-readonly.md)                                  | <span data-ttu-id="d3ad8-123">Указывает, доступен ли входной поток только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-123">Indicates whether the input stream is read-only.</span></span>           |
| <span data-ttu-id="d3ad8-124">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="d3ad8-124">IPin Methods</span></span>                                                                        | <span data-ttu-id="d3ad8-125">Описание</span><span class="sxs-lookup"><span data-stu-id="d3ad8-125">Description</span></span>                                                |
| [<span data-ttu-id="d3ad8-126">**енуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-126">**EnumMediaTypes**</span></span>](ctransinplaceinputpin-enummediatypes.md)                      | <span data-ttu-id="d3ad8-127">Перечисляет предпочтительные типы носителей для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-127">Enumerates the pin's preferred media types.</span></span>                |
| <span data-ttu-id="d3ad8-128">Методы Имеминпутпин</span><span class="sxs-lookup"><span data-stu-id="d3ad8-128">IMemInputPin Methods</span></span>                                                                | <span data-ttu-id="d3ad8-129">Описание</span><span class="sxs-lookup"><span data-stu-id="d3ad8-129">Description</span></span>                                                |
| [<span data-ttu-id="d3ad8-130">**Распределителя**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-130">**GetAllocator**</span></span>](ctransinplaceinputpin-getallocator.md)                          | <span data-ttu-id="d3ad8-131">Извлекает распределитель памяти, предложенный этим ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-131">Retrieves the memory allocator proposed by this pin.</span></span>       |
| [<span data-ttu-id="d3ad8-132">**нотифяллокатор**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-132">**NotifyAllocator**</span></span>](ctransinplaceinputpin-notifyallocator.md)                    | <span data-ttu-id="d3ad8-133">Указывает распределитель для соединения.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-133">Specifies an allocator for the connection.</span></span>                 |
| [<span data-ttu-id="d3ad8-134">**жеталлокаторрекуирементс**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-134">**GetAllocatorRequirements**</span></span>](ctransinplaceinputpin--getallocatorrequirements.md) | <span data-ttu-id="d3ad8-135">Извлекает свойства распределителя, запрошенные ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-135">Retrieves the allocator properties requested by the pin.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="d3ad8-136">Требования</span><span class="sxs-lookup"><span data-stu-id="d3ad8-136">Requirements</span></span>



| <span data-ttu-id="d3ad8-137">Требование</span><span class="sxs-lookup"><span data-stu-id="d3ad8-137">Requirement</span></span> | <span data-ttu-id="d3ad8-138">Значение</span><span class="sxs-lookup"><span data-stu-id="d3ad8-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ad8-139">Header</span><span class="sxs-lookup"><span data-stu-id="d3ad8-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d3ad8-140"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3ad8-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3ad8-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d3ad8-141">Library</span></span><br/> | <dl> <span data-ttu-id="d3ad8-142"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d3ad8-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




