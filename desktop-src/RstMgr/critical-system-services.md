---
title: Критические системные службы
description: Критические системные службы не могут быть остановлены и перезапущены диспетчером перезапуска без перезагрузки системы. Для обновления любого файла или ресурса, используемого одной из этих служб, требуется перезагрузка системы.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8a50eca43a62d24e0ab6363844bef7457aaf05b34251f5d804dacabaead5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010233"
---
# <a name="critical-system-services"></a>Критические системные службы

Критические системные службы не могут быть остановлены и перезапущены диспетчером перезапуска без перезагрузки системы. Для обновления любого файла или ресурса, используемого одной из этих служб, требуется перезагрузка системы.

**, Чтобы определить, является ли процесс критической системной службой.**

1.  Зарегистрируйте процесс с помощью функции [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) .
2.  Вызовите функцию [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) , чтобы получить [**структуру \_ \_ сведений о процессе RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) .
3.  Член **ApplicationType** возвращенной структуры [**\_ \_ сведений о процессе RM**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) содержит значение перечисления [**\_ \_ типа приложения RM**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) . Это значение задается равным **рмкритиЦиал** для критического системного процесса.

К критическим системным службам относятся smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe с помощью вызовов RPC и svchost.exe с DCOM/PnP.

 

 




