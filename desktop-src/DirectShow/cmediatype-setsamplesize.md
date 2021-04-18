---
description: Метод Сетсамплесизе задает фиксированный размер выборки или указывает, что выборки имеют переменный размер.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Кмедиатипе. Сетсамплесизе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675599"
---
# <a name="cmediatypesetsamplesize-method"></a><span data-ttu-id="d871d-103">Кмедиатипе. Сетсамплесизе, метод</span><span class="sxs-lookup"><span data-stu-id="d871d-103">CMediaType.SetSampleSize method</span></span>

<span data-ttu-id="d871d-104">`SetSampleSize`Метод задает фиксированный размер выборки или указывает, что выборки имеют переменный размер.</span><span class="sxs-lookup"><span data-stu-id="d871d-104">The `SetSampleSize` method specifies a fixed sample size, or specifies that samples have a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="d871d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d871d-105">Syntax</span></span>


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a><span data-ttu-id="d871d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d871d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d871d-107">*SZ*</span><span class="sxs-lookup"><span data-stu-id="d871d-107">*sz*</span></span> 
</dt> <dd>

<span data-ttu-id="d871d-108">Размер выборки, в байтах или нуль.</span><span class="sxs-lookup"><span data-stu-id="d871d-108">Sample size, in bytes, or zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d871d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d871d-109">Return value</span></span>

<span data-ttu-id="d871d-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d871d-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d871d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d871d-111">Remarks</span></span>

<span data-ttu-id="d871d-112">Если значение *SZ* равно нулю, то тип носителя использует переменные выбор размера.</span><span class="sxs-lookup"><span data-stu-id="d871d-112">If value of *sz* is zero, the media type uses variable sample sizes.</span></span> <span data-ttu-id="d871d-113">В противном случае размер выборки зафиксирован на *SZ* байт.</span><span class="sxs-lookup"><span data-stu-id="d871d-113">Otherwise, the sample size is fixed at *sz* bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d871d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d871d-114">Requirements</span></span>



| <span data-ttu-id="d871d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d871d-115">Requirement</span></span> | <span data-ttu-id="d871d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d871d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d871d-117">Header</span><span class="sxs-lookup"><span data-stu-id="d871d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d871d-118"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d871d-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d871d-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d871d-119">Library</span></span><br/> | <dl> <span data-ttu-id="d871d-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d871d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d871d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d871d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d871d-122">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="d871d-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




