---
title: Bluetooth и Accept
description: Bluetooth использует функцию Accept для включения входящих попыток подключения к сокету.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- гласит
- Bluetooth
- Bluetooth
- Bluetooth и Accept
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654340"
---
# <a name="bluetooth-and-accept"></a><span data-ttu-id="2e7ba-107">Bluetooth и Accept</span><span class="sxs-lookup"><span data-stu-id="2e7ba-107">Bluetooth and accept</span></span>

<span data-ttu-id="2e7ba-108">Bluetooth использует функцию [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) для включения входящих попыток подключения к сокету.</span><span class="sxs-lookup"><span data-stu-id="2e7ba-108">Bluetooth uses the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function to enable incoming connection attempts on a socket.</span></span> <span data-ttu-id="2e7ba-109">БС \_ -адрес клиентского приложения получается путем считывания раздела, относящегося к транспорту Bluetooth, возвращенной структуры [**SOCKADDR**](/windows/desktop/WinSock/sockaddr-2) .</span><span class="sxs-lookup"><span data-stu-id="2e7ba-109">The BTH\_ADDR of the client application is obtained by reading the Bluetooth transport-specific section of the returned [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) structure.</span></span> <span data-ttu-id="2e7ba-110">Использование функции **Accept** с Bluetooth имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="2e7ba-110">Use of the **accept** function with Bluetooth has the following format:</span></span>

-   <span data-ttu-id="2e7ba-111">Параметр *addr* функции [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) является необязательным указателем на буфер, который получает адрес связывающей сущности, как известно на уровне связи.</span><span class="sxs-lookup"><span data-stu-id="2e7ba-111">The *addr* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to a buffer that receives the address of the connecting entity, as known to the communications layer.</span></span> <span data-ttu-id="2e7ba-112">Возвращается указатель на структуру [**\_ БС SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) с адресом удаленного устройства Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="2e7ba-112">A pointer to a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure with the remote Bluetooth device address is returned.</span></span>
-   <span data-ttu-id="2e7ba-113">Параметр *аддрлен* функции [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) является необязательным указателем на целое число, которое содержит длину адреса в байтах. Целое число должно быть больше или равно значению **sizeof** ([**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span><span class="sxs-lookup"><span data-stu-id="2e7ba-113">The *addrlen* parameter of the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) function is an optional pointer to an integer that contains the length, in bytes, of addr. The integer must be greater or equal to the value of **sizeof** ([**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e7ba-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2e7ba-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e7ba-115">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="2e7ba-115">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="2e7ba-116">**гласит**</span><span class="sxs-lookup"><span data-stu-id="2e7ba-116">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 