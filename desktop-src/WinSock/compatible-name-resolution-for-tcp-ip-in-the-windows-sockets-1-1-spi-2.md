---
description: Сокеты Windows 1,1 определяют ряд подпрограмм, которые использовались для разрешения имен IPv4 в сетях TCP/IP. Эти функции также называются функциями Жетксбии и включают следующее.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Совместимое разрешение имен для TCP/IP в Windows Sockets 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692302"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a><span data-ttu-id="3bd8c-104">Совместимое разрешение имен для TCP/IP в Windows Sockets 1,1 SPI</span><span class="sxs-lookup"><span data-stu-id="3bd8c-104">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI</span></span>

<span data-ttu-id="3bd8c-105">Сокеты Windows 1,1 определяют ряд подпрограмм, которые использовались для разрешения имен IPv4 в сетях TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3bd8c-105">Windows Sockets 1.1 defined a number of routines that were used for IPv4 name resolution with TCP/IP networks.</span></span> <span data-ttu-id="3bd8c-106">Эти функции также называются функциями **жетксбии** и включают следующее.</span><span class="sxs-lookup"><span data-stu-id="3bd8c-106">These are customarily called the **GetXbyY** functions and include the following.</span></span>

[<span data-ttu-id="3bd8c-107">**имя узла**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-107">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)

[<span data-ttu-id="3bd8c-108">**жесостбяддр**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-108">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[<span data-ttu-id="3bd8c-109">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-109">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[<span data-ttu-id="3bd8c-110">**жетпротобинаме**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-110">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[<span data-ttu-id="3bd8c-111">**жетпротобинумбер**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-111">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[<span data-ttu-id="3bd8c-112">**жетсервбинаме**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-112">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[<span data-ttu-id="3bd8c-113">**жетсервбипорт**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-113">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)

<span data-ttu-id="3bd8c-114">Также определены асинхронные версии этих функций.</span><span class="sxs-lookup"><span data-stu-id="3bd8c-114">Asynchronous versions of these functions were also defined.</span></span>

[<span data-ttu-id="3bd8c-115">**всаасинкжесостбяддр**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-115">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[<span data-ttu-id="3bd8c-116">**всаасинкжесостбинаме**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-116">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[<span data-ttu-id="3bd8c-117">**всаасинкжетпротобинаме**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-117">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[<span data-ttu-id="3bd8c-118">**всаасинкжетпротобинумбер**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-118">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[<span data-ttu-id="3bd8c-119">**всаасинкжетсервбинаме**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-119">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[<span data-ttu-id="3bd8c-120">**всаасинкжетсервбипорт**</span><span class="sxs-lookup"><span data-stu-id="3bd8c-120">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

<span data-ttu-id="3bd8c-121">Эти функции относятся к сетям TCP/IP. разработчикам приложений, не зависящих от протокола, не рекомендуется продолжать использовать эти функции, связанные с транспортом.</span><span class="sxs-lookup"><span data-stu-id="3bd8c-121">These functions are specific to TCP/IP networks; developers of protocol-independent applications are discouraged from continuing to utilize these transport-specific functions.</span></span> <span data-ttu-id="3bd8c-122">Тем не менее, чтобы обеспечить максимальную обратную совместимость с сокетами Windows 1,1, предыдущие функции продолжают поддерживаться до тех пор, пока имеется хотя бы один поставщик пространства имен, поддерживающий \_ семейство адресов AF inet.</span><span class="sxs-lookup"><span data-stu-id="3bd8c-122">However, to retain strict backward compatibility with Windows Sockets 1.1, the preceding functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family.</span></span>

<span data-ttu-id="3bd8c-123">*\_32.dllWs2* реализует эти функции совместимости с точки зрения нового, независимого от протокола имени средства разрешения имен с помощью соответствующей последовательности вызовов [**функций всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)и [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .</span><span class="sxs-lookup"><span data-stu-id="3bd8c-123">The *Ws2\_32.dll* implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function calls.</span></span> <span data-ttu-id="3bd8c-124">Ниже приведены сведения о сопоставлении функций **жетксбии** с функциями разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="3bd8c-124">The details of how the **GetXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="3bd8c-125">Ws2 \_32.dll обрабатывает различия между асинхронной и синхронной версиями функций **жетксбии** , так что обсуждаются только реализации синхронных функций **жетксбии** .</span><span class="sxs-lookup"><span data-stu-id="3bd8c-125">The Ws2\_32.dll handles the differences between the asynchronous and synchronous versions of the **GetXbyY** functions, so that only the implementation of the synchronous **GetXbyY** functions are discussed.</span></span>

 

 
