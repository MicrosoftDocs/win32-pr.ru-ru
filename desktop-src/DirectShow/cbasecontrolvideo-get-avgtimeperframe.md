---
description: Метод Get \_ авгтимеперфраме извлекает среднее время для каждого кадра.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Метод CBaseControlVideo.get_AvgTimePerFrame (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688771"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a><span data-ttu-id="f66b3-103">Кбасеконтролвидео. Get \_ авгтимеперфраме, метод</span><span class="sxs-lookup"><span data-stu-id="f66b3-103">CBaseControlVideo.get\_AvgTimePerFrame method</span></span>

<span data-ttu-id="f66b3-104">`get_AvgTimePerFrame`Метод получает среднее время для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="f66b3-104">The `get_AvgTimePerFrame` method retrieves the average time per frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f66b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f66b3-105">Syntax</span></span>


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f66b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f66b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f66b3-107">*павгтимеперфраме*</span><span class="sxs-lookup"><span data-stu-id="f66b3-107">*pAvgTimePerFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="f66b3-108">Указатель на среднее время на кадр.</span><span class="sxs-lookup"><span data-stu-id="f66b3-108">Pointer to the average time per frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f66b3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f66b3-109">Return value</span></span>

<span data-ttu-id="f66b3-110">Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если объем доступной памяти недостаточен.</span><span class="sxs-lookup"><span data-stu-id="f66b3-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="f66b3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f66b3-111">Remarks</span></span>

<span data-ttu-id="f66b3-112">Эта функция члена реализует метод [**ибасиквидео:: Get \_ авгтимеперфраме**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) .</span><span class="sxs-lookup"><span data-stu-id="f66b3-112">This member function implements the [**IBasicVideo::get\_AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) method.</span></span> <span data-ttu-id="f66b3-113">Он вызывает чисто виртуальную функцию члена [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.</span><span class="sxs-lookup"><span data-stu-id="f66b3-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) member function to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="f66b3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f66b3-114">Requirements</span></span>



| <span data-ttu-id="f66b3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f66b3-115">Requirement</span></span> | <span data-ttu-id="f66b3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f66b3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f66b3-117">Header</span><span class="sxs-lookup"><span data-stu-id="f66b3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f66b3-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f66b3-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f66b3-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f66b3-119">Library</span></span><br/> | <dl> <span data-ttu-id="f66b3-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f66b3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f66b3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f66b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f66b3-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="f66b3-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




