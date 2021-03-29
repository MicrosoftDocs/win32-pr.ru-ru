---
description: Перечисление ЕКСПЕРТСТАТУСЕНУМЕРАТИОН содержит значения состояния. Он используется элементом Status структуры ЕКСПЕРТСТАТУС и параметром status в Експертиндикатестатус.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Перечисление ЕКСПЕРТСТАТУСЕНУМЕРАТИОН (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662200"
---
# <a name="expertstatusenumeration-enumeration"></a><span data-ttu-id="293ea-104">Перечисление ЕКСПЕРТСТАТУСЕНУМЕРАТИОН</span><span class="sxs-lookup"><span data-stu-id="293ea-104">EXPERTSTATUSENUMERATION enumeration</span></span>

<span data-ttu-id="293ea-105">Перечисление **експертстатусенумератион** содержит значения состояния.</span><span class="sxs-lookup"><span data-stu-id="293ea-105">The **EXPERTSTATUSENUMERATION** enumeration contains status values.</span></span> <span data-ttu-id="293ea-106">Он используется элементом **Status** структуры [експертстатус](expertstatus.md) и параметром *Status* в [експертиндикатестатус](expertindicatestatus.md).</span><span class="sxs-lookup"><span data-stu-id="293ea-106">It is used by the **Status** member of [EXPERTSTATUS](expertstatus.md) structure and the *Status* parameter in [ExpertIndicateStatus](expertindicatestatus.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="293ea-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="293ea-107">Syntax</span></span>


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a><span data-ttu-id="293ea-108">Константы</span><span class="sxs-lookup"><span data-stu-id="293ea-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="293ea-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**ЕКСПЕРТСТАТУС \_ неактивен**</span><span class="sxs-lookup"><span data-stu-id="293ea-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="293ea-110">Эксперт никогда не начал работу.</span><span class="sxs-lookup"><span data-stu-id="293ea-110">The expert never started.</span></span>

</dd> <dt>

<span data-ttu-id="293ea-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**ЕКСПЕРТСТАТУС \_ Запуск**</span><span class="sxs-lookup"><span data-stu-id="293ea-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS\_STARTING**</span></span>
</dt> <dd>

<span data-ttu-id="293ea-112">Эксперт начинает работу.</span><span class="sxs-lookup"><span data-stu-id="293ea-112">The expert is starting.</span></span>

</dd> <dt>

<span data-ttu-id="293ea-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**ЕКСПЕРТСТАТУС \_ работает**</span><span class="sxs-lookup"><span data-stu-id="293ea-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="293ea-114">Эксперт работает нормально.</span><span class="sxs-lookup"><span data-stu-id="293ea-114">The expert is running normally.</span></span>

</dd> <dt>

<span data-ttu-id="293ea-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**\_проблема експертстатус**</span><span class="sxs-lookup"><span data-stu-id="293ea-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS\_PROBLEM**</span></span>
</dt> <dd>

<span data-ttu-id="293ea-116">Проблема, указанная в *подсостоянии* , прекратила работу эксперта.</span><span class="sxs-lookup"><span data-stu-id="293ea-116">A problem specified in *SubStatus* stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="293ea-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**ЕКСПЕРТСТАТУС \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="293ea-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="293ea-118">Сетевой монитор был остановлен эксперт.</span><span class="sxs-lookup"><span data-stu-id="293ea-118">Network Monitor stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="293ea-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**ЕКСПЕРТСТАТУС \_ Готово**</span><span class="sxs-lookup"><span data-stu-id="293ea-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS\_DONE**</span></span>
</dt> <dd>

<span data-ttu-id="293ea-120">Эксперт успешно завершил работу.</span><span class="sxs-lookup"><span data-stu-id="293ea-120">The expert finished successfully.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="293ea-121">Требования</span><span class="sxs-lookup"><span data-stu-id="293ea-121">Requirements</span></span>



| <span data-ttu-id="293ea-122">Требование</span><span class="sxs-lookup"><span data-stu-id="293ea-122">Requirement</span></span> | <span data-ttu-id="293ea-123">Значение</span><span class="sxs-lookup"><span data-stu-id="293ea-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="293ea-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="293ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="293ea-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="293ea-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="293ea-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="293ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="293ea-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="293ea-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="293ea-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="293ea-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="293ea-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="293ea-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




