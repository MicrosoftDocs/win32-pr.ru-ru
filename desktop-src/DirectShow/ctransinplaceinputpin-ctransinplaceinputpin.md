---
description: Метод конструктора.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Конструктор Ктрансинплацеинпутпин. Ктрансинплацеинпутпин (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a801b2c4286f903ef450cac2fd76252f451f9add
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675168"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="9ed5f-103">Ктрансинплацеинпутпин. Ктрансинплацеинпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="9ed5f-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="9ed5f-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="9ed5f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ed5f-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="9ed5f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ed5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed5f-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="9ed5f-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed5f-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="9ed5f-108">String containing the debug name of the object.</span></span> <span data-ttu-id="9ed5f-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="9ed5f-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ed5f-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="9ed5f-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed5f-111">Указатель на фильтр, создавший этот ПИН-код, который должен быть объектом [**ктрансинплацефилтер**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="9ed5f-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9ed5f-112">*фр*</span><span class="sxs-lookup"><span data-stu-id="9ed5f-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed5f-113">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="9ed5f-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="9ed5f-114">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="9ed5f-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="9ed5f-115">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="9ed5f-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="9ed5f-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="9ed5f-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed5f-117">Строка расширенных символов, содержащая имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="9ed5f-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ed5f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ed5f-118">Remarks</span></span>

<span data-ttu-id="9ed5f-119">Параметр *pName* указывает имя ПИН-кода, которое возвращается методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="9ed5f-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="9ed5f-120">Однако эта строка не используется для идентификатора ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="9ed5f-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="9ed5f-121">Идентификатор ПИН-кода для этого класса всегда находится в.</span><span class="sxs-lookup"><span data-stu-id="9ed5f-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="9ed5f-122">Дополнительные сведения см. в разделе [**ктрансформинпутпин:: QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="9ed5f-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed5f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9ed5f-123">Requirements</span></span>



| <span data-ttu-id="9ed5f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9ed5f-124">Requirement</span></span> | <span data-ttu-id="9ed5f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9ed5f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed5f-126">Header</span><span class="sxs-lookup"><span data-stu-id="9ed5f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9ed5f-127"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed5f-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9ed5f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9ed5f-128">Library</span></span><br/> | <dl> <span data-ttu-id="9ed5f-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed5f-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed5f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ed5f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed5f-131">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="9ed5f-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




