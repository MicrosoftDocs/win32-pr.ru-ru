---
description: Сведения о методе конструктора Кмедиапоситион. Кмедиапоситион (Ктлутил. h). В этом методе используются параметры "pName", "pUnk" и "фр".
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Конструктор Кмедиапоситион. Кмедиапоситион (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105665009"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a><span data-ttu-id="068b0-104">Кмедиапоситион. Кмедиапоситион-конструктор (Ктлутил. h) — pName, pUnk, параметры фр</span><span class="sxs-lookup"><span data-stu-id="068b0-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk, phr parameters</span></span>

<span data-ttu-id="068b0-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="068b0-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="068b0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="068b0-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="068b0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="068b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068b0-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="068b0-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="068b0-109">Указатель на имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="068b0-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="068b0-110">Выделите этот параметр в статической памяти.</span><span class="sxs-lookup"><span data-stu-id="068b0-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="068b0-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="068b0-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="068b0-112">Указатель на владельца этого объекта или **значение NULL** , если объект не является агрегированным.</span><span class="sxs-lookup"><span data-stu-id="068b0-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> <dt>

<span data-ttu-id="068b0-113">*фр*</span><span class="sxs-lookup"><span data-stu-id="068b0-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="068b0-114">Указатель на значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="068b0-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="068b0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="068b0-115">Requirements</span></span>

| <span data-ttu-id="068b0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="068b0-116">Requirement</span></span> | <span data-ttu-id="068b0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="068b0-117">Value</span></span> |
|-|-|
| <span data-ttu-id="068b0-118">Header</span><span class="sxs-lookup"><span data-stu-id="068b0-118">Header</span></span> | <span data-ttu-id="068b0-119">Ктлутил. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="068b0-119">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="068b0-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="068b0-120">Library</span></span>| <span data-ttu-id="068b0-121">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="068b0-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="068b0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="068b0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068b0-123">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="068b0-123">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




