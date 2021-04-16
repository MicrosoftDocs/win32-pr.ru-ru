---
description: В следующем списке описаны константы политики разрядов.
ms.assetid: a085709e-1c61-4ae2-832e-fda59479cef6
title: Константы политики разрядов (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 052d07a5fe538543b66ec8d48c940f63fe82a682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663126"
---
# <a name="discharge-policy-constants"></a><span data-ttu-id="75619-103">Константы политики разрядов</span><span class="sxs-lookup"><span data-stu-id="75619-103">Discharge Policy Constants</span></span>

<span data-ttu-id="75619-104">В следующем списке описаны константы политики разрядов.</span><span class="sxs-lookup"><span data-stu-id="75619-104">The following list describes the discharge policy constants.</span></span>



| <span data-ttu-id="75619-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="75619-105">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="75619-106">Описание</span><span class="sxs-lookup"><span data-stu-id="75619-106">Description</span></span>                                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISCHARGE_POLICY_CRITICAL"></span><span id="discharge_policy_critical"></span><dl> <span data-ttu-id="75619-107"><dt>**Разрядность \_ \_Критическая политика**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="75619-107"><dt>**DISCHARGE\_POLICY\_CRITICAL**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="75619-108">Параметр политики разрядности аккумулятора (структуры [**системного \_ \_ уровня питания**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) используется, когда зарядка батареи ниже критического порогового значения.</span><span class="sxs-lookup"><span data-stu-id="75619-108">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the critical threshold.</span></span><br/> |
| <span id="DISCHARGE_POLICY_LOW"></span><span id="discharge_policy_low"></span><dl> <span data-ttu-id="75619-109"><dt>**Разрядность \_ ПОЛИТИКА \_ Low**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="75619-109"><dt>**DISCHARGE\_POLICY\_LOW**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="75619-110">Параметр политики разрядности аккумулятора (структуры [**системного \_ \_ уровня питания**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ) используется, когда зарядка батареи ниже нижнего порогового значения.</span><span class="sxs-lookup"><span data-stu-id="75619-110">Which of the battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) is used when the battery discharges below the low threshold.</span></span><br/>      |
| <span id="NUM_DISCHARGE_POLICIES"></span><span id="num_discharge_policies"></span><dl> <span data-ttu-id="75619-111"><dt>**Число \_ \_Политики разрядов**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="75619-111"><dt>**NUM\_DISCHARGE\_POLICIES**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="75619-112">Число параметров политики разрядов аккумулятора ([**структур \_ системного \_ уровня питания**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) ).</span><span class="sxs-lookup"><span data-stu-id="75619-112">Number of battery discharge policy settings ([**SYSTEM\_POWER\_LEVEL**](/windows/desktop/api/WinNT/ns-winnt-system_power_level) structures) specified.</span></span><br/>                                                           |



## <a name="requirements"></a><span data-ttu-id="75619-113">Требования</span><span class="sxs-lookup"><span data-stu-id="75619-113">Requirements</span></span>



| <span data-ttu-id="75619-114">Требование</span><span class="sxs-lookup"><span data-stu-id="75619-114">Requirement</span></span> | <span data-ttu-id="75619-115">Значение</span><span class="sxs-lookup"><span data-stu-id="75619-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75619-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75619-116">Minimum supported client</span></span><br/> | <span data-ttu-id="75619-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="75619-117">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="75619-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75619-118">Minimum supported server</span></span><br/> | <span data-ttu-id="75619-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75619-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="75619-120">Header</span><span class="sxs-lookup"><span data-stu-id="75619-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="75619-121"><dt>Файл WinNT. h (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75619-121"><dt>WinNT.h (include Windows.h)</dt></span></span> </dl> |



 

 




