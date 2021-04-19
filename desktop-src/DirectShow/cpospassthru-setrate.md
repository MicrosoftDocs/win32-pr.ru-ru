---
description: 'Метод Сетрате задает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Сетрате.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Кпоспасссру. Сетрате, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675596"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="120a5-104">Кпоспасссру. Сетрате, метод</span><span class="sxs-lookup"><span data-stu-id="120a5-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="120a5-105">`SetRate`Метод задает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="120a5-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="120a5-106">Этот метод реализует метод [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="120a5-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="120a5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="120a5-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="120a5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="120a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="120a5-109">*драте*</span><span class="sxs-lookup"><span data-stu-id="120a5-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="120a5-110">Скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="120a5-110">Playback rate.</span></span> <span data-ttu-id="120a5-111">Не должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="120a5-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="120a5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="120a5-112">Return value</span></span>

<span data-ttu-id="120a5-113">Возвращает E \_ INVALIDARG, если *драте* равен нулю.</span><span class="sxs-lookup"><span data-stu-id="120a5-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="120a5-114">В противном случае возвращает значение **HRESULT** из подключенного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="120a5-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="120a5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="120a5-115">Requirements</span></span>



| <span data-ttu-id="120a5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="120a5-116">Requirement</span></span> | <span data-ttu-id="120a5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="120a5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="120a5-118">Header</span><span class="sxs-lookup"><span data-stu-id="120a5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="120a5-119"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="120a5-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="120a5-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="120a5-120">Library</span></span><br/> | <dl> <span data-ttu-id="120a5-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="120a5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120a5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="120a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120a5-123">**Класс Кпоспасссру**</span><span class="sxs-lookup"><span data-stu-id="120a5-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




