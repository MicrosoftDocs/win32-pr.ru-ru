---
description: Метод Get \_ видеовидс извлекает ширину собственного видео.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Метод CBaseControlVideo.get_VideoWidth (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658130"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a><span data-ttu-id="c866c-103">Кбасеконтролвидео. Get \_ видеовидс, метод</span><span class="sxs-lookup"><span data-stu-id="c866c-103">CBaseControlVideo.get\_VideoWidth method</span></span>

<span data-ttu-id="c866c-104">`get_VideoWidth`Метод получает ширину собственного видео.</span><span class="sxs-lookup"><span data-stu-id="c866c-104">The `get_VideoWidth` method retrieves the width of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="c866c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c866c-105">Syntax</span></span>


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a><span data-ttu-id="c866c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c866c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c866c-107">*пвидеовидс*</span><span class="sxs-lookup"><span data-stu-id="c866c-107">*pVideoWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="c866c-108">Указатель на ширину собственного видео в пикселях.</span><span class="sxs-lookup"><span data-stu-id="c866c-108">Pointer to the width of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c866c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c866c-109">Return value</span></span>

<span data-ttu-id="c866c-110">Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если объем доступной памяти недостаточен.</span><span class="sxs-lookup"><span data-stu-id="c866c-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="c866c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c866c-111">Remarks</span></span>

<span data-ttu-id="c866c-112">Эта функция члена реализует метод [**ибасиквидео:: Get \_ видеовидс**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) .</span><span class="sxs-lookup"><span data-stu-id="c866c-112">This member function implements the [**IBasicVideo::get\_VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) method.</span></span> <span data-ttu-id="c866c-113">Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.</span><span class="sxs-lookup"><span data-stu-id="c866c-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="c866c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c866c-114">Requirements</span></span>



| <span data-ttu-id="c866c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c866c-115">Requirement</span></span> | <span data-ttu-id="c866c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c866c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c866c-117">Header</span><span class="sxs-lookup"><span data-stu-id="c866c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c866c-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c866c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c866c-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c866c-119">Library</span></span><br/> | <dl> <span data-ttu-id="c866c-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c866c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c866c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c866c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c866c-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="c866c-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




