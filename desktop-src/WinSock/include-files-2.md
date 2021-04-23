---
description: Исходный включаемый файл для использования с сокетами Windows 1,1 был файлом заголовка Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Включение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343502"
---
# <a name="include-files"></a><span data-ttu-id="5d61f-103">Включение файлов</span><span class="sxs-lookup"><span data-stu-id="5d61f-103">Include Files</span></span>

<span data-ttu-id="5d61f-104">Исходный включаемый файл для использования с сокетами Windows 1,1 был файлом заголовка *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="5d61f-104">The original include file for use with Windows Sockets 1.1 was the *Winsock.h* header file.</span></span> <span data-ttu-id="5d61f-105">Для упрощения переноса существующего исходного кода, основанного на подсчете сокетов UNIX, в сокеты Windows, в комплектах средств разработки Windows Sockets для Winsock 1,1 было предложено несколько включаемых файлов с теми же именами, что и стандартные файлы UNIX (например, файлы заголовков *sys/Socket. h* и ARPA/inet. h).</span><span class="sxs-lookup"><span data-stu-id="5d61f-105">To ease porting existing source code based on Berkeley UNIX sockets to Windows sockets, Windows Sockets development kits for Winsock 1.1 were encouraged to be supplied with several include files with the same names as standard UNIX include files (the *sys/socket.h* and arpa/inet.h header files, for example).</span></span> <span data-ttu-id="5d61f-106">Однако эти файлы заголовков Winsock с одинаковыми именами просто содержали директиву для включения файла заголовка *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="5d61f-106">However, these similarly-name Winsock header files merely contained a directive to include the *Winsock2.h* header file.</span></span>

<span data-ttu-id="5d61f-107">При освобождении сокетов Windows 2 основной включаемый файл для использования с сокетами Windows был переименован в *Winsock2. h*.</span><span class="sxs-lookup"><span data-stu-id="5d61f-107">When Windows Sockets 2 was released, the primary include file for use with Windows Sockets was renamed to *Winsock2.h*.</span></span> <span data-ttu-id="5d61f-108">Старый исходный файл заголовка *Winsock. h* для Winsock 1,1 также был сохранен для совместимости с более старыми приложениями.</span><span class="sxs-lookup"><span data-stu-id="5d61f-108">The older original *Winsock.h* header file for Winsock 1.1 was also retained for compatibility with older applications.</span></span> <span data-ttu-id="5d61f-109">Разработка приложений, совместимых с Winsock 1,1, устарела, так как была выпущена ОС Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5d61f-109">The development of Winsock 1.1 compatible applications has been deprecated since Windows 2000 was released.</span></span> <span data-ttu-id="5d61f-110">Теперь все приложения должны использовать директиву include *Winsock2. h* в исходных файлах приложения Winsock.</span><span class="sxs-lookup"><span data-stu-id="5d61f-110">All applications should now use use the include *Winsock2.h* directive in Winsock application source files.</span></span>

<span data-ttu-id="5d61f-111">Файл заголовка *Winsock2. h* содержит большинство функций, структур и определений Winsock.</span><span class="sxs-lookup"><span data-stu-id="5d61f-111">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="5d61f-112">Файл заголовка *Ws2tcpip. h* содержит определения, появившиеся в документе о приложении WinSock 2 Protocol-Specific для TCP/IP, который включает более новые функции и структуры, используемые для получения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="5d61f-112">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span> <span data-ttu-id="5d61f-113">К ним относятся семейство функций [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) , которые обеспечивают разрешение имен для адресов IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="5d61f-113">These include the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions that provide name resolution for both IPv4 or IPv6 addresses.</span></span> <span data-ttu-id="5d61f-114">Файл заголовка *Ws2tcpip. h* необходим только в том случае, если приложению требуются эти функции именования, не зависящие от IP.</span><span class="sxs-lookup"><span data-stu-id="5d61f-114">The *Ws2tcpip.h* header file is only needed if these IP-agnostic naming functions are required by the application.</span></span>

<span data-ttu-id="5d61f-115">Файл заголовка *мсвсокк. h* содержит определения для расширений, относящихся к Майкрософт, для сокетов Windows Sockets 2 (например,[**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex)и [**коннектекс**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)).</span><span class="sxs-lookup"><span data-stu-id="5d61f-115">The *Mswsock.h* header file contains definitions for Microsoft-specific extensions to the Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), and [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), for example).</span></span> <span data-ttu-id="5d61f-116">Файл заголовка *мсвсокк. h* обычно не требуется, если приложение не использует эти расширения, относящиеся к Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5d61f-116">The *Mswsock.h* header file is not normally needed unless these Microsoft-specific extensions are used by the application.</span></span>

<span data-ttu-id="5d61f-117">Заголовочный файл *Winsock2. h* внутренне включает основные элементы из файла заголовков *Windows. h* , поэтому \# в приложениях Winsock обычно отсутствует строка include для файла заголовка *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="5d61f-117">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="5d61f-118">Если \# для файла заголовка *Windows. h* требуется строка include, перед ней следует \# указать макрос define Win32 \_ экономичное \_ и \_ среднее.</span><span class="sxs-lookup"><span data-stu-id="5d61f-118">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="5d61f-119">По историческим причинам заголовок *Windows. h* по умолчанию включает в себя файл заголовка *Winsock. h* для сокетов Windows 1,1.</span><span class="sxs-lookup"><span data-stu-id="5d61f-119">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="5d61f-120">Объявления в файле заголовка *Winsock. h* конфликтуют с объявлениями в файле заголовков *Winsock2. h* , который требуется для Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="5d61f-120">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.</span></span> <span data-ttu-id="5d61f-121">\_Макрос экономичного \_ и \_ среднего значения Win32 предотвращает включение *библиотеки Winsock. h* в заголовок *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="5d61f-121">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="5d61f-122">Пример, иллюстрирующий это, показан ниже.</span><span class="sxs-lookup"><span data-stu-id="5d61f-122">An example illustrating this is shown below.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="5d61f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5d61f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d61f-124">Создание базового приложения Winsock</span><span class="sxs-lookup"><span data-stu-id="5d61f-124">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> <dt>

[<span data-ttu-id="5d61f-125">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="5d61f-125">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="5d61f-126">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="5d61f-126">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="5d61f-127">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="5d61f-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
