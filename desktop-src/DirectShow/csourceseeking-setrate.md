---
description: 'Ксаурцесикинг. Сетрате, метод Сетрате задает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Сетрате.'
ms.assetid: 954e2381-207a-47d9-a0a5-87dc325f52b4
title: Ксаурцесикинг. Сетрате, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c37d9c94da4a59a2be9b7258881c5bb22b4aa4c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098742"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="6158a-104">Ксаурцесикинг. Сетрате, метод</span><span class="sxs-lookup"><span data-stu-id="6158a-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="6158a-105">`SetRate`Метод задает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6158a-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="6158a-106">Этот метод реализует метод [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="6158a-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6158a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6158a-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="6158a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6158a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6158a-109">*драте*</span><span class="sxs-lookup"><span data-stu-id="6158a-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="6158a-110">Скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6158a-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6158a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6158a-111">Return value</span></span>

<span data-ttu-id="6158a-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6158a-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6158a-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="6158a-113">Remarks</span></span>

<span data-ttu-id="6158a-114">Этот метод обновляет значение переменной члена [**ксаурцесикинг:: m \_ дратесикинг**](csourceseeking-m-drateseeking.md) , а затем вызывает чистый виртуальный метод [**ксаурцесикинг:: чанжерате**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="6158a-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="6158a-115">Метод не проверяет параметр *драте* .</span><span class="sxs-lookup"><span data-stu-id="6158a-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6158a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6158a-116">Requirements</span></span>



| <span data-ttu-id="6158a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6158a-117">Requirement</span></span> | <span data-ttu-id="6158a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6158a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6158a-119">Header</span><span class="sxs-lookup"><span data-stu-id="6158a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6158a-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6158a-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6158a-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6158a-121">Library</span></span><br/> | <dl> <span data-ttu-id="6158a-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="6158a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6158a-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6158a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6158a-124">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="6158a-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




