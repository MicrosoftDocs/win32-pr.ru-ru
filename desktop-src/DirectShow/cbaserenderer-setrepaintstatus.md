---
description: Метод Сетрепаинтстатус включает или отключает перерисовки событий.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Кбасерендерер. Сетрепаинтстатус, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669343"
---
# <a name="cbaserenderersetrepaintstatus-method"></a><span data-ttu-id="9b42d-103">Кбасерендерер. Сетрепаинтстатус, метод</span><span class="sxs-lookup"><span data-stu-id="9b42d-103">CBaseRenderer.SetRepaintStatus method</span></span>

<span data-ttu-id="9b42d-104">`SetRepaintStatus`Метод включает или отключает перерисовки событий.</span><span class="sxs-lookup"><span data-stu-id="9b42d-104">The `SetRepaintStatus` method enables or disables repaint events.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b42d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b42d-105">Syntax</span></span>


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a><span data-ttu-id="9b42d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b42d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b42d-107">*bRepaint*</span><span class="sxs-lookup"><span data-stu-id="9b42d-107">*bRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="9b42d-108">Логическое значение, указывающее, включены ли события перерисовки.</span><span class="sxs-lookup"><span data-stu-id="9b42d-108">Boolean value indicating whether repaint events are enabled.</span></span> <span data-ttu-id="9b42d-109">Если **значение — true**, фильтр отправит события [**\_ перерисовки EC**](ec-repaint.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="9b42d-109">If **TRUE**, the filter will sent [**EC\_REPAINT**](ec-repaint.md) events to the filter graph manager.</span></span> <span data-ttu-id="9b42d-110">В противном случае он не будет отсылать \_ события ПЕРЕрисовки EC.</span><span class="sxs-lookup"><span data-stu-id="9b42d-110">Otherwise, it will not send EC\_REPAINT events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b42d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b42d-111">Return value</span></span>

<span data-ttu-id="9b42d-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9b42d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b42d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b42d-113">Remarks</span></span>

<span data-ttu-id="9b42d-114">Этот метод гарантирует, что диспетчер графов фильтров не будет переполняться избыточными \_ событиями ПЕРЕрисовки EC.</span><span class="sxs-lookup"><span data-stu-id="9b42d-114">This method ensures that the filter graph manager is not flooded with redundant EC\_REPAINT events.</span></span> <span data-ttu-id="9b42d-115">После того как фильтр отправит событие [**\_ перерисовки EC**](ec-repaint.md) , он вызывает этот метод со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="9b42d-115">After the filter sends an [**EC\_REPAINT**](ec-repaint.md) event, it calls this method with the value **TRUE**.</span></span> <span data-ttu-id="9b42d-116">Фильтр не отправляет дополнительные \_ события ПЕРЕрисовки EC, пока он не получит больше данных.</span><span class="sxs-lookup"><span data-stu-id="9b42d-116">The filter does not send more EC\_REPAINT events until it receives more data.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b42d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9b42d-117">Requirements</span></span>



| <span data-ttu-id="9b42d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9b42d-118">Requirement</span></span> | <span data-ttu-id="9b42d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9b42d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b42d-120">Header</span><span class="sxs-lookup"><span data-stu-id="9b42d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9b42d-121"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b42d-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b42d-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b42d-122">Library</span></span><br/> | <dl> <span data-ttu-id="9b42d-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="9b42d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b42d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b42d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b42d-125">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="9b42d-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




