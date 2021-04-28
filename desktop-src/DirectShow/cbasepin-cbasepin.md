---
description: Метод конструктора Кбасепин. Кбасепин.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Конструктор Кбасепин. Кбасепин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11dea6bd5bc3f766e5f93a04022dab5ba6e51a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099432"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="5ddd9-103">Кбасепин. Кбасепин, конструктор</span><span class="sxs-lookup"><span data-stu-id="5ddd9-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="5ddd9-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ddd9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ddd9-105">Syntax</span></span>


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a><span data-ttu-id="5ddd9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ddd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ddd9-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="5ddd9-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddd9-108">Строка, содержащая имя отладки для объекта.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-108">String containing the debug name for the object.</span></span> <span data-ttu-id="5ddd9-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="5ddd9-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ddd9-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="5ddd9-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddd9-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="5ddd9-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="5ddd9-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddd9-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="5ddd9-114">Может быть той же критической секцией, что и блокировка фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="5ddd9-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ddd9-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="5ddd9-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddd9-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="5ddd9-117">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="5ddd9-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="5ddd9-118">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="5ddd9-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="5ddd9-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddd9-120">Строка расширенных символов, содержащая имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="5ddd9-121">Дополнительные сведения см. в разделе [**кбасепин:: куерипининфо**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="5ddd9-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ddd9-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="5ddd9-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="5ddd9-123">Элемент перечисления [**\_ направления ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий направление ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ddd9-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="5ddd9-124">Remarks</span></span>

<span data-ttu-id="5ddd9-125">Критическая секция, заданная параметром *плокк* , сериализует состояние ПИН-кода, включая его состояние соединения, выбора распределителя, типа носителя и состояния операций записи на диск.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="5ddd9-126">Не используйте этот критический раздел для сериализации операций потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="5ddd9-127">Дополнительные сведения см. [в разделе поток данных в графе фильтра](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="5ddd9-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="5ddd9-128">Фильтр может создавать ПИН-коды в своем методе-конструкторе, поэтому на этом этапе указатель *пфилтер* может не ссылаться на допустимый объект.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="5ddd9-129">Сохранение указателя, но не разыменование его в конструкторе закрепления.</span><span class="sxs-lookup"><span data-stu-id="5ddd9-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ddd9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5ddd9-130">Requirements</span></span>



| <span data-ttu-id="5ddd9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5ddd9-131">Requirement</span></span> | <span data-ttu-id="5ddd9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5ddd9-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddd9-133">Header</span><span class="sxs-lookup"><span data-stu-id="5ddd9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5ddd9-134"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ddd9-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5ddd9-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ddd9-135">Library</span></span><br/> | <dl> <span data-ttu-id="5ddd9-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5ddd9-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ddd9-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5ddd9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddd9-138">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="5ddd9-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




