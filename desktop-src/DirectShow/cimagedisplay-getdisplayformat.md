---
description: Метод Жетдисплайформат извлекает видеоформат, описывающий текущий режим экрана.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Цимажедисплай. Жетдисплайформат, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669066"
---
# <a name="cimagedisplaygetdisplayformat-method"></a><span data-ttu-id="5ae8e-103">Цимажедисплай. Жетдисплайформат, метод</span><span class="sxs-lookup"><span data-stu-id="5ae8e-103">CImageDisplay.GetDisplayFormat method</span></span>

<span data-ttu-id="5ae8e-104">`GetDisplayFormat`Метод извлекает видеоформат, описывающий текущий режим экрана.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-104">The `GetDisplayFormat` method retrieves a video format that describes the current display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae8e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ae8e-105">Syntax</span></span>


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a><span data-ttu-id="5ae8e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ae8e-106">Parameters</span></span>

<span data-ttu-id="5ae8e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5ae8e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ae8e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ae8e-108">Return value</span></span>

<span data-ttu-id="5ae8e-109">Возвращает указатель на структуру [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="5ae8e-109">Returns a pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae8e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="5ae8e-110">Requirements</span></span>



| <span data-ttu-id="5ae8e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="5ae8e-111">Requirement</span></span> | <span data-ttu-id="5ae8e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5ae8e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae8e-113">Header</span><span class="sxs-lookup"><span data-stu-id="5ae8e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5ae8e-114"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ae8e-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ae8e-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ae8e-115">Library</span></span><br/> | <dl> <span data-ttu-id="5ae8e-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5ae8e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae8e-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ae8e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae8e-118">**Класс Цимажедисплай**</span><span class="sxs-lookup"><span data-stu-id="5ae8e-118">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




