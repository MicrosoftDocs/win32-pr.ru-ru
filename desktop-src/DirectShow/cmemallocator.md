---
description: Реализует распределитель, который поддерживает интерфейс Имемаллокатор.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Класс Кмемаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668662"
---
# <a name="cmemallocator-class"></a><span data-ttu-id="43a43-103">Класс Кмемаллокатор</span><span class="sxs-lookup"><span data-stu-id="43a43-103">CMemAllocator class</span></span>

![Иерархия классов кмемаллокатор](images/filter10.png)

<span data-ttu-id="43a43-105">Реализует распределитель, который поддерживает интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="43a43-105">Implements an allocator that supports the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="43a43-106">Этот класс является производным от [**кбасеаллокатор**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="43a43-106">This class derives from [**CBaseAllocator**](cbaseallocator.md).</span></span> <span data-ttu-id="43a43-107">Дополнительные сведения о распределителях см. в документации по [**кбасеаллокатор**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="43a43-107">For more information about allocators, refer to the documentation for [**CBaseAllocator**](cbaseallocator.md).</span></span>



| <span data-ttu-id="43a43-108">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="43a43-108">Protected Member Variables</span></span>                              | <span data-ttu-id="43a43-109">Описание</span><span class="sxs-lookup"><span data-stu-id="43a43-109">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="43a43-110">**m \_ pBuffer**</span><span class="sxs-lookup"><span data-stu-id="43a43-110">**m\_pBuffer**</span></span>](cmemallocator-m-pbuffer.md)           | <span data-ttu-id="43a43-111">Указатель на блок памяти, содержащий буферы.</span><span class="sxs-lookup"><span data-stu-id="43a43-111">Pointer to the memory block that contains the buffers.</span></span>                   |
| <span data-ttu-id="43a43-112">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="43a43-112">Protected Methods</span></span>                                       | <span data-ttu-id="43a43-113">Описание</span><span class="sxs-lookup"><span data-stu-id="43a43-113">Description</span></span>                                                              |
| [<span data-ttu-id="43a43-114">**Free**</span><span class="sxs-lookup"><span data-stu-id="43a43-114">**Free**</span></span>](cmemallocator-free.md)                      | <span data-ttu-id="43a43-115">Метод заполнителя; вызывается во время операции дефиксации.</span><span class="sxs-lookup"><span data-stu-id="43a43-115">Placeholder method; called during a decommit operation.</span></span>                  |
| [<span data-ttu-id="43a43-116">**реаллифри**</span><span class="sxs-lookup"><span data-stu-id="43a43-116">**ReallyFree**</span></span>](cmemallocator-reallyfree.md)          | <span data-ttu-id="43a43-117">Освобождает память для буферов.</span><span class="sxs-lookup"><span data-stu-id="43a43-117">Releases the memory for the buffers.</span></span>                                     |
| [<span data-ttu-id="43a43-118">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="43a43-118">**Alloc**</span></span>](cmemallocator-alloc.md)                    | <span data-ttu-id="43a43-119">Выделяет память для буферов.</span><span class="sxs-lookup"><span data-stu-id="43a43-119">Allocates memory for the buffers.</span></span>                                        |
| <span data-ttu-id="43a43-120">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="43a43-120">Public Methods</span></span>                                          | <span data-ttu-id="43a43-121">Описание</span><span class="sxs-lookup"><span data-stu-id="43a43-121">Description</span></span>                                                              |
| [<span data-ttu-id="43a43-122">**кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="43a43-122">**CMemAllocator**</span></span>](cmemallocator-cmemallocator.md)    | <span data-ttu-id="43a43-123">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="43a43-123">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="43a43-124">**~ Кмемаллокатор**</span><span class="sxs-lookup"><span data-stu-id="43a43-124">**~ CMemAllocator**</span></span>](cmemallocator--cmemallocator.md) | <span data-ttu-id="43a43-125">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="43a43-125">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="43a43-126">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="43a43-126">**CreateInstance**</span></span>](cmemallocator-createinstance.md)  | <span data-ttu-id="43a43-127">Создает новый экземпляр класса **кмемаллокатор** .</span><span class="sxs-lookup"><span data-stu-id="43a43-127">Creates a new instance of the **CMemAllocator** class.</span></span>                   |
| <span data-ttu-id="43a43-128">Методы Имемаллокатор</span><span class="sxs-lookup"><span data-stu-id="43a43-128">IMemAllocator Methods</span></span>                                   | <span data-ttu-id="43a43-129">Описание</span><span class="sxs-lookup"><span data-stu-id="43a43-129">Description</span></span>                                                              |
| [<span data-ttu-id="43a43-130">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="43a43-130">**SetProperties**</span></span>](cmemallocator-setproperties.md)    | <span data-ttu-id="43a43-131">Указывает количество выделяемых буферов и размер каждого буфера.</span><span class="sxs-lookup"><span data-stu-id="43a43-131">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="43a43-132">Требования</span><span class="sxs-lookup"><span data-stu-id="43a43-132">Requirements</span></span>



| <span data-ttu-id="43a43-133">Требование</span><span class="sxs-lookup"><span data-stu-id="43a43-133">Requirement</span></span> | <span data-ttu-id="43a43-134">Значение</span><span class="sxs-lookup"><span data-stu-id="43a43-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a43-135">Header</span><span class="sxs-lookup"><span data-stu-id="43a43-135">Header</span></span><br/>  | <dl> <span data-ttu-id="43a43-136"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43a43-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43a43-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43a43-137">Library</span></span><br/> | <dl> <span data-ttu-id="43a43-138"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="43a43-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a43-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43a43-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a43-140">Предоставление пользовательского распределителя</span><span class="sxs-lookup"><span data-stu-id="43a43-140">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
</dt> </dl>

 

 




