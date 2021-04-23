---
description: Метод Дисплайсамплетимес рисует метки времени для примера мультимедиа поверх видеоизображения.
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: Кдравимаже. Дисплайсамплетимес, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658119"
---
# <a name="cdrawimagedisplaysampletimes-method"></a><span data-ttu-id="1876e-103">Кдравимаже. Дисплайсамплетимес, метод</span><span class="sxs-lookup"><span data-stu-id="1876e-103">CDrawImage.DisplaySampleTimes method</span></span>

<span data-ttu-id="1876e-104">`DisplaySampleTimes`Метод рисует метки времени для примера мультимедиа поверх видеоизображения.</span><span class="sxs-lookup"><span data-stu-id="1876e-104">The `DisplaySampleTimes` method draws the time stamps of a media sample on top of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="1876e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1876e-105">Syntax</span></span>


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="1876e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1876e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1876e-107">*псампле*</span><span class="sxs-lookup"><span data-stu-id="1876e-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="1876e-108">Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца.</span><span class="sxs-lookup"><span data-stu-id="1876e-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1876e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1876e-109">Return value</span></span>

<span data-ttu-id="1876e-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1876e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1876e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1876e-111">Remarks</span></span>

<span data-ttu-id="1876e-112">Этот метод вызывается только в отладочных сборках.</span><span class="sxs-lookup"><span data-stu-id="1876e-112">This method is called only in debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="1876e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1876e-113">Requirements</span></span>



| <span data-ttu-id="1876e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1876e-114">Requirement</span></span> | <span data-ttu-id="1876e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1876e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1876e-116">Header</span><span class="sxs-lookup"><span data-stu-id="1876e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1876e-117"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1876e-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1876e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1876e-118">Library</span></span><br/> | <dl> <span data-ttu-id="1876e-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1876e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1876e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1876e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1876e-121">**Класс Кдравимаже**</span><span class="sxs-lookup"><span data-stu-id="1876e-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




