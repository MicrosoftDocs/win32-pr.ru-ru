---
description: Метод Жетвидеосизе извлекает ширину и высоту собственного видео.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Кбасеконтролвидео. Жетвидеосизе, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657893"
---
# <a name="cbasecontrolvideogetvideosize-method"></a><span data-ttu-id="22e5f-103">Кбасеконтролвидео. Жетвидеосизе, метод</span><span class="sxs-lookup"><span data-stu-id="22e5f-103">CBaseControlVideo.GetVideoSize method</span></span>

<span data-ttu-id="22e5f-104">`GetVideoSize`Метод извлекает ширину и высоту собственного видео.</span><span class="sxs-lookup"><span data-stu-id="22e5f-104">The `GetVideoSize` method retrieves the native video's width and height.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22e5f-105">Syntax</span></span>


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="22e5f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22e5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e5f-107">*пвидс*</span><span class="sxs-lookup"><span data-stu-id="22e5f-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="22e5f-108">Указатель на ширину видео.</span><span class="sxs-lookup"><span data-stu-id="22e5f-108">Pointer to the video width.</span></span>

</dd> <dt>

<span data-ttu-id="22e5f-109">*феигхт*</span><span class="sxs-lookup"><span data-stu-id="22e5f-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="22e5f-110">Указатель на высоту видео.</span><span class="sxs-lookup"><span data-stu-id="22e5f-110">Pointer to the video height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e5f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22e5f-111">Return value</span></span>

<span data-ttu-id="22e5f-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="22e5f-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e5f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="22e5f-113">Requirements</span></span>



| <span data-ttu-id="22e5f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="22e5f-114">Requirement</span></span> | <span data-ttu-id="22e5f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="22e5f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22e5f-116">Header</span><span class="sxs-lookup"><span data-stu-id="22e5f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="22e5f-117"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22e5f-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22e5f-118">Library</span></span><br/> | <dl> <span data-ttu-id="22e5f-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e5f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22e5f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e5f-121">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="22e5f-121">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




