---
description: Метод Жетвидеоформат извлекает образец видео, представляющий текущий формат видео.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Кбасеконтролвидео. Жетвидеоформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657895"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a><span data-ttu-id="e499e-103">Кбасеконтролвидео. Жетвидеоформат, метод</span><span class="sxs-lookup"><span data-stu-id="e499e-103">CBaseControlVideo.GetVideoFormat method</span></span>

<span data-ttu-id="e499e-104">`GetVideoFormat`Метод получает образец видео, представляющий текущий формат видео.</span><span class="sxs-lookup"><span data-stu-id="e499e-104">The `GetVideoFormat` method retrieves a video sample that represents the current video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="e499e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e499e-105">Syntax</span></span>


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a><span data-ttu-id="e499e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e499e-106">Parameters</span></span>

<span data-ttu-id="e499e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e499e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e499e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e499e-108">Return value</span></span>

<span data-ttu-id="e499e-109">Возвращает указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , содержащую текущий формат видео.</span><span class="sxs-lookup"><span data-stu-id="e499e-109">Returns a pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the current video format.</span></span>

## <a name="remarks"></a><span data-ttu-id="e499e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e499e-110">Remarks</span></span>

<span data-ttu-id="e499e-111">Чтобы вернуть и проверить определенную информацию с помощью [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo), объект должен узнать текущий формат видео.</span><span class="sxs-lookup"><span data-stu-id="e499e-111">To return and check certain information through [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), the object must know the current video format.</span></span> <span data-ttu-id="e499e-112">Он получает эти сведения путем вызова чистого виртуального метода, который производные классы должны переопределить.</span><span class="sxs-lookup"><span data-stu-id="e499e-112">It gets this information by calling this pure virtual method that derived classes must override.</span></span> <span data-ttu-id="e499e-113">Эта функция-член вызывается следующими функциями-членами [**кбасеконтролвидео**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="e499e-113">This member function is called by the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="e499e-114">**Кбасеконтролвидео:: Онвидеосизечанже**</span><span class="sxs-lookup"><span data-stu-id="e499e-114">**CBaseControlVideo::OnVideoSizeChange**</span></span>](cbasecontrolvideo-onvideosizechange.md)
-   [<span data-ttu-id="e499e-115">**Кбасеконтролвидео:: Get \_ авгтимеперфраме**</span><span class="sxs-lookup"><span data-stu-id="e499e-115">**CBaseControlVideo::get\_AvgTimePerFrame**</span></span>](cbasecontrolvideo-get-avgtimeperframe.md)
-   [<span data-ttu-id="e499e-116">**Кбасеконтролвидео:: получить \_ скорость**</span><span class="sxs-lookup"><span data-stu-id="e499e-116">**CBaseControlVideo::get\_BitRate**</span></span>](cbasecontrolvideo-get-bitrate.md)
-   [<span data-ttu-id="e499e-117">**Кбасеконтролвидео:: Get \_ битерроррате**</span><span class="sxs-lookup"><span data-stu-id="e499e-117">**CBaseControlVideo::get\_BitErrorRate**</span></span>](cbasecontrolvideo-get-biterrorrate.md)
-   [<span data-ttu-id="e499e-118">**Кбасеконтролвидео:: Get \_ видеовидс**</span><span class="sxs-lookup"><span data-stu-id="e499e-118">**CBaseControlVideo::get\_VideoWidth**</span></span>](cbasecontrolvideo-get-videowidth.md)
-   [<span data-ttu-id="e499e-119">**Кбасеконтролвидео:: Get \_ видеохеигхт**</span><span class="sxs-lookup"><span data-stu-id="e499e-119">**CBaseControlVideo::get\_VideoHeight**</span></span>](cbasecontrolvideo-get-videoheight.md)
-   [<span data-ttu-id="e499e-120">**Кбасеконтролвидео:: Жетвидеопалеттинтриес**</span><span class="sxs-lookup"><span data-stu-id="e499e-120">**CBaseControlVideo::GetVideoPaletteEntries**</span></span>](cbasecontrolvideo-getvideopaletteentries.md)
-   [<span data-ttu-id="e499e-121">**Кбасеконтролвидео:: Жетвидеосизе**</span><span class="sxs-lookup"><span data-stu-id="e499e-121">**CBaseControlVideo::GetVideoSize**</span></span>](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a><span data-ttu-id="e499e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e499e-122">Requirements</span></span>



| <span data-ttu-id="e499e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e499e-123">Requirement</span></span> | <span data-ttu-id="e499e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e499e-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e499e-125">Header</span><span class="sxs-lookup"><span data-stu-id="e499e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e499e-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e499e-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e499e-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e499e-127">Library</span></span><br/> | <dl> <span data-ttu-id="e499e-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e499e-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e499e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e499e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e499e-130">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="e499e-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




