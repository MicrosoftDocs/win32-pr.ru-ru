---
title: Перечисление Свармстатус (Deliveryoptimization. h)
description: Определяет состояние файла в рамках клиента оптимизации доставки.
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- Перечисление Свармстатус
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136991"
---
# <a name="swarmstatus-enumeration"></a><span data-ttu-id="6d05a-104">Перечисление Свармстатус</span><span class="sxs-lookup"><span data-stu-id="6d05a-104">SwarmStatus enumeration</span></span>

<span data-ttu-id="6d05a-105">Определяет состояние файла в рамках клиента оптимизации доставки.</span><span class="sxs-lookup"><span data-stu-id="6d05a-105">Defines the status of a file within the delivery optimization client.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d05a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d05a-106">Syntax</span></span>


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a><span data-ttu-id="6d05a-107">Константы</span><span class="sxs-lookup"><span data-stu-id="6d05a-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6d05a-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span><span class="sxs-lookup"><span data-stu-id="6d05a-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span></span>
</dt> <dd>

<span data-ttu-id="6d05a-109">Файл скачивается.</span><span class="sxs-lookup"><span data-stu-id="6d05a-109">The file is downloading.</span></span>

</dd> <dt>

<span data-ttu-id="6d05a-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span><span class="sxs-lookup"><span data-stu-id="6d05a-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span></span>
</dt> <dd>

<span data-ttu-id="6d05a-111">Загрузка файла завершена.</span><span class="sxs-lookup"><span data-stu-id="6d05a-111">The file download is complete.</span></span>

</dd> <dt>

<span data-ttu-id="6d05a-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span><span class="sxs-lookup"><span data-stu-id="6d05a-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span></span>
</dt> <dd>

<span data-ttu-id="6d05a-113">Файл кэшируется.</span><span class="sxs-lookup"><span data-stu-id="6d05a-113">The file is being cached.</span></span>

</dd> <dt>

<span data-ttu-id="6d05a-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span><span class="sxs-lookup"><span data-stu-id="6d05a-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="6d05a-115">Скачивание файла приостановлено.</span><span class="sxs-lookup"><span data-stu-id="6d05a-115">The file download is paused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d05a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6d05a-116">Requirements</span></span>



| <span data-ttu-id="6d05a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6d05a-117">Requirement</span></span> | <span data-ttu-id="6d05a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6d05a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d05a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d05a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d05a-120">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6d05a-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6d05a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d05a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d05a-122">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6d05a-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d05a-123">Header</span><span class="sxs-lookup"><span data-stu-id="6d05a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d05a-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d05a-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





