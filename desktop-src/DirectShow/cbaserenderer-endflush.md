---
description: Метод Ендфлуш завершает операцию очистки.
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
ms.openlocfilehash: 3bd565bfa21edb9945b901d8e315f3e1d1cd054f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668742"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="30381-103">Кбасерендерер. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="30381-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="30381-104">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="30381-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="30381-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30381-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="30381-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30381-106">Parameters</span></span>

<span data-ttu-id="30381-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="30381-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30381-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30381-108">Return value</span></span>

<span data-ttu-id="30381-109">Возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="30381-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="30381-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30381-110">Remarks</span></span>

<span data-ttu-id="30381-111">Входной ПИН-код фильтра вызывает этот метод при получении вызова метода [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="30381-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="30381-112">Требования</span><span class="sxs-lookup"><span data-stu-id="30381-112">Requirements</span></span>



| <span data-ttu-id="30381-113">Требование</span><span class="sxs-lookup"><span data-stu-id="30381-113">Requirement</span></span> | <span data-ttu-id="30381-114">Значение</span><span class="sxs-lookup"><span data-stu-id="30381-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30381-115">Header</span><span class="sxs-lookup"><span data-stu-id="30381-115">Header</span></span><br/>  | <dl> <span data-ttu-id="30381-116"><dt>Ренбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30381-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30381-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="30381-117">Library</span></span><br/> | <dl> <span data-ttu-id="30381-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="30381-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30381-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30381-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30381-120">**Класс Кбасерендерер**</span><span class="sxs-lookup"><span data-stu-id="30381-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




