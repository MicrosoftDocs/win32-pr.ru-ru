---
description: Метод Сеттимеадвисе настраивает событие таймера со ссылочным временем.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Ккмдкуеуе. Сеттимеадвисе, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674795"
---
# <a name="ccmdqueuesettimeadvise-method"></a><span data-ttu-id="42396-103">Ккмдкуеуе. Сеттимеадвисе, метод</span><span class="sxs-lookup"><span data-stu-id="42396-103">CCmdQueue.SetTimeAdvise method</span></span>

<span data-ttu-id="42396-104">`SetTimeAdvise`Метод настраивает событие таймера со ссылочным временем.</span><span class="sxs-lookup"><span data-stu-id="42396-104">The `SetTimeAdvise` method sets up a timer event with the reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="42396-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42396-105">Syntax</span></span>


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a><span data-ttu-id="42396-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42396-106">Parameters</span></span>

<span data-ttu-id="42396-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="42396-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42396-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42396-108">Return value</span></span>

<span data-ttu-id="42396-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="42396-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42396-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42396-110">Remarks</span></span>

<span data-ttu-id="42396-111">Эта функция-член вызывает метод [**иреференцеклокк:: адвисетиме**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) , чтобы настроить уведомление для самого раннего времени, необходимого в очереди.</span><span class="sxs-lookup"><span data-stu-id="42396-111">This member function calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method to set up a notification for the earliest time required in the queue.</span></span> <span data-ttu-id="42396-112">Отложенные команды времени презентации всегда проверяются.</span><span class="sxs-lookup"><span data-stu-id="42396-112">Presentation-time commands that are deferred are always checked.</span></span> <span data-ttu-id="42396-113">Если граф фильтра находится в режиме выполнения, также проверяются отложенные команды, использующие потоковое время.</span><span class="sxs-lookup"><span data-stu-id="42396-113">If the filter graph is in running mode, deferred commands using stream time are also checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="42396-114">Требования</span><span class="sxs-lookup"><span data-stu-id="42396-114">Requirements</span></span>



| <span data-ttu-id="42396-115">Требование</span><span class="sxs-lookup"><span data-stu-id="42396-115">Requirement</span></span> | <span data-ttu-id="42396-116">Значение</span><span class="sxs-lookup"><span data-stu-id="42396-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42396-117">Header</span><span class="sxs-lookup"><span data-stu-id="42396-117">Header</span></span><br/>  | <dl> <span data-ttu-id="42396-118"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42396-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42396-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="42396-119">Library</span></span><br/> | <dl> <span data-ttu-id="42396-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="42396-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42396-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42396-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42396-122">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="42396-122">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




