---
description: Кбасерендерер. Жетпин, метод Жетпин извлекает ПИН-код.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Кбасерендерер. Жетпин, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119892"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="9d183-103">Кбасерендерер. Жетпин, метод</span><span class="sxs-lookup"><span data-stu-id="9d183-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="9d183-104">`GetPin`Метод извлекает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="9d183-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d183-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d183-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="9d183-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d183-107">*n*</span><span class="sxs-lookup"><span data-stu-id="9d183-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="9d183-108">Номер указанного пин-кода.</span><span class="sxs-lookup"><span data-stu-id="9d183-108">Number of the specified pin.</span></span> <span data-ttu-id="9d183-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9d183-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d183-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d183-110">Return value</span></span>

<span data-ttu-id="9d183-111">Возвращает указатель [**кбасерендерер:: m \_ пинпутпин**](cbaserenderer-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="9d183-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d183-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="9d183-112">Remarks</span></span>

<span data-ttu-id="9d183-113">Этот метод реализует метод [**кбасефилтер:: жетпин**](cbasefilter-getpin.md) , который является чистым виртуальным в классе **кбасефилтер** .</span><span class="sxs-lookup"><span data-stu-id="9d183-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="9d183-114">Фильтр поддерживает ровно один ПИН-код (входной ПИН-код).</span><span class="sxs-lookup"><span data-stu-id="9d183-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="9d183-115">При первом вызове этого метода он создает ПИН-код в качестве нового объекта [**крендереринпутпин**](crendererinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="9d183-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d183-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9d183-116">Requirements</span></span>



| <span data-ttu-id="9d183-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9d183-117">Requirement</span></span> | <span data-ttu-id="9d183-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9d183-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d183-119">Header</span><span class="sxs-lookup"><span data-stu-id="9d183-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9d183-120"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d183-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d183-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9d183-121">Library</span></span><br/> | <dl> <span data-ttu-id="9d183-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9d183-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d183-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9d183-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d183-124">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="9d183-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




