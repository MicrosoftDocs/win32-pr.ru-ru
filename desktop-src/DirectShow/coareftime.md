---
description: Класс Коарефтиме преобразует время ссылки между секундами и 100-наносекундных единицами.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Класс Коарефтиме (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674862"
---
# <a name="coareftime-class"></a><span data-ttu-id="5173a-103">Класс Коарефтиме</span><span class="sxs-lookup"><span data-stu-id="5173a-103">COARefTime class</span></span>

![Иерархия классов коарефтиме](images/cutil05.png)

<span data-ttu-id="5173a-105">`COARefTime`Класс преобразует время ссылки между секундами и 100-наносекундных единицами.</span><span class="sxs-lookup"><span data-stu-id="5173a-105">The `COARefTime` class converts reference times between seconds and 100-nanosecond units.</span></span>

<span data-ttu-id="5173a-106">Этот класс преобразует время между ссылками, совместимыми со службой автоматизации, и временем ссылки, совместимыми с C/C++.</span><span class="sxs-lookup"><span data-stu-id="5173a-106">This class converts between reference times that are compatible with Automation and reference times that are compatible with C/C++.</span></span> <span data-ttu-id="5173a-107">Совместимые с автоматизацией интерфейсы используют значения **Double** для представления времени в секундах.</span><span class="sxs-lookup"><span data-stu-id="5173a-107">Automation-compatible interfaces use **double** values to represent time in seconds.</span></span> <span data-ttu-id="5173a-108">Другие интерфейсы используют 64-битные значения **лонглонг** для представления времени в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="5173a-108">Other interfaces use 64-bit **LONGLONG** values to represent time in 100-nanosecond units.</span></span> <span data-ttu-id="5173a-109">Для этих значений определены следующие типы:</span><span class="sxs-lookup"><span data-stu-id="5173a-109">The following types are defined for these values:</span></span>

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

<span data-ttu-id="5173a-110">Фильтры могут использовать `COARefTime` класс для преобразования между двумя форматами.</span><span class="sxs-lookup"><span data-stu-id="5173a-110">Filters can use the `COARefTime` class to convert between the two formats.</span></span> <span data-ttu-id="5173a-111">Этот класс является производным от класса [**крефтиме**](creftime.md) .</span><span class="sxs-lookup"><span data-stu-id="5173a-111">This class is derived from the [**CRefTime**](creftime.md) class.</span></span>



| <span data-ttu-id="5173a-112">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="5173a-112">Public Methods</span></span>                                          | <span data-ttu-id="5173a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="5173a-113">Description</span></span>                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="5173a-114">**коарефтиме**</span><span class="sxs-lookup"><span data-stu-id="5173a-114">**COARefTime**</span></span>](coareftime-coareftime.md)             | <span data-ttu-id="5173a-115">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5173a-115">Constructor method.</span></span>                                                   |
| <span data-ttu-id="5173a-116">Операторы</span><span class="sxs-lookup"><span data-stu-id="5173a-116">Operators</span></span>                                               | <span data-ttu-id="5173a-117">Описание:</span><span class="sxs-lookup"><span data-stu-id="5173a-117">Description</span></span>                                                           |
| [<span data-ttu-id="5173a-118">**Дважды**</span><span class="sxs-lookup"><span data-stu-id="5173a-118">**double**</span></span>](coareftime-double.md)                     | <span data-ttu-id="5173a-119">Преобразует время ссылки в значение **типа Double** .</span><span class="sxs-lookup"><span data-stu-id="5173a-119">Converts the reference time to a **double** value.</span></span>                    |
| [<span data-ttu-id="5173a-120">**\_время ссылки**</span><span class="sxs-lookup"><span data-stu-id="5173a-120">**REFERENCE\_TIME**</span></span>](coareftime-reference-time.md)    | <span data-ttu-id="5173a-121">Приводит объект к значению **\_ времени ссылки** .</span><span class="sxs-lookup"><span data-stu-id="5173a-121">Casts the object to a **REFERENCE\_TIME** value.</span></span>                      |
| [<span data-ttu-id="5173a-122">**Оператор =**</span><span class="sxs-lookup"><span data-stu-id="5173a-122">**operator =**</span></span>](coareftime-operator-assign.md)        | <span data-ttu-id="5173a-123">Назначает новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="5173a-123">Assigns a new reference time.</span></span>                                         |
| [<span data-ttu-id="5173a-124">**Оператор = =**</span><span class="sxs-lookup"><span data-stu-id="5173a-124">**operator ==**</span></span>](coareftime-operator-eq.md)           | <span data-ttu-id="5173a-125">Проверяет равенство между двумя временами ссылки.</span><span class="sxs-lookup"><span data-stu-id="5173a-125">Tests for equality between two reference times.</span></span>                       |
| [<span data-ttu-id="5173a-126">**operator! =**</span><span class="sxs-lookup"><span data-stu-id="5173a-126">**operator !=**</span></span>](cmediatype-operator-neq.md)          | <span data-ttu-id="5173a-127">Проверяет на неравенство между двумя временем ссылки.</span><span class="sxs-lookup"><span data-stu-id="5173a-127">Tests for inequality between two reference times.</span></span>                     |
| [<span data-ttu-id="5173a-128">**Оператор <**</span><span class="sxs-lookup"><span data-stu-id="5173a-128">**operator <**</span></span>](coareftime-operator-lt.md)         | <span data-ttu-id="5173a-129">Проверяет, что одно время ссылки меньше другого.</span><span class="sxs-lookup"><span data-stu-id="5173a-129">Tests if one reference time is less than another.</span></span>                     |
| [<span data-ttu-id="5173a-130">**Оператор >**</span><span class="sxs-lookup"><span data-stu-id="5173a-130">**operator >**</span></span>](coareftime-operator-gt.md)         | <span data-ttu-id="5173a-131">Проверяет, что одно время ссылки больше другого.</span><span class="sxs-lookup"><span data-stu-id="5173a-131">Tests if one reference time is greater than another.</span></span>                  |
| [<span data-ttu-id="5173a-132">**Оператор <=**</span><span class="sxs-lookup"><span data-stu-id="5173a-132">**operator <=**</span></span>](coareftime-operator-lteq.md)      | <span data-ttu-id="5173a-133">Проверяет, что одно время ссылки меньше или равно другому.</span><span class="sxs-lookup"><span data-stu-id="5173a-133">Tests if one reference time is less than or equal to another.</span></span>         |
| [<span data-ttu-id="5173a-134">**Оператор >=**</span><span class="sxs-lookup"><span data-stu-id="5173a-134">**operator >=**</span></span>](coareftime-operator-gteq.md)      | <span data-ttu-id="5173a-135">Проверяет, что одно время ссылки больше или равно другому.</span><span class="sxs-lookup"><span data-stu-id="5173a-135">Tests if one reference time is greater than or equal to another.</span></span>      |
| [<span data-ttu-id="5173a-136">**operator +**</span><span class="sxs-lookup"><span data-stu-id="5173a-136">**operator +**</span></span>](coareftime-operator-plus.md)          | <span data-ttu-id="5173a-137">Добавляет два времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="5173a-137">Adds two reference times.</span></span>                                             |
| [<span data-ttu-id="5173a-138">\* \* Оператор \* \*</span><span class="sxs-lookup"><span data-stu-id="5173a-138">\*\*operator  \*\*</span></span>](coareftime-operator-minus.md)         | <span data-ttu-id="5173a-139">Вычитает одно время ссылки из другого.</span><span class="sxs-lookup"><span data-stu-id="5173a-139">Subtracts one reference time from another.</span></span>                            |
| [<span data-ttu-id="5173a-140">**operator + =**</span><span class="sxs-lookup"><span data-stu-id="5173a-140">**operator +=**</span></span>](coareftime-operator-plus-assign.md)  | <span data-ttu-id="5173a-141">Добавляет два значения времени ссылки и присваивает результат этому объекту.</span><span class="sxs-lookup"><span data-stu-id="5173a-141">Adds two reference times, and assigns the result to this object.</span></span>      |
| [<span data-ttu-id="5173a-142">**Оператор =**</span><span class="sxs-lookup"><span data-stu-id="5173a-142">**operator  =**</span></span>](coareftime-operator-minus-assign.md) | <span data-ttu-id="5173a-143">Вычитает два значения времени ссылки и присваивает результат этому объекту.</span><span class="sxs-lookup"><span data-stu-id="5173a-143">Subtracts two reference times, and assigns the result to this object.</span></span> |
| [<span data-ttu-id="5173a-144">**станции \***</span><span class="sxs-lookup"><span data-stu-id="5173a-144">**operator \***</span></span>](coareftime-operator-mult.md)         | <span data-ttu-id="5173a-145">Умножает время ссылки на значение.</span><span class="sxs-lookup"><span data-stu-id="5173a-145">Multiplies a reference time by a value.</span></span>                               |
| [<span data-ttu-id="5173a-146">**станции**</span><span class="sxs-lookup"><span data-stu-id="5173a-146">**operator /**</span></span>](coareftime-operator-div.md)           | <span data-ttu-id="5173a-147">Делит время ссылки на значение.</span><span class="sxs-lookup"><span data-stu-id="5173a-147">Divides a reference time by a value.</span></span>                                  |



 

## <a name="requirements"></a><span data-ttu-id="5173a-148">Требования</span><span class="sxs-lookup"><span data-stu-id="5173a-148">Requirements</span></span>



| <span data-ttu-id="5173a-149">Требование</span><span class="sxs-lookup"><span data-stu-id="5173a-149">Requirement</span></span> | <span data-ttu-id="5173a-150">Значение</span><span class="sxs-lookup"><span data-stu-id="5173a-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5173a-151">Header</span><span class="sxs-lookup"><span data-stu-id="5173a-151">Header</span></span><br/>  | <dl> <span data-ttu-id="5173a-152"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5173a-152"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5173a-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5173a-153">Library</span></span><br/> | <dl> <span data-ttu-id="5173a-154"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5173a-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




