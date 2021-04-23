---
description: Метод Чанжерате вызывается при изменении скорости воспроизведения.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Ксаурцесикинг. Чанжерате, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685264"
---
# <a name="csourceseekingchangerate-method"></a><span data-ttu-id="dc8ca-103">Ксаурцесикинг. Чанжерате, метод</span><span class="sxs-lookup"><span data-stu-id="dc8ca-103">CSourceSeeking.ChangeRate method</span></span>

<span data-ttu-id="dc8ca-104">`ChangeRate`Метод вызывается при изменении скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dc8ca-104">The `ChangeRate` method is called when the playback rate changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc8ca-105">Syntax</span></span>


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a><span data-ttu-id="dc8ca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc8ca-106">Parameters</span></span>

<span data-ttu-id="dc8ca-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="dc8ca-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc8ca-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc8ca-108">Return value</span></span>

<span data-ttu-id="dc8ca-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dc8ca-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc8ca-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc8ca-110">Remarks</span></span>

<span data-ttu-id="dc8ca-111">Метод [**ксаурцесикинг:: сетрате**](csourceseeking-setrate.md) вызывает этот метод, который должен реализовываться производным классом.</span><span class="sxs-lookup"><span data-stu-id="dc8ca-111">The [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method calls this method, which the derived class must implement.</span></span> <span data-ttu-id="dc8ca-112">Метод **сетрате** обновляет переменную члена [**ксаурцесикинг:: m \_ дратесикинг**](csourceseeking-m-drateseeking.md) , но не проверяет новое значение.</span><span class="sxs-lookup"><span data-stu-id="dc8ca-112">The **SetRate** method updates the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, but does not validate the new value.</span></span> <span data-ttu-id="dc8ca-113">Нулевую скорость следует всегда отклонять.</span><span class="sxs-lookup"><span data-stu-id="dc8ca-113">A rate of zero should always be rejected.</span></span> <span data-ttu-id="dc8ca-114">Ставки меньше нуля указывают на отрицательное воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="dc8ca-114">Rates less than zero indicate negative playback.</span></span> <span data-ttu-id="dc8ca-115">Большинство фильтров не поддерживает отрицательные тарифы.</span><span class="sxs-lookup"><span data-stu-id="dc8ca-115">Most filters do not support negative rates.</span></span>

<span data-ttu-id="dc8ca-116">В следующем примере показана возможная реализация:</span><span class="sxs-lookup"><span data-stu-id="dc8ca-116">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="dc8ca-117">Требования</span><span class="sxs-lookup"><span data-stu-id="dc8ca-117">Requirements</span></span>



| <span data-ttu-id="dc8ca-118">Требование</span><span class="sxs-lookup"><span data-stu-id="dc8ca-118">Requirement</span></span> | <span data-ttu-id="dc8ca-119">Значение</span><span class="sxs-lookup"><span data-stu-id="dc8ca-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc8ca-120">Header</span><span class="sxs-lookup"><span data-stu-id="dc8ca-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dc8ca-121"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc8ca-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc8ca-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dc8ca-122">Library</span></span><br/> | <dl> <span data-ttu-id="dc8ca-123"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="dc8ca-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc8ca-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc8ca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc8ca-125">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="dc8ca-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




