---
description: Класс Ктрансинплацеаутпутпин реализует выходной ПИН-код, который используется классом Ктрансинплацефилтер.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Класс Ктрансинплацеаутпутпин (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675144"
---
# <a name="ctransinplaceoutputpin-class"></a><span data-ttu-id="ec4ef-103">Класс Ктрансинплацеаутпутпин</span><span class="sxs-lookup"><span data-stu-id="ec4ef-103">CTransInPlaceOutputPin class</span></span>

![Иерархия классов ктрансинплацеаутпутпин](images/tsip02.png)

<span data-ttu-id="ec4ef-105">`CTransInPlaceOutputPin`Класс реализует выходной ПИН-код, используемый классом [**ктрансинплацефилтер**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="ec4ef-105">The `CTransInPlaceOutputPin` class implements an output pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="ec4ef-106">Как правило, наследование от этого класса не требуется.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="ec4ef-107">В этом случае необходимо переопределить метод [**ктрансинплацефилтер:: жетпин**](ctransinplacefilter-getpin.md) фильтра, чтобы создать экземпляры производного класса.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="ec4ef-108">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="ec4ef-108">Protected Member Variables</span></span>                                                      | <span data-ttu-id="ec4ef-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ec4ef-109">Description</span></span>                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="ec4ef-110">**m \_ птипфилтер**</span><span class="sxs-lookup"><span data-stu-id="ec4ef-110">**m\_pTIPFilter**</span></span>](ctransinplaceoutputpin-m-ptipfilter.md)                    | <span data-ttu-id="ec4ef-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-111">Pointer to the filter that created this pin.</span></span>         |
| <span data-ttu-id="ec4ef-112">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="ec4ef-112">Public Methods</span></span>                                                                  | <span data-ttu-id="ec4ef-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ec4ef-113">Description</span></span>                                          |
| [<span data-ttu-id="ec4ef-114">**ктрансинплацеаутпутпин**</span><span class="sxs-lookup"><span data-stu-id="ec4ef-114">**CTransInPlaceOutputPin**</span></span>](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | <span data-ttu-id="ec4ef-115">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-115">Constructor method.</span></span>                                  |
| [<span data-ttu-id="ec4ef-116">**чеккмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ec4ef-116">**CheckMediaType**</span></span>](ctransinplaceoutputpin-checkmediatype.md)                 | <span data-ttu-id="ec4ef-117">Определяет, принимает ли ПИН-код конкретный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-117">Determines if the pin accepts a specific media type.</span></span> |
| [<span data-ttu-id="ec4ef-118">**сеталлокатор**</span><span class="sxs-lookup"><span data-stu-id="ec4ef-118">**SetAllocator**</span></span>](ctransinplaceoutputpin-setallocator.md)                     | <span data-ttu-id="ec4ef-119">Указывает распределитель для соединения.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-119">Specifies an allocator for the connection.</span></span>           |
| [<span data-ttu-id="ec4ef-120">**коннектедимеминпутпин**</span><span class="sxs-lookup"><span data-stu-id="ec4ef-120">**ConnectedIMemInputPin**</span></span>](ctransinplaceoutputpin-connectedimeminputpin.md)   | <span data-ttu-id="ec4ef-121">Получает указатель на нисходящий входной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-121">Retrieves a pointer to the downstream input pin.</span></span>     |
| [<span data-ttu-id="ec4ef-122">**пикаллокатор**</span><span class="sxs-lookup"><span data-stu-id="ec4ef-122">**PeekAllocator**</span></span>](ctransinplaceoutputpin-peekallocator.md)                   | <span data-ttu-id="ec4ef-123">Получает указатель на распределитель контакта.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-123">Retrieves a pointer to the pin's allocator.</span></span>          |
| <span data-ttu-id="ec4ef-124">Методы Ипин</span><span class="sxs-lookup"><span data-stu-id="ec4ef-124">IPin Methods</span></span>                                                                    | <span data-ttu-id="ec4ef-125">Описание</span><span class="sxs-lookup"><span data-stu-id="ec4ef-125">Description</span></span>                                          |
| [<span data-ttu-id="ec4ef-126">**енуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="ec4ef-126">**EnumMediaTypes**</span></span>](ctransinplaceoutputpin-enummediatypes.md)                 | <span data-ttu-id="ec4ef-127">Перечисляет предпочтительные типы носителей для ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ec4ef-127">Enumerates the pin's preferred media types.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="ec4ef-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ec4ef-128">Requirements</span></span>



| <span data-ttu-id="ec4ef-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ec4ef-129">Requirement</span></span> | <span data-ttu-id="ec4ef-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ec4ef-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec4ef-131">Header</span><span class="sxs-lookup"><span data-stu-id="ec4ef-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ec4ef-132"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec4ef-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec4ef-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ec4ef-133">Library</span></span><br/> | <dl> <span data-ttu-id="ec4ef-134"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ec4ef-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




