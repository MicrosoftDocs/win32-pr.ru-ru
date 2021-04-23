---
title: Перечисление MP_REMOVAL_REASON (Мпклиент. h)
description: Причина удаления подписи Фастпас.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON перечисления устаревшие функции среды Windows
- PMP_REMOVAL_REASON указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803539"
---
# <a name="mp_removal_reason-enumeration"></a><span data-ttu-id="239f7-105">\_Перечисление причин удаления пакета управления \_</span><span class="sxs-lookup"><span data-stu-id="239f7-105">MP\_REMOVAL\_REASON enumeration</span></span>

<span data-ttu-id="239f7-106">Причина удаления подписи Фастпас.</span><span class="sxs-lookup"><span data-stu-id="239f7-106">FastPath signature removal reason.</span></span>

## <a name="syntax"></a><span data-ttu-id="239f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="239f7-107">Syntax</span></span>


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a><span data-ttu-id="239f7-108">Константы</span><span class="sxs-lookup"><span data-stu-id="239f7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="239f7-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**Удаление пакета управления \_ \_ неизвестно**</span><span class="sxs-lookup"><span data-stu-id="239f7-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP\_REMOVAL\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="239f7-110">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="239f7-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="239f7-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**\_руководство по удалению пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="239f7-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP\_REMOVAL\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="239f7-112">Вручную.</span><span class="sxs-lookup"><span data-stu-id="239f7-112">Manual.</span></span>

</dd> <dt>

<span data-ttu-id="239f7-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**\_Автоматическое удаление пакета управления \_**</span><span class="sxs-lookup"><span data-stu-id="239f7-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**MP\_REMOVAL\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="239f7-114">Автоматический.</span><span class="sxs-lookup"><span data-stu-id="239f7-114">Automatic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="239f7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="239f7-115">Requirements</span></span>



| <span data-ttu-id="239f7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="239f7-116">Requirement</span></span> | <span data-ttu-id="239f7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="239f7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="239f7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="239f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="239f7-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="239f7-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="239f7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="239f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="239f7-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="239f7-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="239f7-122">Header</span><span class="sxs-lookup"><span data-stu-id="239f7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="239f7-123"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="239f7-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





