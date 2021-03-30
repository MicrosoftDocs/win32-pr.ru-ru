---
title: Структура MPTHREAT_INFOEX_UNUSED (Мпклиент. h)
description: Фиктивная структура для угроз типа изменения без поведения.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED структуры устаревшие функции среды Windows
- Функции PMPTHREAT_INFOEX_UNUSED указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136470"
---
# <a name="mpthreat_infoex_unused-structure"></a><span data-ttu-id="f4111-105">МПСРЕАТ \_ инфоекс \_ неиспользуемая структура</span><span class="sxs-lookup"><span data-stu-id="f4111-105">MPTHREAT\_INFOEX\_UNUSED structure</span></span>

<span data-ttu-id="f4111-106">Фиктивная структура для угроз типа изменения без поведения.</span><span class="sxs-lookup"><span data-stu-id="f4111-106">Dummy structure for non-behavior modification type threats.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4111-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4111-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="f4111-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f4111-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4111-109">**двноне**</span><span class="sxs-lookup"><span data-stu-id="f4111-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="f4111-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f4111-110">Type: **DWORD**</span></span>

<span data-ttu-id="f4111-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f4111-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f4111-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f4111-112">Requirements</span></span>



| <span data-ttu-id="f4111-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f4111-113">Requirement</span></span> | <span data-ttu-id="f4111-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f4111-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4111-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4111-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f4111-116">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f4111-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f4111-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4111-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f4111-118">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f4111-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4111-119">Header</span><span class="sxs-lookup"><span data-stu-id="f4111-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4111-120"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4111-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





