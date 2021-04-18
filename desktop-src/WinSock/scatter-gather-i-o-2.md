---
description: Функции Всарекв, Всареквфром, Всареквмсг, Всасенд, Всасендмсг и Всасендто принимают массив буферов приложений в качестве входных параметров и могут использоваться для точечного или сособираемого (или векторного) ввода-вывода.
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: Точечная или собранная операция ввода-вывода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702091"
---
# <a name="scattergather-io"></a><span data-ttu-id="2b758-103">Точечная или собранная операция ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="2b758-103">Scatter/Gather I/O</span></span>

<span data-ttu-id="2b758-104">Функции [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**всасендмсг**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)и [**всасендто**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) принимают массив буферов приложений в качестве входных параметров и могут использоваться для точечной/собираемой (или векторной) операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="2b758-104">The [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) functions all take an array of application buffers as input parameters and can be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="2b758-105">Это может быть очень полезно в случаях, когда части каждого передаваемого сообщения состоят из одного или нескольких компонентов заголовков фиксированной длины в дополнение к тексту сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b758-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed-length header components in addition to the message body.</span></span> <span data-ttu-id="2b758-106">Такие компоненты заголовков не должны объединяться приложением в один непрерывный буфер перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="2b758-106">Such header components need not be concatenated by the application into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="2b758-107">Как и при получении, компоненты заголовка можно автоматически разбить на отдельные буферы, не выходя за пределы тела сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b758-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body by itself.</span></span>

<span data-ttu-id="2b758-108">При получении в несколько буферов завершение происходит, когда данные поступают из сети, независимо от того, используются ли все указанные буферы.</span><span class="sxs-lookup"><span data-stu-id="2b758-108">When receiving into multiple buffers, completion occurs as data arrives from the network, regardless of whether all the supplied buffers are utilized.</span></span>

 

 
