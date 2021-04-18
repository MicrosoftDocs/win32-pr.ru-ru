---
description: Класс Ксикингпасссру — это вспомогательный объект, создающий объекты Кпоспасссру и Крендерерпоспасссру.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Класс Ксикингпасссру (Сикпт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685118"
---
# <a name="cseekingpassthru-class"></a><span data-ttu-id="5879c-103">Класс Ксикингпасссру</span><span class="sxs-lookup"><span data-stu-id="5879c-103">CSeekingPassThru class</span></span>

<span data-ttu-id="5879c-104">`CSeekingPassThru`Класс является вспомогательным объектом, который создает объекты [**Кпоспасссру**](cpospassthru.md) и [**крендерерпоспасссру**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="5879c-104">The `CSeekingPassThru` class is a helper object that creates [**CPosPassThru**](cpospassthru.md) and [**CRendererPosPassThru**](crendererpospassthru.md) objects.</span></span>

<span data-ttu-id="5879c-105">Классы **кпоспасссру** и **крендерерпоспасссру** являются вспомогательными объектами, которые передают команды поиска в виде вышестоящего, поэтому `CSeekingPassThru` класс является вспомогательным объектом для создания вспомогательных объектов.</span><span class="sxs-lookup"><span data-stu-id="5879c-105">The **CPosPassThru** and **CRendererPosPassThru** classes are helper objects that pass seeking commands upstream, so the `CSeekingPassThru` class is a helper object for creating helper objects.</span></span>

<span data-ttu-id="5879c-106">Необязательно использовать этот класс напрямую.</span><span class="sxs-lookup"><span data-stu-id="5879c-106">It is not necessary to use this class directly.</span></span> <span data-ttu-id="5879c-107">Вместо этого используйте функцию [**креатепоспасссру**](createpospassthru.md) , которая обрабатывает все сведения об использовании этого класса.</span><span class="sxs-lookup"><span data-stu-id="5879c-107">Instead, use the [**CreatePosPassThru**](createpospassthru.md) function, which handles all of the details of using this class.</span></span> <span data-ttu-id="5879c-108">Он имеет больше преимуществ при загрузке объекта из Quartz.dll, что немного сокращает размер кода фильтра.</span><span class="sxs-lookup"><span data-stu-id="5879c-108">It has the further advantage of loading the object from Quartz.dll, which reduces the code size of your filter somewhat.</span></span> <span data-ttu-id="5879c-109">Дополнительные сведения см. в разделе [**кпоспасссру**](cpospassthru.md).</span><span class="sxs-lookup"><span data-stu-id="5879c-109">For more information, see [**CPosPassThru**](cpospassthru.md).</span></span>

<span data-ttu-id="5879c-110">`CSeekingPassThru`Класс предоставляет интерфейс [**исикингпасссру**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) .</span><span class="sxs-lookup"><span data-stu-id="5879c-110">The `CSeekingPassThru` class exposes the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface.</span></span> <span data-ttu-id="5879c-111">Метод [**исикингпасссру:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) Инициализирует объект.</span><span class="sxs-lookup"><span data-stu-id="5879c-111">The [**ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) method initializes the object.</span></span> <span data-ttu-id="5879c-112">После инициализации объекта фильтр может запросить его для интерфейсов [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) и [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="5879c-112">After the object is initialized, the filter can query it for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interfaces.</span></span>



| <span data-ttu-id="5879c-113">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="5879c-113">Public Methods</span></span>                                                  | <span data-ttu-id="5879c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5879c-114">Description</span></span>                        |
|-----------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="5879c-115">**ксикингпасссру**</span><span class="sxs-lookup"><span data-stu-id="5879c-115">**CSeekingPassThru**</span></span>](cseekingpassthru-cseekingpassthru.md)   | <span data-ttu-id="5879c-116">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5879c-116">Constructor method.</span></span>                |
| [<span data-ttu-id="5879c-117">**~ Ксикингпасссру**</span><span class="sxs-lookup"><span data-stu-id="5879c-117">**~CSeekingPassThru**</span></span>](cseekingpassthru--cseekingpassthru.md) | <span data-ttu-id="5879c-118">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="5879c-118">Destructor method.</span></span>                 |
| [<span data-ttu-id="5879c-119">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="5879c-119">**CreateInstance**</span></span>](cseekingpassthru-createinstance.md)       | <span data-ttu-id="5879c-120">Создает экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="5879c-120">Creates an instance of the object.</span></span> |
| <span data-ttu-id="5879c-121">Методы Исикингпасссру</span><span class="sxs-lookup"><span data-stu-id="5879c-121">ISeekingPassThru Methods</span></span>                                        | <span data-ttu-id="5879c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="5879c-122">Description</span></span>                        |
| [<span data-ttu-id="5879c-123">**Ini**</span><span class="sxs-lookup"><span data-stu-id="5879c-123">**Init**</span></span>](cseekingpassthru-init.md)                           | <span data-ttu-id="5879c-124">Инициализирует объект.</span><span class="sxs-lookup"><span data-stu-id="5879c-124">Initializes the object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="5879c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5879c-125">Requirements</span></span>



| <span data-ttu-id="5879c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5879c-126">Requirement</span></span> | <span data-ttu-id="5879c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5879c-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5879c-128">Header</span><span class="sxs-lookup"><span data-stu-id="5879c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5879c-129"><dt>Сикпт. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5879c-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5879c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5879c-130">Library</span></span><br/> | <dl> <span data-ttu-id="5879c-131"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5879c-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




