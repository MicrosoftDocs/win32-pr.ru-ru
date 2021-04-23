---
description: Метод конструктора.
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Конструктор Ктрансформаутпутпин. Ктрансформаутпутпин (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 730149ae67abb2924174954bb8b620a02cfae2b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676061"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a><span data-ttu-id="42225-103">Ктрансформаутпутпин. Ктрансформаутпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="42225-103">CTransformOutputPin.CTransformOutputPin constructor</span></span>

<span data-ttu-id="42225-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="42225-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42225-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42225-105">Syntax</span></span>


```C++
CTransformOutputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="42225-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42225-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="42225-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="42225-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="42225-108">String containing the debug name of the object.</span></span> <span data-ttu-id="42225-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="42225-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="42225-110">*птрансформфилтер*</span><span class="sxs-lookup"><span data-stu-id="42225-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="42225-111">Указатель на фильтр, создавший этот ПИН-код, который должен быть объектом [**ктрансформфилтер**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="42225-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="42225-112">*фр*</span><span class="sxs-lookup"><span data-stu-id="42225-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="42225-113">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="42225-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="42225-114">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="42225-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="42225-115">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="42225-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="42225-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="42225-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="42225-117">Строка расширенных символов, содержащая имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="42225-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42225-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42225-118">Remarks</span></span>

<span data-ttu-id="42225-119">Параметр *pName* указывает имя ПИН-кода, которое возвращается методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="42225-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="42225-120">Однако строка не используется для идентификатора ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="42225-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="42225-121">Идентификатор ПИН-кода для этого класса всегда имеет значение "out".</span><span class="sxs-lookup"><span data-stu-id="42225-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="42225-122">Дополнительные сведения см. в разделе [**QueryId**](ctransformoutputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="42225-122">For more information, see [**QueryId**](ctransformoutputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42225-123">Требования</span><span class="sxs-lookup"><span data-stu-id="42225-123">Requirements</span></span>



| <span data-ttu-id="42225-124">Требование</span><span class="sxs-lookup"><span data-stu-id="42225-124">Requirement</span></span> | <span data-ttu-id="42225-125">Значение</span><span class="sxs-lookup"><span data-stu-id="42225-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42225-126">Header</span><span class="sxs-lookup"><span data-stu-id="42225-126">Header</span></span><br/>  | <dl> <span data-ttu-id="42225-127"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42225-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="42225-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42225-128">Library</span></span><br/> | <dl> <span data-ttu-id="42225-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="42225-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




