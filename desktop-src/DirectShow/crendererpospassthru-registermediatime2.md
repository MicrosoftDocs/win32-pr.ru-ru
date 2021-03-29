---
description: Метод Регистермедиатиме кэширует метки времени из текущего образца.
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
title: Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)
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
ms.openlocfilehash: ff741e58f74770c8a97c13252302d4ef86868af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665470"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="e6c81-103">Крендерерпоспасссру. Регистермедиатиме, метод (Ктлутил. h)</span><span class="sxs-lookup"><span data-stu-id="e6c81-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="e6c81-104">Метод [**регистермедиатиме**](crendererpospassthru-registermediatime.md) кэширует метки времени из текущего образца.</span><span class="sxs-lookup"><span data-stu-id="e6c81-104">The [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6c81-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a><span data-ttu-id="e6c81-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6c81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c81-107">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="e6c81-107">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c81-108">Время начала примера в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="e6c81-108">Sample start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="e6c81-109">*EndTime*</span><span class="sxs-lookup"><span data-stu-id="e6c81-109">*EndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c81-110">Время окончания примера в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="e6c81-110">Sample end time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6c81-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6c81-111">Return value</span></span>

<span data-ttu-id="e6c81-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6c81-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e6c81-113">Возможные значения включают перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e6c81-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e6c81-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e6c81-114">Return code</span></span>                                                                          | <span data-ttu-id="e6c81-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e6c81-115">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="e6c81-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e6c81-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e6c81-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e6c81-117">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6c81-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6c81-118">Remarks</span></span>

<span data-ttu-id="e6c81-119">Этот метод сохраняет значения меток времени, заданные в параметрах *StartTime* и *EndTime*.</span><span class="sxs-lookup"><span data-stu-id="e6c81-119">This method stores the time stamp values given in *StartTime* and *EndTime*.</span></span> <span data-ttu-id="e6c81-120">Метод [**крендерерпоспасссру:: жетмедиатиме**](crendererpospassthru-getmediatime.md) получает те же значения.</span><span class="sxs-lookup"><span data-stu-id="e6c81-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="e6c81-121">Фильтр должен вызывать этот метод для каждого получаемого примера.</span><span class="sxs-lookup"><span data-stu-id="e6c81-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="e6c81-122">Метод перегружен, чтобы принять либо указатель на образец, либо сами значения меток времени.</span><span class="sxs-lookup"><span data-stu-id="e6c81-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c81-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e6c81-123">Requirements</span></span>



| <span data-ttu-id="e6c81-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e6c81-124">Requirement</span></span> | <span data-ttu-id="e6c81-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e6c81-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c81-126">Header</span><span class="sxs-lookup"><span data-stu-id="e6c81-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e6c81-127"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6c81-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6c81-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6c81-128">Library</span></span><br/> | <dl> <span data-ttu-id="e6c81-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e6c81-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




