---
description: Метод Get \_ битерроррате извлекает приблизительную частоту ошибок в битах для видео.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Метод CBaseControlVideo.get_BitErrorRate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657249"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a><span data-ttu-id="37218-103">Кбасеконтролвидео. Get \_ битерроррате, метод</span><span class="sxs-lookup"><span data-stu-id="37218-103">CBaseControlVideo.get\_BitErrorRate method</span></span>

<span data-ttu-id="37218-104">`get_BitErrorRate`Метод извлекает приблизительную частоту ошибок в битах для видео.</span><span class="sxs-lookup"><span data-stu-id="37218-104">The `get_BitErrorRate` method retrieves an approximate bit error rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="37218-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37218-105">Syntax</span></span>


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a><span data-ttu-id="37218-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37218-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37218-107">*пбитерроррате*</span><span class="sxs-lookup"><span data-stu-id="37218-107">*pBitErrorRate*</span></span> 
</dt> <dd>

<span data-ttu-id="37218-108">Указатель на частоту битовых ошибок (одна ошибка для приблизительного числа битов).</span><span class="sxs-lookup"><span data-stu-id="37218-108">Pointer to the bit error rate (one error for approximately this many bits).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37218-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37218-109">Return value</span></span>

<span data-ttu-id="37218-110">Возвращает ошибку с ошибками в случае успеха или E \_ OUTOFMEMORY, если объем доступной памяти недостаточен.</span><span class="sxs-lookup"><span data-stu-id="37218-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="37218-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37218-111">Remarks</span></span>

<span data-ttu-id="37218-112">Эта функция члена реализует метод [**ибасиквидео:: Get \_ битерроррате**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) .</span><span class="sxs-lookup"><span data-stu-id="37218-112">This member function implements the [**IBasicVideo::get\_BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) method.</span></span> <span data-ttu-id="37218-113">Он вызывает чистый виртуальный метод [**кбасеконтролвидео:: жетвидеоформат**](cbasecontrolvideo-getvideoformat.md) для получения структуры [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) из производного класса.</span><span class="sxs-lookup"><span data-stu-id="37218-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) method to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="37218-114">Требования</span><span class="sxs-lookup"><span data-stu-id="37218-114">Requirements</span></span>



| <span data-ttu-id="37218-115">Требование</span><span class="sxs-lookup"><span data-stu-id="37218-115">Requirement</span></span> | <span data-ttu-id="37218-116">Значение</span><span class="sxs-lookup"><span data-stu-id="37218-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37218-117">Header</span><span class="sxs-lookup"><span data-stu-id="37218-117">Header</span></span><br/>  | <dl> <span data-ttu-id="37218-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37218-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37218-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="37218-119">Library</span></span><br/> | <dl> <span data-ttu-id="37218-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="37218-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37218-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37218-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37218-122">**Класс Кбасеконтролвидео**</span><span class="sxs-lookup"><span data-stu-id="37218-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




