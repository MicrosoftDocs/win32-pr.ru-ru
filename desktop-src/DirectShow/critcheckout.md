---
description: Возвращает значение FALSE, если текущий поток является владельцем указанной критической секции.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Функция Критчеккаут (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665465"
---
# <a name="critcheckout-function"></a><span data-ttu-id="03aa2-103">Функция Критчеккаут</span><span class="sxs-lookup"><span data-stu-id="03aa2-103">CritCheckOut function</span></span>

<span data-ttu-id="03aa2-104">Возвращает **значение false** , если текущий поток является владельцем указанной критической секции.</span><span class="sxs-lookup"><span data-stu-id="03aa2-104">Returns **FALSE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="03aa2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03aa2-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="03aa2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03aa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03aa2-107">*пккрит*</span><span class="sxs-lookup"><span data-stu-id="03aa2-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="03aa2-108">Указатель на критический раздел [**ккритсек**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="03aa2-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03aa2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03aa2-109">Return value</span></span>

<span data-ttu-id="03aa2-110">В отладочных сборках возвращает **значение false** , если текущий поток является владельцем этой критической секции, или **true** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="03aa2-110">In debug builds, returns **FALSE** if the current thread is the owner of this critical section, or **TRUE** otherwise.</span></span> <span data-ttu-id="03aa2-111">В розничных сборках всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="03aa2-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03aa2-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03aa2-112">Remarks</span></span>

<span data-ttu-id="03aa2-113">Эта функция является инверсией функции [**критчеккин**](critcheckin.md) .</span><span class="sxs-lookup"><span data-stu-id="03aa2-113">This function is the inverse of the [**CritCheckIn**](critcheckin.md) function.</span></span> <span data-ttu-id="03aa2-114">Если **критчеккин** возвращает **значение true**, **критчеккаут** возвращает **значение false** и наоборот.</span><span class="sxs-lookup"><span data-stu-id="03aa2-114">If **CritCheckIn** returns **TRUE**, **CritCheckOut** returns **FALSE**, and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="03aa2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="03aa2-115">Requirements</span></span>



| <span data-ttu-id="03aa2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="03aa2-116">Requirement</span></span> | <span data-ttu-id="03aa2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="03aa2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03aa2-118">Header</span><span class="sxs-lookup"><span data-stu-id="03aa2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="03aa2-119"><dt>Вксутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03aa2-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="03aa2-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03aa2-120">Library</span></span><br/> | <dl> <span data-ttu-id="03aa2-121"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="03aa2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03aa2-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03aa2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03aa2-123">Функции отладки критического раздела</span><span class="sxs-lookup"><span data-stu-id="03aa2-123">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




