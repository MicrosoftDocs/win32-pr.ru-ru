---
title: Роль диспетчера списка сетей
description: Роль диспетчера списка сетей
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889176"
---
# <a name="the-role-of-network-list-manager"></a><span data-ttu-id="2b76d-103">Роль диспетчера списка сетей</span><span class="sxs-lookup"><span data-stu-id="2b76d-103">The Role of Network List Manager</span></span>

<span data-ttu-id="2b76d-104">До Windows XP и Windows Server 2003 для получения данных о сетевых атрибутах, таких как IP-адрес, контроллер домена или служба доменных имен (DNS), приложениям требовалось вызывать ряд несвязанных интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="2b76d-104">Prior to Windows XP and Windows Server 2003, applications were required to call a number of unrelated APIs to obtain data about network attributes such as the IP address, the domain controller, or the Domain Name System (DNS).</span></span> <span data-ttu-id="2b76d-105">Начиная с Windows XP и Windows Server 2003, в интерфейсе API Winsock, осведомленном о сетевом расположении, указан ограниченный набор функций сетевого расположения.</span><span class="sxs-lookup"><span data-stu-id="2b76d-105">Starting with Windows XP and Windows Server 2003, the Network Location Awareness Winsock API featured a limited set of network location functionality.</span></span> <span data-ttu-id="2b76d-106">В Windows Server 2008 и Windows Vista служба осведомленности сети захватывает сетевые атрибуты в одном расположении и позволяет приложениям запрашивать и получать определенные сети и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="2b76d-106">In Windows Server 2008 and Windows Vista, the Network Awareness service captures the network attributes in one location and allows applications to query and retrieve specific networks and attributes.</span></span> <span data-ttu-id="2b76d-107">Диспетчер списка сетей заменяет функциональные возможности предыдущего API Winsock (доступного в качестве поставщика пространства имен Winsock), сохраняя совместимость с более старыми приложениями с помощью API Winsock.</span><span class="sxs-lookup"><span data-stu-id="2b76d-107">Network List Manager replaces the functionality of the previous Winsock API (available as a Winsock Name Space Provider) while maintaining compatibility with older applications using the Winsock API.</span></span>

 

 




