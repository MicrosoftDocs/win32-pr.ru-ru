---
description: Константы глобальных флагов используются для включения или отключения параметров политики управления питанием пользователей.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Константы глобальных флагов (Поврпроф. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663120"
---
# <a name="global-flags-constants"></a><span data-ttu-id="8a7f8-103">Константы глобальных флагов</span><span class="sxs-lookup"><span data-stu-id="8a7f8-103">Global Flags Constants</span></span>

<span data-ttu-id="8a7f8-104">Константы глобальных флагов используются для включения или отключения параметров политики управления питанием пользователей.</span><span class="sxs-lookup"><span data-stu-id="8a7f8-104">The global flags constants are used to enable or disable user power policy options.</span></span>



| <span data-ttu-id="8a7f8-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="8a7f8-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="8a7f8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8a7f8-106">Description</span></span>                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <span data-ttu-id="8a7f8-107"><dt>**Енаблемултибаттеридисплай**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="8a7f8-107"><dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="8a7f8-108">Включает или отключает отображение нескольких батарей в системном индикаторе питания.</span><span class="sxs-lookup"><span data-stu-id="8a7f8-108">Enables or disables multiple battery display in the system Power Meter.</span></span><br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <span data-ttu-id="8a7f8-109"><dt>**Енаблепассвордлогон**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="8a7f8-109"><dt>**EnablePasswordLogon**</dt> <dt>0x04</dt></span></span> </dl>                         | <span data-ttu-id="8a7f8-110">Включает или отключает обязательное вход в систему при выходе из режима ожидания или перехода в режим гибернации.</span><span class="sxs-lookup"><span data-stu-id="8a7f8-110">Enables or disables requiring password logon when the system resumes from standby or hibernate.</span></span><br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <span data-ttu-id="8a7f8-111"><dt>**Енаблесистрайбаттериметер**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="8a7f8-111"><dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="8a7f8-112">Включает или отключает значок индикатора батареи в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8a7f8-112">Enables or disables the battery meter icon in the system tray.</span></span> <span data-ttu-id="8a7f8-113">Если этот флажок не установлен, значок счетчика аккумулятора не отображается.</span><span class="sxs-lookup"><span data-stu-id="8a7f8-113">When this flag is cleared, the battery meter icon is not displayed.</span></span><br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <span data-ttu-id="8a7f8-114"><dt>**Енаблевидеодимдисплай**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="8a7f8-114"><dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt></span></span> </dl>                 | <span data-ttu-id="8a7f8-115">Включает или отключает поддержку затемнения экрана видео, когда система работает от сети переменного тока на питание от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="8a7f8-115">Enables or disables support for dimming the video display when the system changes from running on AC power to running on battery power.</span></span><br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <span data-ttu-id="8a7f8-116"><dt>**Енаблевакеонринг**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="8a7f8-116"><dt>**EnableWakeOnRing**</dt> <dt>0x08</dt></span></span> </dl>                                     | <span data-ttu-id="8a7f8-117">Включает или отключает поддержку пробуждения по звонку.</span><span class="sxs-lookup"><span data-stu-id="8a7f8-117">Enables or disables wake on ring support.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="8a7f8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8a7f8-118">Requirements</span></span>



| <span data-ttu-id="8a7f8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8a7f8-119">Requirement</span></span> | <span data-ttu-id="8a7f8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8a7f8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7f8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a7f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a7f8-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8a7f8-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8a7f8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a7f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a7f8-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a7f8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a7f8-125">Header</span><span class="sxs-lookup"><span data-stu-id="8a7f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a7f8-126"><dt>Поврпроф. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a7f8-126"><dt>PowrProf.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a7f8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a7f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a7f8-128">**Глобальная \_ \_ Политика управления питанием пользователей \_**</span><span class="sxs-lookup"><span data-stu-id="8a7f8-128">**GLOBAL\_USER\_POWER\_POLICY**</span></span>](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




