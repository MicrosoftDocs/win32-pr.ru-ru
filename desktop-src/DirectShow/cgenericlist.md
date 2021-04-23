---
description: Шаблон класса Кженериклист, реализующий список, зависящий от типа. Дополнительные сведения см. в разделе Кбаселист.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Класс Кженериклист (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657555"
---
# <a name="cgenericlist-class"></a><span data-ttu-id="33a38-104">Класс Кженериклист</span><span class="sxs-lookup"><span data-stu-id="33a38-104">CGenericList class</span></span>

![Иерархия классов кженериклист](images/list01.png)

<span data-ttu-id="33a38-106">`CGenericList`Шаблон класса, реализующий список, зависящий от типа.</span><span class="sxs-lookup"><span data-stu-id="33a38-106">The `CGenericList` class template that implements a type-specific list.</span></span> <span data-ttu-id="33a38-107">Дополнительные сведения см. в разделе [**кбаселист**](cbaselist.md).</span><span class="sxs-lookup"><span data-stu-id="33a38-107">For more information, see [**CBaseList**](cbaselist.md).</span></span>

<span data-ttu-id="33a38-108">Чтобы использовать этот шаблон, объявите переменную типа `CGenericList` с аргументом шаблона, который определяет тип объекта в списке.</span><span class="sxs-lookup"><span data-stu-id="33a38-108">To use this template, declare a variable of type `CGenericList` with a template argument that defines the type of object in the list.</span></span> <span data-ttu-id="33a38-109">Например, следующая инструкция объявляет список объектов [**кбасефилтер**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="33a38-109">For example, the following statement declares a list of [**CBaseFilter**](cbasefilter.md) objects:</span></span>


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



<span data-ttu-id="33a38-110">Для удобства Вкслист. h определяет следующие типы списков:</span><span class="sxs-lookup"><span data-stu-id="33a38-110">For convenience, Wxlist.h defines the following list types:</span></span>

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| <span data-ttu-id="33a38-111">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="33a38-111">Public Methods</span></span>                                          | <span data-ttu-id="33a38-112">Описание</span><span class="sxs-lookup"><span data-stu-id="33a38-112">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="33a38-113">**кженериклист**</span><span class="sxs-lookup"><span data-stu-id="33a38-113">**CGenericList**</span></span>](cgenericlist-cgenericlist.md)       | <span data-ttu-id="33a38-114">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="33a38-114">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="33a38-115">**~ Кженериклист**</span><span class="sxs-lookup"><span data-stu-id="33a38-115">**~CGenericList**</span></span>](cgenericlist--cgenericlist.md)     | <span data-ttu-id="33a38-116">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="33a38-116">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="33a38-117">**жесеадпоситион**</span><span class="sxs-lookup"><span data-stu-id="33a38-117">**GetHeadPosition**</span></span>](cgenericlist-getheadposition.md) | <span data-ttu-id="33a38-118">Извлекает позицию первого элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="33a38-118">Retrieves the position of the first item in the list.</span></span>                    |
| [<span data-ttu-id="33a38-119">**жеттаилпоситион**</span><span class="sxs-lookup"><span data-stu-id="33a38-119">**GetTailPosition**</span></span>](cgenericlist-gettailposition.md) | <span data-ttu-id="33a38-120">Извлекает позицию последнего элемента списка.</span><span class="sxs-lookup"><span data-stu-id="33a38-120">Retrieves the position of the last item of the list.</span></span>                     |
| [<span data-ttu-id="33a38-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="33a38-121">**GetCount**</span></span>](cgenericlist-getcount.md)               | <span data-ttu-id="33a38-122">Возвращает количество элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="33a38-122">Retrieves the number of items in the list.</span></span>                               |
| [<span data-ttu-id="33a38-123">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="33a38-123">**GetNext**</span></span>](cgenericlist-getnext.md)                 | <span data-ttu-id="33a38-124">Извлекает элемент в указанной позиции и перемещает позицию.</span><span class="sxs-lookup"><span data-stu-id="33a38-124">Retrieves the item at the specified position, and advances the position.</span></span> |
| [<span data-ttu-id="33a38-125">**Получить**</span><span class="sxs-lookup"><span data-stu-id="33a38-125">**Get**</span></span>](cgenericlist-get.md)                         | <span data-ttu-id="33a38-126">Извлекает элемент в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="33a38-126">Retrieves the item at the specified position.</span></span>                            |
| [<span data-ttu-id="33a38-127">**Вышлем**</span><span class="sxs-lookup"><span data-stu-id="33a38-127">**GetHead**</span></span>](cgenericlist-gethead.md)                 | <span data-ttu-id="33a38-128">Извлекает элемент в заголовке списка.</span><span class="sxs-lookup"><span data-stu-id="33a38-128">Retrieves the item at the head of the list.</span></span>                              |
| [<span data-ttu-id="33a38-129">**ремовехеад**</span><span class="sxs-lookup"><span data-stu-id="33a38-129">**RemoveHead**</span></span>](cgenericlist-removehead.md)           | <span data-ttu-id="33a38-130">Удаляет первый элемент из списка.</span><span class="sxs-lookup"><span data-stu-id="33a38-130">Removes the first item in the list.</span></span>                                      |
| [<span data-ttu-id="33a38-131">**ремоветаил**</span><span class="sxs-lookup"><span data-stu-id="33a38-131">**RemoveTail**</span></span>](cgenericlist-removetail.md)           | <span data-ttu-id="33a38-132">Удаляет последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="33a38-132">Removes the last item in the list.</span></span>                                       |
| [<span data-ttu-id="33a38-133">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="33a38-133">**Remove**</span></span>](cgenericlist-remove.md)                   | <span data-ttu-id="33a38-134">Удаляет элемент по указанному положению.</span><span class="sxs-lookup"><span data-stu-id="33a38-134">Removes the item at the specified position.</span></span>                              |
| [<span data-ttu-id="33a38-135">**аддбефоре**</span><span class="sxs-lookup"><span data-stu-id="33a38-135">**AddBefore**</span></span>](cgenericlist-addbefore.md)             | <span data-ttu-id="33a38-136">Вставляет элемент или список до указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="33a38-136">Inserts an item or list before the specified position.</span></span>                   |
| [<span data-ttu-id="33a38-137">**аддафтер**</span><span class="sxs-lookup"><span data-stu-id="33a38-137">**AddAfter**</span></span>](cgenericlist-addafter.md)               | <span data-ttu-id="33a38-138">Вставляет элемент или список после указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="33a38-138">Inserts an item or list after the specified position.</span></span>                    |
| [<span data-ttu-id="33a38-139">**аддхеад**</span><span class="sxs-lookup"><span data-stu-id="33a38-139">**AddHead**</span></span>](cgenericlist-addhead.md)                 | <span data-ttu-id="33a38-140">Добавляет элемент или список в начало списка.</span><span class="sxs-lookup"><span data-stu-id="33a38-140">Adds an item or list to the front of the list.</span></span>                           |
| [<span data-ttu-id="33a38-141">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="33a38-141">**AddTail**</span></span>](cgenericlist-addtail.md)                 | <span data-ttu-id="33a38-142">Добавляет элемент или список в конец списка.</span><span class="sxs-lookup"><span data-stu-id="33a38-142">Appends an item or list to the end of the list.</span></span>                          |
| [<span data-ttu-id="33a38-143">**Поиск**</span><span class="sxs-lookup"><span data-stu-id="33a38-143">**Find**</span></span>](cgenericlist-find.md)                       | <span data-ttu-id="33a38-144">Извлекает первую позицию, содержащую указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="33a38-144">Retrieves the first position that holds the specified item.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="33a38-145">Требования</span><span class="sxs-lookup"><span data-stu-id="33a38-145">Requirements</span></span>



| <span data-ttu-id="33a38-146">Требование</span><span class="sxs-lookup"><span data-stu-id="33a38-146">Requirement</span></span> | <span data-ttu-id="33a38-147">Значение</span><span class="sxs-lookup"><span data-stu-id="33a38-147">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a38-148">Header</span><span class="sxs-lookup"><span data-stu-id="33a38-148">Header</span></span><br/>  | <dl> <span data-ttu-id="33a38-149"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33a38-149"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="33a38-150">Библиотека</span><span class="sxs-lookup"><span data-stu-id="33a38-150">Library</span></span><br/> | <dl> <span data-ttu-id="33a38-151"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="33a38-151"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




