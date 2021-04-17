---
description: Класс Кункновн реализует интерфейс IUnknown. Большинство объектов модели COM в DirectShow являются производными от Кункновн.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Класс Кункновн (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679691"
---
# <a name="cunknown-class"></a><span data-ttu-id="0a08a-104">Класс Кункновн</span><span class="sxs-lookup"><span data-stu-id="0a08a-104">CUnknown class</span></span>

![Иерархия классов кункновн](images/cbase01.png)

<span data-ttu-id="0a08a-106">Класс **кункновн** реализует интерфейс **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="0a08a-106">The **CUnknown** class implements the **IUnknown** interface.</span></span> <span data-ttu-id="0a08a-107">Большинство объектов модели COM в DirectShow являются производными от **кункновн**.</span><span class="sxs-lookup"><span data-stu-id="0a08a-107">Most Component Object Model (COM) objects in DirectShow derive from **CUnknown**.</span></span>

<span data-ttu-id="0a08a-108">При реализации COM-объекта может потребоваться наследование его от **кункновн**.</span><span class="sxs-lookup"><span data-stu-id="0a08a-108">If you implement a COM object, you might want to derive it from **CUnknown**.</span></span> <span data-ttu-id="0a08a-109">Наследование от **кункновн** обеспечивает поточно-ориентированную реализацию и позволяет избежать проблем, связанных с реализацией **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="0a08a-109">Deriving from **CUnknown** provides a thread-safe implementation, and saves you the trouble of implementing **IUnknown**.</span></span>

<span data-ttu-id="0a08a-110">Подробное описание использования этого базового класса см. [в разделе Реализация IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0a08a-110">For a detailed discussion of how to use this base class, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span> <span data-ttu-id="0a08a-111">Ниже приведен краткий обзор.</span><span class="sxs-lookup"><span data-stu-id="0a08a-111">What follows is a brief summary:</span></span>

-   <span data-ttu-id="0a08a-112">Включите макрос [**Declare \_ IUnknown**](declare-iunknown.md) в открытый раздел определения класса.</span><span class="sxs-lookup"><span data-stu-id="0a08a-112">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public section of your class definition.</span></span> <span data-ttu-id="0a08a-113">Этот макрос объявляет три метода интерфейса **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="0a08a-113">This macro declares the three methods of the **IUnknown** interface.</span></span>
-   <span data-ttu-id="0a08a-114">Переопределите метод [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) для поддержки интерфейсов, отличных от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="0a08a-114">Override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method to support interfaces other than **IUnknown**.</span></span> <span data-ttu-id="0a08a-115">В этом методе вызовите [**функцию WebMethod**](getinterface.md) для получения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0a08a-115">Within this method, call the [**GetInterface**](getinterface.md) function to retrieve interface pointers.</span></span>
-   <span data-ttu-id="0a08a-116">В конструкторе класса вызовите метод конструктора **кункновн** .</span><span class="sxs-lookup"><span data-stu-id="0a08a-116">In your class constructor, invoke the **CUnknown** constructor method.</span></span>



| <span data-ttu-id="0a08a-117">Защищенные переменные членов</span><span class="sxs-lookup"><span data-stu-id="0a08a-117">Protected Member Variables</span></span>                                                  | <span data-ttu-id="0a08a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0a08a-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="0a08a-119">**«m», \_ cref**</span><span class="sxs-lookup"><span data-stu-id="0a08a-119">**m\_cRef**</span></span>](cunknown-m-cref.md)                                          | <span data-ttu-id="0a08a-120">Число ссылок.</span><span class="sxs-lookup"><span data-stu-id="0a08a-120">Reference count.</span></span>                                                   |
| <span data-ttu-id="0a08a-121">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="0a08a-121">Public Methods</span></span>                                                              | <span data-ttu-id="0a08a-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0a08a-122">Description</span></span>                                                        |
| [<span data-ttu-id="0a08a-123">**кункновн**</span><span class="sxs-lookup"><span data-stu-id="0a08a-123">**CUnknown**</span></span>](cunknown-cunknown.md)                                       | <span data-ttu-id="0a08a-124">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="0a08a-124">Constructor method.</span></span>                                                |
| [<span data-ttu-id="0a08a-125">**~ Кункновн**</span><span class="sxs-lookup"><span data-stu-id="0a08a-125">**~ CUnknown**</span></span>](cunknown--cunknown.md)                                    | <span data-ttu-id="0a08a-126">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="0a08a-126">Destructor method.</span></span> <span data-ttu-id="0a08a-127">Виртуализаци.</span><span class="sxs-lookup"><span data-stu-id="0a08a-127">Virtual.</span></span>                                        |
| [<span data-ttu-id="0a08a-128">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="0a08a-128">**GetOwner**</span></span>](cunknown-getowner.md)                                       | <span data-ttu-id="0a08a-129">Возвращает указатель на управляющий **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="0a08a-129">Gets a pointer to the controlling **IUnknown**.</span></span>                    |
| <span data-ttu-id="0a08a-130">Методы Инонделегатингункновн</span><span class="sxs-lookup"><span data-stu-id="0a08a-130">INonDelegatingUnknown Methods</span></span>                                               | <span data-ttu-id="0a08a-131">Описание</span><span class="sxs-lookup"><span data-stu-id="0a08a-131">Description</span></span>                                                        |
| [<span data-ttu-id="0a08a-132">**нонделегатингаддреф**</span><span class="sxs-lookup"><span data-stu-id="0a08a-132">**NonDelegatingAddRef**</span></span>](cunknown-nondelegatingaddref.md)                 | <span data-ttu-id="0a08a-133">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="0a08a-133">Increments the reference count.</span></span>                                    |
| [<span data-ttu-id="0a08a-134">**нонделегатингкуеринтерфаце**</span><span class="sxs-lookup"><span data-stu-id="0a08a-134">**NonDelegatingQueryInterface**</span></span>](cunknown-nondelegatingqueryinterface.md) | <span data-ttu-id="0a08a-135">Извлекает указатель интерфейса и увеличивает счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="0a08a-135">Retrieves an interface pointer and increments the reference count.</span></span> |
| [<span data-ttu-id="0a08a-136">**нонделегатингрелеасе**</span><span class="sxs-lookup"><span data-stu-id="0a08a-136">**NonDelegatingRelease**</span></span>](cunknown-nondelegatingrelease.md)               | <span data-ttu-id="0a08a-137">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="0a08a-137">Decrements the reference count.</span></span>                                    |



 

## <a name="requirements"></a><span data-ttu-id="0a08a-138">Требования</span><span class="sxs-lookup"><span data-stu-id="0a08a-138">Requirements</span></span>



| <span data-ttu-id="0a08a-139">Требование</span><span class="sxs-lookup"><span data-stu-id="0a08a-139">Requirement</span></span> | <span data-ttu-id="0a08a-140">Значение</span><span class="sxs-lookup"><span data-stu-id="0a08a-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a08a-141">Header</span><span class="sxs-lookup"><span data-stu-id="0a08a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="0a08a-142"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a08a-142"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a08a-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0a08a-143">Library</span></span><br/> | <dl> <span data-ttu-id="0a08a-144"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0a08a-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a08a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a08a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a08a-146">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a08a-146">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




