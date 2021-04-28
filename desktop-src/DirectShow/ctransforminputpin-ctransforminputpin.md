---
description: Метод конструктора Ктрансформинпутпин. Ктрансформинпутпин.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Конструктор Ктрансформинпутпин. Ктрансформинпутпин (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e893b4e1c7d4f396644a468d3d71fa3046fb712
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095052"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a><span data-ttu-id="990be-103">Ктрансформинпутпин. Ктрансформинпутпин, конструктор</span><span class="sxs-lookup"><span data-stu-id="990be-103">CTransformInputPin.CTransformInputPin constructor</span></span>

<span data-ttu-id="990be-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="990be-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="990be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="990be-105">Syntax</span></span>


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="990be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="990be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="990be-107">*побжектнаме*</span><span class="sxs-lookup"><span data-stu-id="990be-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="990be-108">Строка, содержащая имя отладки объекта.</span><span class="sxs-lookup"><span data-stu-id="990be-108">String containing the debug name of the object.</span></span> <span data-ttu-id="990be-109">Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="990be-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="990be-110">*птрансформфилтер*</span><span class="sxs-lookup"><span data-stu-id="990be-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="990be-111">Указатель на фильтр, создавший этот ПИН-код, который должен быть объектом [**ктрансформфилтер**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="990be-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="990be-112">*фр*</span><span class="sxs-lookup"><span data-stu-id="990be-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="990be-113">Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода.</span><span class="sxs-lookup"><span data-stu-id="990be-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="990be-114">Перед созданием объекта инициализируйте значение до " \_ ОК".</span><span class="sxs-lookup"><span data-stu-id="990be-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="990be-115">Значение изменяется только в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="990be-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="990be-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="990be-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="990be-117">Строка расширенных символов, содержащая имя ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="990be-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="990be-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="990be-118">Remarks</span></span>

<span data-ttu-id="990be-119">Параметр *pName* указывает имя ПИН-кода, которое возвращается методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="990be-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="990be-120">Однако строка не используется для идентификатора ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="990be-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="990be-121">Идентификатор ПИН-кода для этого класса всегда имеет значение "in".</span><span class="sxs-lookup"><span data-stu-id="990be-121">The pin identifier for this class is always "In".</span></span> <span data-ttu-id="990be-122">Дополнительные сведения см. в разделе [**QueryId**](ctransforminputpin-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="990be-122">For more information, see [**QueryId**](ctransforminputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="990be-123">Требования</span><span class="sxs-lookup"><span data-stu-id="990be-123">Requirements</span></span>



| <span data-ttu-id="990be-124">Требование</span><span class="sxs-lookup"><span data-stu-id="990be-124">Requirement</span></span> | <span data-ttu-id="990be-125">Значение</span><span class="sxs-lookup"><span data-stu-id="990be-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="990be-126">Header</span><span class="sxs-lookup"><span data-stu-id="990be-126">Header</span></span><br/>  | <dl> <span data-ttu-id="990be-127"><dt>Трансфрм. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="990be-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="990be-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="990be-128">Library</span></span><br/> | <dl> <span data-ttu-id="990be-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="990be-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




