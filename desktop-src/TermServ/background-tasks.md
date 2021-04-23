---
title: Рекомендации для фоновых задач в службы удаленных рабочих столов
description: Чтобы обеспечить максимальную доступность ЦП для всех пользователей, отключите фоновые задачи при работе в среде службы удаленных рабочих столов или создайте эффективные фоновые задачи, которые не требуют больших ресурсов.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681410"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a><span data-ttu-id="5f76f-103">Рекомендации для фоновых задач в службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="5f76f-103">Guidelines for background tasks in Remote Desktop Services</span></span>

<span data-ttu-id="5f76f-104">Фоновые задачи — задачи, выполняемые при простое цикла обработки сообщений приложения, предоставляют механизм для обработки задач с низким приоритетом в однопользовательском окружении.</span><span class="sxs-lookup"><span data-stu-id="5f76f-104">Background tasks—tasks performed when an application's message loop is idle—provide a mechanism for handling low-priority tasks in a single-user environment.</span></span> <span data-ttu-id="5f76f-105">Однако в службы удаленных рабочих столов среде фоновая задача одного пользователя конкурирует за циклы ЦП с задачами переднего плана другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="5f76f-105">In a Remote Desktop Services environment, however, one user's background task competes for CPU cycles with another user's foreground tasks.</span></span> <span data-ttu-id="5f76f-106">Когда несколько пользователей работают как в фоновом режиме, так и на фоне, требования к ЦП значительно выше, чем когда все пользователи запускают только задачи переднего плана.</span><span class="sxs-lookup"><span data-stu-id="5f76f-106">When multiple users are running both foreground and background tasks, the CPU demands are much higher than when all users are running only foreground tasks.</span></span> <span data-ttu-id="5f76f-107">Чтобы обеспечить максимальную доступность ЦП для всех пользователей, отключите фоновые задачи при работе в среде службы удаленных рабочих столов или создайте эффективные фоновые задачи, которые не требуют больших ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f76f-107">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

<span data-ttu-id="5f76f-108">Дополнительные сведения см. [в разделе Обнаружение среды службы удаленных рабочих столов](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5f76f-108">For more information, see [Detecting the Remote Desktop Services environment](detecting-the-terminal-services-environment.md).</span></span> <span data-ttu-id="5f76f-109">После обнаружения среды службы удаленных рабочих столов можно отключить или перенастроить фоновые задачи для приложения, используя тот же набор API-интерфейсов, который использовался для управления задачами.</span><span class="sxs-lookup"><span data-stu-id="5f76f-109">After you detect the Remote Desktop Services environment, you can disable or reconfigure background tasks for the application using the same set of APIs that you used to manage the tasks.</span></span>

 

 




