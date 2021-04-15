---
description: Шаблон класса Имедиаобжектимпл предоставляет базовую реализацию для интерфейса Имедиаобжект. Дополнительные сведения об использовании этого шаблона см. в разделе Использование шаблона класса DMO.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Шаблон класса Имедиаобжектимпл (Дмоимпл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675930"
---
# <a name="imediaobjectimpl-class-template"></a><span data-ttu-id="e593d-104">Шаблон класса Имедиаобжектимпл</span><span class="sxs-lookup"><span data-stu-id="e593d-104">IMediaObjectImpl Class Template</span></span>

<span data-ttu-id="e593d-105">`IMediaObjectImpl`Шаблон класса предоставляет базовую реализацию для интерфейса [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="e593d-105">The `IMediaObjectImpl` class template provides a base implementation for the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="e593d-106">Дополнительные сведения об использовании этого шаблона см. в разделе [Использование шаблона класса DMO](using-the-dmo-class-template.md).</span><span class="sxs-lookup"><span data-stu-id="e593d-106">For more information on using this template, see [Using the DMO Class Template](using-the-dmo-class-template.md).</span></span>

<span data-ttu-id="e593d-107">Этот `IMediaObjectImpl` шаблон предоставляет следующие члены.</span><span class="sxs-lookup"><span data-stu-id="e593d-107">This `IMediaObjectImpl` template exposes the following members.</span></span>



| <span data-ttu-id="e593d-108">Вложенный класс</span><span class="sxs-lookup"><span data-stu-id="e593d-108">Nested Class</span></span>                              | <span data-ttu-id="e593d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e593d-109">Description</span></span>                                  |
|-------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="e593d-110">**локкит**</span><span class="sxs-lookup"><span data-stu-id="e593d-110">**LockIt**</span></span>](imediaobjectimpl-lockit.md) | <span data-ttu-id="e593d-111">Вспомогательный класс, который блокирует и разблокирует DMO.</span><span class="sxs-lookup"><span data-stu-id="e593d-111">Helper class that locks and unlocks the DMO.</span></span> |



 



| <span data-ttu-id="e593d-112">Метод</span><span class="sxs-lookup"><span data-stu-id="e593d-112">Method</span></span>                                                                      | <span data-ttu-id="e593d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e593d-113">Description</span></span>                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="e593d-114">[**чекктипессет**](/previous-versions/ms807621(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-114">[**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))</span></span>                     | <span data-ttu-id="e593d-115">Определяет, имеют ли все необязательные потоки типы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e593d-115">Determines whether all of the non-optional streams have media types.</span></span> |
| <span data-ttu-id="e593d-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-116">[**InputType**](/previous-versions/ms807633(v=msdn.10))</span></span>                             | <span data-ttu-id="e593d-117">Извлекает текущий тип мультимедиа для указанного входного потока.</span><span class="sxs-lookup"><span data-stu-id="e593d-117">Retrieves the current media type for a specified input stream.</span></span>       |
| <span data-ttu-id="e593d-118">[**инпуттипесет**](/previous-versions/ms807638(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-118">[**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))</span></span>                       | <span data-ttu-id="e593d-119">Запрашивает, задан ли тип мультимедиа во входном потоке.</span><span class="sxs-lookup"><span data-stu-id="e593d-119">Queries whether the media type was set on an input stream.</span></span>           |
| <span data-ttu-id="e593d-120">[**интерналакцептингинпут**](/previous-versions/ms809095(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-120">[**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))</span></span>   | <span data-ttu-id="e593d-121">Запрашивает, может ли входной поток принимать больше входных данных.</span><span class="sxs-lookup"><span data-stu-id="e593d-121">Queries whether an input stream can accept more input.</span></span>               |
| <span data-ttu-id="e593d-122">[**интерналчеккинпуттипе**](/previous-versions/ms809096(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-122">[**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))</span></span>   | <span data-ttu-id="e593d-123">Запрашивает, может ли входной поток принимать заданный тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e593d-123">Queries whether an input stream can accept a given media type.</span></span>       |
| <span data-ttu-id="e593d-124">[**интерналчеккаутпуттипе**](/previous-versions/ms809098(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-124">[**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))</span></span> | <span data-ttu-id="e593d-125">Запрашивает, может ли выходной поток принимать заданный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="e593d-125">Queries whether an output stream can accept a given media type.</span></span>      |
| <span data-ttu-id="e593d-126">[**Блокировка**](/previous-versions/ms809100(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-126">[**Lock**](/previous-versions/ms809100(v=msdn.10))</span></span>                                       | <span data-ttu-id="e593d-127">Блокирует DMO</span><span class="sxs-lookup"><span data-stu-id="e593d-127">Locks the DMO</span></span>                                                        |
| <span data-ttu-id="e593d-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-128">[**OutputType**](/previous-versions/ms807644(v=msdn.10))</span></span>                           | <span data-ttu-id="e593d-129">Извлекает текущий тип мультимедиа для указанного потока вывода.</span><span class="sxs-lookup"><span data-stu-id="e593d-129">Retrieves the current media type for a specified output stream.</span></span>      |
| <span data-ttu-id="e593d-130">[**аутпуттипесет**](/previous-versions/ms807649(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-130">[**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))</span></span>                     | <span data-ttu-id="e593d-131">Запрашивает, задан ли тип мультимедиа в выходном потоке.</span><span class="sxs-lookup"><span data-stu-id="e593d-131">Queries whether the media type was set on an output stream.</span></span>          |
| <span data-ttu-id="e593d-132">[**Блокирован**](/previous-versions/ms809101(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e593d-132">[**Unlock**](/previous-versions/ms809101(v=msdn.10))</span></span>                                   | <span data-ttu-id="e593d-133">Разблокирует DMO</span><span class="sxs-lookup"><span data-stu-id="e593d-133">Unlocks the DMO</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="e593d-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e593d-134">Requirements</span></span>



| <span data-ttu-id="e593d-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e593d-135">Requirement</span></span> | <span data-ttu-id="e593d-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e593d-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e593d-137">Header</span><span class="sxs-lookup"><span data-stu-id="e593d-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e593d-138"><dt>Дмоимпл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e593d-138"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="e593d-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e593d-139">Library</span></span><br/> | <dl> <span data-ttu-id="e593d-140"><dt>Дмогуидс. lib; </dt> <dt>Мсдмо. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e593d-140"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e593d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e593d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e593d-142">Справочник по DMO</span><span class="sxs-lookup"><span data-stu-id="e593d-142">DMO Reference</span></span>](dmo-reference.md)
</dt> <dt>

[<span data-ttu-id="e593d-143">Использование шаблона класса DMO</span><span class="sxs-lookup"><span data-stu-id="e593d-143">Using the DMO Class Template</span></span>](using-the-dmo-class-template.md)
</dt> </dl>

 

 
