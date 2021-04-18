---
description: Метод Сетвариаблесизе указывает, что выборки не имеют фиксированного размера.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Кмедиатипе. Сетвариаблесизе, метод (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679948"
---
# <a name="cmediatypesetvariablesize-method"></a><span data-ttu-id="73183-103">Кмедиатипе. Сетвариаблесизе, метод</span><span class="sxs-lookup"><span data-stu-id="73183-103">CMediaType.SetVariableSize method</span></span>

<span data-ttu-id="73183-104">`SetVariableSize`Метод указывает, что выборки не имеют фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="73183-104">The `SetVariableSize` method specifies that samples do not have a fixed size.</span></span>

## <a name="syntax"></a><span data-ttu-id="73183-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73183-105">Syntax</span></span>


```C++
void SetVariableSize();
```



## <a name="parameters"></a><span data-ttu-id="73183-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73183-106">Parameters</span></span>

<span data-ttu-id="73183-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="73183-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73183-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73183-108">Return value</span></span>

<span data-ttu-id="73183-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="73183-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73183-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73183-110">Remarks</span></span>

<span data-ttu-id="73183-111">Этот метод задает для элемента **Бфикседсизесамплес** **значение false**.</span><span class="sxs-lookup"><span data-stu-id="73183-111">This method sets the **bFixedSizeSamples** member to **FALSE**.</span></span> <span data-ttu-id="73183-112">Последующие вызовы метода [**кмедиатипе:: жетсамплесизе**](cmediatype-getsamplesize.md) возвращают ноль.</span><span class="sxs-lookup"><span data-stu-id="73183-112">Subsequent calls to the [**CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) method return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="73183-113">Требования</span><span class="sxs-lookup"><span data-stu-id="73183-113">Requirements</span></span>



| <span data-ttu-id="73183-114">Требование</span><span class="sxs-lookup"><span data-stu-id="73183-114">Requirement</span></span> | <span data-ttu-id="73183-115">Значение</span><span class="sxs-lookup"><span data-stu-id="73183-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73183-116">Header</span><span class="sxs-lookup"><span data-stu-id="73183-116">Header</span></span><br/>  | <dl> <span data-ttu-id="73183-117"><dt>Мтипе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73183-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="73183-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73183-118">Library</span></span><br/> | <dl> <span data-ttu-id="73183-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="73183-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73183-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73183-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73183-121">**Класс Кмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="73183-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




