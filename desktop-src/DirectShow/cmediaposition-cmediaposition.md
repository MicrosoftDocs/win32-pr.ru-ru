---
description: Сведения о методе конструктора Кмедиапоситион. Кмедиапоситион (Ктлутил. h). Этот метод использует параметры "pName" и "pUnk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Конструктор Кмедиапоситион. Кмедиапоситион (Ктлутил. h) — pName, параметры pUnk
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105665011"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a><span data-ttu-id="29aac-104">Конструктор Кмедиапоситион. Кмедиапоситион (Ктлутил. h) — pName, параметры pUnk</span><span class="sxs-lookup"><span data-stu-id="29aac-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk parameters</span></span>

<span data-ttu-id="29aac-105">Метод конструктора.</span><span class="sxs-lookup"><span data-stu-id="29aac-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29aac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29aac-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="29aac-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="29aac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29aac-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="29aac-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="29aac-109">Указатель на имя объекта для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="29aac-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="29aac-110">Выделите этот параметр в статической памяти.</span><span class="sxs-lookup"><span data-stu-id="29aac-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="29aac-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="29aac-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="29aac-112">Указатель на владельца этого объекта или **значение NULL** , если объект не является агрегированным.</span><span class="sxs-lookup"><span data-stu-id="29aac-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29aac-113">Требования</span><span class="sxs-lookup"><span data-stu-id="29aac-113">Requirements</span></span>

| <span data-ttu-id="29aac-114">Требование</span><span class="sxs-lookup"><span data-stu-id="29aac-114">Requirement</span></span> | <span data-ttu-id="29aac-115">Значение</span><span class="sxs-lookup"><span data-stu-id="29aac-115">Value</span></span> |
|-|-|
| <span data-ttu-id="29aac-116">Header</span><span class="sxs-lookup"><span data-stu-id="29aac-116">Header</span></span> | <span data-ttu-id="29aac-117">Ктлутил. h (включение Streams. h)</span><span class="sxs-lookup"><span data-stu-id="29aac-117">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="29aac-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="29aac-118">Library</span></span>| <span data-ttu-id="29aac-119">Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки)</span><span class="sxs-lookup"><span data-stu-id="29aac-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="29aac-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29aac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29aac-121">**Класс Кмедиапоситион**</span><span class="sxs-lookup"><span data-stu-id="29aac-121">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




