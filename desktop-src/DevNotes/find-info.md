---
description: Содержит сведения о контексте поиска.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Структура FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655695"
---
# <a name="find_info-structure"></a><span data-ttu-id="74bf2-103">НАЙТИ \_ структуру сведений</span><span class="sxs-lookup"><span data-stu-id="74bf2-103">FIND\_INFO structure</span></span>

<span data-ttu-id="74bf2-104">Содержит сведения о контексте поиска.</span><span class="sxs-lookup"><span data-stu-id="74bf2-104">Contains search context information.</span></span>

## <a name="syntax"></a><span data-ttu-id="74bf2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74bf2-105">Syntax</span></span>


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a><span data-ttu-id="74bf2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="74bf2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="74bf2-107">**тииндекс**</span><span class="sxs-lookup"><span data-stu-id="74bf2-107">**tiIndex**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-108">**TAGID** индекса для поиска.</span><span class="sxs-lookup"><span data-stu-id="74bf2-108">The **TAGID** for the index to be searched.</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-109">**тикуррент**</span><span class="sxs-lookup"><span data-stu-id="74bf2-109">**tiCurrent**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-110">**TAGID** для текущего найденного элемента.</span><span class="sxs-lookup"><span data-stu-id="74bf2-110">The **TAGID** for the current item that was located.</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-111">**тиендиндекс**</span><span class="sxs-lookup"><span data-stu-id="74bf2-111">**tiEndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-112">**TAGID** для последней записи после FindFirst, если индекс уникален.</span><span class="sxs-lookup"><span data-stu-id="74bf2-112">The **TAGID** for the last record after FindFirst if the index is UNIQUE.</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-113">**tName**</span><span class="sxs-lookup"><span data-stu-id="74bf2-113">**tName**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-114">Тип элемента, который необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="74bf2-114">The type of the item to be located.</span></span> <span data-ttu-id="74bf2-115">См. раздел [типы тегов](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="74bf2-115">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-116">**двиндексрек**</span><span class="sxs-lookup"><span data-stu-id="74bf2-116">**dwIndexRec**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-117">Внутренний счетчик, используемый для наблюдения за тем, где в индексе должна начинаться следующая операция поиска.</span><span class="sxs-lookup"><span data-stu-id="74bf2-117">An internal counter used to track where in the index the next find operation should start.</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-118">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="74bf2-118">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-119">Этот элемент может иметь **\_ \_ уникальный \_ ключ индекса** 0 или шимдб (0x00000001), что означает, что это индекс уникального ключа.</span><span class="sxs-lookup"><span data-stu-id="74bf2-119">This member can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001), which indicates that this is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-120">**уллкэй**</span><span class="sxs-lookup"><span data-stu-id="74bf2-120">**ullKey**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-121">Ключ для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="74bf2-121">The key for the current entry.</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-122">**szName**</span><span class="sxs-lookup"><span data-stu-id="74bf2-122">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-123">Текущая строка (если тип тега — **тег \_ типа \_ стрингреф**).</span><span class="sxs-lookup"><span data-stu-id="74bf2-123">The current string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-124">**двнаме**</span><span class="sxs-lookup"><span data-stu-id="74bf2-124">**dwName**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-125">Текущее значение **DWORD** (если тип тега — **\_ тип \_ DWORD**).</span><span class="sxs-lookup"><span data-stu-id="74bf2-125">The current **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="74bf2-126">**пгуиднаме**</span><span class="sxs-lookup"><span data-stu-id="74bf2-126">**pguidName**</span></span>
</dt> <dd>

<span data-ttu-id="74bf2-127">Текущее значение идентификатора GUID (если тип тега является **\_ \_ двоичным типом ТЕГА** , а тег — **тегом \_ Database \_ ID**).</span><span class="sxs-lookup"><span data-stu-id="74bf2-127">The current GUID value (if the tag type is **TAG\_TYPE\_BINARY** and the TAG is **TAG\_DATABASE\_ID**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74bf2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="74bf2-128">Requirements</span></span>



| <span data-ttu-id="74bf2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="74bf2-129">Requirement</span></span> | <span data-ttu-id="74bf2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="74bf2-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74bf2-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74bf2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="74bf2-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74bf2-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74bf2-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74bf2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="74bf2-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74bf2-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74bf2-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74bf2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bf2-136">**сдбфиндфирстдвординдекседтаг**</span><span class="sxs-lookup"><span data-stu-id="74bf2-136">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




