---
description: Поставщик пространства имен PNRP (NSP) — это бессерверная технология разрешения имен, позволяющая узлам обнаруживать друг друга.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Об PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156547"
---
# <a name="about-pnrp"></a><span data-ttu-id="028b2-103">Об PNRP</span><span class="sxs-lookup"><span data-stu-id="028b2-103">About PNRP</span></span>

<span data-ttu-id="028b2-104">Поставщик пространства имен PNRP (NSP) — это бессерверная технология разрешения имен, позволяющая узлам обнаруживать друг друга.</span><span class="sxs-lookup"><span data-stu-id="028b2-104">The Peer Name Resolution Protocol (PNRP) Namespace Provider (NSP) is a serverless name resolution technology that allows nodes to discover each other.</span></span> <span data-ttu-id="028b2-105">PNRP использует API поставщика пространства имен Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="028b2-105">PNRP uses the Winsock 2 Namespace Provider API.</span></span>

<span data-ttu-id="028b2-106">Поддержка IPv6 необходима для PNRP и является единственным Интернет-протоколом, встроенным в API.</span><span class="sxs-lookup"><span data-stu-id="028b2-106">IPv6 support is required by PNRP and is the only Internet Protocol native to the API.</span></span> <span data-ttu-id="028b2-107">Однако протокол PNRP может разрешать IPv4-адреса через технологии туннелирования 6to4 или [Teredo](/windows/desktop/Teredo/portal) .</span><span class="sxs-lookup"><span data-stu-id="028b2-107">However, PNRP can resolve IPv4 addresses via the 6to4 or [Teredo](/windows/desktop/Teredo/portal) transition technologies.</span></span> <span data-ttu-id="028b2-108">Пользователи Windows XP с пакетом обновления 1 (SP1) должны загрузить [Расширенный сетевой пакет](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) , чтобы включить поддержку IPv6, НЕОБХОДИМУЮ для PNRP.</span><span class="sxs-lookup"><span data-stu-id="028b2-108">Windows XP with Service Pack 1 (SP1) users must download the [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) to enable the IPv6 support required by PNRP.</span></span>

> [!Note]  
> <span data-ttu-id="028b2-109">Приложениям, использующим PNRP в среде с брандмауэром, требуются группы исключений, охватывающие порт, характерный для приложения, а также порт "3540-UDP" для PNRP.</span><span class="sxs-lookup"><span data-stu-id="028b2-109">Applications using PNRP in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="028b2-110">Эти группы исключений должны быть включены при каждом запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="028b2-110">These exception groups should be enabled whenever the application is running.</span></span>

 

<span data-ttu-id="028b2-111">Хотя протокол PNRP 2,0 является собственным для платформ Windows Vista и Windows Server 2008, пользователям Windows XP необходимо загрузить Центр обновления Windows [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) для обновления до PNRP 2,0.</span><span class="sxs-lookup"><span data-stu-id="028b2-111">While PNRP 2.0 is native to the Windows Vista and Windows Server 2008 platforms, Windows XP users must download Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) to upgrade to PNRP 2.0.</span></span>

 

 
