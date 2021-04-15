---
description: 'Чтобы объявить приложение для установки на уровне пользователя, если для установки приложения требуются повышенные привилегии (то есть система), следуйте указаниям в следующем списке:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Объявление приложения Per-User для установки с повышенными привилегиями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662954"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a><span data-ttu-id="2cfa5-103">Объявление приложения Per-User для установки с повышенными привилегиями</span><span class="sxs-lookup"><span data-stu-id="2cfa5-103">Advertising a Per-User Application To Be Installed with Elevated Privileges</span></span>

<span data-ttu-id="2cfa5-104">Чтобы объявить приложение для установки на уровне пользователя, если для установки приложения требуются повышенные привилегии (то есть система), следуйте указаниям в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="2cfa5-104">To advertise an application on a per-user installation basis when the application requires elevated (that is, system) privileges for installation, use the guidelines in the following list:</span></span>

-   <span data-ttu-id="2cfa5-105">Процесс должен быть службой, работающей под системной учетной записью LocalSystem в Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2cfa5-105">Your process must be a service that runs under the LocalSystem system account on Windows XP or later.</span></span>
-   <span data-ttu-id="2cfa5-106">Создайте скрипт объявления, вызвав [**мсиадвертисепродукт**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) или [**мсиадвертисепродуктекс**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span><span class="sxs-lookup"><span data-stu-id="2cfa5-106">Generate an advertise script by calling [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) or [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa).</span></span>
-   <span data-ttu-id="2cfa5-107">Процесс должен олицетворять пользователя, который является целью объявления.</span><span class="sxs-lookup"><span data-stu-id="2cfa5-107">Your process must impersonate the user that is the target for the advertisement.</span></span>
-   <span data-ttu-id="2cfa5-108">Вызовите [**мсиадвертисескрипт**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)и используйте \_ \| \_ ярлыки скриптфлагс качеинфо скриптфлагс регдата \_ APPINFO \| скриптфлагс \_ регдата \_ кнфгинфо \| SCRIPTFLAGS \_ .</span><span class="sxs-lookup"><span data-stu-id="2cfa5-108">Call [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta), and use the flags SCRIPTFLAGS\_CACHEINFO \| SCRIPTFLAGS\_REGDATA\_APPINFO \| SCRIPTFLAGS\_REGDATA\_CNFGINFO \| SCRIPTFLAGS\_SHORTCUTS.</span></span>

<span data-ttu-id="2cfa5-109">При выполнении рекомендаций вы объявляете приложение для указанного пользователя, и когда пользователь выбирает установку, приложение устанавливается с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="2cfa5-109">When you follow the guidelines, you advertise an application to a specified user, and when the user chooses to install, the application is installed with elevated privileges.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cfa5-110">См. также</span><span class="sxs-lookup"><span data-stu-id="2cfa5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cfa5-111">Исправление управляемых пользователем приложений</span><span class="sxs-lookup"><span data-stu-id="2cfa5-111">Patching Per-User Managed Applications</span></span>](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



