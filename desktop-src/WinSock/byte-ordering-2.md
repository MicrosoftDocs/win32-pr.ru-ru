---
description: Необходимо всегда соблюдать осторожность, чтобы учитывать любые различия между порядком байтов, используемым для хранения целых чисел в архитектуре узла, и порядком байтов, используемым для передачи отдельными транспортными протоколами.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: Порядок байтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497469"
---
# <a name="byte-ordering"></a><span data-ttu-id="f22bf-103">Порядок байтов</span><span class="sxs-lookup"><span data-stu-id="f22bf-103">Byte Ordering</span></span>

<span data-ttu-id="f22bf-104">Необходимо всегда соблюдать осторожность, чтобы учитывать любые различия между порядком байтов, используемым для хранения целых чисел в архитектуре узла, и порядком байтов, используемым для передачи отдельными транспортными протоколами.</span><span class="sxs-lookup"><span data-stu-id="f22bf-104">Care must always be taken to account for any differences between the byte ordering used for storing integers by the host architecture and the byte ordering used on the wire by individual transport protocols.</span></span> <span data-ttu-id="f22bf-105">Любая ссылка на адрес или номер порта, передаваемые или из подпрограммы Windows Sockets, должна находиться в сетевом порядке (с обратным порядком байтов) для используемого протокола.</span><span class="sxs-lookup"><span data-stu-id="f22bf-105">Any reference to an address or port number passed to or from a Windows Sockets routine must be in the network order (big-endian) for the protocol being utilized.</span></span> <span data-ttu-id="f22bf-106">В случае IP-адреса это включает IP-адрес и параметры порта структуры [**SOCKADDR**](sockaddr-2.md) (но не параметра *\_ семейства Sin* ).</span><span class="sxs-lookup"><span data-stu-id="f22bf-106">In the case of IP, this includes the IP address and port parameters of a [**sockaddr**](sockaddr-2.md) structure (but not the *sin\_family* parameter).</span></span>

<span data-ttu-id="f22bf-107">Ряд систем UNIX работают с процессорами, представляющими целые числа в сетевом байтом порядке (Big-endian).</span><span class="sxs-lookup"><span data-stu-id="f22bf-107">A number of the UNIX systems operate on CPUs that represent integers in network byte order (big-endian).</span></span> <span data-ttu-id="f22bf-108">Поэтому необходимость преобразования целых чисел из порядка байтов узла в сетевой порядок байтов можно пропустить, не вызывая проблем, даже если это не рекомендуется для переносимости.</span><span class="sxs-lookup"><span data-stu-id="f22bf-108">So the need to convert integers from host byte order to network byte order can be ignored without causing problems even if this is not recommended for portability.</span></span>

<span data-ttu-id="f22bf-109">В отличие от этого, порядок байтов, используемый для представления целых чисел в большинстве процессоров Intel®, имеет прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="f22bf-109">In contrast, the byte ordering used to represent integers by most Intel® CPUs is little-endian.</span></span> <span data-ttu-id="f22bf-110">Поэтому становится обязательным Преобразование целых чисел из байта узла в порядковый байт в сети перед использованием в функциях и структурах Winsock.</span><span class="sxs-lookup"><span data-stu-id="f22bf-110">So it is becomes mandatory that integers be converted from host byte-order to network byte order before being used in Winsock Sockets functions and structures.</span></span>

<span data-ttu-id="f22bf-111">Рассмотрим приложение, которое обычно связывается с сервером через TCP-порт, соответствующий службе времени, но предоставляет пользователю механизм для указания альтернативного порта.</span><span class="sxs-lookup"><span data-stu-id="f22bf-111">Consider an application that normally contacts a server on the TCP port corresponding to the time service, but provides a mechanism for the user to specify an alternative port.</span></span> <span data-ttu-id="f22bf-112">Номер порта, возвращенный [**жетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-getservbyname) , уже находится в сетевом порядке. это формат, необходимый для создания адреса, чтобы перевод не требовался.</span><span class="sxs-lookup"><span data-stu-id="f22bf-112">The port number returned by [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) is already in network order, which is the format required for constructing an address so that no translation is required.</span></span> <span data-ttu-id="f22bf-113">Однако если пользователь выбирает использование другого порта, который вводит как целое число, приложение должно преобразовать его из узла в сетевой порядок TCP/IP (с помощью функции [**хтонс**](/windows/desktop/api/winsock/nf-winsock-htons) или [**всахтонс**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ), прежде чем использовать его для создания адреса.</span><span class="sxs-lookup"><span data-stu-id="f22bf-113">However, if the user elects to use a different port, entered as an integer, the application must convert this from host to TCP/IP network order (using the [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) or [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) function) before using it to construct an address.</span></span> <span data-ttu-id="f22bf-114">И наоборот, если приложение должно отобразить номер порта в адресе (например, возвращено [**жетпирнаме**](/windows/desktop/api/winsock/nf-winsock-getpeername) ), номер порта должен быть преобразован из сети в порядок размещения (с помощью функции [**нтохс**](/windows/desktop/api/winsock/nf-winsock-ntohs) или [**всантохс**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) перед отображением.</span><span class="sxs-lookup"><span data-stu-id="f22bf-114">Conversely, if the application were to display the number of the port within an address (returned by [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) for example), the port number must be converted from network to host order (using the [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) or [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) function) before it can be displayed.</span></span>

<span data-ttu-id="f22bf-115">Так как порядок байтов Intel и Интернета отличается, преобразования, описанные выше, не могут быть предотвращены.</span><span class="sxs-lookup"><span data-stu-id="f22bf-115">Since the Intel and Internet byte orders are different, the conversions described in the preceding are unavoidable.</span></span> <span data-ttu-id="f22bf-116">Средства записи приложений соблюдают, что они должны использовать стандартные функции преобразования, предоставляемые как часть Winsock, вместо написания собственного кода преобразования, так как будущие реализации Winsock, скорее всего, будут работать на системах, для которых порядок размещения идентичен сетевому порядку байтов.</span><span class="sxs-lookup"><span data-stu-id="f22bf-116">Application writers are cautioned that they should use the standard conversion functions provided as part of Winsock rather than writing their own conversion code since future implementations of Winsock are likely to run on systems for which the host order is identical to the network byte order.</span></span> <span data-ttu-id="f22bf-117">Переносимыми могут быть только приложения, использующие стандартные функции преобразования между узлом и сетевым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="f22bf-117">Only applications that use the standard conversion functions between host and network byte order are likely to be portable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f22bf-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f22bf-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f22bf-119">**жетпирнаме**</span><span class="sxs-lookup"><span data-stu-id="f22bf-119">**getpeername**</span></span>](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[<span data-ttu-id="f22bf-120">**жетсервбинаме**</span><span class="sxs-lookup"><span data-stu-id="f22bf-120">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[<span data-ttu-id="f22bf-121">**хтонл**</span><span class="sxs-lookup"><span data-stu-id="f22bf-121">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="f22bf-122">**хтонс**</span><span class="sxs-lookup"><span data-stu-id="f22bf-122">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="f22bf-123">**нтохл**</span><span class="sxs-lookup"><span data-stu-id="f22bf-123">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="f22bf-124">**нтохс**</span><span class="sxs-lookup"><span data-stu-id="f22bf-124">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="f22bf-125">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="f22bf-125">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="f22bf-126">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="f22bf-126">**sockaddr**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="f22bf-127">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="f22bf-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="f22bf-128">**всахтонл**</span><span class="sxs-lookup"><span data-stu-id="f22bf-128">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="f22bf-129">**всахтонс**</span><span class="sxs-lookup"><span data-stu-id="f22bf-129">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="f22bf-130">**всантохл**</span><span class="sxs-lookup"><span data-stu-id="f22bf-130">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="f22bf-131">**всантохс**</span><span class="sxs-lookup"><span data-stu-id="f22bf-131">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



