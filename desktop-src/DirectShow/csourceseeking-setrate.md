---
description: 'Метод Сетрате задает скорость воспроизведения. Этот метод реализует метод Имедиасикинг:: Сетрате.'
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
ms.openlocfilehash: 718a38f3eff9cc1647d09cf142db784f53e4c755
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688888"
---
# <a name="csourceseekingsetrate-method"></a><span data-ttu-id="94900-104">Ксаурцесикинг. Сетрате, метод</span><span class="sxs-lookup"><span data-stu-id="94900-104">CSourceSeeking.SetRate method</span></span>

<span data-ttu-id="94900-105">`SetRate`Метод задает скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="94900-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="94900-106">Этот метод реализует метод [**имедиасикинг:: сетрате**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="94900-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="94900-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94900-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="94900-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="94900-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94900-109">*драте*</span><span class="sxs-lookup"><span data-stu-id="94900-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="94900-110">Скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="94900-110">Playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94900-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94900-111">Return value</span></span>

<span data-ttu-id="94900-112">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94900-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94900-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94900-113">Remarks</span></span>

<span data-ttu-id="94900-114">Этот метод обновляет значение переменной члена [**ксаурцесикинг:: m \_ дратесикинг**](csourceseeking-m-drateseeking.md) , а затем вызывает чистый виртуальный метод [**ксаурцесикинг:: чанжерате**](csourceseeking-changerate.md).</span><span class="sxs-lookup"><span data-stu-id="94900-114">This method updates the value of the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="94900-115">Метод не проверяет параметр *драте* .</span><span class="sxs-lookup"><span data-stu-id="94900-115">The method does not validate the *dRate* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="94900-116">Требования</span><span class="sxs-lookup"><span data-stu-id="94900-116">Requirements</span></span>



| <span data-ttu-id="94900-117">Требование</span><span class="sxs-lookup"><span data-stu-id="94900-117">Requirement</span></span> | <span data-ttu-id="94900-118">Значение</span><span class="sxs-lookup"><span data-stu-id="94900-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94900-119">Header</span><span class="sxs-lookup"><span data-stu-id="94900-119">Header</span></span><br/>  | <dl> <span data-ttu-id="94900-120"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94900-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94900-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94900-121">Library</span></span><br/> | <dl> <span data-ttu-id="94900-122"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="94900-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94900-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94900-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94900-124">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="94900-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




