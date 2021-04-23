---
description: Поставщик системного реестра пытается отправить одно уведомление для каждого возникающего события.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Получение событий реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080533"
---
# <a name="receiving-registry-events"></a><span data-ttu-id="b175e-103">Получение событий реестра</span><span class="sxs-lookup"><span data-stu-id="b175e-103">Receiving Registry Events</span></span>

<span data-ttu-id="b175e-104">Поставщик системного реестра пытается отправить одно уведомление для каждого возникающего события.</span><span class="sxs-lookup"><span data-stu-id="b175e-104">The System Registry provider attempts to send one notification for every event that occurs.</span></span> <span data-ttu-id="b175e-105">Однако поставщик системного реестра не гарантирует, что потребитель получит какие-либо события.</span><span class="sxs-lookup"><span data-stu-id="b175e-105">However, the System Registry provider does not guarantee that the consumer will receive any or all events.</span></span> <span data-ttu-id="b175e-106">Исключением является то, что поставщик системного реестра гарантирует, что потребитель получит одно уведомление для каждой регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="b175e-106">The exception is that the System Registry provider does ensure that a consumer will receive one notification for each event registration.</span></span>

<span data-ttu-id="b175e-107">Например, предположим, что потребитель регистрирует два события изменения дерева, запрашивая уведомления для экземпляров [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) .</span><span class="sxs-lookup"><span data-stu-id="b175e-107">For example, suppose a consumer registers for two tree change events, requesting notification for [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) instances.</span></span> <span data-ttu-id="b175e-108">Каждая регистрация имеет одно и то же значение Hive (поддерево), но другое значение RootPath.</span><span class="sxs-lookup"><span data-stu-id="b175e-108">Each registration has the same Hive (subtree) value but a different RootPath value.</span></span> <span data-ttu-id="b175e-109">Если ключи в обоих путях меняются несколько раз, поставщик системного реестра гарантирует, что потребитель получит уведомление для каждого пути.</span><span class="sxs-lookup"><span data-stu-id="b175e-109">If keys in both paths change multiple times, the System Registry provider guarantees that the consumer will receive a notification for each path.</span></span> <span data-ttu-id="b175e-110">В зависимости от времени отклика реестра и поставщика системного реестра потребитель может получить столько уведомлений, сколько произошло событий.</span><span class="sxs-lookup"><span data-stu-id="b175e-110">Depending on the response time of the registry and the System Registry provider, the consumer may receive as many notifications as there were occurrences of events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b175e-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b175e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b175e-112">Регистрация для событий системного реестра</span><span class="sxs-lookup"><span data-stu-id="b175e-112">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> </dl>

 

 
