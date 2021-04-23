---
description: Метод Исстреамтиме указывает, должна ли команда выполняться во время потока или во время презентации.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Кдеферредкомманд. Исстреамтиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e15b579f911f6461df30c6b5ae9d3fc29f6fa1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680082"
---
# <a name="cdeferredcommandisstreamtime-method"></a><span data-ttu-id="c3d73-103">Кдеферредкомманд. Исстреамтиме, метод</span><span class="sxs-lookup"><span data-stu-id="c3d73-103">CDeferredCommand.IsStreamTime method</span></span>

<span data-ttu-id="c3d73-104">`IsStreamTime`Метод указывает, должна ли команда выполняться во время потока или во время презентации.</span><span class="sxs-lookup"><span data-stu-id="c3d73-104">The `IsStreamTime` method specifies whether the command is to be run at stream time or presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3d73-105">Syntax</span></span>


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a><span data-ttu-id="c3d73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3d73-106">Parameters</span></span>

<span data-ttu-id="c3d73-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c3d73-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3d73-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3d73-108">Return value</span></span>

<span data-ttu-id="c3d73-109">Возвращает **значение true** , если задано потоковое время. в противном случае возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c3d73-109">Returns **TRUE** if set to stream time; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d73-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c3d73-110">Requirements</span></span>



| <span data-ttu-id="c3d73-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c3d73-111">Requirement</span></span> | <span data-ttu-id="c3d73-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c3d73-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d73-113">Header</span><span class="sxs-lookup"><span data-stu-id="c3d73-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c3d73-114"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d73-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3d73-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3d73-115">Library</span></span><br/> | <dl> <span data-ttu-id="c3d73-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d73-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d73-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3d73-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d73-118">**Класс Кдеферредкомманд**</span><span class="sxs-lookup"><span data-stu-id="c3d73-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




