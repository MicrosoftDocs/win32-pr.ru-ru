---
description: Метод "получить \_ скорость" получает приблизительную скорость потока для видео.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Метод CBaseControlVideo.get_BitRate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688769"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a><span data-ttu-id="91de1-103">Метод Кбасеконтролвидео. Get \_ скорость</span><span class="sxs-lookup"><span data-stu-id="91de1-103">CBaseControlVideo.get\_BitRate method</span></span>

<span data-ttu-id="91de1-104">`get_BitRate`Метод извлекает приблизительную скорость потока для видео.</span><span class="sxs-lookup"><span data-stu-id="91de1-104">The `get_BitRate` method retrieves an approximate bit rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="91de1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91de1-105">Syntax</span></span>


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a><span data-ttu-id="91de1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91de1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91de1-107">*пбитрате*</span><span class="sxs-lookup"><span data-stu-id="91de1-107">*pBitRate*</span></span> 
</dt> <dd>

<span data-ttu-id="91de1-108">Указатель на скорость потока в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="91de1-108">Pointer to the bit rate, in bits per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91de1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91de1-109">Return value</span></span>

<span data-ttu-id="91de1-110">Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если недостаточный объем памяти недоступен.</span><span class="sxs-lookup"><span data-stu-id="91de1-110">Returns NOERROR if successful or E\_OUTOFMEMORY if not enough memory is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="91de1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91de1-111">Remarks</span></span>

<span data-ttu-id="91de1-112">Эта функция члена реализует метод [**ибасиквидео:: Get \_ скорость**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) .</span><span class="sxs-lookup"><span data-stu-id="91de1-112">This member function implements the [**IBasicVideo::get\_BitRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) method.</span></span> <span data-ttu-id="91de1-113">Он вызывает чисто виртуальный [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.</span><span class="sxs-lookup"><span data-stu-id="91de1-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="91de1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="91de1-114">Requirements</span></span>



| <span data-ttu-id="91de1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="91de1-115">Requirement</span></span> | <span data-ttu-id="91de1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="91de1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91de1-117">Header</span><span class="sxs-lookup"><span data-stu-id="91de1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="91de1-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91de1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91de1-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="91de1-119">Library</span></span><br/> | <dl> <span data-ttu-id="91de1-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="91de1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91de1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91de1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91de1-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="91de1-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




