---
description: Метод конструктора Ктрансинплацеинпутпин. Ктрансинплацеинпутпин.
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
ms.openlocfilehash: 6f97c89142e43691c91b2a4c0d04721d9112ed49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084762"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a><span data-ttu-id="81563-103">Ктрансинплацеинпутпин. Ктрансинплацеинпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="81563-103">CTransInPlaceInputPin.CTransInPlaceInputPin constructor</span></span>

<span data-ttu-id="81563-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="81563-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81563-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81563-105">Syntax</span></span>


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a><span data-ttu-id="81563-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81563-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81563-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="81563-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="81563-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="81563-108">String containing the debug name of the object.</span></span> <span data-ttu-id="81563-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="81563-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="81563-110">*пфилтер*</span><span class="sxs-lookup"><span data-stu-id="81563-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="81563-111">Указатель на фильтр, создавший этот ПИН-код, который должен быть объектом [**ктрансинплацефилтер**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="81563-111">Pointer to the filter that created this pin, which must be a [**CTransInPlaceFilter**](ctransinplacefilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="81563-112">*фр*</span><span class="sxs-lookup"><span data-stu-id="81563-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="81563-113">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="81563-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="81563-114">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="81563-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="81563-115">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="81563-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="81563-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="81563-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="81563-117">Строка расширенных символов, содержащая имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="81563-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81563-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="81563-118">Remarks</span></span>

<span data-ttu-id="81563-119">Параметр *pName* указывает имя ПИН-кода, которое возвращается методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="81563-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="81563-120">Однако эта строка не используется для идентификатора ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="81563-120">However, this string is not used for the pin identifier.</span></span> <span data-ttu-id="81563-121">Идентификатор ПИН-кода для этого класса всегда находится в.</span><span class="sxs-lookup"><span data-stu-id="81563-121">The pin identifier for this class is always In.</span></span> <span data-ttu-id="81563-122">Дополнительные сведения см. в разделе [**ктрансформинпутпин:: QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="81563-122">For more information, see [**CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81563-123">Требования</span><span class="sxs-lookup"><span data-stu-id="81563-123">Requirements</span></span>



| <span data-ttu-id="81563-124">Требование</span><span class="sxs-lookup"><span data-stu-id="81563-124">Requirement</span></span> | <span data-ttu-id="81563-125">Значение</span><span class="sxs-lookup"><span data-stu-id="81563-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81563-126">Header</span><span class="sxs-lookup"><span data-stu-id="81563-126">Header</span></span><br/>  | <dl> <span data-ttu-id="81563-127"><dt>Трансип. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81563-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81563-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81563-128">Library</span></span><br/> | <dl> <span data-ttu-id="81563-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="81563-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81563-130">См. также</span><span class="sxs-lookup"><span data-stu-id="81563-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81563-131">**Класс Ктрансинплацеинпутпин**</span><span class="sxs-lookup"><span data-stu-id="81563-131">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




