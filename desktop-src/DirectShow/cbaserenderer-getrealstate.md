---
description: Метод Жетреалстате Извлекает состояние фильтра.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Кбасерендерер. Жетреалстате, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657058"
---
# <a name="cbaserenderergetrealstate-method"></a><span data-ttu-id="73ce4-103">Кбасерендерер. Жетреалстате, метод</span><span class="sxs-lookup"><span data-stu-id="73ce4-103">CBaseRenderer.GetRealState method</span></span>

<span data-ttu-id="73ce4-104">`GetRealState`Метод получает состояние фильтра.</span><span class="sxs-lookup"><span data-stu-id="73ce4-104">The `GetRealState` method retrieves the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ce4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73ce4-105">Syntax</span></span>


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a><span data-ttu-id="73ce4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73ce4-106">Parameters</span></span>

<span data-ttu-id="73ce4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="73ce4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73ce4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73ce4-108">Return value</span></span>

<span data-ttu-id="73ce4-109">Возвращает значение [**\_ состояния кбасефилтер:: m**](cbasefilter-m-state.md).</span><span class="sxs-lookup"><span data-stu-id="73ce4-109">Returns the value of [**CBaseFilter::m\_State**](cbasefilter-m-state.md).</span></span> <span data-ttu-id="73ce4-110">Значение является членом перечисляемого типа [**\_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="73ce4-110">The value is a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type.</span></span>

## <a name="remarks"></a><span data-ttu-id="73ce4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73ce4-111">Remarks</span></span>

<span data-ttu-id="73ce4-112">Этот метод предоставляет более простую альтернативу методу [**кбасерендерер::-State**](cbaserenderer-getstate.md) для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="73ce4-112">This method provides a simpler alternative to the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method, for internal use.</span></span>

## <a name="requirements"></a><span data-ttu-id="73ce4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="73ce4-113">Requirements</span></span>



| <span data-ttu-id="73ce4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="73ce4-114">Requirement</span></span> | <span data-ttu-id="73ce4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="73ce4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73ce4-116">Header</span><span class="sxs-lookup"><span data-stu-id="73ce4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="73ce4-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73ce4-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="73ce4-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73ce4-118">Library</span></span><br/> | <dl> <span data-ttu-id="73ce4-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="73ce4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ce4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73ce4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ce4-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="73ce4-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




