---
description: Метод Чанжестоп вызывается при изменении позиции окончания.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Ксаурцесикинг. Чанжестоп, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688762"
---
# <a name="csourceseekingchangestop-method"></a><span data-ttu-id="7894f-103">Ксаурцесикинг. Чанжестоп, метод</span><span class="sxs-lookup"><span data-stu-id="7894f-103">CSourceSeeking.ChangeStop method</span></span>

<span data-ttu-id="7894f-104">`ChangeStop`Метод вызывается при изменении позиции окончания.</span><span class="sxs-lookup"><span data-stu-id="7894f-104">The `ChangeStop` method is called when the stop position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7894f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7894f-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a><span data-ttu-id="7894f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7894f-106">Parameters</span></span>

<span data-ttu-id="7894f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7894f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7894f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7894f-108">Return value</span></span>

<span data-ttu-id="7894f-109">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7894f-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7894f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7894f-110">Remarks</span></span>

<span data-ttu-id="7894f-111">Метод [**ксаурцесикинг:: сетпоситионс**](csourceseeking-setpositions.md) вызывает этот метод, если позиция окончания изменяется.</span><span class="sxs-lookup"><span data-stu-id="7894f-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the stop position changes.</span></span> <span data-ttu-id="7894f-112">Этот метод является чисто виртуальным; производный класс должен реализовать его.</span><span class="sxs-lookup"><span data-stu-id="7894f-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="7894f-113">В следующем примере показана возможная реализация:</span><span class="sxs-lookup"><span data-stu-id="7894f-113">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="7894f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7894f-114">Requirements</span></span>



| <span data-ttu-id="7894f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7894f-115">Requirement</span></span> | <span data-ttu-id="7894f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7894f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7894f-117">Header</span><span class="sxs-lookup"><span data-stu-id="7894f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7894f-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7894f-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7894f-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7894f-119">Library</span></span><br/> | <dl> <span data-ttu-id="7894f-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7894f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7894f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7894f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7894f-122">**Класс Ксаурцесикинг**</span><span class="sxs-lookup"><span data-stu-id="7894f-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




