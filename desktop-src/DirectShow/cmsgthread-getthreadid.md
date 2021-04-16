---
description: Возвращает идентификатор потока.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Кмсгсреад. Жетсреадид, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668657"
---
# <a name="cmsgthreadgetthreadid-method"></a><span data-ttu-id="97a61-103">Кмсгсреад. Жетсреадид, метод</span><span class="sxs-lookup"><span data-stu-id="97a61-103">CMsgThread.GetThreadID method</span></span>

<span data-ttu-id="97a61-104">Возвращает идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="97a61-104">Retrieves the thread's identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a61-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97a61-105">Syntax</span></span>


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a><span data-ttu-id="97a61-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97a61-106">Parameters</span></span>

<span data-ttu-id="97a61-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="97a61-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97a61-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97a61-108">Return value</span></span>

<span data-ttu-id="97a61-109">Возвращает закрытый элемент данных **\_ потока ThreadId** .</span><span class="sxs-lookup"><span data-stu-id="97a61-109">Returns the **m\_ThreadId** private data member.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a61-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97a61-110">Remarks</span></span>

<span data-ttu-id="97a61-111">Эта функция возвращает идентификатор Microsoft Win32 для рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="97a61-111">This function returns the Microsoft Win32 identifier for the worker thread.</span></span> <span data-ttu-id="97a61-112">Эту функцию-член можно вызвать либо в рабочем потоке, либо в клиентском потоке.</span><span class="sxs-lookup"><span data-stu-id="97a61-112">You can call this member function on either the worker thread or a client thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="97a61-113">Требования</span><span class="sxs-lookup"><span data-stu-id="97a61-113">Requirements</span></span>



| <span data-ttu-id="97a61-114">Требование</span><span class="sxs-lookup"><span data-stu-id="97a61-114">Requirement</span></span> | <span data-ttu-id="97a61-115">Значение</span><span class="sxs-lookup"><span data-stu-id="97a61-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a61-116">Header</span><span class="sxs-lookup"><span data-stu-id="97a61-116">Header</span></span><br/>  | <dl> <span data-ttu-id="97a61-117"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97a61-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="97a61-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97a61-118">Library</span></span><br/> | <dl> <span data-ttu-id="97a61-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="97a61-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97a61-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97a61-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a61-121">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="97a61-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




