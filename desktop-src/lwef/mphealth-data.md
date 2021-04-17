---
title: Структура MPHEALTH_DATA (Мпклиент. h)
description: Данные уведомления о работоспособности.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA структуры устаревшие функции среды Windows
- Функции PMPHEALTH_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701089"
---
# <a name="mphealth_data-structure"></a><span data-ttu-id="ac809-105">\_Структура данных мфеалс</span><span class="sxs-lookup"><span data-stu-id="ac809-105">MPHEALTH\_DATA structure</span></span>

<span data-ttu-id="ac809-106">Данные уведомления о работоспособности.</span><span class="sxs-lookup"><span data-stu-id="ac809-106">Health notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac809-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac809-107">Syntax</span></span>


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a><span data-ttu-id="ac809-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ac809-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac809-109">**двнотификатионтипе**</span><span class="sxs-lookup"><span data-stu-id="ac809-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="ac809-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ac809-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ac809-111">Тип уведомления.</span><span class="sxs-lookup"><span data-stu-id="ac809-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="ac809-112">**двнотификатионфлаг**</span><span class="sxs-lookup"><span data-stu-id="ac809-112">**dwNotificationFlag**</span></span>
</dt> <dd>

<span data-ttu-id="ac809-113">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ac809-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ac809-114">Не используется.</span><span class="sxs-lookup"><span data-stu-id="ac809-114">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac809-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ac809-115">Requirements</span></span>



| <span data-ttu-id="ac809-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ac809-116">Requirement</span></span> | <span data-ttu-id="ac809-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ac809-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac809-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac809-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac809-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ac809-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ac809-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac809-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac809-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ac809-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac809-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac809-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac809-123"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac809-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





