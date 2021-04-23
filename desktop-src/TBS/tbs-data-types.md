---
title: Типы данных TBS (TBS. h)
description: TBS определяет следующие типы данных.
ms.assetid: c8de883f-9450-47e2-a352-b6f6b1f8e423
keywords:
- TBS_HCONTEXT
- TBS_COMMAND_PRIORITY
- TBS_COMMAND_LOCALITY
- TBS_OWNERAUTH_TYPE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b6ee71287ee377e5ea301e92636f47d0bd80bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415577"
---
# <a name="tbs-data-types"></a><span data-ttu-id="c2eb6-107">Типы данных TBS</span><span class="sxs-lookup"><span data-stu-id="c2eb6-107">TBS Data Types</span></span>

<span data-ttu-id="c2eb6-108">TBS определяет следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="c2eb6-108">TBS defines the following data types.</span></span>



| <span data-ttu-id="c2eb6-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c2eb6-109">Data type</span></span>                                                                                                | <span data-ttu-id="c2eb6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c2eb6-110">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2eb6-111"><span id="TBS_HCONTEXT"></span><span id="tbs_hcontext"></span>**TBS \_ хконтекст**</span><span class="sxs-lookup"><span data-stu-id="c2eb6-111"><span id="TBS_HCONTEXT"></span><span id="tbs_hcontext"></span>**TBS\_HCONTEXT**</span></span>                          | <span data-ttu-id="c2eb6-112">Обработчик объекта контекста.</span><span class="sxs-lookup"><span data-stu-id="c2eb6-112">Context object handle.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="c2eb6-113"><span id="TBS_COMMAND_PRIORITY"></span><span id="tbs_command_priority"></span>**\_приоритет команды \_ TBS**</span><span class="sxs-lookup"><span data-stu-id="c2eb6-113"><span id="TBS_COMMAND_PRIORITY"></span><span id="tbs_command_priority"></span>**TBS\_COMMAND\_PRIORITY**</span></span> | <span data-ttu-id="c2eb6-114">Приоритет, связанный с командами.</span><span class="sxs-lookup"><span data-stu-id="c2eb6-114">Priority associated with commands.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="c2eb6-115"><span id="TBS_COMMAND_LOCALITY"></span><span id="tbs_command_locality"></span>**\_ \_ Локализация команд TBS**</span><span class="sxs-lookup"><span data-stu-id="c2eb6-115"><span id="TBS_COMMAND_LOCALITY"></span><span id="tbs_command_locality"></span>**TBS\_COMMAND\_LOCALITY**</span></span> | <span data-ttu-id="c2eb6-116">Локальность, из которой отправляется команда.</span><span class="sxs-lookup"><span data-stu-id="c2eb6-116">The locality that the command is submitted from.</span></span><br/>                                                                                                            |
| <span data-ttu-id="c2eb6-117"><span id="TBS_OWNERAUTH_TYPE"></span><span id="tbs_ownerauth_type"></span>**\_тип ОВНЕРАУС \_ TBS**</span><span class="sxs-lookup"><span data-stu-id="c2eb6-117"><span id="TBS_OWNERAUTH_TYPE"></span><span id="tbs_ownerauth_type"></span>**TBS\_OWNERAUTH\_TYPE**</span></span>       | <span data-ttu-id="c2eb6-118">Тип проверки подлинности владельца.</span><span class="sxs-lookup"><span data-stu-id="c2eb6-118">The type of owner authentication.</span></span><br/> <span data-ttu-id="c2eb6-119">**Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** Этот тип данных недоступен.</span><span class="sxs-lookup"><span data-stu-id="c2eb6-119">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This data type is not available.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c2eb6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c2eb6-120">Requirements</span></span>



| <span data-ttu-id="c2eb6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c2eb6-121">Requirement</span></span> | <span data-ttu-id="c2eb6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c2eb6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c2eb6-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2eb6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c2eb6-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2eb6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2eb6-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2eb6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c2eb6-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2eb6-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2eb6-127">Header</span><span class="sxs-lookup"><span data-stu-id="c2eb6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2eb6-128"><dt>TBS. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2eb6-128"><dt>Tbs.h</dt></span></span> </dl> |



 

 





