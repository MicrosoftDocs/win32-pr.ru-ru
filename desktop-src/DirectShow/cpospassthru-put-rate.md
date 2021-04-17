---
description: '\_Метод курса размещения задает скорость воспроизведения. Этот метод реализует метод Имедиапоситион::p UT \_ .'
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Метод CPosPassThru.put_Rate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674836"
---
# <a name="cpospassthruput_rate-method"></a><span data-ttu-id="f06f6-104">Кпоспасссру. помещает \_ метод Rate</span><span class="sxs-lookup"><span data-stu-id="f06f6-104">CPosPassThru.put\_Rate method</span></span>

<span data-ttu-id="f06f6-105">`put_Rate`Метод задает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f06f6-105">The `put_Rate` method sets the playback rate.</span></span> <span data-ttu-id="f06f6-106">Этот метод реализует метод [**имедиапоситион::p UT \_**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .</span><span class="sxs-lookup"><span data-stu-id="f06f6-106">This method implements the [**IMediaPosition::put\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f06f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f06f6-107">Syntax</span></span>


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="f06f6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f06f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f06f6-109">*драте*</span><span class="sxs-lookup"><span data-stu-id="f06f6-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="f06f6-110">Скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f06f6-110">Playback rate.</span></span> <span data-ttu-id="f06f6-111">Не должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="f06f6-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f06f6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f06f6-112">Return value</span></span>

<span data-ttu-id="f06f6-113">Возвращает E \_ INVALIDARG, если *драте* равен нулю.</span><span class="sxs-lookup"><span data-stu-id="f06f6-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="f06f6-114">В противном случае возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="f06f6-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="f06f6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f06f6-115">Remarks</span></span>

<span data-ttu-id="f06f6-116">Отрицательные тарифы указывают на обратную игру.</span><span class="sxs-lookup"><span data-stu-id="f06f6-116">Negative rates indicate reverse play.</span></span> <span data-ttu-id="f06f6-117">Не все носители будут поддерживать обратную воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="f06f6-117">Not all media will support reverse play.</span></span>

## <a name="requirements"></a><span data-ttu-id="f06f6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f06f6-118">Requirements</span></span>



| <span data-ttu-id="f06f6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f06f6-119">Requirement</span></span> | <span data-ttu-id="f06f6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f06f6-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f06f6-121">Header</span><span class="sxs-lookup"><span data-stu-id="f06f6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f06f6-122"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f06f6-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f06f6-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f06f6-123">Library</span></span><br/> | <dl> <span data-ttu-id="f06f6-124"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="f06f6-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f06f6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f06f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f06f6-126">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="f06f6-126">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




