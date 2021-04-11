---
description: Семейство адресов IPX определяет структуру адресации для протоколов, использующих стандартную адресацию сокета IPX. Для этих транспортов адрес конечной точки состоит из номера сети, адреса узла и номера сокета.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Семейство адресов AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145118"
---
# <a name="af_ipx-address-family"></a><span data-ttu-id="b5122-104">Семейство IP- \_ адресов AF</span><span class="sxs-lookup"><span data-stu-id="b5122-104">AF\_IPX Address Family</span></span>

<span data-ttu-id="b5122-105">Семейство адресов IPX определяет структуру адресации для протоколов, использующих стандартную адресацию сокета IPX.</span><span class="sxs-lookup"><span data-stu-id="b5122-105">The IPX address family defines the addressing structure for protocols that use standard IPX socket addressing.</span></span> <span data-ttu-id="b5122-106">Для этих транспортов адрес конечной точки состоит из номера сети, адреса узла и номера сокета.</span><span class="sxs-lookup"><span data-stu-id="b5122-106">For these transports, an endpoint address consists of a network number, node address, and socket number.</span></span>

<span data-ttu-id="b5122-107">Номер сети — это административный домен, который обычно именуется одним сегментом Ethernet или Token Ring.</span><span class="sxs-lookup"><span data-stu-id="b5122-107">The network number is an administrative domain and typically names a single Ethernet or token ring segment.</span></span> <span data-ttu-id="b5122-108">Номер узла — это физический адрес станции.</span><span class="sxs-lookup"><span data-stu-id="b5122-108">The node number is a station's physical address.</span></span> <span data-ttu-id="b5122-109">Сочетание NET и node формируют адрес уникальной станции, который предположительно уникален в мире.</span><span class="sxs-lookup"><span data-stu-id="b5122-109">The combination of net and node form a unique station address that is presumed to be unique in the world.</span></span> <span data-ttu-id="b5122-110">Номера телефонов и узлов представлены в тексте в виде текста ASCII в блоке или пунктирной нотации следующим образом: ' 0101a040, 00001b498765 ' или ' 01-01-a0-40, 00-00-1B-49-87-65 '.</span><span class="sxs-lookup"><span data-stu-id="b5122-110">Net and node numbers are represented in ASCII text in either block or dashed notation as: '0101a040,00001b498765' or '01-01-a0-40,00-00-1b-49-87-65'.</span></span> <span data-ttu-id="b5122-111">Начальные нули не требуются.</span><span class="sxs-lookup"><span data-stu-id="b5122-111">Leading zeros need not be present.</span></span>

<span data-ttu-id="b5122-112">Номер сокета IPX — это номер службы сети или транспорта во многом аналогичен номеру TCP-порта, и его не следует путать с дескриптором сокета WinSock.</span><span class="sxs-lookup"><span data-stu-id="b5122-112">The IPX socket number is a network/transport service number much like a TCP port number and is not to be confused with the Winsock socket descriptor.</span></span> <span data-ttu-id="b5122-113">Номера сокетов IPX являются глобальными для конечной станции и не могут быть привязаны к конкретным адресам сети или узла.</span><span class="sxs-lookup"><span data-stu-id="b5122-113">IPX socket numbers are global to the end station and cannot be bound to specific net/node addresses.</span></span> <span data-ttu-id="b5122-114">Например, если конечная станция имеет две сетевые карты, связанный сокет может отправлять и принимать на обеих картах.</span><span class="sxs-lookup"><span data-stu-id="b5122-114">For instance, if the end station has two network interface cards, a bound socket can send and receive on both cards.</span></span> <span data-ttu-id="b5122-115">В частности, сокеты датаграммы посылают датаграммы на обеих картах.</span><span class="sxs-lookup"><span data-stu-id="b5122-115">In particular, datagram sockets would receive broadcast datagrams on both cards.</span></span>

> [!Caution]  
> <span data-ttu-id="b5122-116">SOCKADDR \_ IPX имеет длину 14 байт и короче 16-байтовой структуры [**SOCKADDR**](sockaddr-2.md) Reference.</span><span class="sxs-lookup"><span data-stu-id="b5122-116">SOCKADDR\_IPX is 14 bytes long and is shorter than the 16-byte [**sockaddr**](sockaddr-2.md) reference structure.</span></span> <span data-ttu-id="b5122-117">Реализации IPX/SPX могут принимать 16-байтовую длину, а также истинную длину.</span><span class="sxs-lookup"><span data-stu-id="b5122-117">IPX/SPX implementations may accept the 16-byte length as well as the true length.</span></span> <span data-ttu-id="b5122-118">Если вы используете SOCKADDR \_ IPX и жестко запрограммированную длину 16 байт, реализация может предположить, что у нее есть доступ к 2 байтам, следующим за структурой.</span><span class="sxs-lookup"><span data-stu-id="b5122-118">If you use SOCKADDR\_IPX and a hard-coded length of 16 bytes, the implementation may assume that it has access to the 2 bytes following your structure.</span></span>

 



| <span data-ttu-id="b5122-119">Поле</span><span class="sxs-lookup"><span data-stu-id="b5122-119">Field</span></span>           | <span data-ttu-id="b5122-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b5122-120">Value</span></span>                                    |
|-----------------|------------------------------------------|
| <span data-ttu-id="b5122-121">**\_семейство SA**</span><span class="sxs-lookup"><span data-stu-id="b5122-121">**sa\_family**</span></span>  | <span data-ttu-id="b5122-122">Семейство адресов AF \_ IPX в порядке узлов.</span><span class="sxs-lookup"><span data-stu-id="b5122-122">Address family AF\_IPX in host order.</span></span>    |
| <span data-ttu-id="b5122-123">**SA \_ нетнум**</span><span class="sxs-lookup"><span data-stu-id="b5122-123">**Sa\_netnum**</span></span>  | <span data-ttu-id="b5122-124">Идентификатор сети IPX в сетевом порядке.</span><span class="sxs-lookup"><span data-stu-id="b5122-124">IPX network identifier in network order.</span></span> |
| <span data-ttu-id="b5122-125">**SA \_ ноденум**</span><span class="sxs-lookup"><span data-stu-id="b5122-125">**Sa\_nodenum**</span></span> | <span data-ttu-id="b5122-126">Адрес узла станции с правом на запись.</span><span class="sxs-lookup"><span data-stu-id="b5122-126">Station node address, flushed right.</span></span>     |
| <span data-ttu-id="b5122-127">**\_Сокет SA**</span><span class="sxs-lookup"><span data-stu-id="b5122-127">**Sa\_socket**</span></span>  | <span data-ttu-id="b5122-128">Номер сокета IPX в сетевом порядке.</span><span class="sxs-lookup"><span data-stu-id="b5122-128">IPX socket number in network order.</span></span>      |



 

 

 



