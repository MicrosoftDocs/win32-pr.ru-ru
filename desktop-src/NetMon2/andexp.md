---
description: Структура АНДЕКСП содержит массив совпадений шаблонов, используемых для вычисления данных кадра.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Структура АНДЕКСП (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346835"
---
# <a name="andexp-structure"></a><span data-ttu-id="ed619-103">Структура АНДЕКСП</span><span class="sxs-lookup"><span data-stu-id="ed619-103">ANDEXP structure</span></span>

<span data-ttu-id="ed619-104">Структура **андексп** содержит массив совпадений шаблонов, используемых для вычисления данных кадра.</span><span class="sxs-lookup"><span data-stu-id="ed619-104">The **ANDEXP** structure contains an array of pattern matches used to evaluate frame data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed619-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed619-105">Syntax</span></span>


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a><span data-ttu-id="ed619-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ed619-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed619-107">**нпаттернматчес**</span><span class="sxs-lookup"><span data-stu-id="ed619-107">**nPatternMatches**</span></span>
</dt> <dd>

<span data-ttu-id="ed619-108">Число совпадений шаблонов.</span><span class="sxs-lookup"><span data-stu-id="ed619-108">Number of pattern matches.</span></span>

</dd> <dt>

<span data-ttu-id="ed619-109">**паттернматч**</span><span class="sxs-lookup"><span data-stu-id="ed619-109">**PatternMatch**</span></span>
</dt> <dd>

<span data-ttu-id="ed619-110">Массив элементов сопоставления шаблона.</span><span class="sxs-lookup"><span data-stu-id="ed619-110">Array of pattern match elements.</span></span> <span data-ttu-id="ed619-111">Обратите внимание, что каждая структура **андексп** может содержать до четырех элементов соответствия шаблону.</span><span class="sxs-lookup"><span data-stu-id="ed619-111">Note that each **ANDEXP** structure can contain up to four pattern match elements.</span></span> <span data-ttu-id="ed619-112">Дополнительные сведения об этом элементе см. в разделе [фильтры записи](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ed619-112">For more information about this member, see [Capture Filters](capture-filters.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed619-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed619-113">Remarks</span></span>

<span data-ttu-id="ed619-114">Шаблоны в массиве **паттернматч** \[ Max \_ Patterns \] соединяются как одноранговые в операторах логического или в формате</span><span class="sxs-lookup"><span data-stu-id="ed619-114">The patterns in the **PatternMatch**\[MAX\_PATTERNS\] array are joined as peers in logical OR statements in the format</span></span>

<span data-ttu-id="ed619-115">(Шаблон 1 \| \| Шаблон 2 \| \| шаблон 3).</span><span class="sxs-lookup"><span data-stu-id="ed619-115">(Pattern 1 \|\| Pattern 2 \|\| Pattern 3).</span></span>

<span data-ttu-id="ed619-116">Дополнительные сведения о реализации этой структуры см. в разделе [фильтры записи](capture-filters.md) .</span><span class="sxs-lookup"><span data-stu-id="ed619-116">For more information about implementing this structure, see [Capture Filters](capture-filters.md) .</span></span>

## <a name="requirements"></a><span data-ttu-id="ed619-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ed619-117">Requirements</span></span>



| <span data-ttu-id="ed619-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ed619-118">Requirement</span></span> | <span data-ttu-id="ed619-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ed619-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed619-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed619-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed619-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed619-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ed619-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed619-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed619-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed619-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed619-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ed619-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed619-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed619-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed619-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed619-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed619-127">паттернматч</span><span class="sxs-lookup"><span data-stu-id="ed619-127">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




