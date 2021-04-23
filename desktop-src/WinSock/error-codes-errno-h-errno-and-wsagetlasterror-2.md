---
description: В приложениях Winsock коды ошибок извлекаются с помощью функции Всажетластеррор, подстановка сокетов Windows для функции Windows GetLastError.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: Коды ошибок — "ошибка", "h_errno" и "Всажетластеррор"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701537"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a><span data-ttu-id="ae78b-103">Коды ошибок — код возврата, h \_ и всажетластеррор</span><span class="sxs-lookup"><span data-stu-id="ae78b-103">Error Codes - errno, h\_errno and WSAGetLastError</span></span>

<span data-ttu-id="ae78b-104">В приложениях Winsock коды ошибок извлекаются с помощью функции [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , подстановка сокетов Windows для функции Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="ae78b-104">In Winsock applications, error codes are retrieved using the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function, the Windows Sockets substitute for the Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span> <span data-ttu-id="ae78b-105">Коды ошибок, возвращаемые сокетами Windows, похожи на константы кода ошибки сокета UNIX, но все константы имеют префикс WSA.</span><span class="sxs-lookup"><span data-stu-id="ae78b-105">The error codes returned by Windows Sockets are similar to UNIX socket error code constants, but the constants are all prefixed with WSA.</span></span> <span data-ttu-id="ae78b-106">Таким образом, в приложениях Winsock возвращается код ошибки ВСАЕВАУЛДБЛОКК, а в приложениях UNIX возвращается код ошибки ЕВАУЛДБЛОКК.</span><span class="sxs-lookup"><span data-stu-id="ae78b-106">So in Winsock applications the WSAEWOULDBLOCK error code would be returned, while in UNIX applications the EWOULDBLOCK error code would be returned.</span></span>

<span data-ttu-id="ae78b-107">Коды ошибок, заданные сокетами Windows, не предоставляются *через переменную* "код ошибки".</span><span class="sxs-lookup"><span data-stu-id="ae78b-107">Error codes set by Windows Sockets are not made available through the *errno* variable.</span></span> <span data-ttu-id="ae78b-108">Кроме того, для класса **жетксбии** функций коды ошибок не становятся доступными через переменную *h н. \_*</span><span class="sxs-lookup"><span data-stu-id="ae78b-108">Additionally, for the **getXbyY** class of functions, error codes are not made available through the *h\_errno* variable.</span></span> <span data-ttu-id="ae78b-109">Функция [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) предназначена для обеспечения надежного способа для потока в многопоточном процессе получения сведений об ошибках для каждого потока.</span><span class="sxs-lookup"><span data-stu-id="ae78b-109">The [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function is intended to provide a reliable way for a thread in a multithreaded process to obtain per-thread error information.</span></span>

<span data-ttu-id="ae78b-110">Для совместимости с BIND UNIX (BSD) ранние версии Windows (Windows 95 с обновлением Windows Socket 2 и Windows 98, например) переопределяют регулярные константы BIND, обычно находящиеся в *обновлении* в формате "сбой Windows Socket".</span><span class="sxs-lookup"><span data-stu-id="ae78b-110">For compatibility with Berkeley UNIX (BSD), early versions of Windows (Windows 95 with the Windows Socket 2 Update and Windows 98, for example) redefined regular Berkeley error constants typically found in *errno.h* on BSD as the equivalent Windows Sockets WSA errors.</span></span> <span data-ttu-id="ae78b-111">Например, ЕКОННРЕФУСЕД был определен как **всаеконнрефусед** в файле заголовка *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="ae78b-111">So for example, ECONNREFUSED was defined as **WSAECONNREFUSED** in the *Winsock.h* header file.</span></span> <span data-ttu-id="ae78b-112">В последующих версиях Windows (Windows NT 3,1 и более поздних версий) эти определения были добавлены в комментарий, чтобы избежать конфликтов с использованием файла с параметром "переключать *. h* " в Microsoft C/C++ и Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ae78b-112">In subsequent versions of Windows (Windows NT 3.1 and later) these defines were commented out to avoid conflicts with *errno.h* used with Microsoft C/C++ and Visual Studio.</span></span>

<span data-ttu-id="ae78b-113">Заголовочный файл *Winsock2. h* , входящий в состав пакета средств разработки программного обеспечения (SDK) для платформы Microsoft Windows, пакета SDK и Visual Studio, по-прежнему содержит заметку в виде блока \# ifdef 0 и \# endif, который определяет коды ошибок сокета BSD так же, как и константы WSA.</span><span class="sxs-lookup"><span data-stu-id="ae78b-113">The *Winsock2.h* header file included with the Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK), and Visual Studio still contains a commented out block of defines within an \#ifdef 0 and \#endif block that define the BSD socket error codes to be the same as the WSA error constants.</span></span> <span data-ttu-id="ae78b-114">Их можно использовать для обеспечения некоторой совместимости с программированием сокетов UNIX, BSD и Linux.</span><span class="sxs-lookup"><span data-stu-id="ae78b-114">These can be used to provide some compatibility with UNIX, BSD, and Linux socket programming.</span></span> <span data-ttu-id="ae78b-115">Для совместимости с BSD приложение может изменить параметр *Winsock2. h* и раскомментировать этот блок.</span><span class="sxs-lookup"><span data-stu-id="ae78b-115">For compatibility with BSD, an application may choose to change the *Winsock2.h* and uncomment this block.</span></span> <span data-ttu-id="ae78b-116">Однако разработчикам приложений настоятельно не рекомендуется раскомментировать этот блок, так как из-за неизбежного возникновения конфликтов с ошибкой возврата *. h* в большинстве приложений.</span><span class="sxs-lookup"><span data-stu-id="ae78b-116">However, application developers are strongly discouraged from uncommenting this block because of inevitable conflicts with *errno.h* in most applications.</span></span> <span data-ttu-id="ae78b-117">Кроме того, ошибки сокета BSD определяются как значения, отличные от используемых в программах UNIX, BSD и Linux.</span><span class="sxs-lookup"><span data-stu-id="ae78b-117">Also, the BSD socket errors are defined to very different values than are used in UNIX, BSD, and Linux programs.</span></span> <span data-ttu-id="ae78b-118">Разработчикам приложений настоятельно рекомендуется использовать постоянные ошибки WSA в приложениях сокетов.</span><span class="sxs-lookup"><span data-stu-id="ae78b-118">Application developers are very strongly encouraged to use the WSA error constants in socket applications.</span></span>

<span data-ttu-id="ae78b-119">Эти определения остаются в комментарии в заголовке *Winsock2. h* в \# блоке ifdef 0 и \# endif.</span><span class="sxs-lookup"><span data-stu-id="ae78b-119">These defines remain commented out in the *Winsock2.h* header within an \#ifdef 0 and \#endif block.</span></span> <span data-ttu-id="ae78b-120">Если разработчик приложения настаивает на использовании кодов ошибок BSD для совместимости, то приложение может включить строку в форму:</span><span class="sxs-lookup"><span data-stu-id="ae78b-120">If an application developer insists on using the BSD error codes for compatibility, then an application may choose to include a line of the form:</span></span>


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



<span data-ttu-id="ae78b-121">Это позволяет сетевому коду, написанному для использования глобального кода, правильно работать в *среде с одним* потоком.</span><span class="sxs-lookup"><span data-stu-id="ae78b-121">This allows networking code which was written to use the global *errno* to work correctly in a single-threaded environment.</span></span> <span data-ttu-id="ae78b-122">Есть некоторые очень серьезные недостатки.</span><span class="sxs-lookup"><span data-stu-id="ae78b-122">There are some very serious drawbacks.</span></span> <span data-ttu-id="ae78b-123">Если исходный файл включает в себя код, который проверяет, что используется *как для* сокетов, так и для функций, не являющихся сокетами, этот механизм использовать нельзя.</span><span class="sxs-lookup"><span data-stu-id="ae78b-123">If a source file includes code which inspects *errno* for both socket and non-socket functions, this mechanism cannot be used.</span></span> <span data-ttu-id="ae78b-124">Более того, приложению не может быть *присвоено новое значение.*</span><span class="sxs-lookup"><span data-stu-id="ae78b-124">Furthermore, it is not possible for an application to assign a new value to *errno*.</span></span> <span data-ttu-id="ae78b-125">(В сокетах Windows для этой цели может использоваться функция [**всасетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) .)</span><span class="sxs-lookup"><span data-stu-id="ae78b-125">(In Windows Sockets, the function [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) may be used for this purpose.)</span></span>

<span data-ttu-id="ae78b-126">Типичный стиль BSD</span><span class="sxs-lookup"><span data-stu-id="ae78b-126">Typical BSD Style</span></span>


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="ae78b-127">Предпочтительный стиль</span><span class="sxs-lookup"><span data-stu-id="ae78b-127">Preferred Style</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="ae78b-128">Несмотря на то, что для обеспечения совместимости предоставляются константы ошибок, соответствующие сокетам Berkeley 4,3, приложениям настоятельно рекомендуется использовать определения кодов ошибок WSA.</span><span class="sxs-lookup"><span data-stu-id="ae78b-128">Although error constants consistent with Berkeley Sockets 4.3 are provided for compatibility purposes, applications are strongly encouraged to use the WSA error code definitions.</span></span> <span data-ttu-id="ae78b-129">Это обусловлено тем, что коды ошибок, возвращаемые определенными функциями сокетов Windows, относятся к стандартному диапазону кодов ошибок, как определено в Microsoft C ©.</span><span class="sxs-lookup"><span data-stu-id="ae78b-129">This is because error codes returned by certain Windows Sockets functions fall into the standard range of error codes as defined by Microsoft C©.</span></span> <span data-ttu-id="ae78b-130">Таким образом, более эффективной версией предыдущего фрагмента исходного кода является:</span><span class="sxs-lookup"><span data-stu-id="ae78b-130">Thus, a better version of the preceding source code fragment is:</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



<span data-ttu-id="ae78b-131">Исходная спецификация Winsock 1,1, определенная в 1995, рекомендует набор кодов ошибок и список возможных ошибок, которые могут быть возвращены в результате каждой функции.</span><span class="sxs-lookup"><span data-stu-id="ae78b-131">The original Winsock 1.1 specification defined in 1995 recommended a set of error codes, and listed the possible errors that can be returned as a result of each function.</span></span> <span data-ttu-id="ae78b-132">Windows Sockets 2 добавил функции и функции с другими кодами ошибок сокетов Windows, возвращаемыми в дополнение к тем, которые перечислены в исходной спецификации Winsock.</span><span class="sxs-lookup"><span data-stu-id="ae78b-132">Windows Sockets 2 added functions and features with other Windows Sockets error codes returned in addition to those listed in the original Winsock specification.</span></span> <span data-ttu-id="ae78b-133">В течение времени были добавлены дополнительные функции для улучшения использования Winsock для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="ae78b-133">Additional functions have been added over time to enhance Winsock for use by developers.</span></span> <span data-ttu-id="ae78b-134">Например, добавлены новые функции службы имен (например,[**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)), поддерживающие IPv6 и IPv4 в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ae78b-134">For example, new name service functions ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), for example) were added that support both IPv6 and IPv4 on Windows XP and later.</span></span> <span data-ttu-id="ae78b-135">Некоторые из старых функций службы имен с протоколом IPv4 (например, класс **жетксбии** функций) являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="ae78b-135">Some of the older IPv4-only name service functions (the **getXbyY** class of functions, for example) have been deprecated.</span></span>

<span data-ttu-id="ae78b-136">Полный список возможных кодов ошибок, возвращаемых функциями сокетов Windows, приведен в разделе [коды ошибок сокетов Windows](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="ae78b-136">A complete list of possible error codes returned by Windows Sockets functions is given in the section on [Windows Sockets Error Codes](windows-sockets-error-codes-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae78b-137">См. также</span><span class="sxs-lookup"><span data-stu-id="ae78b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae78b-138">Обработка ошибок Winsock</span><span class="sxs-lookup"><span data-stu-id="ae78b-138">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="ae78b-139">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="ae78b-139">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="ae78b-140">Коды ошибок сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="ae78b-140">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="ae78b-141">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="ae78b-141">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
