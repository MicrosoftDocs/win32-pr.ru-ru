---
description: Кпоспасссру. Жетмедиатиме, метод Жетмедиатиме извлекает метки времени для текущего образца.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Кпоспасссру. Жетмедиатиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095262"
---
# <a name="cpospassthrugetmediatime-method"></a><span data-ttu-id="57969-103">Кпоспасссру. Жетмедиатиме, метод</span><span class="sxs-lookup"><span data-stu-id="57969-103">CPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="57969-104">`GetMediaTime`Метод получает метки времени для текущего образца.</span><span class="sxs-lookup"><span data-stu-id="57969-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="57969-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57969-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="57969-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57969-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57969-107">*пстарттиме*</span><span class="sxs-lookup"><span data-stu-id="57969-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="57969-108">Указатель на переменную, которая получает время начала в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="57969-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="57969-109">*пендтиме*</span><span class="sxs-lookup"><span data-stu-id="57969-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="57969-110">Указатель на переменную, которая получает время окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="57969-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57969-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57969-111">Return value</span></span>

<span data-ttu-id="57969-112">Возвращает значение E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="57969-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="57969-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="57969-113">Remarks</span></span>

<span data-ttu-id="57969-114">Переопределите этот метод, если фильтр кэширует метки времени на получаемых образцах.</span><span class="sxs-lookup"><span data-stu-id="57969-114">Override this method if your filter caches the time stamps on the samples it receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="57969-115">Требования</span><span class="sxs-lookup"><span data-stu-id="57969-115">Requirements</span></span>



| <span data-ttu-id="57969-116">Требование</span><span class="sxs-lookup"><span data-stu-id="57969-116">Requirement</span></span> | <span data-ttu-id="57969-117">Значение</span><span class="sxs-lookup"><span data-stu-id="57969-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57969-118">Header</span><span class="sxs-lookup"><span data-stu-id="57969-118">Header</span></span><br/>  | <dl> <span data-ttu-id="57969-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57969-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57969-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="57969-120">Library</span></span><br/> | <dl> <span data-ttu-id="57969-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="57969-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57969-122">См. также</span><span class="sxs-lookup"><span data-stu-id="57969-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57969-123">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="57969-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




