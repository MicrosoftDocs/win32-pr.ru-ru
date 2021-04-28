---
description: Метод конструктора Каммсжевент. Каммсжевент.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Конструктор Каммсжевент. Каммсжевент (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096541"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="264cb-103">Каммсжевент. Каммсжевент, конструктор</span><span class="sxs-lookup"><span data-stu-id="264cb-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="264cb-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="264cb-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="264cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="264cb-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="264cb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="264cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="264cb-107">*фр*</span><span class="sxs-lookup"><span data-stu-id="264cb-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="264cb-108">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="264cb-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="264cb-109">Если конструктор завершается неудачно, этот параметр получает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="264cb-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="264cb-110">Если это происходит, объект находится в недопустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="264cb-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="264cb-111">Для обеспечения обратной совместимости с более ранними версиями стрмбасе. lib этот параметр по умолчанию **имеет значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="264cb-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="264cb-112">Однако рекомендуется передать значение, отличное от **null** , чтобы вызывающий объект мог проверить состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="264cb-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="264cb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="264cb-113">Requirements</span></span>



| <span data-ttu-id="264cb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="264cb-114">Requirement</span></span> | <span data-ttu-id="264cb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="264cb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="264cb-116">Header</span><span class="sxs-lookup"><span data-stu-id="264cb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="264cb-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="264cb-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="264cb-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="264cb-118">Library</span></span><br/> | <dl> <span data-ttu-id="264cb-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="264cb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="264cb-120">См. также</span><span class="sxs-lookup"><span data-stu-id="264cb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="264cb-121">**Класс Каммсжевент**</span><span class="sxs-lookup"><span data-stu-id="264cb-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




