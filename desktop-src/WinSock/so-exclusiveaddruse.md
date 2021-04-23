---
description: '\_Параметр ексклусивеаддрусе Socket предотвращает принудительное привязку других сокетов к тому же адресу и порту.'
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Параметр SO_EXCLUSIVEADDRUSE Socket (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701501"
---
# <a name="so_exclusiveaddruse-socket-option"></a><span data-ttu-id="4b4b8-103">SO, \_ параметр ексклусивеаддрусе Socket</span><span class="sxs-lookup"><span data-stu-id="4b4b8-103">SO\_EXCLUSIVEADDRUSE socket option</span></span>

<span data-ttu-id="4b4b8-104">\_Параметр ексклусивеаддрусе Socket предотвращает принудительное привязку других сокетов к тому же адресу и порту.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-104">The SO\_EXCLUSIVEADDRUSE socket option prevents other sockets from being forcibly bound to the same address and port.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b4b8-105">Syntax</span></span>

<span data-ttu-id="4b4b8-106">Параметр SO \_ ексклусивеаддрусе предотвращает принудительное связывание других сокетов с одним и тем же адресом и портом. практика, включенная с помощью \_ параметра so реусеаддр Socket.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-106">The SO\_EXCLUSIVEADDRUSE option prevents other sockets from being forcibly bound to the same address and port, a practice enabled by the SO\_REUSEADDR socket option.</span></span> <span data-ttu-id="4b4b8-107">Такое повторное использование может быть выполнено вредоносными приложениями для нарушения работы приложения.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-107">Such reuse can be executed by malicious applications to disrupt the application.</span></span> <span data-ttu-id="4b4b8-108">\_Параметр ексклусивеаддрусе очень удобен для системных служб, которым требуется высокий уровень доступности.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-108">The SO\_EXCLUSIVEADDRUSE option is very useful to system services requiring high availability.</span></span>

<span data-ttu-id="4b4b8-109">В следующем примере кода показана установка этого параметра.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-109">The following code example illustrates setting this option.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



<span data-ttu-id="4b4b8-110">Чтобы обеспечить любой результат, \_ перед вызовом функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) необходимо задать параметр so ексклусиваддрусе (это также относится к \_ параметру so реусеаддр).</span><span class="sxs-lookup"><span data-stu-id="4b4b8-110">To have any effect, the SO\_EXCLUSIVADDRUSE option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called (this also applies to the SO\_REUSEADDR option).</span></span> <span data-ttu-id="4b4b8-111">В таблице 1 перечислены последствия установки \_ параметра so ексклусивеаддрусе.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-111">Table 1 lists the effects of setting the SO\_EXCLUSIVEADDRUSE option.</span></span> <span data-ttu-id="4b4b8-112">Подстановочный знак указывает на привязку к подстановочному адресу, например 0.0.0.0 для IPv4 и:: для IPv6.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-112">Wildcard indicates binding to the wildcard address, such as 0.0.0.0 for IPv4 and :: for IPv6.</span></span> <span data-ttu-id="4b4b8-113">Особая указывает на привязку к определенному интерфейсу, например привязку IP-адреса, назначенного адаптеру.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-113">Specific indicates binding to a specific interface, such as binding an IP address assigned to an adapter.</span></span> <span data-ttu-id="4b4b8-114">Specific2 Указывает привязку к определенному адресу, отличному от адреса, связанного с в конкретном случае.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-114">Specific2 indicates binding to a specific address other than the address bound to in the Specific case.</span></span>

> [!Note]  
> <span data-ttu-id="4b4b8-115">Вариант Specific2 применяется только в том случае, если первая привязка выполняется с конкретным адресом. для случая, когда первый сокет привязан к подстановочному знаку, запись для конкретного охватывает все конкретные варианты адресов.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-115">The Specific2 case is applicable only when the first bind is performed with a specific address; for the case in which the first socket is bound to the wildcard, the entry for Specific covers all specific address cases.</span></span>

 

<span data-ttu-id="4b4b8-116">Например, рассмотрим компьютер с двумя интерфейсами IP: 10.0.0.1 и 10.99.99.99.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-116">For example, consider a computer with two IP interfaces: 10.0.0.1 and 10.99.99.99.</span></span> <span data-ttu-id="4b4b8-117">Если первая привязка — 10.0.0.1 и порт 5150 с \_ установленным параметром so ексклусивеаддрусе, вторая привязка к 10.99.99.99 и port 5150 с любыми параметрами или вообще не задается.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-117">If the first bind is to 10.0.0.1 and port 5150 with the SO\_EXCLUSIVEADDRUSE option set, then the second bind to 10.99.99.99 and port 5150 with any or no options set succeeds.</span></span> <span data-ttu-id="4b4b8-118">Однако если первый сокет привязан к адресу с подстановочным знаком (0.0.0.0) и порту 5150 с таким образом \_ , все последующие привязки к одному и тому же порту, независимо от IP-адреса, будут завершаться сбоем с всаеаддринусе (10048) или всаеакцесс (10013), в зависимости от того, какие параметры были заданы во втором сокете привязки.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-118">However, if the first socket is bound to the wildcard address (0.0.0.0) and port 5150 with SO\_EXCLUSIVEADDRUSE set, any subsequent bind to the same port—regardless of IP address—will fail with either WSAEADDRINUSE (10048) or WSAEACCESS (10013), depending on which options were set on the second bind socket.</span></span>

### <a name="bind-behavior-with-various-options-set"></a><span data-ttu-id="4b4b8-119">Поведение привязки с различными наборами параметров</span><span class="sxs-lookup"><span data-stu-id="4b4b8-119">Bind Behavior with Various Options Set</span></span>



<span data-ttu-id="4b4b8-120">Вторая привязка</span><span class="sxs-lookup"><span data-stu-id="4b4b8-120">Second bind</span></span>

<span data-ttu-id="4b4b8-121">Первая привязка</span><span class="sxs-lookup"><span data-stu-id="4b4b8-121">First bind</span></span>

<span data-ttu-id="4b4b8-122">*Итак, \_ ексклусивеаддрусе*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-122">*SO\_EXCLUSIVEADDRUSE*</span></span>

<span data-ttu-id="4b4b8-123">*Нет параметров* или *поэтому \_ реусеаддр*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-123">*No options* or *SO\_REUSEADDR*</span></span>

<span data-ttu-id="4b4b8-124">*Подстановочный знак*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-124">*Wildcard*</span></span>

<span data-ttu-id="4b4b8-125">*Specific*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-125">*Specific*</span></span>

<span data-ttu-id="4b4b8-126">*Подстановочный знак*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-126">*Wildcard*</span></span>

<span data-ttu-id="4b4b8-127">*Specific*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-127">*Specific*</span></span>

<span data-ttu-id="4b4b8-128">$ {ROWSPAN3} $*so \_ ексклусивеаддрусе*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4b4b8-128">${ROWSPAN3}$*SO\_EXCLUSIVEADDRUSE*${REMOVE}$</span></span>  

<span data-ttu-id="4b4b8-129">*Подстановочный знак*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-129">*Wildcard*</span></span>

<span data-ttu-id="4b4b8-130">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-130">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-131">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-131">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-132">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-132">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-133">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-133">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-134">*Specific*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-134">*Specific*</span></span>

<span data-ttu-id="4b4b8-135">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-135">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-136">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-136">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-137">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-137">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-138">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-138">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-139">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-139">*Specific2*</span></span>

<span data-ttu-id="4b4b8-140">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-140">n/a</span></span>

<span data-ttu-id="4b4b8-141">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-141">Success</span></span>

<span data-ttu-id="4b4b8-142">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-142">n/a</span></span>

<span data-ttu-id="4b4b8-143">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-143">Success</span></span>

<span data-ttu-id="4b4b8-144">$ {ROWSPAN3} $*нет параметров*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4b4b8-144">${ROWSPAN3}$*No options*${REMOVE}$</span></span>  

<span data-ttu-id="4b4b8-145">*Подстановочный знак*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-145">*Wildcard*</span></span>

<span data-ttu-id="4b4b8-146">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-146">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-147">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-147">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-148">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-148">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-149">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-149">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-150">*Specific*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-150">*Specific*</span></span>

<span data-ttu-id="4b4b8-151">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-151">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-152">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-152">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-153">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-153">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-154">Сбой (10048)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-154">Fail (10048)</span></span>

<span data-ttu-id="4b4b8-155">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-155">*Specific2*</span></span>

<span data-ttu-id="4b4b8-156">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-156">n/a</span></span>

<span data-ttu-id="4b4b8-157">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-157">Success</span></span>

<span data-ttu-id="4b4b8-158">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-158">n/a</span></span>

<span data-ttu-id="4b4b8-159">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-159">Success</span></span>

<span data-ttu-id="4b4b8-160">$ {ROWSPAN3} $*so \_ реусеаддр*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4b4b8-160">${ROWSPAN3}$*SO\_REUSEADDR*${REMOVE}$</span></span>  

<span data-ttu-id="4b4b8-161">*Подстановочный знак*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-161">*Wildcard*</span></span>

<span data-ttu-id="4b4b8-162">Сбой (10013)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-162">Fail (10013)</span></span>

<span data-ttu-id="4b4b8-163">Сбой (10013)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-163">Fail (10013)</span></span>

<span data-ttu-id="4b4b8-164">Успех\*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-164">Success\*</span></span>

<span data-ttu-id="4b4b8-165">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-165">Success</span></span>

<span data-ttu-id="4b4b8-166">*Specific*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-166">*Specific*</span></span>

<span data-ttu-id="4b4b8-167">Сбой (10013)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-167">Fail (10013)</span></span>

<span data-ttu-id="4b4b8-168">Сбой (10013)</span><span class="sxs-lookup"><span data-stu-id="4b4b8-168">Fail (10013)</span></span>

<span data-ttu-id="4b4b8-169">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-169">Success</span></span>

<span data-ttu-id="4b4b8-170">Успех\*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-170">Success\*</span></span>

<span data-ttu-id="4b4b8-171">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="4b4b8-171">*Specific2*</span></span>

<span data-ttu-id="4b4b8-172">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-172">n/a</span></span>

<span data-ttu-id="4b4b8-173">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-173">Success</span></span>

<span data-ttu-id="4b4b8-174">Недоступно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-174">n/a</span></span>

<span data-ttu-id="4b4b8-175">Успешно</span><span class="sxs-lookup"><span data-stu-id="4b4b8-175">Success</span></span>

<span data-ttu-id="4b4b8-176">\* Поведение не определено, в котором сокет будет принимать пакеты.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-176">\* The behavior is undefined as to which socket will receive packets.</span></span>



 

<span data-ttu-id="4b4b8-177">Если первая привязка задает параметр без параметров или \_ реусеаддр, а вторая привязка делает так \_ реусеаддр, то второй сокет переберет порт и поведение, относительно того, какой сокет будет принимать пакеты, не определен.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-177">In the case where the first bind sets no options or SO\_REUSEADDR, and the second bind performs a SO\_REUSEADDR, the second socket has overtaken the port and behavior regarding which socket will receive packets is undetermined.</span></span> <span data-ttu-id="4b4b8-178">Итак, \_ ексклусивеаддрусе была введена для решения этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-178">SO\_EXCLUSIVEADDRUSE was introduced to address this situation.</span></span>

<span data-ttu-id="4b4b8-179">Сокет с таким образом \_ ексклусивеаддрусе набор нельзя всегда использовать повторно сразу после закрытия сокета.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-179">A socket with SO\_EXCLUSIVEADDRUSE set cannot always be reused immediately after socket closure.</span></span> <span data-ttu-id="4b4b8-180">Например, если сокет прослушивания с установленным флагом Exclusive принимает соединение, после которого закрывается Прослушивающий сокет, другой сокет не может выполнить привязку к тому же порту, что и первый Прослушивающий сокет с флагом Exclusive, пока принятое соединение больше не будет активно.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-180">For example, if a listening socket with the exclusive flag set accepts a connection after which the listening socket is closed, another socket cannot bind to the same port as the first listening socket with the exclusive flag until the accepted connection is no longer active.</span></span>

<span data-ttu-id="4b4b8-181">Такая ситуация может быть довольно сложной; Несмотря на то, что сокет был закрыт, базовый транспорт может не завершить свое подключение.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-181">This situation can be quite complicated; even though the socket has been closed, the underlying transport may not terminate its connection.</span></span> <span data-ttu-id="4b4b8-182">Даже после закрытия сокета система должна отправить все буферизованные данные, передать корректное отключение к одноранговой сети и дождаться корректного отключения от однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-182">Even after the socket is closed, the system must send all of the buffered data, transmit a graceful disconnect to the peer, and wait for a graceful disconnect from the peer.</span></span> <span data-ttu-id="4b4b8-183">Поэтому возможно, что базовый транспорт никогда не освобождает подключение, например, когда одноранговый узел объявляет окно нулевого размера или другие подобные атаки.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-183">It is therefore possible that the underlying transport may never release the connection, such as when the peer advertises a zero-size window, or other such attacks.</span></span> <span data-ttu-id="4b4b8-184">В предыдущем примере сокет прослушивания был закрыт после того, как было принято клиентское подключение.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-184">In the previous example, the listening socket was closed after a client connection was accepted.</span></span> <span data-ttu-id="4b4b8-185">Теперь, даже если клиентское подключение закрыто, порт по-прежнему может не использоваться повторно, если подключение клиента остается в активном состоянии из-за неподтвержденных данных и т. д.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-185">Now even if the client connection is closed, the port still may not be reused if the client connection remains in an active state because of unacknowledged data, and so forth.</span></span>

<span data-ttu-id="4b4b8-186">Чтобы избежать такой ситуации, приложения должны обеспечить корректное завершение работы: вызвать [**Завершение работы**](/windows/desktop/api/winsock/nf-winsock-shutdown) с \_ флагом SD Send, а затем [](/windows/desktop/api/winsock/nf-winsock-recv) дождаться цикла приема, пока не будут возвращены нулевые байты.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-186">To avoid this situation, applications should ensure a graceful shutdown: call [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag, then wait in a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) loop until zero bytes are returned.</span></span> <span data-ttu-id="4b4b8-187">Это позволяет избежать проблемы, связанной с повторной попыткой использования порта, гарантирует, что все данные были получены одноранговым узлом, и убедитесь, что все данные успешно получены одноранговым узлом.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-187">Doing so avoids the problem associated with port reuse, guarantees all data was received by the peer, and assures the peer that all its data was successfully received.</span></span>

<span data-ttu-id="4b4b8-188">Параметр SO-1 \_ может быть установлен на сокете для предотвращения перехода порта в одно из активных состояний ожидания, однако это не рекомендуется, так как может привести к нежелательным последствиям, так как это может привести к сбросу соединения.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-188">The SO\_LINGER option may be set on a socket to prevent the port going into one of the active wait states; however, doing so is discouraged because it can lead to undesired effects, because it can cause the connection to be reset.</span></span> <span data-ttu-id="4b4b8-189">Например, если данные были получены, но еще не подтверждены одноранговым узлом, а локальный компьютер закрывает сокет с установленным параметром " \_ Ожидание", подключение сбрасывается и узел отклоняет неподтвержденные данные.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-189">For example, if data has been received but not yet acknowledged by the peer, and the local computer closes the socket with SO\_LINGER set, the connection is reset and the peer discards the unacknowledged data.</span></span> <span data-ttu-id="4b4b8-190">Кроме того, выбор подходящего времени для задержки является сложной задачей. значение слишком мало для большого количества прерванных подключений, в то время как большое время ожидания может привести к тому, что система будет уязвима к атакам типа "отказ в обслуживании", установив множество соединений и предотвращая выполнение множества потоков приложения.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-190">Also, picking a suitable time to linger is difficult; a value too small results in many aborted connections, while a large timeout can leave the system vulnerable to denial of service attacks by establishing many connections, and thereby stalling numerous application threads.</span></span>

> [!Note]  
> <span data-ttu-id="4b4b8-191">Перед закрытием сокета, использующего \_ параметр so ексклусивеаддрусе, необходимо корректно завершить работу.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-191">A socket that is using the SO\_EXCLUSIVEADDRUSE option must be shut down properly prior to closing it.</span></span> <span data-ttu-id="4b4b8-192">Несоблюдение этого требования может привести к атаке типа "отказ в обслуживании", если связанная служба должна перезапуститься.</span><span class="sxs-lookup"><span data-stu-id="4b4b8-192">Failure to do so can cause a denial of service attack if the associated service needs to restart.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b4b8-193">Требования</span><span class="sxs-lookup"><span data-stu-id="4b4b8-193">Requirements</span></span>



| <span data-ttu-id="4b4b8-194">Требование</span><span class="sxs-lookup"><span data-stu-id="4b4b8-194">Requirement</span></span> | <span data-ttu-id="4b4b8-195">Значение</span><span class="sxs-lookup"><span data-stu-id="4b4b8-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4b8-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b4b8-196">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4b8-197">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b4b8-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4b4b8-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b4b8-198">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4b8-199">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4b4b8-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b4b8-200">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4b4b8-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b4b8-201"><dt>Winsock2. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b4b8-201"><dt>Winsock2.h</dt></span></span> </dl> |



 

 




