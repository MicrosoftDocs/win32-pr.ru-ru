---
title: Вопросы безопасности контрольной точки
description: При создании контрольной точки необходимо учитывать следующие аспекты безопасности.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986690"
---
# <a name="control-point-security-considerations"></a><span data-ttu-id="668d9-103">Вопросы безопасности контрольной точки</span><span class="sxs-lookup"><span data-stu-id="668d9-103">Control Point Security Considerations</span></span>

<span data-ttu-id="668d9-104">При создании контрольной точки необходимо учитывать следующие аспекты безопасности.</span><span class="sxs-lookup"><span data-stu-id="668d9-104">When you are creating a control point, you need to take into consideration the following security issues.</span></span>

-   <span data-ttu-id="668d9-105">Все операции поиска контрольных точек по умолчанию отправляются с TTL, равным 1.</span><span class="sxs-lookup"><span data-stu-id="668d9-105">All control point searches are by default sent with a TTL of 1.</span></span> <span data-ttu-id="668d9-106">Это означает, что обнаруживаются только устройства в одной подсети.</span><span class="sxs-lookup"><span data-stu-id="668d9-106">This means that only devices within the same subnet are discovered.</span></span> <span data-ttu-id="668d9-107">В реестре можно настроить более высокий срок жизни.</span><span class="sxs-lookup"><span data-stu-id="668d9-107">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="668d9-108">Описание устройства и службы загружается только в том случае, если оно имеется на том же устройстве, которое отправило объявление устройства.</span><span class="sxs-lookup"><span data-stu-id="668d9-108">A device's device and service description is only downloaded if it is present on the same device which sent the device announcement.</span></span>
-   <span data-ttu-id="668d9-109">Устройство отправляет запросы на управление и подписку только в том случае, если URL-адреса элемента управления и подписки находятся на одном устройстве, которое отправило объявления устройств.</span><span class="sxs-lookup"><span data-stu-id="668d9-109">A device is only sent control and subscription requests if its control and subscription URLs are on the same device that sent the device announcements.</span></span>

 

 




