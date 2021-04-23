---
description: Протокол Kerberos состоит из трех подпротоколов.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Подпротоколы Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264820"
---
# <a name="kerberos-subprotocols"></a><span data-ttu-id="c68de-103">Подпротоколы Kerberos</span><span class="sxs-lookup"><span data-stu-id="c68de-103">Kerberos Subprotocols</span></span>

<span data-ttu-id="c68de-104">[*Протокол Kerberos*](../secgloss/k-gly.md) состоит из трех подпротоколов.</span><span class="sxs-lookup"><span data-stu-id="c68de-104">The [*Kerberos protocol*](../secgloss/k-gly.md) is composed of three subprotocols.</span></span>



| <span data-ttu-id="c68de-105">Подпротокол</span><span class="sxs-lookup"><span data-stu-id="c68de-105">Subprotocol</span></span>                                                                         | <span data-ttu-id="c68de-106">Значение</span><span class="sxs-lookup"><span data-stu-id="c68de-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c68de-107">Проверка подлинности службы Exchange</span><span class="sxs-lookup"><span data-stu-id="c68de-107">Authentication Service Exchange</span></span>](authentication-service-exchange.md)<br/>   | <span data-ttu-id="c68de-108">В этом подпротоколе [*центр распространения ключей*](../secgloss/k-gly.md) (KDC) предоставляет клиенту [*ключ сеанса*](../secgloss/s-gly.md) входа и билет на предоставление билета (TGT).</span><span class="sxs-lookup"><span data-stu-id="c68de-108">In this subprotocol, the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) gives the client a logon [*session key*](../secgloss/s-gly.md) and a ticket-granting ticket (TGT).</span></span><br/> |
| [<span data-ttu-id="c68de-109">Предоставление билета службой Exchange</span><span class="sxs-lookup"><span data-stu-id="c68de-109">Ticket-Granting Service Exchange</span></span>](ticket-granting-service-exchange.md)<br/> | <span data-ttu-id="c68de-110">В этом подпротоколе KDC распространяет ключ сеанса службы и билет для службы.</span><span class="sxs-lookup"><span data-stu-id="c68de-110">In this subprotocol, the KDC distributes a service session key and a ticket for the service.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="c68de-111">Обмен данными между клиентом и сервером</span><span class="sxs-lookup"><span data-stu-id="c68de-111">Client/Server Exchange</span></span>](client-server-exchange.md)<br/>                     | <span data-ttu-id="c68de-112">В этом подпротоколе клиент предоставляет билет на к допуску службы.</span><span class="sxs-lookup"><span data-stu-id="c68de-112">In this subprotocol, the client presents the ticket for admission to a service.</span></span><br/>                                                                                                                                                                                                                         |



 

 

 
