---
description: Использует функцию Microsoft Win32 Жетсреадприорити для получения приоритета текущего рабочего потока.
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: Кмсгсреад. Жетсреадприорити, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665347"
---
# <a name="cmsgthreadgetthreadpriority-method"></a><span data-ttu-id="48c23-103">Кмсгсреад. Жетсреадприорити, метод</span><span class="sxs-lookup"><span data-stu-id="48c23-103">CMsgThread.GetThreadPriority method</span></span>

<span data-ttu-id="48c23-104">Использует функцию Microsoft Win32 **жетсреадприорити** для получения приоритета текущего рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="48c23-104">Uses the Microsoft Win32 **GetThreadPriority** function to retrieve the priority of the current worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48c23-105">Syntax</span></span>


```C++
int GetThreadPriority();
```



## <a name="parameters"></a><span data-ttu-id="48c23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48c23-106">Parameters</span></span>

<span data-ttu-id="48c23-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="48c23-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48c23-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48c23-108">Return value</span></span>

<span data-ttu-id="48c23-109">Возвращает приоритет потока в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="48c23-109">Returns the thread priority as an integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c23-110">Требования</span><span class="sxs-lookup"><span data-stu-id="48c23-110">Requirements</span></span>



| <span data-ttu-id="48c23-111">Требование</span><span class="sxs-lookup"><span data-stu-id="48c23-111">Requirement</span></span> | <span data-ttu-id="48c23-112">Значение</span><span class="sxs-lookup"><span data-stu-id="48c23-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c23-113">Header</span><span class="sxs-lookup"><span data-stu-id="48c23-113">Header</span></span><br/>  | <dl> <span data-ttu-id="48c23-114"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48c23-114"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="48c23-115">Библиотека</span><span class="sxs-lookup"><span data-stu-id="48c23-115">Library</span></span><br/> | <dl> <span data-ttu-id="48c23-116"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="48c23-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c23-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48c23-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c23-118">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="48c23-118">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




