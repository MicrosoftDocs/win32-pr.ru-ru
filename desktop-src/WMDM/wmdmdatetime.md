---
title: Структура ВМДМДАТЕТИМЕ
description: Структура ВМДМДАТЕТИМЕ содержит дату и время суток.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Структура ВМДМДАТЕТИМЕ Windows Media диспетчер устройств
- Указатель структуры ПВМДМДАТЕТИМЕ Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694464"
---
# <a name="wmdmdatetime-structure"></a><span data-ttu-id="87909-105">Структура ВМДМДАТЕТИМЕ</span><span class="sxs-lookup"><span data-stu-id="87909-105">WMDMDATETIME structure</span></span>

<span data-ttu-id="87909-106">Структура **вмдмдатетиме** содержит дату и время суток.</span><span class="sxs-lookup"><span data-stu-id="87909-106">The **WMDMDATETIME** structure contains a date and time of day.</span></span>

## <a name="syntax"></a><span data-ttu-id="87909-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87909-107">Syntax</span></span>


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a><span data-ttu-id="87909-108">Члены</span><span class="sxs-lookup"><span data-stu-id="87909-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="87909-109">**веар**</span><span class="sxs-lookup"><span data-stu-id="87909-109">**wYear**</span></span>
</dt> <dd>

<span data-ttu-id="87909-110">Слово, содержащее год из четырех цифр.</span><span class="sxs-lookup"><span data-stu-id="87909-110">Word containing the four-digit year.</span></span>

</dd> <dt>

<span data-ttu-id="87909-111">**вмонс**</span><span class="sxs-lookup"><span data-stu-id="87909-111">**wMonth**</span></span>
</dt> <dd>

<span data-ttu-id="87909-112">Слово, содержащее месяц (1-12).</span><span class="sxs-lookup"><span data-stu-id="87909-112">Word containing the month (1-12).</span></span>

</dd> <dt>

<span data-ttu-id="87909-113">**вдай**</span><span class="sxs-lookup"><span data-stu-id="87909-113">**wDay**</span></span>
</dt> <dd>

<span data-ttu-id="87909-114">Слово, содержащее день месяца (1-31).</span><span class="sxs-lookup"><span data-stu-id="87909-114">Word containing the day of the month (1-31).</span></span>

</dd> <dt>

<span data-ttu-id="87909-115">**вхаур**</span><span class="sxs-lookup"><span data-stu-id="87909-115">**wHour**</span></span>
</dt> <dd>

<span data-ttu-id="87909-116">Слово, содержащее час (0-23).</span><span class="sxs-lookup"><span data-stu-id="87909-116">Word containing the hour (0-23).</span></span>

</dd> <dt>

<span data-ttu-id="87909-117">**вминуте**</span><span class="sxs-lookup"><span data-stu-id="87909-117">**wMinute**</span></span>
</dt> <dd>

<span data-ttu-id="87909-118">Слово, содержащее минуту (0-59).</span><span class="sxs-lookup"><span data-stu-id="87909-118">Word containing the minute (0-59).</span></span>

</dd> <dt>

<span data-ttu-id="87909-119">**всеконд**</span><span class="sxs-lookup"><span data-stu-id="87909-119">**wSecond**</span></span>
</dt> <dd>

<span data-ttu-id="87909-120">Слово, содержащее второе (0-59).</span><span class="sxs-lookup"><span data-stu-id="87909-120">Word containing the second (0-59).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87909-121">Требования</span><span class="sxs-lookup"><span data-stu-id="87909-121">Requirements</span></span>



| <span data-ttu-id="87909-122">Требование</span><span class="sxs-lookup"><span data-stu-id="87909-122">Requirement</span></span> | <span data-ttu-id="87909-123">Значение</span><span class="sxs-lookup"><span data-stu-id="87909-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="87909-124">Header</span><span class="sxs-lookup"><span data-stu-id="87909-124">Header</span></span><br/> | <dl> <span data-ttu-id="87909-125"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87909-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87909-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87909-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87909-127">**Имдспстораже:: GETDATE**</span><span class="sxs-lookup"><span data-stu-id="87909-127">**IMDSPStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[<span data-ttu-id="87909-128">**Ивмдмстораже:: GETDATE**</span><span class="sxs-lookup"><span data-stu-id="87909-128">**IWMDMStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[<span data-ttu-id="87909-129">**вмдмригхтс**</span><span class="sxs-lookup"><span data-stu-id="87909-129">**WMDMRIGHTS**</span></span>](wmdmrights.md)
</dt> <dt>

[<span data-ttu-id="87909-130">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="87909-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





