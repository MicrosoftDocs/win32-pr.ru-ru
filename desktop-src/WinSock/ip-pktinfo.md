---
description: Позволяет приложению включать или отключать возврат сведений о пакетах функцией Всареквмсг на сокете IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: Параметр IP_PKTINFO Socket (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2134b31ead9efeb032b4ed72fcaedcd4cc9f67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343492"
---
# <a name="ip_pktinfo-socket-option"></a><span data-ttu-id="2f596-103">IP- \_ пктинфо сокета</span><span class="sxs-lookup"><span data-stu-id="2f596-103">IP\_PKTINFO socket option</span></span>

<span data-ttu-id="2f596-104">\_Параметр сокета IP пктинфо позволяет приложению включать или отключать возврат сведений о пакетах функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) на сокете IPv4.</span><span class="sxs-lookup"><span data-stu-id="2f596-104">The IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv4 socket..</span></span>

<span data-ttu-id="2f596-105">Чтобы запросить состояние этого параметра сокета, вызовите функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="2f596-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="2f596-106">Чтобы установить этот параметр, вызовите функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="2f596-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="2f596-107">Значение параметра сокета</span><span class="sxs-lookup"><span data-stu-id="2f596-107">Socket option value</span></span>

<span data-ttu-id="2f596-108">Константа, представляющая этот параметр сокета, составляет 19.</span><span class="sxs-lookup"><span data-stu-id="2f596-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f596-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f596-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="2f596-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f596-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f596-111">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2f596-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f596-112">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="2f596-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="2f596-113">*уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f596-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f596-114">Уровень, на котором определен параметр.</span><span class="sxs-lookup"><span data-stu-id="2f596-114">The level at which the option is defined.</span></span> <span data-ttu-id="2f596-115">Для этой операции используйте **\_ IP-адрес иппрото** .</span><span class="sxs-lookup"><span data-stu-id="2f596-115">Use **IPPROTO\_IP** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f596-116">*optname* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f596-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f596-117">Параметр сокета, для которого необходимо получить или задать значение.</span><span class="sxs-lookup"><span data-stu-id="2f596-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="2f596-118">\_Для этой операции используйте IP-пктинфо.</span><span class="sxs-lookup"><span data-stu-id="2f596-118">Use IP\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f596-119">*оптвал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2f596-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f596-120">Указатель на буфер, содержащий значение для устанавливаемого параметра.</span><span class="sxs-lookup"><span data-stu-id="2f596-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="2f596-121">Этот параметр должен указывать на буфер, который больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2f596-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="2f596-122">Это значение рассматривается как логическое значение с 0, которое указывает **false** (отключено), и ненулевое значение, указывающее на значение **true** (включено).</span><span class="sxs-lookup"><span data-stu-id="2f596-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="2f596-123">*оптлен* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2f596-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f596-124">Указатель на размер (в байтах) буфера *оптвал* .</span><span class="sxs-lookup"><span data-stu-id="2f596-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="2f596-125">Этот размер должен быть больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2f596-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f596-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f596-126">Return value</span></span>

<span data-ttu-id="2f596-127">Если операция завершается успешно, функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) или [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2f596-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="2f596-128">Если операция завершается неудачно, возвращается значение ошибки СОКЕТа \_ и можно получить конкретный код ошибки, вызвав [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="2f596-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="2f596-129">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="2f596-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="2f596-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2f596-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f596-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="2f596-132">Перед использованием этой функции должен быть выполнен успешный вызов [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="2f596-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="2f596-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="2f596-134">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="2f596-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="2f596-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="2f596-136">Один из параметров *оптвал* или *оптлен* указывает на память, которая не находится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f596-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="2f596-137">Эта ошибка также возвращается, если значение, на которое указывает параметр *оптлен* , меньше, чем размер значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2f596-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="2f596-138"><dt>**[всаеинпрогресс](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="2f596-139">Выполняется блокировка вызова Windows Sockets 1,1, или поставщик услуг все еще обрабатывает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="2f596-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="2f596-140"><dt>**[всаеинвал](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="2f596-141">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="2f596-141">An invalid argument was supplied.</span></span> <span data-ttu-id="2f596-142">Эта ошибка возвращается, если параметр *уровня* неизвестен или недопустим.</span><span class="sxs-lookup"><span data-stu-id="2f596-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="2f596-143">В Windows Vista и более поздних версиях эта ошибка также возвращается, если сокет находился в переходном состоянии.</span><span class="sxs-lookup"><span data-stu-id="2f596-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2f596-144"><dt>**[всаенопротупт](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="2f596-145">Параметр неизвестен или не поддерживается указанным семейством протоколов.</span><span class="sxs-lookup"><span data-stu-id="2f596-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="2f596-146">Эта ошибка возвращается, если параметр *типа* для дескриптора сокета, переданного в параметре *s* , не **Сокк \_ дграм** или **Сокк \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="2f596-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="2f596-147"><dt>**[всаенотсокк](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="2f596-148">Дескриптор не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="2f596-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="2f596-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f596-149">Remarks</span></span>

<span data-ttu-id="2f596-150">Функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , вызываемая с \_ параметром сокета IP пктинфо, позволяет приложению определить, должны ли сведения о пакете возвращаться функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)для сокета IPv4.</span><span class="sxs-lookup"><span data-stu-id="2f596-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IP\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv4 socket.</span></span>

<span data-ttu-id="2f596-151">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , вызываемая с \_ параметром сокета IP пктинфо, позволяет приложению включать или отключать возврат сведений о пакетах функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="2f596-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="2f596-152">Параметр IP \_ пктинфо для сокета по умолчанию отключен (имеет значение **false**).</span><span class="sxs-lookup"><span data-stu-id="2f596-152">The IP\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="2f596-153">Если этот параметр сокета включен на сокете IPv4 типа **Сокк \_ Дграм** или **сокк \_ RAW**, функция [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) возвращает сведения о пакете в структуре [**всамсг**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) , на которую указывает параметр *лпмсг* .</span><span class="sxs-lookup"><span data-stu-id="2f596-153">When this socket option is enabled on an IPv4 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="2f596-154">Один из объектов данных элемента управления в возвращенной структуре **всамсг** будет содержать структуру [**в \_ пктинфо**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) , используемую для хранения полученных сведений об адресе пакета.</span><span class="sxs-lookup"><span data-stu-id="2f596-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="2f596-155">Для датаграмм, полученных функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) по протоколу IPv4, элемент **управления** полученной структуры [**всамсг**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) будет содержать структуру [**всабуф**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) , содержащую структуру **всакмсгхдр** .</span><span class="sxs-lookup"><span data-stu-id="2f596-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv4, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="2f596-156">Элемент **\_ уровня КМСГ** этой структуры **всакмсгхдр** будет содержать **иппрото \_ IP**, член **\_ типа КМСГ** этой структуры будет содержать **IP- \_ пктинфо**, а элемент **\_ данных КМСГ** будет содержать [**в \_ пктинфо**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) структуру, используемую для хранения полученной информации об адресе пакета IPv4.</span><span class="sxs-lookup"><span data-stu-id="2f596-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IP**, the **cmsg\_type** member of this structure would contain **IP\_PKTINFO**, and the **cmsg\_data** member would contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received IPv4 packet address information.</span></span> <span data-ttu-id="2f596-157">Адресом IPv4 в структуре **в \_ Пктинфо** является IPv4-адрес, с которого получен пакет.</span><span class="sxs-lookup"><span data-stu-id="2f596-157">The IPv4 address in the **in\_pktinfo** structure is the IPv4 address from which the packet was received.</span></span>

<span data-ttu-id="2f596-158">Для сокета датаграмм с двумя стеками, если приложению требуется функция [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) , возвращающая сведения о пакете в структуре [**всамсг**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) для датаграмм, полученных по протоколу IPv4, то \_ параметр сокета IP пктинфо должен быть установлен в значение true на сокете.</span><span class="sxs-lookup"><span data-stu-id="2f596-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then IP\_PKTINFO socket option must be set to true on the socket.</span></span> <span data-ttu-id="2f596-159">Если только параметр [IPv6 \_ пктинфо](ipv6-pktinfo.md) имеет значение true для сокета, сведения о пакете будут предоставлены для датаграмм, полученных по протоколу IPv6, но могут не предоставляться для датаграмм, полученных по протоколу IPv4.</span><span class="sxs-lookup"><span data-stu-id="2f596-159">If only the [IPV6\_PKTINFO](ipv6-pktinfo.md) option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="2f596-160">Если приложение пытается установить \_ параметр сокета IP пктинфо для сокета датаграмм с двойным стеком и протокол IPv4 отключен в системе, то функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) завершится ошибкой, а [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) вернет ошибку [всаеинвал](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="2f596-160">If an application tries to set the IP\_PKTINFO socket option on a dual-stack datagram socket and IPv4 is disabled on the system, then the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function will fail and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) will return with an error of [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="2f596-161">Эта же ошибка также возвращается функцией **сетсоккопт** в результате других ошибок.</span><span class="sxs-lookup"><span data-stu-id="2f596-161">This same error is also returned by the **setsockopt** function as a result of other errors.</span></span> <span data-ttu-id="2f596-162">Если приложение пытается установить \_ параметр сокета IP-уровня иппрото на сокете с двойным стеком и завершается с помощью [всаеинвал](windows-sockets-error-codes-2.md), то приложение должно определить, отключена ли на локальном компьютере IPv4.</span><span class="sxs-lookup"><span data-stu-id="2f596-162">If an application tries to set an IPPROTO\_IP level socket option on a dual-stack socket and it fails with [WSAEINVAL](windows-sockets-error-codes-2.md), then the application should determine if IPv4 is disabled on the local computer.</span></span> <span data-ttu-id="2f596-163">Один из методов, который можно использовать для определения того, включен или отключен протокол IPv4, заключается в вызове функции [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) с параметром *AF* , установленным в AF \_ INET для попытки и создания сокета IPv4.</span><span class="sxs-lookup"><span data-stu-id="2f596-163">One method that can be used to detect if IPv4 is enabled or disabled is to call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function with the *af* parameter set to AF\_INET to try and create an IPv4 socket.</span></span> <span data-ttu-id="2f596-164">Если функция **сокета** завершается с ошибкой и **Всажетластеррор** возвращает ошибку [всаеафносуппорт](windows-sockets-error-codes-2.md), это означает, что протокол IPv4 не включен.</span><span class="sxs-lookup"><span data-stu-id="2f596-164">If the **socket** function fails and **WSAGetLastError** returns an error of [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), then it means IPv4 is not enabled.</span></span> <span data-ttu-id="2f596-165">В этом случае ошибка функции **сетсоккопт** при попытке установить \_ параметр сокета IP-пктинфо может быть проигнорирована приложением.</span><span class="sxs-lookup"><span data-stu-id="2f596-165">In this case, a **setsockopt** function failure when attempting to set the IP\_PKTINFO socket option can be ignored by the application.</span></span> <span data-ttu-id="2f596-166">В противном случае при попытке установить \_ параметр сокета IP пктинфо следует считать непредвиденной ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2f596-166">Otherwise a failure when attempting to set the IP\_PKTINFO socket option should be treated as an unexpected error.</span></span>

<span data-ttu-id="2f596-167">Обратите внимание, что заголовочный файл *Ws2ipdef. h* автоматически включается в *Ws2tcpip. h* и никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="2f596-167">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f596-168">Требования</span><span class="sxs-lookup"><span data-stu-id="2f596-168">Requirements</span></span>



| <span data-ttu-id="2f596-169">Требование</span><span class="sxs-lookup"><span data-stu-id="2f596-169">Requirement</span></span> | <span data-ttu-id="2f596-170">Значение</span><span class="sxs-lookup"><span data-stu-id="2f596-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f596-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f596-171">Minimum supported client</span></span><br/> | <span data-ttu-id="2f596-172">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2f596-172">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="2f596-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f596-173">Minimum supported server</span></span><br/> | <span data-ttu-id="2f596-174">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f596-174">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2f596-175">Header</span><span class="sxs-lookup"><span data-stu-id="2f596-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f596-176"><dt>Ws2ipdef. h (включение Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f596-176"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f596-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f596-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f596-178">Сокеты с двумя стеками</span><span class="sxs-lookup"><span data-stu-id="2f596-178">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="2f596-179">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="2f596-179">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="2f596-180">**в \_ пктинфо**</span><span class="sxs-lookup"><span data-stu-id="2f596-180">**in\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[<span data-ttu-id="2f596-181">**\_Параметры IP-сокета иппрото**</span><span class="sxs-lookup"><span data-stu-id="2f596-181">**IPPROTO\_IP Socket Options**</span></span>](ipproto-ip-socket-options.md)
</dt> <dt>

[<span data-ttu-id="2f596-182">\_ПКТИНФО IPv6</span><span class="sxs-lookup"><span data-stu-id="2f596-182">IPV6\_PKTINFO</span></span>](ipv6-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="2f596-183">**сетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="2f596-183">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="2f596-184">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="2f596-184">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="2f596-185">**всамсг**</span><span class="sxs-lookup"><span data-stu-id="2f596-185">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="2f596-186">**LPFN_WSARECVMSG (Всареквмсг)**</span><span class="sxs-lookup"><span data-stu-id="2f596-186">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
