---
description: Метод Ресетендофстреам сбрасывает флаги конца потока.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Кбасерендерер. Ресетендофстреам, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669400"
---
# <a name="cbaserendererresetendofstream-method"></a><span data-ttu-id="b6289-103">Кбасерендерер. Ресетендофстреам, метод</span><span class="sxs-lookup"><span data-stu-id="b6289-103">CBaseRenderer.ResetEndOfStream method</span></span>

<span data-ttu-id="b6289-104">`ResetEndOfStream`Метод сбрасывает флаги конца потока.</span><span class="sxs-lookup"><span data-stu-id="b6289-104">The `ResetEndOfStream` method resets the end-of-stream flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6289-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6289-105">Syntax</span></span>


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="b6289-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6289-106">Parameters</span></span>

<span data-ttu-id="b6289-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b6289-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6289-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6289-108">Return value</span></span>

<span data-ttu-id="b6289-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b6289-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6289-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6289-110">Remarks</span></span>

<span data-ttu-id="b6289-111">Этот метод очищает предыдущее условие конца потока.</span><span class="sxs-lookup"><span data-stu-id="b6289-111">This method clears the previous end-of-stream condition.</span></span> <span data-ttu-id="b6289-112">На этом этапе фильтр может принимать новые данные.</span><span class="sxs-lookup"><span data-stu-id="b6289-112">At that point, the filter can receive new data.</span></span> <span data-ttu-id="b6289-113">Методы [**кбасерендерер:: останавливают**](cbaserenderer-stop.md) и [**Кбасерендерер:: бегинфлуш**](cbaserenderer-beginflush.md) вызывают этот метод.</span><span class="sxs-lookup"><span data-stu-id="b6289-113">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6289-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b6289-114">Requirements</span></span>



| <span data-ttu-id="b6289-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b6289-115">Requirement</span></span> | <span data-ttu-id="b6289-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b6289-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6289-117">Header</span><span class="sxs-lookup"><span data-stu-id="b6289-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b6289-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6289-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6289-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b6289-119">Library</span></span><br/> | <dl> <span data-ttu-id="b6289-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="b6289-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6289-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6289-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6289-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="b6289-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




