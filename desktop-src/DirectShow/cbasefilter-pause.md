---
description: Кбасефилтер. Pause, метод Pause приостанавливает фильтр. Этот метод реализует метод Имедиафилтер::P Аусе.
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Метод Кбасефилтер. Pause (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee91393a574d0135e66e5a9c1e1e6b0325a0b4de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120092"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="fef59-104">Кбасефилтер. Pause, метод</span><span class="sxs-lookup"><span data-stu-id="fef59-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="fef59-105">`Pause`Метод приостанавливает фильтр.</span><span class="sxs-lookup"><span data-stu-id="fef59-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="fef59-106">Этот метод реализует метод [**имедиафилтер::P Аусе**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="fef59-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fef59-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="fef59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fef59-108">Parameters</span></span>

<span data-ttu-id="fef59-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fef59-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fef59-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fef59-110">Return value</span></span>

<span data-ttu-id="fef59-111">Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="fef59-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fef59-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="fef59-112">Remarks</span></span>

<span data-ttu-id="fef59-113">Этот метод вызывает метод [**кбасепин:: Active**](cbasepin-active.md) для каждого подключенного контакта фильтра.</span><span class="sxs-lookup"><span data-stu-id="fef59-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="fef59-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fef59-114">Requirements</span></span>



| <span data-ttu-id="fef59-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fef59-115">Requirement</span></span> | <span data-ttu-id="fef59-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fef59-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef59-117">Header</span><span class="sxs-lookup"><span data-stu-id="fef59-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fef59-118"><dt>Амфилтер. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fef59-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fef59-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fef59-119">Library</span></span><br/> | <dl> <span data-ttu-id="fef59-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="fef59-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fef59-121">См. также</span><span class="sxs-lookup"><span data-stu-id="fef59-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fef59-122">**Класс Кбасефилтер**</span><span class="sxs-lookup"><span data-stu-id="fef59-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




