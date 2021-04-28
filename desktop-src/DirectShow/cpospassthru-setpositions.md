---
description: 'Кпоспасссру. Сетпоситионс, метод Сетпоситионс задает текущее расположение и точку окончания. Этот метод реализует метод Имедиасикинг:: Сетпоситионс.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Кпоспасссру. Сетпоситионс, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8c61f24ab51ffe7fa161830ef9a0c8bdd167256
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085482"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="8d224-104">Кпоспасссру. Сетпоситионс, метод</span><span class="sxs-lookup"><span data-stu-id="8d224-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="8d224-105">`SetPositions`Метод задает текущее расположение и точку окончания.</span><span class="sxs-lookup"><span data-stu-id="8d224-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="8d224-106">Этот метод реализует метод [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="8d224-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d224-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d224-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8d224-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d224-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d224-109">*пкуррент*</span><span class="sxs-lookup"><span data-stu-id="8d224-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="8d224-110">Указатель на переменную, указывающую текущее расположение в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="8d224-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="8d224-111">*двкуррентфлагс*</span><span class="sxs-lookup"><span data-stu-id="8d224-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8d224-112">Побитовое сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="8d224-112">Bitwise combination of flags.</span></span> <span data-ttu-id="8d224-113">Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="8d224-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="8d224-114">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="8d224-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="8d224-115">Указатель на переменную, задающую время окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="8d224-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="8d224-116">*двстопфлагс*</span><span class="sxs-lookup"><span data-stu-id="8d224-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8d224-117">Побитовое сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="8d224-117">Bitwise combination of flags.</span></span> <span data-ttu-id="8d224-118">Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="8d224-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d224-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d224-119">Return value</span></span>

<span data-ttu-id="8d224-120">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="8d224-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d224-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8d224-121">Requirements</span></span>



| <span data-ttu-id="8d224-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8d224-122">Requirement</span></span> | <span data-ttu-id="8d224-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8d224-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d224-124">Header</span><span class="sxs-lookup"><span data-stu-id="8d224-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8d224-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d224-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d224-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d224-126">Library</span></span><br/> | <dl> <span data-ttu-id="8d224-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="8d224-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d224-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8d224-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d224-129">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="8d224-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




