---
description: В следующем списке приведены краткие описания каждой структуры Winsock TCP/IP. Для получения дополнительных сведений о любой структуре щелкните имя структуры.
ms.assetid: 9c9a4639-4b51-4e00-b790-a0a5841c6ed3
title: Структуры Winsock TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e350fc6fe12f6881d08d6757c739f9480d59afa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711373"
---
# <a name="winsock-tcpip-structures"></a><span data-ttu-id="59815-104">Структуры Winsock TCP/IP</span><span class="sxs-lookup"><span data-stu-id="59815-104">Winsock TCP/IP Structures</span></span>

<span data-ttu-id="59815-105">В следующем списке приведены краткие описания каждой структуры Winsock TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="59815-105">The following list provides concise descriptions of each Winsock TCP/IP structure.</span></span> <span data-ttu-id="59815-106">Для получения дополнительных сведений о любой структуре щелкните имя структуры.</span><span class="sxs-lookup"><span data-stu-id="59815-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="59815-107">Структура TCP/IP</span><span class="sxs-lookup"><span data-stu-id="59815-107">TCP/IP Structure</span></span>                                 | <span data-ttu-id="59815-108">Описание</span><span class="sxs-lookup"><span data-stu-id="59815-108">Description</span></span>                                                                                                                              |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59815-109">**\_сведения об интерфейсе**</span><span class="sxs-lookup"><span data-stu-id="59815-109">**INTERFACE\_INFO**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info)      | <span data-ttu-id="59815-110">Используется с командой IOCTL для получения сведений об IP-адресе интерфейса.</span><span class="sxs-lookup"><span data-stu-id="59815-110">Used with the ioctl command to obtain information about an interface IP address.</span></span>                                                         |
| [<span data-ttu-id="59815-111">**\_сведения об интерфейсе \_ ex**</span><span class="sxs-lookup"><span data-stu-id="59815-111">**INTERFACE\_INFO\_EX**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) | <span data-ttu-id="59815-112">Используется с командой **\_ ioctl получить \_ \_ список интерфейсов** для получения сведений об IP-адресе интерфейса, включая адреса IPv6.</span><span class="sxs-lookup"><span data-stu-id="59815-112">Used with the **SIO\_GET\_INTERFACE\_LIST IOCTL** command to obtain information about an interface IP address, including IPv6 addresses.</span></span> |
| [<span data-ttu-id="59815-113">**SOCKADDR \_ Gen**</span><span class="sxs-lookup"><span data-stu-id="59815-113">**sockaddr\_gen**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-sockaddr_gen)            | <span data-ttu-id="59815-114">Предоставляет сведения об универсальном адресе сокета.</span><span class="sxs-lookup"><span data-stu-id="59815-114">Provides generic socket address information.</span></span> <span data-ttu-id="59815-115">Используется со структурой [**\_ сведений об интерфейсе**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) .</span><span class="sxs-lookup"><span data-stu-id="59815-115">Used with the [**INTERFACE\_INFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) structure.</span></span>                        |



 

 

 



