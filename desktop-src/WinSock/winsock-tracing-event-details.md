---
description: Сведения о трассировке событий сети Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Сведения о трассировке событий сети Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265764"
---
# <a name="winsock-network-event-tracing-details"></a><span data-ttu-id="5ea40-103">Сведения о трассировке событий сети Winsock</span><span class="sxs-lookup"><span data-stu-id="5ea40-103">Winsock Network Event Tracing Details</span></span>

<span data-ttu-id="5ea40-104">Ниже приведены сведения о каждом из событий сети Winsock, которые можно отслеживать, и описание параметров и сведений, регистрируемых в журнале.</span><span class="sxs-lookup"><span data-stu-id="5ea40-104">The following details each of the Winsock network events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="socket-creation"></a><span data-ttu-id="5ea40-105">Создание сокета</span><span class="sxs-lookup"><span data-stu-id="5ea40-105">Socket Creation</span></span>

<span data-ttu-id="5ea40-106">ИД события = 1</span><span class="sxs-lookup"><span data-stu-id="5ea40-106">Event ID = 1</span></span>

<span data-ttu-id="5ea40-107">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-107">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-108">Для создания сокетов отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-108">The following Winsock events are traced for socket creation:</span></span>

-   <span data-ttu-id="5ea40-109">Дескрипторы сокетов, созданные вызовами функций [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) или [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-109">Socket handles created by calls to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) functions.</span></span>
-   <span data-ttu-id="5ea40-110">Принятые дескрипторы сокетов для прослушивающих сокетов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-110">Accepted socket handles on listening sockets.</span></span>
-   <span data-ttu-id="5ea40-111">Дескрипторы сокетов, созданные с помощью вызовов функции [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-111">Socket handles created by calls to the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="5ea40-112">Дескрипторы сокетов повторно используются вызовами функций [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex) или [**коннектекс**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-112">Socket handles re-used by calls to the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) or [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) functions.</span></span>

<span data-ttu-id="5ea40-113">Для события создания сокета регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-113">The following parameters are logged for a socket creation event:</span></span>



| <span data-ttu-id="5ea40-114">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-114">Parameter</span></span>                                                                                                        | <span data-ttu-id="5ea40-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="5ea40-117">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-117">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>             | <span data-ttu-id="5ea40-119">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-119">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>соккеттипе</span><span class="sxs-lookup"><span data-stu-id="5ea40-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span></span><br/>     | <span data-ttu-id="5ea40-121">Тип сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-121">The type of the socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ea40-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>См</span><span class="sxs-lookup"><span data-stu-id="5ea40-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocol</span></span><br/>             | <span data-ttu-id="5ea40-123">Протокол сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-123">The protocol of the socket.</span></span><br/>                                                 |
| <span data-ttu-id="5ea40-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>усермодепид</span><span class="sxs-lookup"><span data-stu-id="5ea40-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span></span><br/> | <span data-ttu-id="5ea40-125">Идентификатор процесса пользовательского режима, который создал сокет.</span><span class="sxs-lookup"><span data-stu-id="5ea40-125">The user-mode process ID that created the socket.</span></span><br/>                           |



 

## <a name="socket-bind"></a><span data-ttu-id="5ea40-126">Привязка сокета</span><span class="sxs-lookup"><span data-stu-id="5ea40-126">Socket Bind</span></span>

<span data-ttu-id="5ea40-127">ИД события = 2 (IPv4), ИД события = 3 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-127">Event ID = 2 (IPv4), Event ID = 3 (IPv6)</span></span>

<span data-ttu-id="5ea40-128">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-128">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-129">Для операции привязки отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-129">The following Winsock events are traced for a bind operation:</span></span>

-   <span data-ttu-id="5ea40-130">Явная или неявная привязка маркера сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-130">Implicit or explicit binding of a socket handle.</span></span>

<span data-ttu-id="5ea40-131">Для события привязки регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-131">The following parameters are logged for a bind event:</span></span>



| <span data-ttu-id="5ea40-132">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-132">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-133">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-133">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-135">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-135">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-137">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-137">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ea40-139">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5ea40-139">The local IP address.</span></span><br/>                                                       |
| <span data-ttu-id="5ea40-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ea40-141">Номер локального IP-порта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-141">The local IP port number.</span></span><br/>                                                   |
| <span data-ttu-id="5ea40-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Состояние</span><span class="sxs-lookup"><span data-stu-id="5ea40-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="5ea40-143">Состояние или код ошибки, возвращенные для операции привязки.</span><span class="sxs-lookup"><span data-stu-id="5ea40-143">The status or error code returned for the bind operation.</span></span><br/>                   |



 

## <a name="failed-bind"></a><span data-ttu-id="5ea40-144">Сбой привязки</span><span class="sxs-lookup"><span data-stu-id="5ea40-144">Failed Bind</span></span>

<span data-ttu-id="5ea40-145">ИД события = 40</span><span class="sxs-lookup"><span data-stu-id="5ea40-145">Event ID = 40</span></span>

<span data-ttu-id="5ea40-146">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-146">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-147">Следующие события Winsock отслеживаются для неудачной операции привязки:</span><span class="sxs-lookup"><span data-stu-id="5ea40-147">The following Winsock events are traced for a failed bind operation:</span></span>

-   <span data-ttu-id="5ea40-148">Явная или неявная привязка неудачного маркера сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-148">Implicit or explicit binding of a socket handle that fails.</span></span>

<span data-ttu-id="5ea40-149">Для события привязки с ошибками регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-149">The following parameters are logged for a failed bind event:</span></span>



| <span data-ttu-id="5ea40-150">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-150">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-151">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-151">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-153">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-153">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-155">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-155">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-157">Код ошибки, возвращенный для неудачной операции привязки.</span><span class="sxs-lookup"><span data-stu-id="5ea40-157">The error code returned for the failing bind operation.</span></span><br/>                     |



 

## <a name="socket-connect"></a><span data-ttu-id="5ea40-158">Подключение к сокету</span><span class="sxs-lookup"><span data-stu-id="5ea40-158">Socket Connect</span></span>

<span data-ttu-id="5ea40-159">ИД события = 4 (IPv4), ИД события = 5 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-159">Event ID = 4 (IPv4), Event ID = 5 (IPv6)</span></span>

<span data-ttu-id="5ea40-160">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-160">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-161">Следующие события Winsock отслеживаются для запроса операции подключения (вызов функции [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**коннектекс**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**всаконнект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)или [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ):</span><span class="sxs-lookup"><span data-stu-id="5ea40-161">The following Winsock events are traced for a connect operation request (a call to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function):</span></span>

-   <span data-ttu-id="5ea40-162">Подключение сокета к назначению для сокета, ориентированного на соединение или без подключения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-162">Connecting a socket to a destination for either a connection-oriented or a connectionless socket.</span></span>

<span data-ttu-id="5ea40-163">Для события Connect регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-163">The following parameters are logged for a connect event:</span></span>



| <span data-ttu-id="5ea40-164">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-164">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-165">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-165">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-167">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-167">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-169">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-169">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ea40-171">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5ea40-171">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="5ea40-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ea40-173">Номер удаленного IP-порта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-173">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="connect-completed"></a><span data-ttu-id="5ea40-174">Подключение завершено</span><span class="sxs-lookup"><span data-stu-id="5ea40-174">Connect Completed</span></span>

<span data-ttu-id="5ea40-175">ИД события = 6</span><span class="sxs-lookup"><span data-stu-id="5ea40-175">Event ID = 6</span></span>

<span data-ttu-id="5ea40-176">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-176">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-177">Следующие события Winsock отслеживаются для выполнения подключения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-177">The following Winsock events are traced for a connect completed:</span></span>

-   <span data-ttu-id="5ea40-178">Операция подключения завершена.</span><span class="sxs-lookup"><span data-stu-id="5ea40-178">The connect operation is completed.</span></span>

<span data-ttu-id="5ea40-179">Для события "Connect Completed" регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-179">The following parameters are logged for a connect completed event:</span></span>



| <span data-ttu-id="5ea40-180">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-180">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-181">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-181">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-183">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-183">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-185">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-185">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-187">Код ошибки, возвращенный для операции подключения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-187">The error code returned for the connect operation.</span></span><br/>                          |



 

## <a name="afd-initiated-abort"></a><span data-ttu-id="5ea40-188">Прерывание AFD-Initiated</span><span class="sxs-lookup"><span data-stu-id="5ea40-188">AFD-Initiated Abort</span></span>

<span data-ttu-id="5ea40-189">ИД события = 7</span><span class="sxs-lookup"><span data-stu-id="5ea40-189">Event ID = 7</span></span>

<span data-ttu-id="5ea40-190">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-190">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-191">Следующие события Winsock отслеживаются для прерываний, инициированных Winsock, или операций отмены.</span><span class="sxs-lookup"><span data-stu-id="5ea40-191">The following Winsock events are traced for Winsock-initiated aborts or cancel operations:</span></span>

-   <span data-ttu-id="5ea40-192">Прервано из-за непрочитанных данных приема, помещенных в буфер после закрытия.</span><span class="sxs-lookup"><span data-stu-id="5ea40-192">An abort due to unread receive data buffered after close.</span></span>
-   <span data-ttu-id="5ea40-193">Прерывание после вызова функции [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) с тем, *как* параметр получил значение \_ Receive SD, и вызов функции [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) с ожидающими получением данных.</span><span class="sxs-lookup"><span data-stu-id="5ea40-193">An abort after a call to the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function with the *how* parameter set to SD\_RECEIVE and a call to the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function with receive data pending.</span></span>
-   <span data-ttu-id="5ea40-194">Прерывание после неудачной попытки очистить конечную точку.</span><span class="sxs-lookup"><span data-stu-id="5ea40-194">An abort after a failed attempt to flush the endpoint.</span></span>
-   <span data-ttu-id="5ea40-195">Прерывание после внутренней ошибки Winsock.</span><span class="sxs-lookup"><span data-stu-id="5ea40-195">An abort after an internal Winsock error occurred.</span></span>
-   <span data-ttu-id="5ea40-196">Прервано из-за подключения с ошибками, и приложение ранее запросило, что подключение было прервано в определенных обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="5ea40-196">An abort due to a connection with errors and the application previously requested that the connection be aborted on certain circumstances.</span></span> <span data-ttu-id="5ea40-197">Примером такого случая может быть приложение, которое установило НАСТОЛЬКОе \_ время ожидания, равное нулю, и в соединении остались неподтвержденные данные.</span><span class="sxs-lookup"><span data-stu-id="5ea40-197">One example of this case would be an application that set SO\_LINGER with a timeout of zero and there is still unacknowledged data on the connection.</span></span>
-   <span data-ttu-id="5ea40-198">Прерывание соединения не полностью связано с принимающей конечной точкой.</span><span class="sxs-lookup"><span data-stu-id="5ea40-198">An abort on a connection not fully associated with accepting endpoint.</span></span>
-   <span data-ttu-id="5ea40-199">Прерывание неудачного вызова функции [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) или [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-199">An abort on a failed call to the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) or [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function.</span></span>
-   <span data-ttu-id="5ea40-200">Прерывание из-за неудачной операции получения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-200">An abort due to a failed receive operation.</span></span>
-   <span data-ttu-id="5ea40-201">Прерывание из-за самонастраивающийся события.</span><span class="sxs-lookup"><span data-stu-id="5ea40-201">An abort due to a Plug and Play event.</span></span>
-   <span data-ttu-id="5ea40-202">Прерывание из-за неудачного запроса на очистку.</span><span class="sxs-lookup"><span data-stu-id="5ea40-202">An abort due to a failed flush request.</span></span>
-   <span data-ttu-id="5ea40-203">Прерывание из-за неудачного запроса на получение данных.</span><span class="sxs-lookup"><span data-stu-id="5ea40-203">An abort due to a failed expedited data receive request.</span></span>
-   <span data-ttu-id="5ea40-204">Прерывание из-за сбоя запроса на отправку.</span><span class="sxs-lookup"><span data-stu-id="5ea40-204">An abort due to a failed send request.</span></span>
-   <span data-ttu-id="5ea40-205">Прерывание из-за отмены запроса на отправку.</span><span class="sxs-lookup"><span data-stu-id="5ea40-205">An abort due to canceled send request.</span></span>
-   <span data-ttu-id="5ea40-206">Прерывание из-за отмененного вызова функции [**трансмитпаккетс**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-206">An abort due to a canceled called to the [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) function.</span></span>

<span data-ttu-id="5ea40-207">Следующие параметры регистрируются для операции аварийного завершения или отмены, инициированной Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-207">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="5ea40-208">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-208">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-209">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-209">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-211">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-211">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-213">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-213">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Оправдан</span><span class="sxs-lookup"><span data-stu-id="5ea40-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="5ea40-215">Причина операции прерывания или отмены.</span><span class="sxs-lookup"><span data-stu-id="5ea40-215">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="transport-initiated-abort"></a><span data-ttu-id="5ea40-216">Прерывание Transport-Initiated</span><span class="sxs-lookup"><span data-stu-id="5ea40-216">Transport-Initiated Abort</span></span>

<span data-ttu-id="5ea40-217">ИД события = 8</span><span class="sxs-lookup"><span data-stu-id="5ea40-217">Event ID = 8</span></span>

<span data-ttu-id="5ea40-218">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-218">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-219">Следующие события Winsock отслеживаются для операций аварийного завершения или отмены, инициированного транспортом.</span><span class="sxs-lookup"><span data-stu-id="5ea40-219">The following Winsock events are traced for transport-initiated abort or cancel operations:</span></span>

-   <span data-ttu-id="5ea40-220">Сброс, обозначенный транспортом.</span><span class="sxs-lookup"><span data-stu-id="5ea40-220">Reset indicated by the transport.</span></span>

<span data-ttu-id="5ea40-221">Следующие параметры регистрируются для операции аварийного завершения или отмены, инициированной Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-221">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="5ea40-222">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-222">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-223">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-223">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-225">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-225">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-227">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-227">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Оправдан</span><span class="sxs-lookup"><span data-stu-id="5ea40-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="5ea40-229">Причина операции прерывания или отмены.</span><span class="sxs-lookup"><span data-stu-id="5ea40-229">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="failed-send-request"></a><span data-ttu-id="5ea40-230">Не удалось отправить запрос</span><span class="sxs-lookup"><span data-stu-id="5ea40-230">Failed Send Request</span></span>

<span data-ttu-id="5ea40-231">ИД события = 9</span><span class="sxs-lookup"><span data-stu-id="5ea40-231">Event ID = 9</span></span>

<span data-ttu-id="5ea40-232">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-232">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-233">Следующие события Winsock отслеживаются на наличие ошибок в запросах [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) или [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :</span><span class="sxs-lookup"><span data-stu-id="5ea40-233">The following Winsock events are traced for errors on [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests:</span></span>

-   <span data-ttu-id="5ea40-234">Ошибки, возвращенные при неудачных запросах [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) или [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-234">Errors returned on failed [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests.</span></span>

<span data-ttu-id="5ea40-235">Для запросов send, которые приводят к ошибке, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-235">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="5ea40-236">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-236">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-237">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-237">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-239">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-239">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-241">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-241">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-243">Код ошибки, возвращенный для операции.</span><span class="sxs-lookup"><span data-stu-id="5ea40-243">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a><span data-ttu-id="5ea40-244">Неудачный запрос Всасендмсг</span><span class="sxs-lookup"><span data-stu-id="5ea40-244">Failed WsaSendMsg Request</span></span>

<span data-ttu-id="5ea40-245">ИД события = 10</span><span class="sxs-lookup"><span data-stu-id="5ea40-245">Event ID = 10</span></span>

<span data-ttu-id="5ea40-246">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-246">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-247">Следующие события Winsock отслеживаются для ошибок в запросах [**всасендмсг**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :</span><span class="sxs-lookup"><span data-stu-id="5ea40-247">The following Winsock events are traced for errors on [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests:</span></span>

-   <span data-ttu-id="5ea40-248">Ошибки, возвращенные при неудачных запросах [**всасендмсг**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-248">Errors returned on failed [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests.</span></span>

<span data-ttu-id="5ea40-249">Для запросов send, которые приводят к ошибке, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-249">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="5ea40-250">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-250">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-251">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-251">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-253">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-253">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-255">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-255">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-257">Код ошибки, возвращенный для операции.</span><span class="sxs-lookup"><span data-stu-id="5ea40-257">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recv-request"></a><span data-ttu-id="5ea40-258">Неудачный запрос recv</span><span class="sxs-lookup"><span data-stu-id="5ea40-258">Failed Recv Request</span></span>

<span data-ttu-id="5ea40-259">ИД события = 11</span><span class="sxs-lookup"><span data-stu-id="5ea40-259">Event ID = 11</span></span>

<span data-ttu-id="5ea40-260">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-260">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-261">Следующие события Winsock отслеживаются на наличие ошибок в запросах [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)или [**всареквекс**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :</span><span class="sxs-lookup"><span data-stu-id="5ea40-261">The following Winsock events are traced for errors on [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), or [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) requests:</span></span>

-   <span data-ttu-id="5ea40-262">Ошибки, возвращенные при неудачных запросах на получение.</span><span class="sxs-lookup"><span data-stu-id="5ea40-262">Errors returned on failed receive requests.</span></span>

<span data-ttu-id="5ea40-263">Для запросов send, которые приводят к ошибке, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-263">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="5ea40-264">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-264">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-265">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-265">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-267">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-267">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-269">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-269">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-271">Код ошибки, возвращенный для операции.</span><span class="sxs-lookup"><span data-stu-id="5ea40-271">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recvfrom-request"></a><span data-ttu-id="5ea40-272">Неудачный запрос Реквфром</span><span class="sxs-lookup"><span data-stu-id="5ea40-272">Failed Recvfrom Request</span></span>

<span data-ttu-id="5ea40-273">ИД события = 12</span><span class="sxs-lookup"><span data-stu-id="5ea40-273">Event ID = 12</span></span>

<span data-ttu-id="5ea40-274">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-274">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-275">Следующие события Winsock отслеживаются для ошибок в запросах [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) или [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :</span><span class="sxs-lookup"><span data-stu-id="5ea40-275">The following Winsock events are traced for errors on [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests:</span></span>

-   <span data-ttu-id="5ea40-276">Ошибки, возвращенные при неудачных запросах [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) или [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-276">Errors returned on failed [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests.</span></span>

<span data-ttu-id="5ea40-277">Для запроса [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) или [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) , который приводит к ошибке, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-277">The following parameters are logged for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) request that results in an error:</span></span>



| <span data-ttu-id="5ea40-278">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-278">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-279">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-279">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-281">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-281">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-283">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-283">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-285">Код ошибки, возвращенный для операции.</span><span class="sxs-lookup"><span data-stu-id="5ea40-285">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="socket-close"></a><span data-ttu-id="5ea40-286">Закрытие сокета</span><span class="sxs-lookup"><span data-stu-id="5ea40-286">Socket Close</span></span>

<span data-ttu-id="5ea40-287">ИД события = 13</span><span class="sxs-lookup"><span data-stu-id="5ea40-287">Event ID = 13</span></span>

<span data-ttu-id="5ea40-288">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-288">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-289">Для операций закрытия сокета отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-289">The following Winsock events are traced for socket close operations:</span></span>

-   <span data-ttu-id="5ea40-290">Маркер сокета закрыт.</span><span class="sxs-lookup"><span data-stu-id="5ea40-290">A socket handle is closed.</span></span>

<span data-ttu-id="5ea40-291">Для события закрытия сокета регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-291">The following parameters are logged for a socket close event:</span></span>



| <span data-ttu-id="5ea40-292">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-292">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-293">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-293">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-295">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-295">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-297">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-297">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-299">Возвращаемое значение для операции закрытия сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-299">The return value for the socket close operation.</span></span><br/>                            |



 

## <a name="socket-cleanup"></a><span data-ttu-id="5ea40-300">Очистка сокета</span><span class="sxs-lookup"><span data-stu-id="5ea40-300">Socket Cleanup</span></span>

<span data-ttu-id="5ea40-301">ИД события = 14</span><span class="sxs-lookup"><span data-stu-id="5ea40-301">Event ID = 14</span></span>

<span data-ttu-id="5ea40-302">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-302">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-303">Следующие события Winsock отслеживаются для операций очистки сокета (Shutdown):</span><span class="sxs-lookup"><span data-stu-id="5ea40-303">The following Winsock events are traced for socket cleanup (shutdown) operations:</span></span>

-   <span data-ttu-id="5ea40-304">Функция [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) вызывается на сокете.</span><span class="sxs-lookup"><span data-stu-id="5ea40-304">The [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function is called on a socket.</span></span>
-   <span data-ttu-id="5ea40-305">Транспорт указывает на сбой корректного отключения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-305">The transport indicates a failed graceful disconnect.</span></span>

<span data-ttu-id="5ea40-306">Для событий очистки сокета (завершения работы) или события закрытия сокета регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-306">The following parameters are logged for a socket cleanup (shutdown) or socket close event:</span></span>



| <span data-ttu-id="5ea40-307">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-307">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-308">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-308">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-310">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-310">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-312">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-312">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-314">Возвращаемое значение для операции очистки сокета (Shutdown).</span><span class="sxs-lookup"><span data-stu-id="5ea40-314">The return value for the socket cleanup (shutdown) operation.</span></span><br/>               |



 

## <a name="socket-accept"></a><span data-ttu-id="5ea40-315">Принятие сокета</span><span class="sxs-lookup"><span data-stu-id="5ea40-315">Socket Accept</span></span>

<span data-ttu-id="5ea40-316">ИД события = 15 (IPv4), ИД события = 16 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-316">Event ID = 15 (IPv4), Event ID = 16 (IPv6)</span></span>

<span data-ttu-id="5ea40-317">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-317">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-318">Следующие события Winsock отслеживаются для запроса функции [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex)или [**всаакцепт**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) :</span><span class="sxs-lookup"><span data-stu-id="5ea40-318">The following Winsock events are traced for an [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request:</span></span>

-   <span data-ttu-id="5ea40-319">Запрос функции [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex)или [**всаакцепт**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) на маркере сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-319">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request on a socket handle.</span></span>

<span data-ttu-id="5ea40-320">Для события Accept регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-320">The following parameters are logged for an accept event:</span></span>



| <span data-ttu-id="5ea40-321">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-321">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-322">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-322">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-324">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-324">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-326">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-326">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ea40-328">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5ea40-328">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="5ea40-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ea40-330">Номер удаленного IP-порта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-330">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="5ea40-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Состояние</span><span class="sxs-lookup"><span data-stu-id="5ea40-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="5ea40-332">Код состояния или ошибки, возвращенный для операции Accept.</span><span class="sxs-lookup"><span data-stu-id="5ea40-332">The status or error code returned for the accept operation.</span></span><br/>                 |



 

## <a name="accept-failed"></a><span data-ttu-id="5ea40-333">Не удалось принять</span><span class="sxs-lookup"><span data-stu-id="5ea40-333">Accept Failed</span></span>

<span data-ttu-id="5ea40-334">ИД события = 17</span><span class="sxs-lookup"><span data-stu-id="5ea40-334">Event ID = 17</span></span>

<span data-ttu-id="5ea40-335">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="5ea40-335">Level = 4 (Information)</span></span>

<span data-ttu-id="5ea40-336">Следующие события Winsock отслеживаются для неудачной операции Accept:</span><span class="sxs-lookup"><span data-stu-id="5ea40-336">The following Winsock events are traced for a failed accept operation:</span></span>

-   <span data-ttu-id="5ea40-337">Запрос [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex)или [**всаакцепт**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) для неудачного маркера сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-337">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) request on a socket handle that fails.</span></span>

<span data-ttu-id="5ea40-338">Для события принятия ошибки в журнале регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-338">The following parameters are logged for a failed accept event:</span></span>



| <span data-ttu-id="5ea40-339">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-339">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-340">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-340">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-342">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-342">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-344">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-344">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-346">Код ошибки, возвращенный для неудачной операции Accept.</span><span class="sxs-lookup"><span data-stu-id="5ea40-346">The error code returned for the failing accept operation.</span></span><br/>                   |



 

## <a name="send-posted"></a><span data-ttu-id="5ea40-347">Отправка отправлена</span><span class="sxs-lookup"><span data-stu-id="5ea40-347">Send Posted</span></span>

<span data-ttu-id="5ea40-348">ИД события = 18</span><span class="sxs-lookup"><span data-stu-id="5ea40-348">Event ID = 18</span></span>

<span data-ttu-id="5ea40-349">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-349">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-350">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-350">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-351">Следующие события Winsock отслеживаются для операций отправки и получения буфера сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-351">The following Winsock events are traced for socket send and receive buffer post operations:</span></span>

-   <span data-ttu-id="5ea40-352">Приложение отправляет сообщение отправки.</span><span class="sxs-lookup"><span data-stu-id="5ea40-352">An application posts a send.</span></span>
-   <span data-ttu-id="5ea40-353">Операция отправки завершается в Winsock.</span><span class="sxs-lookup"><span data-stu-id="5ea40-353">A send operation completes to Winsock.</span></span>

<span data-ttu-id="5ea40-354">Для операций отправки сокетов регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-354">The following parameters are logged for socket send operations:</span></span>



| <span data-ttu-id="5ea40-355">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-355">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-356">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-356">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-358">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-358">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ea40-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-360">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-360">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ea40-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>фастпас</span><span class="sxs-lookup"><span data-stu-id="5ea40-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ea40-362">Логическое значение, указывающее, использовался ли быстрый ввод-вывод в пути.</span><span class="sxs-lookup"><span data-stu-id="5ea40-362">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ea40-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ea40-364">Число буферов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-364">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ea40-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-366">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-366">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-367">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-367">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ea40-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-369">Длина буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-369">The length of the buffer.</span></span> <span data-ttu-id="5ea40-370">Для цепочек буферов Этот параметр представляет собой общее число байтов во всех буферах в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-370">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="5ea40-371">Если Фастпас имеет значение true, то адрес пользовательского режима для первого буфера в массиве буферов заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-371">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ea40-372">Если Фастпас имеет значение false, адрес буфера ядра Winsock заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-372">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="receive-posted"></a><span data-ttu-id="5ea40-373">Получение Отправлено</span><span class="sxs-lookup"><span data-stu-id="5ea40-373">Receive Posted</span></span>

<span data-ttu-id="5ea40-374">ИД события = 19</span><span class="sxs-lookup"><span data-stu-id="5ea40-374">Event ID = 19</span></span>

<span data-ttu-id="5ea40-375">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-375">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-376">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-376">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-377">Для операций записи в буфер приема сокета отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-377">The following Winsock events are traced for socket receive buffer post operations:</span></span>

-   <span data-ttu-id="5ea40-378">Приложение отправляет сообщение о приеме.</span><span class="sxs-lookup"><span data-stu-id="5ea40-378">An application posts a receive.</span></span>
-   <span data-ttu-id="5ea40-379">Операция получения завершается в Winsock.</span><span class="sxs-lookup"><span data-stu-id="5ea40-379">A receive operation completes to Winsock.</span></span>

<span data-ttu-id="5ea40-380">Для операций получения сокета регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-380">The following parameters are logged for socket receive operations:</span></span>



| <span data-ttu-id="5ea40-381">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-381">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-382">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-382">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-384">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-384">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ea40-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-386">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-386">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ea40-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>фастпас</span><span class="sxs-lookup"><span data-stu-id="5ea40-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ea40-388">Логическое значение, указывающее, использовался ли быстрый ввод-вывод в пути.</span><span class="sxs-lookup"><span data-stu-id="5ea40-388">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ea40-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ea40-390">Число буферов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-390">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ea40-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-392">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-392">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-393">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-393">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ea40-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-395">Длина буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-395">The length of the buffer.</span></span> <span data-ttu-id="5ea40-396">Для цепочек буферов Этот параметр представляет собой общее число байтов во всех буферах в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-396">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="5ea40-397">Если Фастпас имеет значение true, то адрес пользовательского режима для первого буфера в массиве буферов заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-397">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ea40-398">Если Фастпас имеет значение false, адрес буфера ядра Winsock заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-398">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recvfrom-posted"></a><span data-ttu-id="5ea40-399">Реквфром Опубликовано</span><span class="sxs-lookup"><span data-stu-id="5ea40-399">RecvFrom Posted</span></span>

<span data-ttu-id="5ea40-400">ИД события = 20</span><span class="sxs-lookup"><span data-stu-id="5ea40-400">Event ID = 20</span></span>

<span data-ttu-id="5ea40-401">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-401">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-402">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-402">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-403">Следующие события Winsock отслеживаются для операции записи в буфер [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) на сокете:</span><span class="sxs-lookup"><span data-stu-id="5ea40-403">The following Winsock events are traced for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="5ea40-404">Приложение отправляет операцию получения от.</span><span class="sxs-lookup"><span data-stu-id="5ea40-404">An application posts a receive from operation.</span></span>

<span data-ttu-id="5ea40-405">Для операции реквфром регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-405">The following parameters are logged for the recvfrom operation:</span></span>



| <span data-ttu-id="5ea40-406">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-406">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-407">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-407">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-409">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-409">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ea40-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-411">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-411">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ea40-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>фастпас</span><span class="sxs-lookup"><span data-stu-id="5ea40-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ea40-413">Логическое значение, указывающее, использовался ли быстрый ввод-вывод в пути.</span><span class="sxs-lookup"><span data-stu-id="5ea40-413">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ea40-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ea40-415">Число буферов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-415">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ea40-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-417">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-417">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-418">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-418">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ea40-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-420">Длина буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-420">The length of the buffer.</span></span> <span data-ttu-id="5ea40-421">Для цепочек буферов Этот параметр представляет собой общее число байтов во всех буферах в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-421">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="5ea40-422">Если Фастпас имеет значение true, то адрес пользовательского режима для первого буфера в массиве буферов заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-422">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ea40-423">Если Фастпас имеет значение false, адрес буфера ядра Winsock заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-423">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="sendto-posted"></a><span data-ttu-id="5ea40-424">Отправлена SendTo</span><span class="sxs-lookup"><span data-stu-id="5ea40-424">SendTo Posted</span></span>

<span data-ttu-id="5ea40-425">ИД события = 21 (IPv4), ИД события = 22 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-425">Event ID = 21 (IPv4), Event ID = 22 (IPv6)</span></span>

<span data-ttu-id="5ea40-426">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-426">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-427">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-427">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-428">Следующие события Winsock отслеживаются для операции POST в буфере [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) на сокете:</span><span class="sxs-lookup"><span data-stu-id="5ea40-428">The following Winsock events are traced for a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="5ea40-429">Приложение отправляет сообщение отправки.</span><span class="sxs-lookup"><span data-stu-id="5ea40-429">An application posts a send from.</span></span>

<span data-ttu-id="5ea40-430">Для операции [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-430">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation:</span></span>



| <span data-ttu-id="5ea40-431">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-431">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-432">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-432">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-434">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-434">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="5ea40-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-436">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-436">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="5ea40-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>фастпас</span><span class="sxs-lookup"><span data-stu-id="5ea40-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="5ea40-438">Логическое значение, указывающее, использовался ли быстрый ввод-вывод в пути.</span><span class="sxs-lookup"><span data-stu-id="5ea40-438">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="5ea40-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ea40-440">Число буферов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-440">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5ea40-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-442">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-442">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-443">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-443">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="5ea40-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-445">Длина буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-445">The length of the buffer.</span></span> <span data-ttu-id="5ea40-446">Для цепочек буферов Этот параметр представляет собой общее число байтов во всех буферах в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-446">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |
| <span data-ttu-id="5ea40-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ea40-448">Удаленный IP-адрес сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-448">The remote IP address of the socket.</span></span><br/>                                                                                            |
| <span data-ttu-id="5ea40-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ea40-450">Номер удаленного IP-порта сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-450">The remote IP port number of the socket.</span></span><br/>                                                                                        |



 

<span data-ttu-id="5ea40-451">Если Фастпас имеет значение true, то адрес пользовательского режима для первого буфера в массиве буферов заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-451">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="5ea40-452">Если Фастпас имеет значение false, адрес буфера ядра Winsock заносится в параметр buffer.</span><span class="sxs-lookup"><span data-stu-id="5ea40-452">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recv-completed"></a><span data-ttu-id="5ea40-453">Recv завершено</span><span class="sxs-lookup"><span data-stu-id="5ea40-453">Recv Completed</span></span>

<span data-ttu-id="5ea40-454">ИД события = 23</span><span class="sxs-lookup"><span data-stu-id="5ea40-454">Event ID = 23</span></span>

<span data-ttu-id="5ea40-455">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-455">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-456">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-456">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-457">Следующие события Winsock отслеживаются для завершенных операций получения сокета:</span><span class="sxs-lookup"><span data-stu-id="5ea40-457">The following Winsock events are traced for socket receive completed operations:</span></span>

-   <span data-ttu-id="5ea40-458">Операция отправки завершается транспортом.</span><span class="sxs-lookup"><span data-stu-id="5ea40-458">A send operation completes to the transport.</span></span>
-   <span data-ttu-id="5ea40-459">Операция получения завершается транспортом.</span><span class="sxs-lookup"><span data-stu-id="5ea40-459">A receive operation completes to the transport.</span></span>

<span data-ttu-id="5ea40-460">Следующие параметры регистрируются для завершения отправки или получения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-460">The following parameters are logged for a send completed or receive completed:</span></span>



| <span data-ttu-id="5ea40-461">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-461">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-462">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-462">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-464">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-464">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="5ea40-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-466">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-466">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="5ea40-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-468">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-468">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-469">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-469">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="5ea40-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-471">Длина буфера полученного байта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-471">The length of the buffer of bytes received.</span></span> <span data-ttu-id="5ea40-472">Для цепочек буферов Этот параметр представляет собой общее число байтов, полученных во всех буферах в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-472">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |



 

## <a name="send-completed"></a><span data-ttu-id="5ea40-473">Отправка завершена</span><span class="sxs-lookup"><span data-stu-id="5ea40-473">Send Completed</span></span>

<span data-ttu-id="5ea40-474">ИД события = 24</span><span class="sxs-lookup"><span data-stu-id="5ea40-474">Event ID = 24</span></span>

<span data-ttu-id="5ea40-475">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-475">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-476">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-476">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-477">Следующие события Winsock отслеживаются для завершенных операций отправки сокета:</span><span class="sxs-lookup"><span data-stu-id="5ea40-477">The following Winsock events are traced for socket send completed operations:</span></span>

-   <span data-ttu-id="5ea40-478">Операция отправки завершается транспортом.</span><span class="sxs-lookup"><span data-stu-id="5ea40-478">A send operation completes to the transport.</span></span>

<span data-ttu-id="5ea40-479">Для выполнения отправки регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-479">The following parameters are logged for a send completed:</span></span>



| <span data-ttu-id="5ea40-480">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-480">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-481">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-481">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-483">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-483">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="5ea40-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-485">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-485">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="5ea40-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-487">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-487">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-488">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-488">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="5ea40-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-490">Длина буфера отправленных байтов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-490">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="5ea40-491">Для цепочек буферов Этот параметр представляет собой общее число байтов, отправленных из всех буферов в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-491">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |



 

## <a name="sendmsg-completed"></a><span data-ttu-id="5ea40-492">Сендмсг завершено</span><span class="sxs-lookup"><span data-stu-id="5ea40-492">SendMsg Completed</span></span>

<span data-ttu-id="5ea40-493">ИД события = 25</span><span class="sxs-lookup"><span data-stu-id="5ea40-493">Event ID = 25</span></span>

<span data-ttu-id="5ea40-494">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-494">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-495">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-495">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-496">При выполнении операции POST buffer [**всасендмсг**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) в сокете отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-496">The following Winsock events are traced when a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="5ea40-497">Приложение завершает операцию [**всасендмсг**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-497">An application completes a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) operation.</span></span>

<span data-ttu-id="5ea40-498">Для завершения [**всасендмсг**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-498">The following parameters are logged for the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) completion:</span></span>



| <span data-ttu-id="5ea40-499">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-499">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-500">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-500">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-502">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-502">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="5ea40-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-504">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-504">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="5ea40-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ea40-506">Число буферов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-506">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="5ea40-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-508">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-508">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-509">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-509">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="5ea40-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-511">Длина буфера отправленных байтов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-511">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="5ea40-512">Для цепочек буферов Этот параметр представляет собой общее число байтов, отправленных из всех буферов в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-512">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="5ea40-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ea40-514">Удаленный IP-адрес сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-514">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="5ea40-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ea40-516">Номер удаленного IP-порта сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-516">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="recvfrom-completed"></a><span data-ttu-id="5ea40-517">Реквфром завершено</span><span class="sxs-lookup"><span data-stu-id="5ea40-517">RecvFrom Completed</span></span>

<span data-ttu-id="5ea40-518">ИД события = 26 (IPv4), ИД события = 27 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-518">Event ID = 26 (IPv4), Event ID = 27 (IPv6)</span></span>

<span data-ttu-id="5ea40-519">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-519">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-520">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-520">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-521">При выполнении операции POST buffer [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) в сокете отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-521">The following Winsock events are traced when a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="5ea40-522">Приложение завершает операцию [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-522">An application completes a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) operation.</span></span>

<span data-ttu-id="5ea40-523">Для завершения [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-523">The following parameters are logged for the [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) completion:</span></span>



| <span data-ttu-id="5ea40-524">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-524">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-525">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-525">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-527">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-527">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="5ea40-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-529">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-529">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="5ea40-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ea40-531">Число буферов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-531">The buffer count.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="5ea40-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-533">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-533">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-534">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-534">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="5ea40-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-536">Длина буфера полученного байта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-536">The length of the buffer of bytes received.</span></span> <span data-ttu-id="5ea40-537">Для цепочек буферов Этот параметр представляет собой общее число байтов, полученных во всех буферах в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-537">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="5ea40-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ea40-539">Удаленный IP-адрес сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-539">The remote IP address of the socket.</span></span><br/>                                                                                                     |
| <span data-ttu-id="5ea40-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ea40-541">Номер удаленного IP-порта сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-541">The remote IP port number of the socket.</span></span><br/>                                                                                                 |



 

## <a name="sendto-completed"></a><span data-ttu-id="5ea40-542">Выполнение функции SendTo завершено</span><span class="sxs-lookup"><span data-stu-id="5ea40-542">SendTo Completed</span></span>

<span data-ttu-id="5ea40-543">ИД события = 28</span><span class="sxs-lookup"><span data-stu-id="5ea40-543">Event ID = 28</span></span>

<span data-ttu-id="5ea40-544">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-544">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-545">Чтобы диагностировать повреждение буфера пользователя (например, когда приложение повторно использует тот же буфер в другом вызове Send или Receive, пока он еще используется), буфер данных записывается в журнал при его передаче в Winsock и по завершении базового транспорта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-545">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="5ea40-546">При выполнении операции POST буфера [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) на сокете отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-546">The following Winsock events are traced when a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="5ea40-547">Приложение завершает операцию [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-547">An application completes a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation.</span></span>

<span data-ttu-id="5ea40-548">Для завершения процедуры [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-548">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) completion:</span></span>



| <span data-ttu-id="5ea40-549">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-549">Parameter</span></span>                                                                                                            | <span data-ttu-id="5ea40-550">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-550">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="5ea40-552">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-552">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="5ea40-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="5ea40-554">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-554">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="5ea40-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="5ea40-556">Число буферов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-556">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="5ea40-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Двойной</span><span class="sxs-lookup"><span data-stu-id="5ea40-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="5ea40-558">Виртуальный адрес буфера.</span><span class="sxs-lookup"><span data-stu-id="5ea40-558">The virtual address of the buffer.</span></span> <span data-ttu-id="5ea40-559">Для цепочек буферов Этот параметр является виртуальным адресом первого буфера в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-559">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="5ea40-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span><span class="sxs-lookup"><span data-stu-id="5ea40-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="5ea40-561">Длина буфера отправленных байтов.</span><span class="sxs-lookup"><span data-stu-id="5ea40-561">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="5ea40-562">Для цепочек буферов Этот параметр представляет собой общее число байтов, отправленных из всех буферов в цепочке.</span><span class="sxs-lookup"><span data-stu-id="5ea40-562">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="5ea40-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="5ea40-564">Удаленный IP-адрес сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-564">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="5ea40-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="5ea40-566">Номер удаленного IP-порта сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-566">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="socket-option-set"></a><span data-ttu-id="5ea40-567">Набор параметров сокета</span><span class="sxs-lookup"><span data-stu-id="5ea40-567">Socket Option Set</span></span>

<span data-ttu-id="5ea40-568">ИД события = 29</span><span class="sxs-lookup"><span data-stu-id="5ea40-568">Event ID = 29</span></span>

<span data-ttu-id="5ea40-569">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-569">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-570">Каждый раз, когда приложение изменяет определенные значения параметров сокета и ioctl, новые значения будут занесены в журнал.</span><span class="sxs-lookup"><span data-stu-id="5ea40-570">Whenever an application changes certain socket option values and Ioctls, the new values will be logged.</span></span> <span data-ttu-id="5ea40-571">Параметры, регистрируемые в журнале, можно использовать для диагностики низкой производительности или странного поведения в приложениях.</span><span class="sxs-lookup"><span data-stu-id="5ea40-571">The options logged can be used to diagnose poor performance or strange behavior in applications.</span></span> <span data-ttu-id="5ea40-572">Для определенных параметров сокета и ioctl отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-572">The following Winsock events are traced for certain socket options and Ioctls:</span></span>

-   <span data-ttu-id="5ea40-573">Итак, \_ сндбуф изменения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-573">SO\_SNDBUF changes.</span></span>
-   <span data-ttu-id="5ea40-574">Итак, \_ рквбуф изменения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-574">SO\_RCVBUF changes.</span></span>
-   <span data-ttu-id="5ea40-575">фионбио</span><span class="sxs-lookup"><span data-stu-id="5ea40-575">FIONBIO</span></span>
-   <span data-ttu-id="5ea40-576">\_Включение \_ циклической \_ очереди в SIO</span><span class="sxs-lookup"><span data-stu-id="5ea40-576">SIO\_ENABLE\_CIRCULAR\_QUEUEING</span></span>
-   <span data-ttu-id="5ea40-577">SIO \_ UDP \_ коннресет</span><span class="sxs-lookup"><span data-stu-id="5ea40-577">SIO\_UDP\_CONNRESET</span></span>
-   <span data-ttu-id="5ea40-578">Итак, \_ убинлине</span><span class="sxs-lookup"><span data-stu-id="5ea40-578">SO\_OOBINLINE</span></span>

<span data-ttu-id="5ea40-579">Для вызовов функций [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) и [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) , которые изменяют любое из указанных выше значений, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-579">The following parameters are logged for [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function calls that change any of the above values:</span></span>



| <span data-ttu-id="5ea40-580">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-580">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-581">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-581">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-583">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-583">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-585">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-585">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Функцию</span><span class="sxs-lookup"><span data-stu-id="5ea40-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span></span><br/>         | <span data-ttu-id="5ea40-587">Измененный параметр сокета или IOCTL.</span><span class="sxs-lookup"><span data-stu-id="5ea40-587">The socket option or Ioctl that is changed.</span></span> <br/>                                |
| <span data-ttu-id="5ea40-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="5ea40-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span><br/>             | <span data-ttu-id="5ea40-589">Новое значение параметра сокета или IOCTL.</span><span class="sxs-lookup"><span data-stu-id="5ea40-589">The new value for the socket option or Ioctl.</span></span> <br/>                              |



 

## <a name="selectpoll-posted"></a><span data-ttu-id="5ea40-590">Выбор/опрос отправлен</span><span class="sxs-lookup"><span data-stu-id="5ea40-590">Select/Poll Posted</span></span>

<span data-ttu-id="5ea40-591">ИД события = 30</span><span class="sxs-lookup"><span data-stu-id="5ea40-591">Event ID = 30</span></span>

<span data-ttu-id="5ea40-592">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-592">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-593">Если приложение вызывает функцию [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-593">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="5ea40-594">Приложение отправляет запрос [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-594">Application posts a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) request.</span></span>

<span data-ttu-id="5ea40-595">Для событий [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-595">The following parameters are logged for [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) events:</span></span>



| <span data-ttu-id="5ea40-596">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-596">Parameter</span></span>                                                                                                        | <span data-ttu-id="5ea40-597">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-597">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="5ea40-599">Идентификатор процесса-владельца.</span><span class="sxs-lookup"><span data-stu-id="5ea40-599">The owning process ID.</span></span><br/>                                                                              |
| <span data-ttu-id="5ea40-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span><span class="sxs-lookup"><span data-stu-id="5ea40-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span></span><br/> | <span data-ttu-id="5ea40-601">Число дескрипторов, переданных приложением (допустимо только для инициирующего события).</span><span class="sxs-lookup"><span data-stu-id="5ea40-601">The number of handles passed in by the application (only valid on the initiating event).</span></span><br/>            |
| <span data-ttu-id="5ea40-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Счетчик</span><span class="sxs-lookup"><span data-stu-id="5ea40-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span></span><br/>                 | <span data-ttu-id="5ea40-603">Максимальное время ожидания для функции [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-603">The maximum time for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function to wait.</span></span><br/> |



 

## <a name="selectpoll-completed"></a><span data-ttu-id="5ea40-604">Выбор/Опрос завершен</span><span class="sxs-lookup"><span data-stu-id="5ea40-604">Select/Poll Completed</span></span>

<span data-ttu-id="5ea40-605">ИД события = 31</span><span class="sxs-lookup"><span data-stu-id="5ea40-605">Event ID = 31</span></span>

<span data-ttu-id="5ea40-606">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-606">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-607">Если приложение вызывает функцию [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-607">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="5ea40-608">Winsock завершает вызов [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-608">Winsock completes a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) call.</span></span>

<span data-ttu-id="5ea40-609">При завершении операции [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) в журнале регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-609">The following parameters are logged when a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation completes:</span></span>



| <span data-ttu-id="5ea40-610">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-610">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-611">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-611">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-613">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-613">The kernel EPROCESS structure address for the process.</span></span><br/>                                              |
| <span data-ttu-id="5ea40-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-615">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-615">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                         |
| <span data-ttu-id="5ea40-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>План</span><span class="sxs-lookup"><span data-stu-id="5ea40-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="5ea40-617">Код ошибки, возвращенный для операции [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) или [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-617">The error code returned for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation.</span></span><br/> |



 

## <a name="wsaeventselect"></a><span data-ttu-id="5ea40-618">всаевентселект</span><span class="sxs-lookup"><span data-stu-id="5ea40-618">WSAEventSelect</span></span>

<span data-ttu-id="5ea40-619">ИД события = 32</span><span class="sxs-lookup"><span data-stu-id="5ea40-619">Event ID = 32</span></span>

<span data-ttu-id="5ea40-620">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-620">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-621">При вызове приложением функции [**всаевентселект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-621">The following Winsock events are traced when an application calls the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function:</span></span>

-   <span data-ttu-id="5ea40-622">Регистрирует маску событий, переданную в функцию [**всаевентселект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="5ea40-622">Log the event mask passed in the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

<span data-ttu-id="5ea40-623">Для вызовов функций [**всаевентселект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-623">The following parameters are logged for [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function calls:</span></span>



| <span data-ttu-id="5ea40-624">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-624">Parameter</span></span>                                                                                                | <span data-ttu-id="5ea40-625">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-625">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>         | <span data-ttu-id="5ea40-627">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-627">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>     | <span data-ttu-id="5ea40-629">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-629">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>евентмаск</span><span class="sxs-lookup"><span data-stu-id="5ea40-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span></span><br/> | <span data-ttu-id="5ea40-631">Значение маски событий.</span><span class="sxs-lookup"><span data-stu-id="5ea40-631">The value for the event mask.</span></span> <br/>                                              |



 

## <a name="dropped-datagram"></a><span data-ttu-id="5ea40-632">Удалена датаграмма</span><span class="sxs-lookup"><span data-stu-id="5ea40-632">Dropped Datagram</span></span>

<span data-ttu-id="5ea40-633">ИД события = 33 (IPv4), ИД события = 34 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-633">Event ID = 33 (IPv4), Event ID = 34 (IPv6)</span></span>

<span data-ttu-id="5ea40-634">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-634">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-635">Для диагностики проблем, связанных с приложениями датаграмм, отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-635">To help diagnose issues around datagram applications, the following Winsock events are traced:</span></span>

-   <span data-ttu-id="5ea40-636">При поступлении датаграммы, и она удаляется из-за недостатка места в буфере.</span><span class="sxs-lookup"><span data-stu-id="5ea40-636">When a datagram arrives and it is dropped do to insufficient buffer space.</span></span>
-   <span data-ttu-id="5ea40-637">На подключенной датаграмме, если данные поступают из источника, отличного от подключенного назначения.</span><span class="sxs-lookup"><span data-stu-id="5ea40-637">On a connected datagram, if data arrives from a source other than connected destination.</span></span>

<span data-ttu-id="5ea40-638">Для сброшенных датаграмм записываются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-638">The following parameters are logged for dropped datagrams:</span></span>



| <span data-ttu-id="5ea40-639">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-639">Parameter</span></span>                                                                                                    | <span data-ttu-id="5ea40-640">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-640">Description</span></span>                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>             | <span data-ttu-id="5ea40-642">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-642">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>         | <span data-ttu-id="5ea40-644">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-644">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span><span class="sxs-lookup"><span data-stu-id="5ea40-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span></span><br/> | <span data-ttu-id="5ea40-646">Размер пакета, который был удален.</span><span class="sxs-lookup"><span data-stu-id="5ea40-646">The size of the packet that was dropped.</span></span> <br/>                                   |
| <span data-ttu-id="5ea40-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>             | <span data-ttu-id="5ea40-648">IP-адрес источника пакета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-648">The IP address of the source of the packet.</span></span> <br/>                                |
| <span data-ttu-id="5ea40-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                         | <span data-ttu-id="5ea40-650">Номер IP-порта источника пакета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-650">The IP port number of the source of the packet.</span></span><br/>                             |
| <span data-ttu-id="5ea40-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Оправдан</span><span class="sxs-lookup"><span data-stu-id="5ea40-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>                 | <span data-ttu-id="5ea40-652">Код ошибки или причина удаления пакета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-652">The error code or reason the packet was dropped.</span></span><br/>                            |



 

## <a name="connection-indicated"></a><span data-ttu-id="5ea40-653">Указанное подключение</span><span class="sxs-lookup"><span data-stu-id="5ea40-653">Connection Indicated</span></span>

<span data-ttu-id="5ea40-654">ИД события = 35 (IPv4), ИД события = 36 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-654">Event ID = 35 (IPv4), Event ID = 36 (IPv6)</span></span>

<span data-ttu-id="5ea40-655">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-655">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-656">Для указанных операций подключения отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-656">The following Winsock events are traced for connection indicated operations:</span></span>

-   <span data-ttu-id="5ea40-657">Приложение получает запрос на подключение.</span><span class="sxs-lookup"><span data-stu-id="5ea40-657">An application receives a connection request.</span></span>

<span data-ttu-id="5ea40-658">Для подключений, указанных из событий транспорта, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-658">The following parameters are logged for connections indicated from transport events:</span></span>



| <span data-ttu-id="5ea40-659">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-659">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-660">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-660">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-662">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-662">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-664">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-664">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="5ea40-666">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5ea40-666">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="5ea40-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="5ea40-668">Номер удаленного IP-порта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-668">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="data-indicated"></a><span data-ttu-id="5ea40-669">Указанные данные</span><span class="sxs-lookup"><span data-stu-id="5ea40-669">Data Indicated</span></span>

<span data-ttu-id="5ea40-670">ИД события = 37</span><span class="sxs-lookup"><span data-stu-id="5ea40-670">Event ID = 37</span></span>

<span data-ttu-id="5ea40-671">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-671">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-672">Следующие события Winsock отслеживаются для указанных операций данных:</span><span class="sxs-lookup"><span data-stu-id="5ea40-672">The following Winsock events are traced for data indicated operations:</span></span>

-   <span data-ttu-id="5ea40-673">Приложение получает данные на подключенном сокете.</span><span class="sxs-lookup"><span data-stu-id="5ea40-673">An application receives data on a connected socket.</span></span>

<span data-ttu-id="5ea40-674">Для данных, указанных из событий транспорта, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-674">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="5ea40-675">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-675">Parameter</span></span>                                                                                                                        | <span data-ttu-id="5ea40-676">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-676">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="5ea40-678">Идентификатор процесса-владельца.</span><span class="sxs-lookup"><span data-stu-id="5ea40-678">The owning process ID.</span></span><br/>                                                      |
| <span data-ttu-id="5ea40-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="5ea40-680">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-680">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Указано байт</span><span class="sxs-lookup"><span data-stu-id="5ea40-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="5ea40-682">Число байтов, полученных на сокете.</span><span class="sxs-lookup"><span data-stu-id="5ea40-682">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="data-indicated-from-transport"></a><span data-ttu-id="5ea40-683">Данные, указанные из транспорта</span><span class="sxs-lookup"><span data-stu-id="5ea40-683">Data Indicated from Transport</span></span>

<span data-ttu-id="5ea40-684">ИД события = 38 (IPv4), ИД события = 39 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="5ea40-684">Event ID = 38 (IPv4), Event ID = 39 (IPv6)</span></span>

<span data-ttu-id="5ea40-685">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-685">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-686">Для данных, указанных в операциях транспорта, отслеживаются следующие события Winsock:</span><span class="sxs-lookup"><span data-stu-id="5ea40-686">The following Winsock events are traced for data indicated from transport operations:</span></span>

-   <span data-ttu-id="5ea40-687">Приложение отправляет запрос на получение и получает данные.</span><span class="sxs-lookup"><span data-stu-id="5ea40-687">An application posts a receive request and receives data.</span></span>

<span data-ttu-id="5ea40-688">Для данных, указанных из событий транспорта, регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="5ea40-688">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="5ea40-689">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-689">Parameter</span></span>                                                                                                                        | <span data-ttu-id="5ea40-690">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-690">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="5ea40-692">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-692">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="5ea40-694">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-694">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="5ea40-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span><span class="sxs-lookup"><span data-stu-id="5ea40-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                                 | <span data-ttu-id="5ea40-696">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5ea40-696">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="5ea40-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</span><span class="sxs-lookup"><span data-stu-id="5ea40-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                             | <span data-ttu-id="5ea40-698">Номер удаленного IP-порта.</span><span class="sxs-lookup"><span data-stu-id="5ea40-698">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="5ea40-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Указано байт</span><span class="sxs-lookup"><span data-stu-id="5ea40-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="5ea40-700">Число байтов, полученных на сокете.</span><span class="sxs-lookup"><span data-stu-id="5ea40-700">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a><span data-ttu-id="5ea40-701">Отсоединение указано от транспорта</span><span class="sxs-lookup"><span data-stu-id="5ea40-701">Disconnect Indicated from Transport</span></span>

<span data-ttu-id="5ea40-702">ИД события = 41</span><span class="sxs-lookup"><span data-stu-id="5ea40-702">Event ID = 41</span></span>

<span data-ttu-id="5ea40-703">Уровень = 5 (подробный)</span><span class="sxs-lookup"><span data-stu-id="5ea40-703">Level = 5 (Verbose)</span></span>

<span data-ttu-id="5ea40-704">Следующие события Winsock отслеживаются для операций отключения, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="5ea40-704">The following Winsock events are traced for disconnect indicated operations:</span></span>

-   <span data-ttu-id="5ea40-705">Приложение получает уведомление об отключении.</span><span class="sxs-lookup"><span data-stu-id="5ea40-705">An application receives a disconnect indication.</span></span>

<span data-ttu-id="5ea40-706">Следующие параметры регистрируются для отключения от транспортных событий.</span><span class="sxs-lookup"><span data-stu-id="5ea40-706">The following parameters are logged for disconnect indicated from transport events:</span></span>



| <span data-ttu-id="5ea40-707">Параметр</span><span class="sxs-lookup"><span data-stu-id="5ea40-707">Parameter</span></span>                                                                                            | <span data-ttu-id="5ea40-708">Описание</span><span class="sxs-lookup"><span data-stu-id="5ea40-708">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea40-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Процесс</span><span class="sxs-lookup"><span data-stu-id="5ea40-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="5ea40-710">Адрес структуры ЕПРОЦЕСС ядра для процесса.</span><span class="sxs-lookup"><span data-stu-id="5ea40-710">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="5ea40-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Конечной</span><span class="sxs-lookup"><span data-stu-id="5ea40-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="5ea40-712">Адрес сокета ядра Winsock, используемый в качестве уникального идентификатора сокета.</span><span class="sxs-lookup"><span data-stu-id="5ea40-712">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5ea40-713">См. также</span><span class="sxs-lookup"><span data-stu-id="5ea40-713">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ea40-714">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="5ea40-714">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5ea40-715">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="5ea40-715">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5ea40-716">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="5ea40-716">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="5ea40-717">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="5ea40-717">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
