---
description: При использовании многоадресной рассылки обычно необходимо указать область, в которой должна выполняться многоадресная рассылка.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE код команды для Всаиоктл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080537"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a><span data-ttu-id="26257-103">\_Код команды многоадресной области ввода/вывода \_ для всаиоктл</span><span class="sxs-lookup"><span data-stu-id="26257-103">SIO\_MULTICAST\_SCOPE Command Code for WSAIoctl</span></span>

<span data-ttu-id="26257-104">При использовании многоадресной рассылки обычно необходимо указать *область* , в которой должна выполняться многоадресная рассылка.</span><span class="sxs-lookup"><span data-stu-id="26257-104">When multicasting is employed, it is usually necessary to specify the *scope* over which the multicast should occur.</span></span> <span data-ttu-id="26257-105">Область определяется как количество сегментов маршрутизируемых сетей, подпадающих под действие.</span><span class="sxs-lookup"><span data-stu-id="26257-105">Scope is defined as the number of routed network segments to be covered.</span></span> <span data-ttu-id="26257-106">Нулевая область означает, что многоадресная передача не будет помещаться в сеть, но может быть распределена между сокетами на локальном узле.</span><span class="sxs-lookup"><span data-stu-id="26257-106">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="26257-107">Значение области, равное 1 (по умолчанию), указывает, что передача будет размещена на канале передачи, но не будет пересекать маршрутизаторы.</span><span class="sxs-lookup"><span data-stu-id="26257-107">A scope value of 1 (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="26257-108">Более высокие значения области определяют количество маршрутизаторов, которые могут быть перепутаны.</span><span class="sxs-lookup"><span data-stu-id="26257-108">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="26257-109">Обратите внимание, что это соответствует параметру срока жизни (TTL) в многоадресной IP-рассылке.</span><span class="sxs-lookup"><span data-stu-id="26257-109">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

<span data-ttu-id="26257-110">Функция [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) используется для присоединение конечного узла к сеансу MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="26257-110">The function [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) is used to join a leaf node into the multipoint session.</span></span> <span data-ttu-id="26257-111">Сведения об использовании этой функции см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="26257-111">See the following for a discussion on how this function is utilized.</span></span>

 

 



