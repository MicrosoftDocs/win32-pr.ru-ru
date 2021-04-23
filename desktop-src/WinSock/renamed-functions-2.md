---
description: В двух случаях необходимо переименовать функции, которые используются в сокетах Berkeley, чтобы избежать конфликта с другими функциями Microsoft Windows API.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Переименованные функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898582"
---
# <a name="renamed-functions"></a><span data-ttu-id="61efd-103">Переименованные функции</span><span class="sxs-lookup"><span data-stu-id="61efd-103">Renamed Functions</span></span>

<span data-ttu-id="61efd-104">В двух случаях необходимо переименовать функции, которые используются в сокетах Berkeley, чтобы избежать конфликта с другими функциями Microsoft Windows API.</span><span class="sxs-lookup"><span data-stu-id="61efd-104">In two cases it was necessary to rename functions that are used in Berkeley Sockets in order to avoid clashes with other Microsoft Windows API functions.</span></span>

## <a name="close-and-closesocket"></a><span data-ttu-id="61efd-105">Закрыть и функции closesocket</span><span class="sxs-lookup"><span data-stu-id="61efd-105">Close and Closesocket</span></span>

<span data-ttu-id="61efd-106">Сокеты представлены стандартными дескрипторами файлов в сокетах Berkeley, поэтому функцию **Close** можно использовать для закрытия сокетов, а также обычных файлов.</span><span class="sxs-lookup"><span data-stu-id="61efd-106">Sockets are represented by standard file descriptors in Berkeley Sockets, so the **close** function can be used to close sockets as well as regular files.</span></span> <span data-ttu-id="61efd-107">Хотя ни одно из сокетов Windows не позволяет реализовать использование обычных дескрипторов файлов для обнаружения сокетов, ничего не требуется.</span><span class="sxs-lookup"><span data-stu-id="61efd-107">While nothing in Windows Sockets prevents an implementation from using regular file handles to identify sockets, nothing requires it either.</span></span> <span data-ttu-id="61efd-108">В Windows сокеты должны быть закрыты с помощью подпрограммы [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .</span><span class="sxs-lookup"><span data-stu-id="61efd-108">On Windows, sockets must be closed by using the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) routine.</span></span> <span data-ttu-id="61efd-109">В Windows использование функции **Close** для закрытия сокета неверно, и последствия этого действия не определены в этой спецификации.</span><span class="sxs-lookup"><span data-stu-id="61efd-109">ON Windows, using the **close** function to close a socket is incorrect and the effects of doing so are undefined by this specification.</span></span>

## <a name="ioctl-and-ioctlsocketwsaioctl"></a><span data-ttu-id="61efd-110">IOCTL и Иоктлсоккет/Всаиоктл</span><span class="sxs-lookup"><span data-stu-id="61efd-110">Ioctl and Ioctlsocket/WSAIoctl</span></span>

<span data-ttu-id="61efd-111">Различные системы времени выполнения языка C используют IOCTL для целей, не связанных с сокетами Windows.</span><span class="sxs-lookup"><span data-stu-id="61efd-111">Various C language run-time systems use the IOCTLs for purposes unrelated to Windows Sockets.</span></span> <span data-ttu-id="61efd-112">Как следствие, функция [**иоктлсоккет**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) и функция [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) были определены для выполнения функций сокета, которые были выполнены с помощью **ioctl** и **fcntl** в распределении программного обеспечения Berkeley.</span><span class="sxs-lookup"><span data-stu-id="61efd-112">As a consequence, the [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) function and the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function were defined to handle socket functions that were performed by **IOCTL** and **fcntl** in the Berkeley Software Distribution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61efd-113">См. также</span><span class="sxs-lookup"><span data-stu-id="61efd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61efd-114">**функции closesocket**</span><span class="sxs-lookup"><span data-stu-id="61efd-114">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="61efd-115">**иоктлсоккет**</span><span class="sxs-lookup"><span data-stu-id="61efd-115">**ioctlsocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[<span data-ttu-id="61efd-116">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="61efd-116">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="61efd-117">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="61efd-117">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="61efd-118">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="61efd-118">**WSAIoctl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



