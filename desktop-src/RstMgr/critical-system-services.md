---
title: Критические системные службы
description: Критические системные службы не могут быть остановлены и перезапущены диспетчером перезапуска без перезагрузки системы. Для обновления любого файла или ресурса, используемого одной из этих служб, требуется перезагрузка системы.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068667"
---
# <a name="critical-system-services"></a><span data-ttu-id="f7897-104">Критические системные службы</span><span class="sxs-lookup"><span data-stu-id="f7897-104">Critical System Services</span></span>

<span data-ttu-id="f7897-105">Критические системные службы не могут быть остановлены и перезапущены диспетчером перезапуска без перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="f7897-105">Critical system services cannot be stopped and restarted by the Restart Manager without a system restart.</span></span> <span data-ttu-id="f7897-106">Для обновления любого файла или ресурса, используемого одной из этих служб, требуется перезагрузка системы.</span><span class="sxs-lookup"><span data-stu-id="f7897-106">Updates to any file or resource in use by one of these services requires a system restart.</span></span>

<span data-ttu-id="f7897-107">**, Чтобы определить, является ли процесс критической системной службой.**</span><span class="sxs-lookup"><span data-stu-id="f7897-107">**To determine whether a process is a critical system service.**</span></span>

1.  <span data-ttu-id="f7897-108">Зарегистрируйте процесс с помощью функции [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .</span><span class="sxs-lookup"><span data-stu-id="f7897-108">Register the process using the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function.</span></span>
2.  <span data-ttu-id="f7897-109">Вызовите функцию [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) , чтобы получить [**структуру \_ \_ сведений о процессе RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .</span><span class="sxs-lookup"><span data-stu-id="f7897-109">Call the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to get the [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure.</span></span>
3.  <span data-ttu-id="f7897-110">Член **ApplicationType** возвращенной структуры [**\_ \_ сведений о процессе RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) содержит значение перечисления [**\_ \_ типа приложения RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) .</span><span class="sxs-lookup"><span data-stu-id="f7897-110">The **ApplicationType** member of the returned [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structure contains a [**RM\_APP\_TYPE**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) enumeration value.</span></span> <span data-ttu-id="f7897-111">Это значение задается равным **рмкритиЦиал** для критического системного процесса.</span><span class="sxs-lookup"><span data-stu-id="f7897-111">This value is set to **RmCriticial** for a critical system process.</span></span>

<span data-ttu-id="f7897-112">К критическим системным службам относятся smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe с помощью вызовов RPC и svchost.exe с DCOM/PnP.</span><span class="sxs-lookup"><span data-stu-id="f7897-112">Critical system services include smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe with RPCSS, and svchost.exe with Dcom/PnP.</span></span>

 

 




