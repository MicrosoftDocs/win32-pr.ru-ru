---
description: Метод Кбаселист реализует список абтракт. Шаблон класса Кженериклист, производный от Кбаселист, обеспечивает проверку типов и более простой интерфейс, чем класс Кбаселист.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Класс Кбаселист (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665326"
---
# <a name="cbaselist-class"></a><span data-ttu-id="8a8b4-104">Класс Кбаселист</span><span class="sxs-lookup"><span data-stu-id="8a8b4-104">CBaseList class</span></span>

![Иерархия классов кбаселист](images/list01.png)

<span data-ttu-id="8a8b4-106">Метод **кбаселист** реализует список абтракт.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-106">The **CBaseList** method implements an abtract list.</span></span> <span data-ttu-id="8a8b4-107">Шаблон класса [**кженериклист**](cgenericlist.md) , производный от **кбаселист**, обеспечивает проверку типов и более простой интерфейс, чем класс **кбаселист** .</span><span class="sxs-lookup"><span data-stu-id="8a8b4-107">The [**CGenericList**](cgenericlist.md) class template, which derives from **CBaseList**, provides type checking and a simpler interface than the **CBaseList** class.</span></span>

<span data-ttu-id="8a8b4-108">Класс **кбаселист** моделируется после класса **коблист** в библиотеке Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="8a8b4-108">The **CBaseList** class is modeled after the **CObList** class in the Microsoft Foundation Classes (MFC) library.</span></span> <span data-ttu-id="8a8b4-109">Позиции в списке представлены структурой позиции.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-109">Positions within the list are represented by a POSITION structure.</span></span> <span data-ttu-id="8a8b4-110">Вызывающий объект не должен обращаться к внутренним элементам структуры ПОЗИЦИОНИРОВАНИЯ; рассматривать его как указатель на узел списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-110">The caller should not access the internal members of the POSITION structure; treat it as a pointer to a list node.</span></span> <span data-ttu-id="8a8b4-111">Расположение объекта в списке остается действительным до тех пор, пока объект не будет удален.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-111">The position of an object in the list remains valid until the object is deleted.</span></span>

<span data-ttu-id="8a8b4-112">В списке не требуется поддержка каких бы то ни было объектов, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-112">The list does not require any support by the objects it contains.</span></span> <span data-ttu-id="8a8b4-113">Он не выполняет Управление хранением и копирование объектов.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-113">It performs no storage management or copying on the objects.</span></span> <span data-ttu-id="8a8b4-114">Объекты могут находиться в нескольких списках.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-114">Objects can be in multiple lists.</span></span>

<span data-ttu-id="8a8b4-115">Примерно половина методов в этом классе действует на одиночные объекты.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-115">Roughly half of the methods in this class act on single objects.</span></span> <span data-ttu-id="8a8b4-116">Эти методы имеют суффикс-I в имени метода.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-116">These methods have the suffix - I in the method name.</span></span> <span data-ttu-id="8a8b4-117">Другие методы работают со всеми списками.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-117">The other methods act on entire lists.</span></span> <span data-ttu-id="8a8b4-118">Например, метод [**кбаселист:: аддафтер**](cbaselist-addafter.md) добавляет список в другой список.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-118">For example, the [**CBaseList::AddAfter**](cbaselist-addafter.md) method appends a list to another list.</span></span> <span data-ttu-id="8a8b4-119">Операции с одним объектом возвращают значения позиций или **значение NULL** при сбое.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-119">Single-object operations return POSITION values, or **NULL** on failure.</span></span> <span data-ttu-id="8a8b4-120">Операции List возвращают **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-120">List operations return **TRUE** if successful or **FALSE** otherwise.</span></span>



| <span data-ttu-id="8a8b4-121">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="8a8b4-121">Protected Member Variables</span></span>                             | <span data-ttu-id="8a8b4-122">Описание</span><span class="sxs-lookup"><span data-stu-id="8a8b4-122">Description</span></span>                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="8a8b4-123">**\_число м**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-123">**m\_Count**</span></span>](cbaselist-m-count.md)                  | <span data-ttu-id="8a8b4-124">Число элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-124">Number of items in the list.</span></span>                                              |
| [<span data-ttu-id="8a8b4-125">**m \_ пфирст**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-125">**m\_pFirst**</span></span>](cbaselist-m-pfirst.md)                | <span data-ttu-id="8a8b4-126">Указатель на первый узел в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-126">Pointer to the first node in the list.</span></span>                                    |
| [<span data-ttu-id="8a8b4-127">**m \_ пласт**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-127">**m\_pLast**</span></span>](cbaselist-m-plast.md)                  | <span data-ttu-id="8a8b4-128">Указатель на последний узел в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-128">Pointer to the last node in the list.</span></span>                                     |
| <span data-ttu-id="8a8b4-129">Защищенные методы</span><span class="sxs-lookup"><span data-stu-id="8a8b4-129">Protected Methods</span></span>                                      | <span data-ttu-id="8a8b4-130">Описание</span><span class="sxs-lookup"><span data-stu-id="8a8b4-130">Description</span></span>                                                               |
| [<span data-ttu-id="8a8b4-131">**жетнексти**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-131">**GetNextI**</span></span>](cbaselist-getnexti.md)                 | <span data-ttu-id="8a8b4-132">Извлекает элемент в указанной позиции и перемещает позицию.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-132">Retrieves the item at the specified position, and advances the position.</span></span>  |
| [<span data-ttu-id="8a8b4-133">**жети**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-133">**GetI**</span></span>](cbaselist-geti.md)                         | <span data-ttu-id="8a8b4-134">Извлекает элемент в указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-134">Retrieves the item at the specified position.</span></span>                             |
| [<span data-ttu-id="8a8b4-135">**финди**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-135">**FindI**</span></span>](cbaselist-findi.md)                       | <span data-ttu-id="8a8b4-136">Извлекает первую позицию, содержащую указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-136">Retrieves the first position that holds the specified item.</span></span>               |
| [<span data-ttu-id="8a8b4-137">**ремовехеади**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-137">**RemoveHeadI**</span></span>](cbaselist-removeheadi.md)           | <span data-ttu-id="8a8b4-138">Удаляет первый элемент из списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-138">Removes the first item in the list.</span></span>                                       |
| [<span data-ttu-id="8a8b4-139">**ремоветаили**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-139">**RemoveTailI**</span></span>](cbaselist-removetaili.md)           | <span data-ttu-id="8a8b4-140">Удаляет последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-140">Removes the last item in the list.</span></span>                                        |
| [<span data-ttu-id="8a8b4-141">**ремовеи**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-141">**RemoveI**</span></span>](cbaselist-removei.md)                   | <span data-ttu-id="8a8b4-142">Удаляет элемент по указанному положению.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-142">Removes the item at the specified position.</span></span>                               |
| [<span data-ttu-id="8a8b4-143">**аддтаили**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-143">**AddTailI**</span></span>](cbaselist-addtaili.md)                 | <span data-ttu-id="8a8b4-144">Добавляет элемент в конец списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-144">Adds an item to the end of the list.</span></span>                                      |
| [<span data-ttu-id="8a8b4-145">**аддхеади**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-145">**AddHeadI**</span></span>](cbaselist-addheadi.md)                 | <span data-ttu-id="8a8b4-146">Добавляет элемент в начало списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-146">Adds an item to the front of the list.</span></span>                                    |
| [<span data-ttu-id="8a8b4-147">**аддафтери**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-147">**AddAfterI**</span></span>](cbaselist-addafteri.md)               | <span data-ttu-id="8a8b4-148">Вставляет элемент после указанной позиции.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-148">Inserts an item after the specified position.</span></span>                             |
| [<span data-ttu-id="8a8b4-149">**аддбефореи**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-149">**AddBeforeI**</span></span>](cbaselist-addbeforei.md)             | <span data-ttu-id="8a8b4-150">Вставляет элемент перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-150">Inserts an item before the specified position.</span></span>                            |
| <span data-ttu-id="8a8b4-151">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="8a8b4-151">Public Methods</span></span>                                         | <span data-ttu-id="8a8b4-152">Описание</span><span class="sxs-lookup"><span data-stu-id="8a8b4-152">Description</span></span>                                                               |
| [<span data-ttu-id="8a8b4-153">**кбаселист**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-153">**CBaseList**</span></span>](cbaselist-cbaselist.md)               | <span data-ttu-id="8a8b4-154">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-154">Constructor method.</span></span>                                                       |
| [<span data-ttu-id="8a8b4-155">**~ Кбаселист**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-155">**~ CBaseList**</span></span>](cbaselist--cbaselist.md)            | <span data-ttu-id="8a8b4-156">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-156">Destructor method.</span></span>                                                        |
| [<span data-ttu-id="8a8b4-157">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-157">**RemoveAll**</span></span>](cbaselist-removeall.md)               | <span data-ttu-id="8a8b4-158">Удаляет все узлы из списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-158">Removes all nodes from the list.</span></span>                                          |
| [<span data-ttu-id="8a8b4-159">**жесеадпоситиони**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-159">**GetHeadPositionI**</span></span>](cbaselist-getheadpositioni.md) | <span data-ttu-id="8a8b4-160">Извлекает позицию первого элемента в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-160">Retrieves the position of the first item in the list.</span></span>                     |
| [<span data-ttu-id="8a8b4-161">**жеттаилпоситиони**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-161">**GetTailPositionI**</span></span>](cbaselist-gettailpositioni.md) | <span data-ttu-id="8a8b4-162">Извлекает позицию последнего элемента списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-162">Retrieves the position of the last item of the list.</span></span>                      |
| [<span data-ttu-id="8a8b4-163">**жеткаунти**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-163">**GetCountI**</span></span>](cbaselist-getcounti.md)               | <span data-ttu-id="8a8b4-164">Возвращает количество элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-164">Retrieves the number of items in the list.</span></span>                                |
| [<span data-ttu-id="8a8b4-165">**Далее**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-165">**Next**</span></span>](cbaselist-next.md)                         | <span data-ttu-id="8a8b4-166">Извлекает следующее расположение в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-166">Retrieves the next position in the list.</span></span>                                  |
| [<span data-ttu-id="8a8b4-167">**Ранее**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-167">**Prev**</span></span>](cbaselist-prev.md)                         | <span data-ttu-id="8a8b4-168">Извлекает предыдущее расположение в списке.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-168">Retrieves the previous position in the list.</span></span>                              |
| [<span data-ttu-id="8a8b4-169">**аддхеад**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-169">**AddHead**</span></span>](cbaselist-addhead.md)                   | <span data-ttu-id="8a8b4-170">Вставляет еще один список в начале этого списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-170">Inserts another list at the front of this list.</span></span>                           |
| [<span data-ttu-id="8a8b4-171">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-171">**AddTail**</span></span>](cbaselist-addtail.md)                   | <span data-ttu-id="8a8b4-172">Добавляет еще один список в конец списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-172">Appends another list to the end of this list.</span></span>                             |
| [<span data-ttu-id="8a8b4-173">**аддафтер**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-173">**AddAfter**</span></span>](cbaselist-addafter.md)                 | <span data-ttu-id="8a8b4-174">Вставляет список после указанной должности.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-174">Inserts a list after the specified position.</span></span>                              |
| [<span data-ttu-id="8a8b4-175">**аддбефоре**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-175">**AddBefore**</span></span>](cbaselist-addbefore.md)               | <span data-ttu-id="8a8b4-176">Вставляет список перед указанной позицией.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-176">Inserts a list before the specified position.</span></span>                             |
| [<span data-ttu-id="8a8b4-177">**моветотаил**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-177">**MoveToTail**</span></span>](cbaselist-movetotail.md)             | <span data-ttu-id="8a8b4-178">Разделяет список и добавляет к концу другого списка часть заголовка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-178">Splits the list and appends the head portion to the tail of another list.</span></span> |
| [<span data-ttu-id="8a8b4-179">**моветохеад**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-179">**MoveToHead**</span></span>](cbaselist-movetohead.md)             | <span data-ttu-id="8a8b4-180">Разделяет список и вставляет фрагмент хвоста в заголовок другого списка.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-180">Splits the list and inserts the tail portion at the head of another list.</span></span> |
| [<span data-ttu-id="8a8b4-181">**Отмена**</span><span class="sxs-lookup"><span data-stu-id="8a8b4-181">**Reverse**</span></span>](cbaselist-reverse.md)                   | <span data-ttu-id="8a8b4-182">Изменяет порядок списка на обратный.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-182">Reverses the order of the list.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="8a8b4-183">Требования</span><span class="sxs-lookup"><span data-stu-id="8a8b4-183">Requirements</span></span>



| <span data-ttu-id="8a8b4-184">Требование</span><span class="sxs-lookup"><span data-stu-id="8a8b4-184">Requirement</span></span> | <span data-ttu-id="8a8b4-185">Значение</span><span class="sxs-lookup"><span data-stu-id="8a8b4-185">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8b4-186">Header</span><span class="sxs-lookup"><span data-stu-id="8a8b4-186">Header</span></span><br/>  | <dl> <span data-ttu-id="8a8b4-187"><dt>Вкслист. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a8b4-187"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8a8b4-188">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a8b4-188">Library</span></span><br/> | <dl> <span data-ttu-id="8a8b4-189"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8a8b4-189"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a8b4-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a8b4-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8b4-191">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="8a8b4-191">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




