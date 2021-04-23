---
description: Метод NotReady сигнализирует, что переход состояния еще не завершен.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Кбасерендерер. NotReady, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669415"
---
# <a name="cbaserenderernotready-method"></a><span data-ttu-id="7373c-103">Кбасерендерер. NotReady, метод</span><span class="sxs-lookup"><span data-stu-id="7373c-103">CBaseRenderer.NotReady method</span></span>

<span data-ttu-id="7373c-104">`NotReady`Метод сигнализирует, что переход состояния еще не завершен.</span><span class="sxs-lookup"><span data-stu-id="7373c-104">The `NotReady` method signals that a state transition is not yet complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="7373c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7373c-105">Syntax</span></span>


```C++
void NotReady();
```



## <a name="parameters"></a><span data-ttu-id="7373c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7373c-106">Parameters</span></span>

<span data-ttu-id="7373c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7373c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7373c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7373c-108">Return value</span></span>

<span data-ttu-id="7373c-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7373c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7373c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7373c-110">Remarks</span></span>

<span data-ttu-id="7373c-111">Этот метод приводит к тому, что метод [**кбасерендерер::**](cbaserenderer-getstate.md) noreturn возвращает в качестве \_ \_ промежуточного состояния VFW S \_ , что означает, что фильтр все еще переходит в текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="7373c-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return VFW\_S\_STATE\_INTERMEDIATE, which indicates that the filter is still transitioning to its current state.</span></span> <span data-ttu-id="7373c-112">Фильтр вызывает этот метод при ожидании перехода состояния.</span><span class="sxs-lookup"><span data-stu-id="7373c-112">The filter calls this method whenever a state transition is pending.</span></span> <span data-ttu-id="7373c-113">(Это происходит, когда фильтр приостанавливается, пока не будет получен пример.)</span><span class="sxs-lookup"><span data-stu-id="7373c-113">(This occurs when the filter pauses, until it receives a sample.)</span></span>

## <a name="requirements"></a><span data-ttu-id="7373c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7373c-114">Requirements</span></span>



| <span data-ttu-id="7373c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7373c-115">Requirement</span></span> | <span data-ttu-id="7373c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7373c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7373c-117">Header</span><span class="sxs-lookup"><span data-stu-id="7373c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7373c-118"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7373c-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7373c-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7373c-119">Library</span></span><br/> | <dl> <span data-ttu-id="7373c-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="7373c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7373c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7373c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7373c-122">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="7373c-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="7373c-123">**чеккреади**</span><span class="sxs-lookup"><span data-stu-id="7373c-123">**CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="7373c-124">**Ready**</span><span class="sxs-lookup"><span data-stu-id="7373c-124">**Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




