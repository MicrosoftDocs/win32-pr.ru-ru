---
title: Разработка и развертывание в сети
description: Большинство разработчиков пишут и проверяют свое программное обеспечение в быстрой надежной локальной сети.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067850"
---
# <a name="development-vs-deployment-in-the-network"></a><span data-ttu-id="3f2ce-103">Разработка и развертывание в сети</span><span class="sxs-lookup"><span data-stu-id="3f2ce-103">Development vs. Deployment in the Network</span></span>

<span data-ttu-id="3f2ce-104">Большинство разработчиков пишут и проверяют свое программное обеспечение в быстрой надежной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f2ce-104">Most developers write and test their software on a fast reliable LAN.</span></span> <span data-ttu-id="3f2ce-105">Их клиент и сервер часто находятся в одном сегменте сети.</span><span class="sxs-lookup"><span data-stu-id="3f2ce-105">Their client and server are often on the same network segment.</span></span> <span data-ttu-id="3f2ce-106">В таких обстоятельствах сеть редко не отвечает, и связь редко теряется.</span><span class="sxs-lookup"><span data-stu-id="3f2ce-106">In such circumstances the network is rarely unresponsive, and connectivity rarely lost.</span></span> <span data-ttu-id="3f2ce-107">Однако при развертывании в клиентской среде клиент и сервер часто бывают в разных сегментах сети, возможно географически удаленно, и сервер сильно загружен с другими клиентами.</span><span class="sxs-lookup"><span data-stu-id="3f2ce-107">When deployed in a customer environment however, client and server are often on different network segments, possibly geographically remote, and the server is heavily loaded with other clients.</span></span> <span data-ttu-id="3f2ce-108">Иными словами: скорость реагирования сети не может быть предпринята.</span><span class="sxs-lookup"><span data-stu-id="3f2ce-108">In other words: network responsiveness cannot be assumed.</span></span>

<span data-ttu-id="3f2ce-109">В этой статье объясняется, как создать надежную архитектуру клиента/сервера в неопределенной части, представленной ненадежной сетью и потенциально недоступными серверами.</span><span class="sxs-lookup"><span data-stu-id="3f2ce-109">This article explains how to construct robust client/server architectures in the face of uncertainty introduced by an intrinsically unreliable network and potentially unavailable servers.</span></span>

 

 




