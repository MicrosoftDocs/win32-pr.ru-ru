---
description: Метод конструктора. Конструктор блокирует указанный объект критической секции.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Конструктор Каутолокк. Каутолокк (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668492"
---
# <a name="cautolockcautolock-constructor"></a><span data-ttu-id="5c0d0-104">Каутолокк. Каутолокк, конструктор</span><span class="sxs-lookup"><span data-stu-id="5c0d0-104">CAutoLock.CAutoLock constructor</span></span>

<span data-ttu-id="5c0d0-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="5c0d0-105">Constructor method.</span></span> <span data-ttu-id="5c0d0-106">Конструктор блокирует указанный объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="5c0d0-106">The constructor locks the specified critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c0d0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c0d0-107">Syntax</span></span>


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a><span data-ttu-id="5c0d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c0d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c0d0-109">*плокк*</span><span class="sxs-lookup"><span data-stu-id="5c0d0-109">*plock*</span></span> 
</dt> <dd>

<span data-ttu-id="5c0d0-110">Указатель на объект [**ккритсек**](ccritsec.md) , который содержит объект критической секции.</span><span class="sxs-lookup"><span data-stu-id="5c0d0-110">Pointer to a [**CCritSec**](ccritsec.md) object, which contains a critical section object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c0d0-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5c0d0-111">Requirements</span></span>



| <span data-ttu-id="5c0d0-112">Требование</span><span class="sxs-lookup"><span data-stu-id="5c0d0-112">Requirement</span></span> | <span data-ttu-id="5c0d0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5c0d0-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c0d0-114">Header</span><span class="sxs-lookup"><span data-stu-id="5c0d0-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5c0d0-115"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c0d0-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5c0d0-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c0d0-116">Library</span></span><br/> | <dl> <span data-ttu-id="5c0d0-117"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="5c0d0-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c0d0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c0d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c0d0-119">**Класс Каутолокк**</span><span class="sxs-lookup"><span data-stu-id="5c0d0-119">**CAutoLock Class**</span></span>](cautolock.md)
</dt> </dl>

 

 




