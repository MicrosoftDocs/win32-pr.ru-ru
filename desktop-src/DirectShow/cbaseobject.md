---
description: Класс Кбасеобжект является абстрактным классом для реализации объектов DirectShow. Для реализации объектов модели COM используйте класс Кункновн, производный от Кбасеобжект.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Класс Кбасеобжект (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665408"
---
# <a name="cbaseobject-class"></a><span data-ttu-id="99115-104">Класс Кбасеобжект</span><span class="sxs-lookup"><span data-stu-id="99115-104">CBaseObject class</span></span>

<span data-ttu-id="99115-105">Класс **кбасеобжект** является абстрактным классом для реализации объектов DirectShow.</span><span class="sxs-lookup"><span data-stu-id="99115-105">The **CBaseObject** class is an abstract class for implementing DirectShow objects.</span></span> <span data-ttu-id="99115-106">Для реализации объектов модели COM используйте класс [**кункновн**](cunknown.md) , производный от **кбасеобжект**.</span><span class="sxs-lookup"><span data-stu-id="99115-106">To implement Component Object Model (COM) objects, use the [**CUnknown**](cunknown.md) class, which derives from **CBaseObject**.</span></span>



| <span data-ttu-id="99115-107">Методы класса</span><span class="sxs-lookup"><span data-stu-id="99115-107">Class Methods</span></span>                                      | <span data-ttu-id="99115-108">Описание</span><span class="sxs-lookup"><span data-stu-id="99115-108">Description</span></span>                            |
|----------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="99115-109">**кбасеобжект**</span><span class="sxs-lookup"><span data-stu-id="99115-109">**CBaseObject**</span></span>](cbaseobject-cbaseobject.md)     | <span data-ttu-id="99115-110">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="99115-110">Constructor method.</span></span>                    |
| [<span data-ttu-id="99115-111">**~ Кбасеобжект**</span><span class="sxs-lookup"><span data-stu-id="99115-111">**~CBaseObject**</span></span>](cbaseobject--cbaseobject.md)   | <span data-ttu-id="99115-112">Метод деструктора.</span><span class="sxs-lookup"><span data-stu-id="99115-112">Destructor method.</span></span>                     |
| [<span data-ttu-id="99115-113">**обжектсактиве**</span><span class="sxs-lookup"><span data-stu-id="99115-113">**ObjectsActive**</span></span>](cbaseobject-objectsactive.md) | <span data-ttu-id="99115-114">Возвращает число активных объектов.</span><span class="sxs-lookup"><span data-stu-id="99115-114">Retrieves the count of active objects.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="99115-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99115-115">Remarks</span></span>

<span data-ttu-id="99115-116">Большая часть базовых классов DirectShow является производной от **кбасеобжект**.</span><span class="sxs-lookup"><span data-stu-id="99115-116">Most of the DirectShow base classes derive from **CBaseObject**.</span></span> <span data-ttu-id="99115-117">Этот класс предоставляет помощь при отладке, сохраняя количество всех объектов DirectShow, активных во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="99115-117">This class provides debugging assistance by keeping a count of all the DirectShow objects active during run time.</span></span> <span data-ttu-id="99115-118">Число объектов хранится в переменной статического члена класса:</span><span class="sxs-lookup"><span data-stu-id="99115-118">The object count is stored in a class-static member variable:</span></span>


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



<span data-ttu-id="99115-119">В отладочных сборках библиотека DLL будет утверждать, если она выгружается, пока число объектов больше нуля.</span><span class="sxs-lookup"><span data-stu-id="99115-119">In debug builds, the DLL will assert if it is unloaded while the object count is greater than zero.</span></span> <span data-ttu-id="99115-120">Это упрощает мониторинг утечек, вызванных проблемами подсчета ссылок.</span><span class="sxs-lookup"><span data-stu-id="99115-120">This makes it easier to track down leaks caused by reference-counting problems.</span></span>

<span data-ttu-id="99115-121">Конструктор **кбасеобжект** принимает один аргумент — имя отладки для объекта.</span><span class="sxs-lookup"><span data-stu-id="99115-121">The **CBaseObject** constructor takes one argument, a debugging name for the object.</span></span> <span data-ttu-id="99115-122">Это имя хранится в глобальной таблице в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="99115-122">This name is stored in a global table in the DLL.</span></span> <span data-ttu-id="99115-123">Функция [**дбгдумпобжектрегистер**](dbgdumpobjectregister.md) форматирует список объектов, активных в библиотеке DLL, и отправляет их в выходные данные отладки.</span><span class="sxs-lookup"><span data-stu-id="99115-123">The [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function formats a list of the objects active in the DLL, and sends it to the debug output.</span></span>

## <a name="requirements"></a><span data-ttu-id="99115-124">Требования</span><span class="sxs-lookup"><span data-stu-id="99115-124">Requirements</span></span>



| <span data-ttu-id="99115-125">Требование</span><span class="sxs-lookup"><span data-stu-id="99115-125">Requirement</span></span> | <span data-ttu-id="99115-126">Значение</span><span class="sxs-lookup"><span data-stu-id="99115-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99115-127">Header</span><span class="sxs-lookup"><span data-stu-id="99115-127">Header</span></span><br/>  | <dl> <span data-ttu-id="99115-128"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99115-128"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="99115-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="99115-129">Library</span></span><br/> | <dl> <span data-ttu-id="99115-130"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="99115-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99115-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99115-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99115-132">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="99115-132">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




