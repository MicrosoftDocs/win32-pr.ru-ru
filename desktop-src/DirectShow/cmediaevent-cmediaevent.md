---
description: Метод конструктора Кмедиаевент. Кмедиаевент.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Конструктор Кмедиаевент. Кмедиаевент (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095562"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="ffa4e-103">Кмедиаевент. Кмедиаевент, конструктор</span><span class="sxs-lookup"><span data-stu-id="ffa4e-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="ffa4e-104">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="ffa4e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa4e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffa4e-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="ffa4e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffa4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa4e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ffa4e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa4e-108">Указатель на имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="ffa4e-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="ffa4e-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ffa4e-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ffa4e-110">Указатель на владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="ffa4e-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffa4e-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="ffa4e-111">Remarks</span></span>

<span data-ttu-id="ffa4e-112">Выделите параметр *pName* в статической памяти.</span><span class="sxs-lookup"><span data-stu-id="ffa4e-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="ffa4e-113">Это имя отображается в терминале отладки при создании и удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="ffa4e-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa4e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ffa4e-114">Requirements</span></span>



| <span data-ttu-id="ffa4e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ffa4e-115">Requirement</span></span> | <span data-ttu-id="ffa4e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ffa4e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa4e-117">Header</span><span class="sxs-lookup"><span data-stu-id="ffa4e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ffa4e-118"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa4e-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ffa4e-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ffa4e-119">Library</span></span><br/> | <dl> <span data-ttu-id="ffa4e-120"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa4e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa4e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="ffa4e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa4e-122">**Класс Кмедиаевент**</span><span class="sxs-lookup"><span data-stu-id="ffa4e-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




