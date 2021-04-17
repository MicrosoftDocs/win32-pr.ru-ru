---
description: В следующем списке приведены краткие описания каждой структуры Winsock ATM. Для получения дополнительных сведений о любой структуре щелкните имя структуры.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Структуры Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711375"
---
# <a name="winsock-atm-structures"></a><span data-ttu-id="035ed-104">Структуры Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="035ed-104">Winsock ATM Structures</span></span>

<span data-ttu-id="035ed-105">В следующем списке приведены краткие описания каждой структуры Winsock ATM.</span><span class="sxs-lookup"><span data-stu-id="035ed-105">The following list provides concise descriptions of each Winsock ATM structure.</span></span> <span data-ttu-id="035ed-106">Для получения дополнительных сведений о любой структуре щелкните имя структуры.</span><span class="sxs-lookup"><span data-stu-id="035ed-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="035ed-107">Структура ATM</span><span class="sxs-lookup"><span data-stu-id="035ed-107">ATM Structure</span></span>                           | <span data-ttu-id="035ed-108">Описание</span><span class="sxs-lookup"><span data-stu-id="035ed-108">Description</span></span>                                                |
|-----------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="035ed-109">**ATM- \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="035ed-109">**ATM\_ADDRESS**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | <span data-ttu-id="035ed-110">Хранит данные об ATM-адресах для сокетов на основе ATM.</span><span class="sxs-lookup"><span data-stu-id="035ed-110">Stores ATM address data for ATM-based sockets.</span></span>             |
| [<span data-ttu-id="035ed-111">**\_БХЛИ ATM**</span><span class="sxs-lookup"><span data-stu-id="035ed-111">**ATM\_BHLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | <span data-ttu-id="035ed-112">Определяет сведения о B-ХЛИ для соответствующего сокета ATM.</span><span class="sxs-lookup"><span data-stu-id="035ed-112">Identifies B-HLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="035ed-113">**\_БЛЛИ ATM**</span><span class="sxs-lookup"><span data-stu-id="035ed-113">**ATM\_BLLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | <span data-ttu-id="035ed-114">Определяет сведения о B-лли для соответствующего сокета ATM.</span><span class="sxs-lookup"><span data-stu-id="035ed-114">Identifies B-LLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="035ed-115">**SOCKADDR \_ ATM**</span><span class="sxs-lookup"><span data-stu-id="035ed-115">**sockaddr\_atm**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | <span data-ttu-id="035ed-116">Хранит сведения об адресе сокета для сокетов ATM.</span><span class="sxs-lookup"><span data-stu-id="035ed-116">Stores socket address information for ATM sockets.</span></span>         |



 

<span data-ttu-id="035ed-117">Для собственных служб ATM используйте AF \_ ATM для семейства адресов и SOCKADDR в качестве структуры адресов сокетов [**\_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) .</span><span class="sxs-lookup"><span data-stu-id="035ed-117">For native ATM services, use AF\_ATM for address family and the [**sockaddr\_atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) socket address structure.</span></span> <span data-ttu-id="035ed-118">Чтобы открыть собственный сокет ATM, передайте \_ соккный ATM-код, \_ а также атмпрото \_ AAL5 или атмпрото \_ аалусер в функцию [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) соответственно.</span><span class="sxs-lookup"><span data-stu-id="035ed-118">To open a native ATM socket, pass AF\_ATM, SOCK\_RAW, and ATMPROTO\_AAL5 or ATMPROTO\_AALUSER into the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function, respectively.</span></span>

 

 



