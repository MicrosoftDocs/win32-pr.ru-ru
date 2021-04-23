---
description: Метод Сетсинк задает объект Икуалитиконтрол, который будет принимать сообщения о контроле качества.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Кбасевидеорендерер. Сетсинк, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675000"
---
# <a name="cbasevideorenderersetsink-method"></a><span data-ttu-id="324f2-103">Кбасевидеорендерер. Сетсинк, метод</span><span class="sxs-lookup"><span data-stu-id="324f2-103">CBaseVideoRenderer.SetSink method</span></span>

<span data-ttu-id="324f2-104">`SetSink`Метод задает объект [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) , который будет принимать сообщения качества.</span><span class="sxs-lookup"><span data-stu-id="324f2-104">The `SetSink` method sets the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object that will receive quality messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="324f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="324f2-105">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="324f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="324f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="324f2-107">*пикк*</span><span class="sxs-lookup"><span data-stu-id="324f2-107">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="324f2-108">Указатель на объект [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) , в который должны отправляться уведомления.</span><span class="sxs-lookup"><span data-stu-id="324f2-108">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object to which the notifications should be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="324f2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="324f2-109">Return value</span></span>

<span data-ttu-id="324f2-110">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="324f2-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="324f2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="324f2-111">Remarks</span></span>

<span data-ttu-id="324f2-112">Эта функция члена реализует метод [**икуалитиконтрол:: сетсинк**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) для модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="324f2-112">This member function implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method on the video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="324f2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="324f2-113">Requirements</span></span>



| <span data-ttu-id="324f2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="324f2-114">Requirement</span></span> | <span data-ttu-id="324f2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="324f2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="324f2-116">Header</span><span class="sxs-lookup"><span data-stu-id="324f2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="324f2-117"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="324f2-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="324f2-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="324f2-118">Library</span></span><br/> | <dl> <span data-ttu-id="324f2-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="324f2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="324f2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="324f2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324f2-121">**Класс Кбасевидеорендерер**</span><span class="sxs-lookup"><span data-stu-id="324f2-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




