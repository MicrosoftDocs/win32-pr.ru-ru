---
description: 'Метод Cancel отменяет ранее поставленный в очередь запрос Кдеферредкомманд:: Invoke.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Метод Кдеферредкомманд. Cancel (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658021"
---
# <a name="cdeferredcommandcancel-method"></a><span data-ttu-id="e18a3-103">Кдеферредкомманд. Cancel, метод</span><span class="sxs-lookup"><span data-stu-id="e18a3-103">CDeferredCommand.Cancel method</span></span>

<span data-ttu-id="e18a3-104">`Cancel`Метод отменяет ранее поставленный в очередь запрос [**кдеферредкомманд:: Invoke**](cdeferredcommand-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="e18a3-104">The `Cancel` method cancels a previously queued [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="e18a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e18a3-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="e18a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e18a3-106">Parameters</span></span>

<span data-ttu-id="e18a3-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e18a3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e18a3-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e18a3-108">Return value</span></span>

<span data-ttu-id="e18a3-109">Возвращает VFW \_ E \_ уже \_ отменено, если **m \_ пкуеуе** имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e18a3-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="e18a3-110">Возвращает **значение HRESULT** из [**ккмдкуеуе:: Remove**](ccmdqueue-remove.md) , если вызов создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e18a3-110">Returns an **HRESULT** from [**CCmdQueue::Remove**](ccmdqueue-remove.md) if the call generates an error.</span></span> <span data-ttu-id="e18a3-111">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="e18a3-111">Returns S\_OK if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e18a3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e18a3-112">Remarks</span></span>

<span data-ttu-id="e18a3-113">Эта функция члена реализует метод [**идеферредкомманд:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .</span><span class="sxs-lookup"><span data-stu-id="e18a3-113">This member function implements the [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e18a3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e18a3-114">Requirements</span></span>



| <span data-ttu-id="e18a3-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e18a3-115">Requirement</span></span> | <span data-ttu-id="e18a3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e18a3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e18a3-117">Header</span><span class="sxs-lookup"><span data-stu-id="e18a3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e18a3-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e18a3-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e18a3-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e18a3-119">Library</span></span><br/> | <dl> <span data-ttu-id="e18a3-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="e18a3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e18a3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e18a3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18a3-122">**Класс Кдеферредкомманд**</span><span class="sxs-lookup"><span data-stu-id="e18a3-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




