---
description: Сокеты Windows 2 не предполагают, что сетевой порядок байтов для всех протоколов одинаков.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Расширенные подпрограммы преобразования Byte-Order
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541602"
---
# <a name="extended-byte-order-conversion-routines"></a><span data-ttu-id="e1199-103">Расширенные подпрограммы преобразования Byte-Order</span><span class="sxs-lookup"><span data-stu-id="e1199-103">Extended Byte-Order Conversion Routines</span></span>

<span data-ttu-id="e1199-104">Сокеты Windows 2 не предполагают, что сетевой порядок байтов для всех протоколов одинаков.</span><span class="sxs-lookup"><span data-stu-id="e1199-104">Windows Sockets 2 does not assume that the network byte order for all protocols is the same.</span></span> <span data-ttu-id="e1199-105">Для преобразования 16-разрядных и 32-разрядных количеств в байты и из сетевого порядка байтов предоставляется набор подпрограмм преобразования.</span><span class="sxs-lookup"><span data-stu-id="e1199-105">A set of conversion routines is supplied for converting 16-bit and 32-bit quantities to and from network byte order.</span></span> <span data-ttu-id="e1199-106">Эти подпрограммы принимают в качестве входного параметра маркер сокета, имеющий связанную с ним структуру [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="e1199-106">These routines take as an input parameter the socket handle that has a [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure associated with it.</span></span> <span data-ttu-id="e1199-107">Элемент **нетворкбитеордер** структуры **\_ сведений о всапротокол** указывает нужный порядок байтов в сети (в настоящее время это либо с обратным порядком байтов, либо с прямым порядком байтов).</span><span class="sxs-lookup"><span data-stu-id="e1199-107">The **NetworkByteOrder** member of the **WSAPROTOCOL\_INFO** structure specifies the desired network byte order (currently either big-endian or little-endian).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1199-108">См. также</span><span class="sxs-lookup"><span data-stu-id="e1199-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1199-109">**хтонл**</span><span class="sxs-lookup"><span data-stu-id="e1199-109">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="e1199-110">**хтонс**</span><span class="sxs-lookup"><span data-stu-id="e1199-110">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="e1199-111">**нтохл**</span><span class="sxs-lookup"><span data-stu-id="e1199-111">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="e1199-112">**нтохс**</span><span class="sxs-lookup"><span data-stu-id="e1199-112">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="e1199-113">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="e1199-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="e1199-114">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="e1199-114">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="e1199-115">**всахтонл**</span><span class="sxs-lookup"><span data-stu-id="e1199-115">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="e1199-116">**всахтонс**</span><span class="sxs-lookup"><span data-stu-id="e1199-116">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="e1199-117">**всантохл**</span><span class="sxs-lookup"><span data-stu-id="e1199-117">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="e1199-118">**всантохс**</span><span class="sxs-lookup"><span data-stu-id="e1199-118">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[<span data-ttu-id="e1199-119">**\_сведения о всапротокол**</span><span class="sxs-lookup"><span data-stu-id="e1199-119">**WSAPROTOCOL\_INFO**</span></span>](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
