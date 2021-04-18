---
description: Неактивный метод вызывается при переключении состояния на Stopped.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Метод Кбасерендерер. Inactive (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665387"
---
# <a name="cbaserendererinactive-method"></a><span data-ttu-id="8b7ea-103">Кбасерендерер. Inactive, метод</span><span class="sxs-lookup"><span data-stu-id="8b7ea-103">CBaseRenderer.Inactive method</span></span>

<span data-ttu-id="8b7ea-104">`Inactive`Метод вызывается при переключении состояния на Stopped.</span><span class="sxs-lookup"><span data-stu-id="8b7ea-104">The `Inactive` method is called when the state is switched to stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b7ea-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="8b7ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b7ea-106">Parameters</span></span>

<span data-ttu-id="8b7ea-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8b7ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b7ea-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b7ea-108">Return value</span></span>

<span data-ttu-id="8b7ea-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8b7ea-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b7ea-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b7ea-110">Remarks</span></span>

<span data-ttu-id="8b7ea-111">Входной ПИН-код вызывает этот метод из собственного метода [**крендереринпутпин:: Inactive**](crendererinputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="8b7ea-111">The input pin calls this method from its own [**CRendererInputPin::Inactive**](crendererinputpin-inactive.md) method.</span></span> <span data-ttu-id="8b7ea-112">Фильтр вызывает метод [**кбасерендерер:: клеарпендингсампле**](cbaserenderer-clearpendingsample.md) , чтобы освободить самый последний пример.</span><span class="sxs-lookup"><span data-stu-id="8b7ea-112">The filter calls the [**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) method to release the most recent sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b7ea-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8b7ea-113">Requirements</span></span>



| <span data-ttu-id="8b7ea-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8b7ea-114">Requirement</span></span> | <span data-ttu-id="8b7ea-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8b7ea-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7ea-116">Header</span><span class="sxs-lookup"><span data-stu-id="8b7ea-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8b7ea-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b7ea-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b7ea-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8b7ea-118">Library</span></span><br/> | <dl> <span data-ttu-id="8b7ea-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8b7ea-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b7ea-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b7ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b7ea-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="8b7ea-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




