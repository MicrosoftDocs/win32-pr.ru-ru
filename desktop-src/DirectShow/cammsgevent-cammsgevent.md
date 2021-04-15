---
description: Метод конструктора.
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
ms.openlocfilehash: 0d207afae53a715728d8307656b0c2427ce9574c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669293"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="30915-103">Каммсжевент. Каммсжевент, конструктор</span><span class="sxs-lookup"><span data-stu-id="30915-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="30915-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="30915-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30915-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30915-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="30915-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30915-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30915-107">*фр*</span><span class="sxs-lookup"><span data-stu-id="30915-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="30915-108">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30915-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="30915-109">Если конструктор завершается неудачно, этот параметр получает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="30915-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="30915-110">Если это происходит, объект находится в недопустимом состоянии.</span><span class="sxs-lookup"><span data-stu-id="30915-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="30915-111">Для обеспечения обратной совместимости с более ранними версиями стрмбасе. lib этот параметр по умолчанию **имеет значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="30915-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="30915-112">Однако рекомендуется передать значение, отличное от **null** , чтобы вызывающий объект мог проверить состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="30915-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30915-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30915-113">Requirements</span></span>



| <span data-ttu-id="30915-114">Требование</span><span class="sxs-lookup"><span data-stu-id="30915-114">Requirement</span></span> | <span data-ttu-id="30915-115">Значение</span><span class="sxs-lookup"><span data-stu-id="30915-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30915-116">Header</span><span class="sxs-lookup"><span data-stu-id="30915-116">Header</span></span><br/>  | <dl> <span data-ttu-id="30915-117"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30915-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="30915-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="30915-118">Library</span></span><br/> | <dl> <span data-ttu-id="30915-119"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="30915-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30915-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30915-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30915-121">**Класс Каммсжевент**</span><span class="sxs-lookup"><span data-stu-id="30915-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




