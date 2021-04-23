---
description: Метод Чеккреади запрашивает, завершена ли смена состояния.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Кбасерендерер. Чеккреади, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657482"
---
# <a name="cbaserenderercheckready-method"></a><span data-ttu-id="c831b-103">Кбасерендерер. Чеккреади, метод</span><span class="sxs-lookup"><span data-stu-id="c831b-103">CBaseRenderer.CheckReady method</span></span>

<span data-ttu-id="c831b-104">`CheckReady`Метод запрашивает, завершена ли смена состояния.</span><span class="sxs-lookup"><span data-stu-id="c831b-104">The `CheckReady` method queries whether a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="c831b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c831b-105">Syntax</span></span>


```C++
BOOL CheckReady();
```



## <a name="parameters"></a><span data-ttu-id="c831b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c831b-106">Parameters</span></span>

<span data-ttu-id="c831b-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c831b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c831b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c831b-108">Return value</span></span>

<span data-ttu-id="c831b-109">Возвращает **значение true** , если переход состояния завершен, или **false** , если фильтр все еще переходит в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="c831b-109">Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.</span></span>

## <a name="requirements"></a><span data-ttu-id="c831b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c831b-110">Requirements</span></span>



| <span data-ttu-id="c831b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c831b-111">Requirement</span></span> | <span data-ttu-id="c831b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c831b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c831b-113">Header</span><span class="sxs-lookup"><span data-stu-id="c831b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c831b-114"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c831b-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c831b-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c831b-115">Library</span></span><br/> | <dl> <span data-ttu-id="c831b-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c831b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c831b-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c831b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c831b-118">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="c831b-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="c831b-119">**Кбасерендерер:: NotReady**</span><span class="sxs-lookup"><span data-stu-id="c831b-119">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> <dt>

[<span data-ttu-id="c831b-120">**Кбасерендерер:: Ready**</span><span class="sxs-lookup"><span data-stu-id="c831b-120">**CBaseRenderer::Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




