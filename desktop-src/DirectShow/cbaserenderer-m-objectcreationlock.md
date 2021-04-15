---
description: Блокировка для защиты создания объектов внутри фильтра.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Элемент Кбасерендерер:: m_ObjectCreationLock (Ренбасе. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669193"
---
# <a name="cbaserendererm_objectcreationlock-member"></a><span data-ttu-id="4589d-103">Элемент Кбасерендерер:: m \_ обжекткреатионлокк</span><span class="sxs-lookup"><span data-stu-id="4589d-103">CBaseRenderer::m\_ObjectCreationLock member</span></span>

<span data-ttu-id="4589d-104">Блокировка для защиты создания объектов внутри фильтра.</span><span class="sxs-lookup"><span data-stu-id="4589d-104">Lock to protect the creation of objects inside the filter.</span></span> <span data-ttu-id="4589d-105">Фильтр удерживает эту блокировку при создании входного ПИН-кода ([**кбасерендерер:: m \_ пинпутпин**](cbaserenderer-m-pinputpin.md)) или объекта [**крендерерпоспасссру**](crendererpospassthru.md) ([**кбасерендерер:: m \_ ппоситион**](cbaserenderer-m-pposition.md)).</span><span class="sxs-lookup"><span data-stu-id="4589d-105">The filter holds this lock when it creates the input pin ([**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md)) or the [**CRendererPosPassThru**](crendererpospassthru.md) object ([**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md)).</span></span> <span data-ttu-id="4589d-106">Эта блокировка предотвращает одновременную попытку создания одного из этих объектов несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="4589d-106">This lock prevents multiple threads from attempting to create one of these objects at the same time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4589d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4589d-107">Syntax</span></span>


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a><span data-ttu-id="4589d-108">Требования</span><span class="sxs-lookup"><span data-stu-id="4589d-108">Requirements</span></span>



| <span data-ttu-id="4589d-109">Требование</span><span class="sxs-lookup"><span data-stu-id="4589d-109">Requirement</span></span> | <span data-ttu-id="4589d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4589d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4589d-111">Header</span><span class="sxs-lookup"><span data-stu-id="4589d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="4589d-112"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4589d-112"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4589d-113">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4589d-113">Library</span></span><br/> | <dl> <span data-ttu-id="4589d-114"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="4589d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4589d-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4589d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4589d-116">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="4589d-116">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




