---
description: Активный метод вызывается при переключении состояния на приостановку или выполнение.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Метод Кбасерендерер. Active (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668753"
---
# <a name="cbaserendereractive-method"></a><span data-ttu-id="86ac9-103">Кбасерендерер. активный метод</span><span class="sxs-lookup"><span data-stu-id="86ac9-103">CBaseRenderer.Active method</span></span>

<span data-ttu-id="86ac9-104">`Active`Метод вызывается при переключении состояния на приостановку или выполнение.</span><span class="sxs-lookup"><span data-stu-id="86ac9-104">The `Active` method is called when the state is switched to paused or running.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ac9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86ac9-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="86ac9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86ac9-106">Parameters</span></span>

<span data-ttu-id="86ac9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="86ac9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86ac9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="86ac9-108">Return value</span></span>

<span data-ttu-id="86ac9-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="86ac9-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="86ac9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86ac9-110">Remarks</span></span>

<span data-ttu-id="86ac9-111">Входной ПИН-код вызывает этот метод из собственного метода [**крендереринпутпин:: Active**](crendererinputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="86ac9-111">The input pin calls this method from its own [**CRendererInputPin::Active**](crendererinputpin-active.md) method.</span></span> <span data-ttu-id="86ac9-112">Этот метод не выполняет никаких действий в базовом классе.</span><span class="sxs-lookup"><span data-stu-id="86ac9-112">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ac9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="86ac9-113">Requirements</span></span>



| <span data-ttu-id="86ac9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="86ac9-114">Requirement</span></span> | <span data-ttu-id="86ac9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="86ac9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86ac9-116">Header</span><span class="sxs-lookup"><span data-stu-id="86ac9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="86ac9-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86ac9-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="86ac9-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="86ac9-118">Library</span></span><br/> | <dl> <span data-ttu-id="86ac9-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="86ac9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ac9-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86ac9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ac9-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="86ac9-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




