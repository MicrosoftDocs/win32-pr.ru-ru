---
description: 'Метод Сетпоситионс задает текущую и заданную позиции. Этот метод реализует метод Имедиасикинг:: Сетпоситионс.'
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
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658014"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="5028a-104">Кпоспасссру. Сетпоситионс, метод</span><span class="sxs-lookup"><span data-stu-id="5028a-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="5028a-105">`SetPositions`Метод задает текущее расположение и точку окончания.</span><span class="sxs-lookup"><span data-stu-id="5028a-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="5028a-106">Этот метод реализует метод [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="5028a-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5028a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5028a-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5028a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5028a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5028a-109">*пкуррент*</span><span class="sxs-lookup"><span data-stu-id="5028a-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="5028a-110">Указатель на переменную, указывающую текущее расположение в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="5028a-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="5028a-111">*двкуррентфлагс*</span><span class="sxs-lookup"><span data-stu-id="5028a-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5028a-112">Побитовое сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="5028a-112">Bitwise combination of flags.</span></span> <span data-ttu-id="5028a-113">Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="5028a-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="5028a-114">*пстоп*</span><span class="sxs-lookup"><span data-stu-id="5028a-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="5028a-115">Указатель на переменную, задающую время окончания в единицах текущего формата времени.</span><span class="sxs-lookup"><span data-stu-id="5028a-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="5028a-116">*двстопфлагс*</span><span class="sxs-lookup"><span data-stu-id="5028a-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5028a-117">Побитовое сочетание флагов.</span><span class="sxs-lookup"><span data-stu-id="5028a-117">Bitwise combination of flags.</span></span> <span data-ttu-id="5028a-118">Дополнительные сведения см. в разделе [**имедиасикинг:: сетпоситионс**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="5028a-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5028a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5028a-119">Return value</span></span>

<span data-ttu-id="5028a-120">Возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="5028a-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5028a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="5028a-121">Requirements</span></span>



| <span data-ttu-id="5028a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="5028a-122">Requirement</span></span> | <span data-ttu-id="5028a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="5028a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5028a-124">Header</span><span class="sxs-lookup"><span data-stu-id="5028a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5028a-125"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5028a-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5028a-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5028a-126">Library</span></span><br/> | <dl> <span data-ttu-id="5028a-127"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5028a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5028a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5028a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5028a-129">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="5028a-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




