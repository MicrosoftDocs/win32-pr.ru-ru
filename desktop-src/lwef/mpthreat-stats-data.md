---
title: Структура MPTHREAT_STATS_DATA (Мпклиент. h)
description: Дополнительные данные статистики угроз.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- MPTHREAT_STATS_DATA структуры устаревшие функции среды Windows
- Функции PMPTHREAT_STATS_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135794"
---
# <a name="mpthreat_stats_data-structure"></a><span data-ttu-id="da072-105">\_ \_ Структура данных статистики мпсреат</span><span class="sxs-lookup"><span data-stu-id="da072-105">MPTHREAT\_STATS\_DATA structure</span></span>

<span data-ttu-id="da072-106">Дополнительные данные статистики угроз.</span><span class="sxs-lookup"><span data-stu-id="da072-106">Additional threat statistics data.</span></span>

## <a name="syntax"></a><span data-ttu-id="da072-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da072-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a><span data-ttu-id="da072-108">Члены</span><span class="sxs-lookup"><span data-stu-id="da072-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="da072-109">**двсреаткаунт**</span><span class="sxs-lookup"><span data-stu-id="da072-109">**dwThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="da072-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="da072-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="da072-111">Число угроз.</span><span class="sxs-lookup"><span data-stu-id="da072-111">Number of threats.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da072-112">Требования</span><span class="sxs-lookup"><span data-stu-id="da072-112">Requirements</span></span>



| <span data-ttu-id="da072-113">Требование</span><span class="sxs-lookup"><span data-stu-id="da072-113">Requirement</span></span> | <span data-ttu-id="da072-114">Значение</span><span class="sxs-lookup"><span data-stu-id="da072-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da072-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da072-115">Minimum supported client</span></span><br/> | <span data-ttu-id="da072-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="da072-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="da072-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da072-117">Minimum supported server</span></span><br/> | <span data-ttu-id="da072-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="da072-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da072-119">Header</span><span class="sxs-lookup"><span data-stu-id="da072-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="da072-120"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="da072-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





