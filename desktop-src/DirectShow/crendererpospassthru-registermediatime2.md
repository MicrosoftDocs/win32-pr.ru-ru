---
description: Метод Регистермедиатиме кэширует метки времени из текущего образца. Этот метод использует параметры *StartTime* и *EndTime* .
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Метод Крендерерпоспасссру. Регистермедиатиме (Ктлутил. h) — параметры StartTime и EndTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7d9fca04be9381fc739467647fedfa064040a0
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187829"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh---starttime-and-endtime-parameters"></a><span data-ttu-id="3b0c3-104">Метод Крендерерпоспасссру. Регистермедиатиме (Ктлутил. h) — параметры StartTime и EndTime</span><span class="sxs-lookup"><span data-stu-id="3b0c3-104">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h) - StartTime and EndTime parameters</span></span>

<span data-ttu-id="3b0c3-105">Метод [**регистермедиатиме**](crendererpospassthru-registermediatime.md) кэширует метки времени из текущего образца.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-105">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0c3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b0c3-106">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="3b0c3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b0c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b0c3-108">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="3b0c3-108">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3b0c3-109">Время начала примера в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-109">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3b0c3-110">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="3b0c3-110">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3b0c3-111">Время окончания примера в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-111">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b0c3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b0c3-112">Return value</span></span>

<span data-ttu-id="3b0c3-113">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3b0c3-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3b0c3-114">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3b0c3-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3b0c3-115">Return code</span></span>                                                                          | <span data-ttu-id="3b0c3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3b0c3-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="3b0c3-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3b0c3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3b0c3-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-118">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b0c3-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="3b0c3-119">Remarks</span></span>

<span data-ttu-id="3b0c3-120">Этот метод сохраняет значения меток времени, заданные в параметрах *StartTime* и *EndTime*.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-120">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="3b0c3-121">Метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) получает те же значения.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-121">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="3b0c3-122">Фильтр должен вызывать этот метод для каждого получаемого примера.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-122">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="3b0c3-123">Метод перегружен, чтобы принять либо указатель на образец, либо сами значения меток времени.</span><span class="sxs-lookup"><span data-stu-id="3b0c3-123">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b0c3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="3b0c3-124">Requirements</span></span>



| <span data-ttu-id="3b0c3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="3b0c3-125">Requirement</span></span> | <span data-ttu-id="3b0c3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3b0c3-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0c3-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3b0c3-127">Header</span></span>  | <span data-ttu-id="3b0c3-128">Ктлутил. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="3b0c3-128">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="3b0c3-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b0c3-129">Library</span></span> | <span data-ttu-id="3b0c3-130">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="3b0c3-130">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




