---
description: Класс Цимажеаллокатор реализует распределитель, который управляет независимыми от устройства точечными рисунками (DIB) GDI. Этот класс является производным от класса Кбасеаллокатор. Он создает примеры носителей, реализованные с помощью класса Цимажесампле.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Класс Цимажеаллокатор (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674993"
---
# <a name="cimageallocator-class"></a><span data-ttu-id="4f158-105">Класс Цимажеаллокатор</span><span class="sxs-lookup"><span data-stu-id="4f158-105">CImageAllocator class</span></span>

![Иерархия классов Цимажеаллокатор](images/wutil04.png)

<span data-ttu-id="4f158-107">`CImageAllocator`Класс реализует распределитель, который управляет независимыми от устройства точечными рисунками (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="4f158-107">The `CImageAllocator` class implements an allocator that manages GDI device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="4f158-108">Этот класс является производным от класса [**кбасеаллокатор**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="4f158-108">This class derives from the [**CBaseAllocator**](cbaseallocator.md) class.</span></span> <span data-ttu-id="4f158-109">Он создает примеры носителей, реализованные с помощью класса [**Цимажесампле**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="4f158-109">It creates media samples that are implemented using the [**CImageSample**](cimagesample.md) class.</span></span>

<span data-ttu-id="4f158-110">Распределитель совместно используется двумя подключенными контактами, но всегда принадлежит одному из фильтров в соединении.</span><span class="sxs-lookup"><span data-stu-id="4f158-110">An allocator is shared by two connected pins, but is always owned by one of the filters in the connection.</span></span> <span data-ttu-id="4f158-111">Фильтр, который использует, `CImageAllocator` должен отследить, предоставлен ли распределитель самим или другим фильтром.</span><span class="sxs-lookup"><span data-stu-id="4f158-111">A filter that uses `CImageAllocator` must keep track of whether the allocator was provided by itself or by the other filter.</span></span> <span data-ttu-id="4f158-112">Если распределитель был предоставлен самим собой, то фильтр-владелец может полагаться на тот факт, что все образцы мультимедиа из распределителя являются **Цимажесампле** объектами.</span><span class="sxs-lookup"><span data-stu-id="4f158-112">If the allocator was provided by itself, the owning filter can rely on the fact that all media samples from the allocator are **CImageSample** objects.</span></span> <span data-ttu-id="4f158-113">Таким образом, можно использовать объект **Цимажесампле** для получения сведений о DIB, который хранится в структуре [**дибдата**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="4f158-113">It can therefore use the **CImageSample** object to obtain information about the DIB, which is stored in a [**DIBDATA**](dibdata.md) structure.</span></span>

<span data-ttu-id="4f158-114">Фильтр-владелец должен вызывать **нотифимедиатипе** при каждом изменении типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4f158-114">The owning filter should call **NotifyMediaType** whenever the media type changes.</span></span>



| <span data-ttu-id="4f158-115">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="4f158-115">Protected Member Variables</span></span>                                     | <span data-ttu-id="4f158-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4f158-116">Description</span></span>                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="4f158-117">**m \_ пфилтер**</span><span class="sxs-lookup"><span data-stu-id="4f158-117">**m\_pFilter**</span></span>](cimageallocator-m-pfilter.md)                | <span data-ttu-id="4f158-118">Указатель на фильтр-владелец.</span><span class="sxs-lookup"><span data-stu-id="4f158-118">Pointer to the owning filter.</span></span>                                            |
| [<span data-ttu-id="4f158-119">**m \_ пмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="4f158-119">**m\_pMediaType**</span></span>](cimageallocator-m-pmediatype.md)          | <span data-ttu-id="4f158-120">Указатель на текущий тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4f158-120">Pointer to the current media type.</span></span>                                       |
| <span data-ttu-id="4f158-121">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="4f158-121">Protected Methods</span></span>                                              | <span data-ttu-id="4f158-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4f158-122">Description</span></span>                                                              |
| [<span data-ttu-id="4f158-123">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="4f158-123">**Alloc**</span></span>](cimageallocator-alloc.md)                         | <span data-ttu-id="4f158-124">Выделяет память для буферов.</span><span class="sxs-lookup"><span data-stu-id="4f158-124">Allocates memory for the buffers.</span></span>                                        |
| [<span data-ttu-id="4f158-125">**чекксизес**</span><span class="sxs-lookup"><span data-stu-id="4f158-125">**CheckSizes**</span></span>](cimageallocator-checksizes.md)               | <span data-ttu-id="4f158-126">Проверяет свойства распределителя для текущего типа носителя.</span><span class="sxs-lookup"><span data-stu-id="4f158-126">Checks allocator properties against the current media type.</span></span>              |
| [<span data-ttu-id="4f158-127">**креатедиб**</span><span class="sxs-lookup"><span data-stu-id="4f158-127">**CreateDIB**</span></span>](cimageallocator-createdib.md)                 | <span data-ttu-id="4f158-128">Создает DIB.</span><span class="sxs-lookup"><span data-stu-id="4f158-128">Creates a DIB.</span></span>                                                           |
| [<span data-ttu-id="4f158-129">**креатеимажесампле**</span><span class="sxs-lookup"><span data-stu-id="4f158-129">**CreateImageSample**</span></span>](cimageallocator-createimagesample.md) | <span data-ttu-id="4f158-130">Создает пример носителя.</span><span class="sxs-lookup"><span data-stu-id="4f158-130">Creates a media sample.</span></span> <span data-ttu-id="4f158-131">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="4f158-131">Virtual.</span></span>                                         |
| [<span data-ttu-id="4f158-132">**Бесплатный**</span><span class="sxs-lookup"><span data-stu-id="4f158-132">**Free**</span></span>](cimageallocator-free.md)                           | <span data-ttu-id="4f158-133">Освобождает всю буферную память.</span><span class="sxs-lookup"><span data-stu-id="4f158-133">Releases all of the buffer memory.</span></span>                                       |
| <span data-ttu-id="4f158-134">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="4f158-134">Public Methods</span></span>                                                 | <span data-ttu-id="4f158-135">Описание</span><span class="sxs-lookup"><span data-stu-id="4f158-135">Description</span></span>                                                              |
| [<span data-ttu-id="4f158-136">**Цимажеаллокатор**</span><span class="sxs-lookup"><span data-stu-id="4f158-136">**CImageAllocator**</span></span>](cimageallocator-cimageallocator.md)     | <span data-ttu-id="4f158-137">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="4f158-137">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="4f158-138">**нотифимедиатипе**</span><span class="sxs-lookup"><span data-stu-id="4f158-138">**NotifyMediaType**</span></span>](cimageallocator-notifymediatype.md)     | <span data-ttu-id="4f158-139">Информирует объект о текущем типе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4f158-139">Informs the object of the current media type.</span></span>                            |
| <span data-ttu-id="4f158-140">Методы Имемаллокатор</span><span class="sxs-lookup"><span data-stu-id="4f158-140">IMemAllocator Methods</span></span>                                          | <span data-ttu-id="4f158-141">Описание</span><span class="sxs-lookup"><span data-stu-id="4f158-141">Description</span></span>                                                              |
| [<span data-ttu-id="4f158-142">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="4f158-142">**SetProperties**</span></span>](cimageallocator-setproperties.md)         | <span data-ttu-id="4f158-143">Указывает количество выделяемых буферов и размер каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="4f158-143">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4f158-144">Требования</span><span class="sxs-lookup"><span data-stu-id="4f158-144">Requirements</span></span>



| <span data-ttu-id="4f158-145">Требование</span><span class="sxs-lookup"><span data-stu-id="4f158-145">Requirement</span></span> | <span data-ttu-id="4f158-146">Значение</span><span class="sxs-lookup"><span data-stu-id="4f158-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f158-147">Header</span><span class="sxs-lookup"><span data-stu-id="4f158-147">Header</span></span><br/>  | <dl> <span data-ttu-id="4f158-148"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f158-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f158-149">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f158-149">Library</span></span><br/> | <dl> <span data-ttu-id="4f158-150"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4f158-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f158-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f158-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f158-152">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="4f158-152">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




