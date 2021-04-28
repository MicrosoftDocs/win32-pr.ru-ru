---
description: Кбасерендерер. Ендфлуш, метод Ендфлуш завершает операцию очистки.
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Кбасерендерер. Ендфлуш, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87e29f405430ca87943773d19793ffc1941ec42c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095912"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="ef11a-103">Кбасерендерер. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="ef11a-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="ef11a-104">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="ef11a-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef11a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef11a-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="ef11a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef11a-106">Parameters</span></span>

<span data-ttu-id="ef11a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ef11a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef11a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef11a-108">Return value</span></span>

<span data-ttu-id="ef11a-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ef11a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef11a-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="ef11a-110">Remarks</span></span>

<span data-ttu-id="ef11a-111">Входной ПИН-код фильтра вызывает этот метод при получении вызова метода [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="ef11a-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef11a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ef11a-112">Requirements</span></span>



| <span data-ttu-id="ef11a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ef11a-113">Requirement</span></span> | <span data-ttu-id="ef11a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ef11a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef11a-115">Header</span><span class="sxs-lookup"><span data-stu-id="ef11a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ef11a-116"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef11a-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef11a-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef11a-117">Library</span></span><br/> | <dl> <span data-ttu-id="ef11a-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ef11a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef11a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ef11a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef11a-120">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="ef11a-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




