---
description: Метод Get \_ фрамесдравн извлекает \_ переменную члена m кфрамесдравн, выдавая число кадров, рисуемых после начала потоковой передачи.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: Метод CBaseVideoRenderer.get_FramesDrawn (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675213"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a><span data-ttu-id="0ac4b-103">Кбасевидеорендерер. Get \_ фрамесдравн, метод</span><span class="sxs-lookup"><span data-stu-id="0ac4b-103">CBaseVideoRenderer.get\_FramesDrawn method</span></span>

<span data-ttu-id="0ac4b-104">`get_FramesDrawn`Метод получает переменную члена **m \_ кфрамесдравн** , выдавая число кадров, созданных с момента начала потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-104">The `get_FramesDrawn` method retrieves the **m\_cFramesDrawn** member variable, giving the number of frames drawn since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ac4b-105">Syntax</span></span>


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a><span data-ttu-id="0ac4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ac4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac4b-107">*пкфрамесдравн*</span><span class="sxs-lookup"><span data-stu-id="0ac4b-107">*pcFramesDrawn*</span></span> 
</dt> <dd>

<span data-ttu-id="0ac4b-108">Указатель на число рисуемых кадров.</span><span class="sxs-lookup"><span data-stu-id="0ac4b-108">Pointer to the number of frames drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac4b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ac4b-109">Return value</span></span>

<span data-ttu-id="0ac4b-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ac4b-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ac4b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ac4b-111">Remarks</span></span>

<span data-ttu-id="0ac4b-112">Эта функция члена реализует метод [**икуалпроп:: Get \_ фрамесдравн**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .</span><span class="sxs-lookup"><span data-stu-id="0ac4b-112">This member function implements the [**IQualProp::get\_FramesDrawn**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac4b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0ac4b-113">Requirements</span></span>



| <span data-ttu-id="0ac4b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="0ac4b-114">Requirement</span></span> | <span data-ttu-id="0ac4b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0ac4b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac4b-116">Header</span><span class="sxs-lookup"><span data-stu-id="0ac4b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0ac4b-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4b-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ac4b-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ac4b-118">Library</span></span><br/> | <dl> <span data-ttu-id="0ac4b-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="0ac4b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac4b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ac4b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac4b-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="0ac4b-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




