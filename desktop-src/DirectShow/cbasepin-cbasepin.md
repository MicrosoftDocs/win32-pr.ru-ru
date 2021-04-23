---
description: Метод конструктора.
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
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669306"
---
# <a name="cbasepincbasepin-constructor"></a><span data-ttu-id="0ed2b-103">Кбасепин. Кбасепин, конструктор</span><span class="sxs-lookup"><span data-stu-id="0ed2b-103">CBasePin.CBasePin constructor</span></span>

<span data-ttu-id="0ed2b-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ed2b-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0ed2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ed2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed2b-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="0ed2b-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed2b-108">Строка, содержащая имя отладки для объекта.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-108">String containing the debug name for the object.</span></span> <span data-ttu-id="0ed2b-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0ed2b-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ed2b-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="0ed2b-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed2b-111">Указатель на фильтр, создавший этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="0ed2b-112">*плокк*</span><span class="sxs-lookup"><span data-stu-id="0ed2b-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed2b-113">Указатель на [**ккритсек**](ccritsec.md) блокировку, используемый для сериализации изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="0ed2b-114">Может быть той же критической секцией, что и блокировка фильтра, [**кбасефилтер:: m \_ плокк**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="0ed2b-114">Can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ed2b-115">*фр*</span><span class="sxs-lookup"><span data-stu-id="0ed2b-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed2b-116">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="0ed2b-117">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="0ed2b-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="0ed2b-118">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="0ed2b-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="0ed2b-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed2b-120">Строка расширенных символов, содержащая имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-120">Wide-character string containing the name of the pin.</span></span> <span data-ttu-id="0ed2b-121">Дополнительные сведения см. в разделе [**кбасепин:: куерипининфо**](cbasepin-querypininfo.md).</span><span class="sxs-lookup"><span data-stu-id="0ed2b-121">For more information, see [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ed2b-122">*dir*</span><span class="sxs-lookup"><span data-stu-id="0ed2b-122">*dir*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed2b-123">Элемент перечисления [**\_ направления ПИН-кода**](/windows/win32/api/strmif/ne-strmif-pin_direction) , указывающий направление ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-123">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumeration specifying the direction of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ed2b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ed2b-124">Remarks</span></span>

<span data-ttu-id="0ed2b-125">Критическая секция, заданная параметром *плокк* , сериализует состояние ПИН-кода, включая его состояние соединения, выбора распределителя, типа носителя и состояния операций записи на диск.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-125">The critical section specified by *pLock* serializes the pin's state, including its connection status, choice of allocator, media type, and the status of flush operations.</span></span> <span data-ttu-id="0ed2b-126">Не используйте этот критический раздел для сериализации операций потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-126">Do not use this critical section to serialize streaming operations.</span></span> <span data-ttu-id="0ed2b-127">Дополнительные сведения см. [в разделе поток данных в графе фильтра](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="0ed2b-127">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="0ed2b-128">Фильтр может создавать ПИН-коды в своем методе-конструкторе, поэтому на этом этапе указатель *пфилтер* может не ссылаться на допустимый объект.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-128">A filter might create pins in its constructor method, so at this point the *pFilter* pointer might not refer to a valid object.</span></span> <span data-ttu-id="0ed2b-129">Сохранение указателя, но не разыменование его в конструкторе закрепления.</span><span class="sxs-lookup"><span data-stu-id="0ed2b-129">Store the pointer, but do not dereference it while inside the pin's constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed2b-130">Требования</span><span class="sxs-lookup"><span data-stu-id="0ed2b-130">Requirements</span></span>



| <span data-ttu-id="0ed2b-131">Требование</span><span class="sxs-lookup"><span data-stu-id="0ed2b-131">Requirement</span></span> | <span data-ttu-id="0ed2b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="0ed2b-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed2b-133">Header</span><span class="sxs-lookup"><span data-stu-id="0ed2b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0ed2b-134"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ed2b-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ed2b-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ed2b-135">Library</span></span><br/> | <dl> <span data-ttu-id="0ed2b-136"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0ed2b-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed2b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ed2b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed2b-138">**Класс Кбасепин**</span><span class="sxs-lookup"><span data-stu-id="0ed2b-138">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




