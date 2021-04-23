---
title: Структура MPSTATUS_DATAEX_UNUSED (Мпклиент. h)
description: Фиктивная структура для не-SRP.
ms.assetid: 396744CE-2435-4591-B0CF-A4392C88640F
keywords:
- MPSTATUS_DATAEX_UNUSED структуры устаревшие функции среды Windows
- Функции PMPSTATUS_DATAEX_UNUSED указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSTATUS_DATAEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfcbc987a97a8cc47501a24e633c5da2d776a42d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137642"
---
# <a name="mpstatus_dataex_unused-structure"></a><span data-ttu-id="d77be-105">МПСТАТУС \_ датаекс \_ неиспользуемая структура</span><span class="sxs-lookup"><span data-stu-id="d77be-105">MPSTATUS\_DATAEX\_UNUSED structure</span></span>

<span data-ttu-id="d77be-106">Фиктивная структура для не-SRP.</span><span class="sxs-lookup"><span data-stu-id="d77be-106">Dummy structure for non-SRP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d77be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d77be-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATAEX_UNUSED {
  DWORD dwNone;
} MPSTATUS_DATAEX_UNUSED, *PMPSTATUS_DATAEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="d77be-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d77be-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d77be-109">**двноне**</span><span class="sxs-lookup"><span data-stu-id="d77be-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="d77be-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d77be-110">Type: **DWORD**</span></span>

<span data-ttu-id="d77be-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d77be-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d77be-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d77be-112">Requirements</span></span>



| <span data-ttu-id="d77be-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d77be-113">Requirement</span></span> | <span data-ttu-id="d77be-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d77be-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d77be-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d77be-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d77be-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d77be-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d77be-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d77be-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d77be-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d77be-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d77be-119">Header</span><span class="sxs-lookup"><span data-stu-id="d77be-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d77be-120"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d77be-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





