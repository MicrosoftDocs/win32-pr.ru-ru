---
description: Метод конструктора.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Конструктор Ксаурцестреам. Ксаурцестреам (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657167"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="657d8-103">Ксаурцестреам. Ксаурцестреам, конструктор</span><span class="sxs-lookup"><span data-stu-id="657d8-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="657d8-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="657d8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="657d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="657d8-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="657d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="657d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657d8-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="657d8-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="657d8-108">Указатель на строку, содержащую имя отладки ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="657d8-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="657d8-109">*фр*</span><span class="sxs-lookup"><span data-stu-id="657d8-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="657d8-110">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="657d8-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="657d8-111">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="657d8-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="657d8-112">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="657d8-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="657d8-113">*утверждены руководителем*</span><span class="sxs-lookup"><span data-stu-id="657d8-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="657d8-114">Указатель на фильтр [**ксаурце**](csource.md) , который создал этот ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="657d8-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="657d8-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="657d8-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="657d8-116">Указатель на строку, содержащую имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="657d8-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="657d8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="657d8-117">Remarks</span></span>

<span data-ttu-id="657d8-118">Строка, заданная в параметре *побжектнаме* , используется только в целях отладки.</span><span class="sxs-lookup"><span data-stu-id="657d8-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="657d8-119">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="657d8-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="657d8-120">Строка, заданная в параметре *pName* , является именем, возвращаемым методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="657d8-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="657d8-121">`CSourceStream`Класс не использует это имя для идентификатора ПИН-кода, возвращаемого методом [**ксаурцестреам:: QueryId**](csourcestream-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="657d8-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="657d8-122">Вместо этого **QueryId** вычисляет идентификатор ПИН-кода на основе PIN-кода.</span><span class="sxs-lookup"><span data-stu-id="657d8-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="657d8-123">(Идентификаторы ПИН-кода поддерживают сохраняемость графа.</span><span class="sxs-lookup"><span data-stu-id="657d8-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="657d8-124">Дополнительные сведения см. в разделе [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="657d8-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="657d8-125">Конструктор автоматически добавляет ПИН-код в фильтр владельца путем вызова [**ксаурце:: аддпин**](csource-addpin.md).</span><span class="sxs-lookup"><span data-stu-id="657d8-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="657d8-126">Требования</span><span class="sxs-lookup"><span data-stu-id="657d8-126">Requirements</span></span>



| <span data-ttu-id="657d8-127">Требование</span><span class="sxs-lookup"><span data-stu-id="657d8-127">Requirement</span></span> | <span data-ttu-id="657d8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="657d8-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="657d8-129">Header</span><span class="sxs-lookup"><span data-stu-id="657d8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="657d8-130"><dt>Source. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="657d8-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="657d8-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="657d8-131">Library</span></span><br/> | <dl> <span data-ttu-id="657d8-132"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="657d8-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="657d8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="657d8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657d8-134">**Класс Ксаурцестреам**</span><span class="sxs-lookup"><span data-stu-id="657d8-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




