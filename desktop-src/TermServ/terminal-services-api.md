---
title: службы удаленных рабочих столов API
description: Службы удаленных рабочих столов API в основном используется для клиентских и серверных приложений и приложений для службы удаленных рабочих столов администрирования.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888136"
---
# <a name="remote-desktop-services-api"></a><span data-ttu-id="fb726-103">службы удаленных рабочих столов API</span><span class="sxs-lookup"><span data-stu-id="fb726-103">Remote Desktop Services API</span></span>

<span data-ttu-id="fb726-104">Большинство приложений выполняются без изменения в службы удаленных рабочих столов (ранее назывались службами терминалов) и не требуют использования службы удаленных рабочих столов API.</span><span class="sxs-lookup"><span data-stu-id="fb726-104">Most applications run without modification in a Remote Desktop Services (formerly known as Terminal Services) environment and do not need to use the Remote Desktop Services API.</span></span> <span data-ttu-id="fb726-105">Службы удаленных рабочих столов API в основном используется для клиентских и серверных приложений и приложений для службы удаленных рабочих столов администрирования.</span><span class="sxs-lookup"><span data-stu-id="fb726-105">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

<span data-ttu-id="fb726-106">Службы удаленных рабочих столов API — это набор вызовов функций в Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="fb726-106">The Remote Desktop Services API is a set of function calls into Wtsapi32.dll.</span></span> <span data-ttu-id="fb726-107">Чтобы разработать приложение для работы как в службы удаленных рабочих столов, так и в неслужбы удаленных рабочих столовных средах, используйте динамическую компоновку во время выполнения, чтобы проверить наличие Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="fb726-107">To design your application to run in both Remote Desktop Services and non-Remote Desktop Services environments, use run-time dynamic linking to check for the presence of Wtsapi32.dll.</span></span> <span data-ttu-id="fb726-108">Дополнительные сведения см. [в разделе Связывание во время выполнения с Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="fb726-108">For more information, see [Run-Time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="fb726-109">Службы удаленных рабочих столов API позволяет приложениям выполнять следующие задачи в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="fb726-109">The Remote Desktop Services API enables applications to perform the following tasks in a Remote Desktop Services environment:</span></span>

-   <span data-ttu-id="fb726-110">[Службы удаленных рабочих столов администрирование](terminal-services-administration.md), например перечисление и удаленный рабочий стол Управление серверами узла сеансов удаленных рабочих столов (которые ранее назывались серверами терминалов) в домене или перечисление и управление сеансами и процессами на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="fb726-110">[Remote Desktop Services Administration](terminal-services-administration.md), such as enumerating and managing Remote Desktop Session Host (RD Session Host) servers (formerly known as terminal servers) in a domain or enumerating and managing sessions and processes on an RD Session Host server.</span></span>
-   <span data-ttu-id="fb726-111">Усовершенствование клиентских и серверных приложений в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="fb726-111">Enhancing client/server applications in a Remote Desktop Services environment.</span></span>
-   <span data-ttu-id="fb726-112">Использование [службы удаленных рабочих столов виртуальных каналов](terminal-services-virtual-channels.md) для взаимодействия между клиентскими и серверными модулями приложения.</span><span class="sxs-lookup"><span data-stu-id="fb726-112">Using [Remote Desktop Services Virtual Channels](terminal-services-virtual-channels.md) to communicate between client and server modules of an application.</span></span>
-   <span data-ttu-id="fb726-113">[Установка и получение службы удаленных рабочих столов сведений о пользовательской конфигурации](terminal-services-user-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="fb726-113">[Setting and retrieving Remote Desktop Services specific user configuration information](terminal-services-user-configuration.md).</span></span>

 

 




