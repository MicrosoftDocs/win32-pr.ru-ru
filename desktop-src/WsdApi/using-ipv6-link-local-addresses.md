---
description: Локальная адресация IPv6 в сообщениях SOAP обеспечивает уникальную задачу, так как адреса IPv6 для локальной связи должны быть осмысленными, но идентификатор области имеет только значение для локального компьютера.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Использование локальных адресов IPv6-канала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155235"
---
# <a name="using-ipv6-link-local-addresses"></a><span data-ttu-id="ed130-103">Использование локальных адресов IPv6-канала</span><span class="sxs-lookup"><span data-stu-id="ed130-103">Using IPv6 Link-Local Addresses</span></span>

<span data-ttu-id="ed130-104">Локальная адресация IPv6 в сообщениях SOAP обеспечивает уникальную задачу, так как адреса IPv6 для локальной связи должны быть осмысленными, но идентификатор области имеет только значение для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="ed130-104">IPv6 link-local addressing in SOAP messages provides a unique challenge, as IPv6 link-local addresses require a scope ID to be meaningful, but the scope ID only has meaning for the local machine.</span></span> <span data-ttu-id="ed130-105">Все реализации клиентов и устройств должны удалить идентификатор области перед отправкой IPv6-адреса локальной связи в сообщении SOAP.</span><span class="sxs-lookup"><span data-stu-id="ed130-105">All client and device implementations must remove the scope ID before sending an IPv6 link-local address in a SOAP message.</span></span> <span data-ttu-id="ed130-106">Кроме того, если в сообщении получен адрес локальной связи IPv6, то интерфейс, на котором было получено сообщение, должен быть известен, поэтому полный локальный адрес ссылки с ИДЕНТИФИКАТОРом области можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="ed130-106">Additionally, when an IPv6 link-local address is received in a message, the interface the message was received on must be known so the complete link local address with scope ID can be reconstructed.</span></span>

 

 



