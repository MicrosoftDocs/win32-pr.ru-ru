---
description: Использует функцию Microsoft Win32 Сетсреадприорити для установки нового значения приоритета потока.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Кмсгсреад. Сетсреадприорити, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669396"
---
# <a name="cmsgthreadsetthreadpriority-method"></a><span data-ttu-id="d9ff9-103">Кмсгсреад. Сетсреадприорити, метод</span><span class="sxs-lookup"><span data-stu-id="d9ff9-103">CMsgThread.SetThreadPriority method</span></span>

<span data-ttu-id="d9ff9-104">Использует функцию Microsoft Win32 **сетсреадприорити** для установки нового значения приоритета потока.</span><span class="sxs-lookup"><span data-stu-id="d9ff9-104">Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ff9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9ff9-105">Syntax</span></span>


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a><span data-ttu-id="d9ff9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9ff9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9ff9-107">*нприорити*</span><span class="sxs-lookup"><span data-stu-id="d9ff9-107">*nPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="d9ff9-108">Приоритет потока.</span><span class="sxs-lookup"><span data-stu-id="d9ff9-108">Priority of the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9ff9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9ff9-109">Return value</span></span>

<span data-ttu-id="d9ff9-110">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d9ff9-110">Returns one of the following values.</span></span>



| <span data-ttu-id="d9ff9-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d9ff9-111">Return code</span></span>                                                                              | <span data-ttu-id="d9ff9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d9ff9-112">Description</span></span>                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="d9ff9-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d9ff9-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="d9ff9-114">Приоритет был успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="d9ff9-114">Priority was successfully set.</span></span><br/> |
| <dl> <span data-ttu-id="d9ff9-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d9ff9-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d9ff9-116">Приоритет не задан.</span><span class="sxs-lookup"><span data-stu-id="d9ff9-116">Priority was not set.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="d9ff9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9ff9-117">Remarks</span></span>

<span data-ttu-id="d9ff9-118">Клиент и рабочий поток могут вызывать эту функцию члена.</span><span class="sxs-lookup"><span data-stu-id="d9ff9-118">The client and the worker thread can call this member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9ff9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d9ff9-119">Requirements</span></span>



| <span data-ttu-id="d9ff9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d9ff9-120">Requirement</span></span> | <span data-ttu-id="d9ff9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d9ff9-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ff9-122">Header</span><span class="sxs-lookup"><span data-stu-id="d9ff9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d9ff9-123"><dt>Мсгсрд. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9ff9-123"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d9ff9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9ff9-124">Library</span></span><br/> | <dl> <span data-ttu-id="d9ff9-125"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d9ff9-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9ff9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9ff9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ff9-127">**Класс Кмсгсреад**</span><span class="sxs-lookup"><span data-stu-id="d9ff9-127">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




