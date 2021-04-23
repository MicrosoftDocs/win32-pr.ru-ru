---
title: Архитектура диспетчера списка сетей
description: Архитектура диспетчера списка сетей
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986833"
---
# <a name="network-list-manager-architecture"></a><span data-ttu-id="06fed-103">Архитектура диспетчера списка сетей</span><span class="sxs-lookup"><span data-stu-id="06fed-103">Network List Manager Architecture</span></span>

<span data-ttu-id="06fed-104">Диспетчер списка сетей запускается как служба в контексте Svchost.exe и запускается во время процедуры загрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="06fed-104">Network List Manager runs as a service in the context of Svchost.exe and is started during the computer boot procedure.</span></span> <span data-ttu-id="06fed-105">Служба диспетчера списков сетей поддерживает таблицу доступных сетей и сетевых атрибутов, получаемых приложениями через API диспетчера списка сетей.</span><span class="sxs-lookup"><span data-stu-id="06fed-105">The Network List Manager service maintains a table of available networks and network attributes that are retrieved by applications through the Network List Manager API.</span></span> <span data-ttu-id="06fed-106">Диспетчер списков сетей предоставляет основные функции для фильтрации и запроса службы диспетчера списков сетей для конкретных сетей и получения атрибутов этих сетей.</span><span class="sxs-lookup"><span data-stu-id="06fed-106">Network List Manager provides basic functions to filter and query the Network List Manager service for specific networks and retrieve the attributes of these networks.</span></span> <span data-ttu-id="06fed-107">На следующей схеме показана архитектура диспетчера списка сетей и взаимодействие между службой диспетчера списка сетей и клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="06fed-107">The following diagram shows the Network List Manager architecture and the interaction between the Network List Manager service and the client application.</span></span>

![Схема архитектуры сетевой осведомленности](images/architecture.png)

 

 




