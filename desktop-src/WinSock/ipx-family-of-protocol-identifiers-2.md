---
description: Параметр протокола в Socket и Всасоккет — это идентификатор, который устанавливает тип сети и метод для определения различных транспортных протоколов, работающих в сети.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Семейство идентификаторов протоколов IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145025"
---
# <a name="ipx-family-of-protocol-identifiers"></a><span data-ttu-id="61e92-103">Семейство идентификаторов протоколов IPX</span><span class="sxs-lookup"><span data-stu-id="61e92-103">IPX Family of Protocol Identifiers</span></span>

<span data-ttu-id="61e92-104">Параметр *протокола* в [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) и [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) — это идентификатор, который устанавливает тип сети и метод для определения различных транспортных протоколов, работающих в сети.</span><span class="sxs-lookup"><span data-stu-id="61e92-104">The *protocol* parameter in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) is an identifier that establishes a network type and a method for identifying the various transport protocols that run on the network.</span></span> <span data-ttu-id="61e92-105">В отличие от IP, IPX не использует одно значение протокола для выбора транспортного стека.</span><span class="sxs-lookup"><span data-stu-id="61e92-105">Unlike IP, IPX does not use a single protocol value for selecting a transport stack.</span></span> <span data-ttu-id="61e92-106">Поскольку нет необходимости использовать определенное значение для каждого транспортного протокола, мы можем назначить их удобным для приложений Winsock.</span><span class="sxs-lookup"><span data-stu-id="61e92-106">Since there is no network requirement to use a specific value for each transport protocol, we are free to assign them in a manner convenient for Winsock applications.</span></span> <span data-ttu-id="61e92-107">Мы не будем использовать значения 0 – 255, чтобы избежать конфликтов с соответствующими \_ значениями протокола PF inet.</span><span class="sxs-lookup"><span data-stu-id="61e92-107">We avoid values 0–255 in order to avoid collisions with the corresponding PF\_INET protocol values.</span></span>



| <span data-ttu-id="61e92-108">Имя</span><span class="sxs-lookup"><span data-stu-id="61e92-108">Name</span></span>         | <span data-ttu-id="61e92-109">Значение</span><span class="sxs-lookup"><span data-stu-id="61e92-109">Value</span></span>       | <span data-ttu-id="61e92-110">Типы сокетов</span><span class="sxs-lookup"><span data-stu-id="61e92-110">Socket types</span></span>              | <span data-ttu-id="61e92-111">Описание</span><span class="sxs-lookup"><span data-stu-id="61e92-111">Description</span></span>                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| <span data-ttu-id="61e92-112">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="61e92-112">Reserved</span></span>     | <span data-ttu-id="61e92-113">0–255</span><span class="sxs-lookup"><span data-stu-id="61e92-113">0-255</span></span>       |                           | <span data-ttu-id="61e92-114">Зарезервировано для \_ значений протокола PF inet.</span><span class="sxs-lookup"><span data-stu-id="61e92-114">Reserved for PF\_INET protocol values.</span></span>              |
| <span data-ttu-id="61e92-115">НСПРОТО \_ IPX</span><span class="sxs-lookup"><span data-stu-id="61e92-115">NSPROTO\_IPX</span></span> | <span data-ttu-id="61e92-116">1000-1255</span><span class="sxs-lookup"><span data-stu-id="61e92-116">1000 - 1255</span></span> | <span data-ttu-id="61e92-117">Сокк \_ ДГРАМ Сокк \_ RAW</span><span class="sxs-lookup"><span data-stu-id="61e92-117">SOCK\_DGRAM SOCK\_RAW</span></span>     | <span data-ttu-id="61e92-118">Служба датаграмм для IPX.</span><span class="sxs-lookup"><span data-stu-id="61e92-118">Datagram service for IPX.</span></span>                           |
| <span data-ttu-id="61e92-119">НСПРОТО \_ SPX</span><span class="sxs-lookup"><span data-stu-id="61e92-119">NSPROTO\_SPX</span></span> | <span data-ttu-id="61e92-120">1256</span><span class="sxs-lookup"><span data-stu-id="61e92-120">1256</span></span>        | <span data-ttu-id="61e92-121">Сокк \_ Stream Сокк \_ секпкт</span><span class="sxs-lookup"><span data-stu-id="61e92-121">SOCK\_STREAM SOCK\_SEQPKT</span></span> | <span data-ttu-id="61e92-122">Надежный обмен пакетами с использованием пакетов фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="61e92-122">Reliable packet exchange using fixed-sized packets.</span></span> |



 

> [!Note]  
> <span data-ttu-id="61e92-123">Если \_ указан нспрото SPX, Протокол SPX II автоматически используется, если обе конечные точки способны сделать это.</span><span class="sxs-lookup"><span data-stu-id="61e92-123">When NSPROTO\_SPX is specified, the SPX II protocol is automatically utilized if both endpoints are capable of doing so.</span></span>

 

 

 



