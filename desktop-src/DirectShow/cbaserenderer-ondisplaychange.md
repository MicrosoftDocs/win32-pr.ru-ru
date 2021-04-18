---
description: Метод Ондисплайчанже отправляет событие EC о \_ \_ смене дисплея в Диспетчер графа фильтров.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Кбасерендерер. Ондисплайчанже, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658056"
---
# <a name="cbaserendererondisplaychange-method"></a><span data-ttu-id="74bb2-103">Кбасерендерер. Ондисплайчанже, метод</span><span class="sxs-lookup"><span data-stu-id="74bb2-103">CBaseRenderer.OnDisplayChange method</span></span>

<span data-ttu-id="74bb2-104">`OnDisplayChange`Метод отправляет событие [**EC о \_ \_ смене дисплея**](ec-display-changed.md) в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="74bb2-104">The `OnDisplayChange` method posts an [**EC\_DISPLAY\_CHANGED**](ec-display-changed.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="74bb2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74bb2-105">Syntax</span></span>


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a><span data-ttu-id="74bb2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="74bb2-106">Parameters</span></span>

<span data-ttu-id="74bb2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="74bb2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74bb2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74bb2-108">Return value</span></span>

<span data-ttu-id="74bb2-109">Возвращает **значение true** , если событие было опубликовано, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="74bb2-109">Returns **TRUE** if the event was posted, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="74bb2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74bb2-110">Remarks</span></span>

<span data-ttu-id="74bb2-111">Модули подготовки видео должны вызывать этот метод в ответ на \_ сообщения ДИСПЛАЙЧАНЖЕ WM.</span><span class="sxs-lookup"><span data-stu-id="74bb2-111">Video renderers should call this method in response to WM\_DISPLAYCHANGE messages.</span></span> <span data-ttu-id="74bb2-112">Если входной ПИН-код подключен, метод отправляет \_ \_ событие EC "изменение дисплея" в Диспетчер графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="74bb2-112">If the input pin is connected, the method sends an EC\_DISPLAY\_CHANGED event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="74bb2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="74bb2-113">Requirements</span></span>



| <span data-ttu-id="74bb2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="74bb2-114">Requirement</span></span> | <span data-ttu-id="74bb2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="74bb2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74bb2-116">Header</span><span class="sxs-lookup"><span data-stu-id="74bb2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="74bb2-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74bb2-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="74bb2-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="74bb2-118">Library</span></span><br/> | <dl> <span data-ttu-id="74bb2-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="74bb2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74bb2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74bb2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bb2-121">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="74bb2-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




