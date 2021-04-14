---
description: Обновления, требующие взаимодействия с пользователем, не могут быть установлены приложениями Центр обновления Windows Agent (WUA), если приложения WUA выполняются в контексте службы вторичного входа в систему.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Использование агента WUA из процесса вторичного входа в систему (Запуск от имени)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692471"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a><span data-ttu-id="bfd80-103">Использование агента WUA из процесса вторичного входа в систему (Запуск от имени)</span><span class="sxs-lookup"><span data-stu-id="bfd80-103">Using WUA from a Secondary Logon (Run As) Process</span></span>

<span data-ttu-id="bfd80-104">Обновления, требующие взаимодействия с пользователем, не могут быть установлены приложениями Центр обновления Windows Agent (WUA), если приложения WUA выполняются в контексте службы вторичного входа в систему.</span><span class="sxs-lookup"><span data-stu-id="bfd80-104">Updates that require user interaction cannot be installed by Windows Update Agent (WUA) applications if the WUA applications are running in the context of the Secondary Logon service.</span></span>

<span data-ttu-id="bfd80-105">Если процесс, вызывающий WUA, выполняется в контексте службы запуска от имени или службы вторичного входа в систему, попытка установить обновление, требующее взаимодействия с пользователем, завершится неудачей и возвратит ошибку **Wu \_ E \_ без \_ интерактивного \_ пользователя** .</span><span class="sxs-lookup"><span data-stu-id="bfd80-105">If the process that is calling WUA is running in the context of the RunAs service or the Secondary Logon service, an attempt to install an update that requires user interaction fails and returns the **WU\_E\_NO\_INTERACTIVE\_USER** error.</span></span>

<span data-ttu-id="bfd80-106">В Microsoft Windows программы можно запускать от имени пользователя, который отличается от пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="bfd80-106">In Microsoft Windows, you can run programs as a user who differs from the user who is currently logged on.</span></span> <span data-ttu-id="bfd80-107">Для этого необходимо запустить службу вторичного входа в систему.</span><span class="sxs-lookup"><span data-stu-id="bfd80-107">To do this the Secondary Logon service must be running.</span></span>

 

 



