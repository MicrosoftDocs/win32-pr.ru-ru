---
description: Метод Сеттемпоралкомпрессион указывает, сжимаются ли образцы с использованием временного (упакованного) сжатия.
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Кмедиатипе. Сеттемпоралкомпрессион, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675597"
---
# <a name="cmediatypesettemporalcompression-method"></a><span data-ttu-id="8a1bd-103">Кмедиатипе. Сеттемпоралкомпрессион, метод</span><span class="sxs-lookup"><span data-stu-id="8a1bd-103">CMediaType.SetTemporalCompression method</span></span>

<span data-ttu-id="8a1bd-104">`SetTemporalCompression`Метод указывает, сжимаются ли образцы с использованием временного (упакованного) сжатия.</span><span class="sxs-lookup"><span data-stu-id="8a1bd-104">The `SetTemporalCompression` method specifies whether samples are compressed using temporal (interframe) compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a1bd-105">Syntax</span></span>


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a><span data-ttu-id="8a1bd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a1bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a1bd-107">*бкомпрессед*</span><span class="sxs-lookup"><span data-stu-id="8a1bd-107">*bCompressed*</span></span> 
</dt> <dd>

<span data-ttu-id="8a1bd-108">Логическое значение, указывающее, использует ли поток временное сжатие.</span><span class="sxs-lookup"><span data-stu-id="8a1bd-108">Boolean value that specifies whether the stream uses temporal compression.</span></span> <span data-ttu-id="8a1bd-109">Если поток использует временное сжатие, установите значение **true**.</span><span class="sxs-lookup"><span data-stu-id="8a1bd-109">If the stream uses temporal compression, set the value to **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a1bd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a1bd-110">Return value</span></span>

<span data-ttu-id="8a1bd-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="8a1bd-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a1bd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a1bd-112">Remarks</span></span>

<span data-ttu-id="8a1bd-113">Этот метод задает элемент **бтемпоралкомпрессион** .</span><span class="sxs-lookup"><span data-stu-id="8a1bd-113">This method sets the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a1bd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8a1bd-114">Requirements</span></span>



| <span data-ttu-id="8a1bd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8a1bd-115">Requirement</span></span> | <span data-ttu-id="8a1bd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8a1bd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1bd-117">Header</span><span class="sxs-lookup"><span data-stu-id="8a1bd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8a1bd-118"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a1bd-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="8a1bd-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a1bd-119">Library</span></span><br/> | <dl> <span data-ttu-id="8a1bd-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8a1bd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a1bd-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a1bd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1bd-122">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="8a1bd-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




