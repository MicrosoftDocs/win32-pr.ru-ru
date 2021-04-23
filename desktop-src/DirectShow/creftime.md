---
description: Класс Крефтиме является вспомогательным классом для управления временем ссылок.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Класс Крефтиме (Рефтиме. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657285"
---
# <a name="creftime-class"></a><span data-ttu-id="712f5-103">Класс Крефтиме</span><span class="sxs-lookup"><span data-stu-id="712f5-103">CRefTime class</span></span>

![Иерархия классов крефтиме](images/cutil05.png)

<span data-ttu-id="712f5-105">`CRefTime`Класс является вспомогательным классом для управления временем ссылок.</span><span class="sxs-lookup"><span data-stu-id="712f5-105">The `CRefTime` class is a helper class for managing reference times.</span></span>

<span data-ttu-id="712f5-106">*Время ссылки* — это единица времени, представленная в единицах измерения в 100 нс.</span><span class="sxs-lookup"><span data-stu-id="712f5-106">A *reference time* is a unit of time represented in 100-nanosecond units.</span></span> <span data-ttu-id="712f5-107">Этот класс использует тот же макет данных, что [**и \_ ссылочный**](reference-time.md) тип данных, но добавляет некоторые методы и операторы, обеспечивающие сравнение, преобразование и арифметические функции.</span><span class="sxs-lookup"><span data-stu-id="712f5-107">This class shares the same data layout as the [**REFERENCE\_TIME**](reference-time.md) data type, but adds some methods and operators that provide comparison, conversion, and arithmetic functions.</span></span> <span data-ttu-id="712f5-108">Дополнительные сведения о времени ссылки см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="712f5-108">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>



| <span data-ttu-id="712f5-109">Открытые переменные члена</span><span class="sxs-lookup"><span data-stu-id="712f5-109">Public Member Variables</span></span>                                                 | <span data-ttu-id="712f5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="712f5-110">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="712f5-111">**\_время m**</span><span class="sxs-lookup"><span data-stu-id="712f5-111">**m\_time**</span></span>](creftime-m-time.md)                                      | <span data-ttu-id="712f5-112">Указывает значение **\_ времени ссылки** .</span><span class="sxs-lookup"><span data-stu-id="712f5-112">Specifies the **REFERENCE\_TIME** value.</span></span>              |
| <span data-ttu-id="712f5-113">Открытые методы</span><span class="sxs-lookup"><span data-stu-id="712f5-113">Public Methods</span></span>                                                          | <span data-ttu-id="712f5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="712f5-114">Description</span></span>                                           |
| [<span data-ttu-id="712f5-115">**крефтиме**</span><span class="sxs-lookup"><span data-stu-id="712f5-115">**CRefTime**</span></span>](creftime-creftime.md)                                   | <span data-ttu-id="712f5-116">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="712f5-116">Constructor method.</span></span>                                   |
| [<span data-ttu-id="712f5-117">**Единицы измерения**</span><span class="sxs-lookup"><span data-stu-id="712f5-117">**GetUnits**</span></span>](creftime-getunits.md)                                   | <span data-ttu-id="712f5-118">Извлекает время ссылки в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="712f5-118">Retrieves the reference time in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="712f5-119">**МС)**</span><span class="sxs-lookup"><span data-stu-id="712f5-119">**Millisecs**</span></span>](creftime-millisecs.md)                                 | <span data-ttu-id="712f5-120">Преобразует время ссылки в миллисекунды.</span><span class="sxs-lookup"><span data-stu-id="712f5-120">Converts the reference time to milliseconds.</span></span>          |
| <span data-ttu-id="712f5-121">Операторы</span><span class="sxs-lookup"><span data-stu-id="712f5-121">Operators</span></span>                                                               | <span data-ttu-id="712f5-122">Описание:</span><span class="sxs-lookup"><span data-stu-id="712f5-122">Description</span></span>                                           |
| [<span data-ttu-id="712f5-123">**время ссылки оператора \_ ()**</span><span class="sxs-lookup"><span data-stu-id="712f5-123">**operator REFERENCE\_TIME()**</span></span>](creftime-operator-reference-time-.md) | <span data-ttu-id="712f5-124">Приводит объект к **ссылочному типу данных \_ времени** .</span><span class="sxs-lookup"><span data-stu-id="712f5-124">Casts the object to a **REFERENCE\_TIME** data type.</span></span>  |
| [<span data-ttu-id="712f5-125">**Оператор =**</span><span class="sxs-lookup"><span data-stu-id="712f5-125">**operator=**</span></span>](creftime-operator-assign.md)                           | <span data-ttu-id="712f5-126">Назначает новое время ссылки.</span><span class="sxs-lookup"><span data-stu-id="712f5-126">Assigns a new reference time.</span></span>                         |
| [<span data-ttu-id="712f5-127">**operator + =**</span><span class="sxs-lookup"><span data-stu-id="712f5-127">**operator+=**</span></span>](creftime-operator-plus-assign.md)                     | <span data-ttu-id="712f5-128">Добавляет два времени ссылки.</span><span class="sxs-lookup"><span data-stu-id="712f5-128">Adds two reference times.</span></span>                             |
| [<span data-ttu-id="712f5-129">**Оператор =**</span><span class="sxs-lookup"><span data-stu-id="712f5-129">**operator =**</span></span>](creftime-operator-minus-assign.md)                    | <span data-ttu-id="712f5-130">Вычитает одно время ссылки из другого.</span><span class="sxs-lookup"><span data-stu-id="712f5-130">Subtracts one reference time from another.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="712f5-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="712f5-131">Remarks</span></span>

<span data-ttu-id="712f5-132">Использование этого класса может привести к возникновению трудностей.</span><span class="sxs-lookup"><span data-stu-id="712f5-132">There is a potential pitfall with using this class.</span></span> <span data-ttu-id="712f5-133">Если применить оператор + = с объектом **крефтиме** в качестве левого операнда и переменной типа **Long** в качестве правого операнда, компилятор будет неявно приводить правый операнд к объекту **крефтиме** .</span><span class="sxs-lookup"><span data-stu-id="712f5-133">If you apply the += operator with a **CRefTime** object as the left operand and a variable of type **LONG** as the right operand, the compiler will implicitly coerce the right operand into a **CRefTime** object.</span></span> <span data-ttu-id="712f5-134">Это приведение использует конструктор **крефтиме** , который преобразует миллисекунды в ссылочные \_ единицы времени; в результате правый операнд умножается на 10 000:</span><span class="sxs-lookup"><span data-stu-id="712f5-134">This coercion uses the **CRefTime** constructor that converts milliseconds into REFERENCE\_TIME units; as a result, the right operand is multiplied by 10,000:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



<span data-ttu-id="712f5-135">Однако то же самое не происходит при использовании оператора +:</span><span class="sxs-lookup"><span data-stu-id="712f5-135">However, the same thing does not happen using the + operator:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a><span data-ttu-id="712f5-136">Требования</span><span class="sxs-lookup"><span data-stu-id="712f5-136">Requirements</span></span>



| <span data-ttu-id="712f5-137">Требование</span><span class="sxs-lookup"><span data-stu-id="712f5-137">Requirement</span></span> | <span data-ttu-id="712f5-138">Значение</span><span class="sxs-lookup"><span data-stu-id="712f5-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="712f5-139">Header</span><span class="sxs-lookup"><span data-stu-id="712f5-139">Header</span></span><br/>  | <dl> <span data-ttu-id="712f5-140"><dt>Рефтиме. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="712f5-140"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="712f5-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="712f5-141">Library</span></span><br/> | <dl> <span data-ttu-id="712f5-142"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="712f5-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




