---
description: 'Крендерединпутпин. Ендфлуш, метод Ендфлуш завершает операцию очистки. Этот метод реализует метод Ипин:: Ендфлуш.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Крендерединпутпин. Ендфлуш, метод (Амекстра. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098922"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="47f78-104">Крендерединпутпин. Ендфлуш, метод</span><span class="sxs-lookup"><span data-stu-id="47f78-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="47f78-105">`EndFlush`Метод завершает операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="47f78-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="47f78-106">Этот метод реализует метод [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="47f78-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f78-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47f78-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="47f78-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="47f78-108">Parameters</span></span>

<span data-ttu-id="47f78-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="47f78-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47f78-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47f78-110">Return value</span></span>

<span data-ttu-id="47f78-111">Возвращает \_ ОК, если успешно, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="47f78-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="47f78-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="47f78-112">Remarks</span></span>

<span data-ttu-id="47f78-113">Этот метод очищает все ожидающие события [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="47f78-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f78-114">Требования</span><span class="sxs-lookup"><span data-stu-id="47f78-114">Requirements</span></span>



| <span data-ttu-id="47f78-115">Требование</span><span class="sxs-lookup"><span data-stu-id="47f78-115">Requirement</span></span> | <span data-ttu-id="47f78-116">Значение</span><span class="sxs-lookup"><span data-stu-id="47f78-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f78-117">Header</span><span class="sxs-lookup"><span data-stu-id="47f78-117">Header</span></span><br/>  | <dl> <span data-ttu-id="47f78-118"><dt>Амекстра. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47f78-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47f78-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="47f78-119">Library</span></span><br/> | <dl> <span data-ttu-id="47f78-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="47f78-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f78-121">См. также</span><span class="sxs-lookup"><span data-stu-id="47f78-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f78-122">**Класс Крендерединпутпин**</span><span class="sxs-lookup"><span data-stu-id="47f78-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




