---
description: Получает маркер для потока в объекте Кмсгсреад.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Кмсгсреад. Жетсреадхандле, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675660"
---
# <a name="cmsgthreadgetthreadhandle-method"></a><span data-ttu-id="be29e-103">Кмсгсреад. Жетсреадхандле, метод</span><span class="sxs-lookup"><span data-stu-id="be29e-103">CMsgThread.GetThreadHandle method</span></span>

<span data-ttu-id="be29e-104">Получает маркер для потока в объекте [**кмсгсреад**](cmsgthread.md) .</span><span class="sxs-lookup"><span data-stu-id="be29e-104">Retrieves the handle to the thread in the [**CMsgThread**](cmsgthread.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="be29e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be29e-105">Syntax</span></span>


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a><span data-ttu-id="be29e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be29e-106">Parameters</span></span>

<span data-ttu-id="be29e-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="be29e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be29e-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be29e-108">Return value</span></span>

<span data-ttu-id="be29e-109">Возвращает обработчик потока.</span><span class="sxs-lookup"><span data-stu-id="be29e-109">Returns the thread handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="be29e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be29e-110">Remarks</span></span>

<span data-ttu-id="be29e-111">Этот поток может быть передан в функции ожидания, например [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="be29e-111">The thread handle can be passed to wait functions, such as [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span> <span data-ttu-id="be29e-112">Дескриптор потока получает сигнал при завершении потока.</span><span class="sxs-lookup"><span data-stu-id="be29e-112">The thread handle is signaled when the thread has exited.</span></span>

## <a name="requirements"></a><span data-ttu-id="be29e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="be29e-113">Requirements</span></span>



| <span data-ttu-id="be29e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="be29e-114">Requirement</span></span> | <span data-ttu-id="be29e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="be29e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be29e-116">Header</span><span class="sxs-lookup"><span data-stu-id="be29e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="be29e-117"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be29e-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be29e-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be29e-118">Library</span></span><br/> | <dl> <span data-ttu-id="be29e-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="be29e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be29e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be29e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be29e-121">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="be29e-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

