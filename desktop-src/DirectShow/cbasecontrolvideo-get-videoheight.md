---
description: Метод Get \_ видеохеигхт извлекает высоту собственного видео.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Метод CBaseControlVideo.get_VideoHeight (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688764"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a><span data-ttu-id="7faa7-103">Кбасеконтролвидео. Get \_ видеохеигхт, метод</span><span class="sxs-lookup"><span data-stu-id="7faa7-103">CBaseControlVideo.get\_VideoHeight method</span></span>

<span data-ttu-id="7faa7-104">`get_VideoHeight`Метод получает высоту собственного видео.</span><span class="sxs-lookup"><span data-stu-id="7faa7-104">The `get_VideoHeight` method retrieves the height of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faa7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7faa7-105">Syntax</span></span>


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a><span data-ttu-id="7faa7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7faa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7faa7-107">*пвидеохеигхт*</span><span class="sxs-lookup"><span data-stu-id="7faa7-107">*pVideoHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="7faa7-108">Указатель на высоту собственного видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7faa7-108">Pointer to the height of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7faa7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7faa7-109">Return value</span></span>

<span data-ttu-id="7faa7-110">Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если объем доступной памяти недостаточен.</span><span class="sxs-lookup"><span data-stu-id="7faa7-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="7faa7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7faa7-111">Remarks</span></span>

<span data-ttu-id="7faa7-112">Эта функция члена реализует метод [**ибасиквидео:: Get \_ видеохеигхт**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) .</span><span class="sxs-lookup"><span data-stu-id="7faa7-112">This member function implements the [**IBasicVideo::get\_VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) method.</span></span> <span data-ttu-id="7faa7-113">Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.</span><span class="sxs-lookup"><span data-stu-id="7faa7-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="7faa7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7faa7-114">Requirements</span></span>



| <span data-ttu-id="7faa7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7faa7-115">Requirement</span></span> | <span data-ttu-id="7faa7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7faa7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7faa7-117">Header</span><span class="sxs-lookup"><span data-stu-id="7faa7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7faa7-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7faa7-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7faa7-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7faa7-119">Library</span></span><br/> | <dl> <span data-ttu-id="7faa7-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7faa7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7faa7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7faa7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7faa7-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="7faa7-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




