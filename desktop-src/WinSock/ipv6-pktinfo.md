---
description: Позволяет приложению включать или отключать возврат сведений о пакетах функцией Всареквмсг на сокете IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: Параметр IPV6_PKTINFO Socket (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692283"
---
# <a name="ipv6_pktinfo-socket-option"></a><span data-ttu-id="631d2-103">\_Параметр сокета ПКТИНФО IPv6</span><span class="sxs-lookup"><span data-stu-id="631d2-103">IPV6\_PKTINFO socket option</span></span>

<span data-ttu-id="631d2-104">\_Параметр сокета ПКТИНФО IPv6 позволяет приложению включать или отключать возврат сведений о пакетах функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) на сокете IPv6.</span><span class="sxs-lookup"><span data-stu-id="631d2-104">The IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv6 socket..</span></span>

<span data-ttu-id="631d2-105">Чтобы запросить состояние этого параметра сокета, вызовите функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="631d2-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="631d2-106">Чтобы установить этот параметр, вызовите функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="631d2-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="631d2-107">Значение параметра сокета</span><span class="sxs-lookup"><span data-stu-id="631d2-107">Socket option value</span></span>

<span data-ttu-id="631d2-108">Константа, представляющая этот параметр сокета, составляет 19.</span><span class="sxs-lookup"><span data-stu-id="631d2-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="631d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="631d2-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="631d2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="631d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="631d2-111">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="631d2-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="631d2-112">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="631d2-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="631d2-113">*уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="631d2-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="631d2-114">Уровень, на котором определен параметр.</span><span class="sxs-lookup"><span data-stu-id="631d2-114">The level at which the option is defined.</span></span> <span data-ttu-id="631d2-115">Для этой операции используйте **\_ IPv6 иппрото** .</span><span class="sxs-lookup"><span data-stu-id="631d2-115">Use **IPPROTO\_IPV6** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="631d2-116">*optname* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="631d2-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="631d2-117">Параметр сокета, для которого необходимо получить или задать значение.</span><span class="sxs-lookup"><span data-stu-id="631d2-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="631d2-118">\_Для этой операции используйте ПКТИНФО IPv6.</span><span class="sxs-lookup"><span data-stu-id="631d2-118">Use IPV6\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="631d2-119">*оптвал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="631d2-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="631d2-120">Указатель на буфер, содержащий значение для устанавливаемого параметра.</span><span class="sxs-lookup"><span data-stu-id="631d2-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="631d2-121">Этот параметр должен указывать на буфер, который больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="631d2-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="631d2-122">Это значение рассматривается как логическое значение с 0, которое указывает **false** (отключено), и ненулевое значение, указывающее на значение **true** (включено).</span><span class="sxs-lookup"><span data-stu-id="631d2-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="631d2-123">*оптлен* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="631d2-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="631d2-124">Указатель на размер (в байтах) буфера *оптвал* .</span><span class="sxs-lookup"><span data-stu-id="631d2-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="631d2-125">Этот размер должен быть больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="631d2-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="631d2-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="631d2-126">Return value</span></span>

<span data-ttu-id="631d2-127">Если операция завершается успешно, функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) или [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="631d2-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="631d2-128">Если операция завершается неудачно, возвращается значение ошибки СОКЕТа \_ и можно получить конкретный код ошибки, вызвав [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="631d2-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="631d2-129">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="631d2-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="631d2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="631d2-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="631d2-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="631d2-132">Перед использованием этой функции должен быть выполнен успешный вызов [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="631d2-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="631d2-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="631d2-134">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="631d2-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="631d2-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="631d2-136">Один из параметров *оптвал* или *оптлен* указывает на память, которая не находится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="631d2-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="631d2-137">Эта ошибка также возвращается, если значение, на которое указывает параметр *оптлен* , меньше, чем размер значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="631d2-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="631d2-138"><dt>**[всаеинпрогресс](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="631d2-139">Выполняется блокировка вызова Windows Sockets 1,1, или поставщик услуг все еще обрабатывает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="631d2-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="631d2-140"><dt>**[всаеинвал](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="631d2-141">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="631d2-141">An invalid argument was supplied.</span></span> <span data-ttu-id="631d2-142">Эта ошибка возвращается, если параметр *уровня* неизвестен или недопустим.</span><span class="sxs-lookup"><span data-stu-id="631d2-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="631d2-143">В Windows Vista и более поздних версиях эта ошибка также возвращается, если сокет находился в переходном состоянии.</span><span class="sxs-lookup"><span data-stu-id="631d2-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="631d2-144"><dt>**[всаенопротупт](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="631d2-145">Параметр неизвестен или не поддерживается указанным семейством протоколов.</span><span class="sxs-lookup"><span data-stu-id="631d2-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="631d2-146">Эта ошибка возвращается, если параметр *типа* для дескриптора сокета, переданного в параметре *s* , не **Сокк \_ дграм** или **Сокк \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="631d2-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="631d2-147"><dt>**[всаенотсокк](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="631d2-148">Дескриптор не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="631d2-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="631d2-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="631d2-149">Remarks</span></span>

<span data-ttu-id="631d2-150">Функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , вызываемая с \_ параметром сокета IPv6 пктинфо, позволяет приложению определить, должны ли сведения о пакете возвращаться функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)для сокета IPv6.</span><span class="sxs-lookup"><span data-stu-id="631d2-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IPV6\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv6 socket.</span></span>

<span data-ttu-id="631d2-151">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , вызываемая с \_ параметром сокета IPv6 пктинфо, позволяет приложению включать или отключать возврат сведений о пакетах функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="631d2-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="631d2-152">Параметр IPV6 \_ пктинфо для сокета по умолчанию отключен (имеет значение **false**).</span><span class="sxs-lookup"><span data-stu-id="631d2-152">The IPV6\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="631d2-153">Если этот параметр сокета включен на сокете IPv6 типа **Сокк \_ Дграм** или **сокк \_ RAW**, функция [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) возвращает сведения о пакете в структуре [**всамсг**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) , на которую указывает параметр *лпмсг* .</span><span class="sxs-lookup"><span data-stu-id="631d2-153">When this socket option is enabled on an IPv6 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="631d2-154">Один из объектов данных элемента управления в возвращенной структуре **всамсг** будет содержать структуру [**in6 \_ пктинфо**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) , используемую для хранения полученных сведений об адресе пакета.</span><span class="sxs-lookup"><span data-stu-id="631d2-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="631d2-155">Для датаграмм, полученных функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) по протоколу IPv6, элемент **управления** в полученной [**структуре всамсг**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) будет содержать структуру [**всабуф**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) , содержащую структуру **всакмсгхдр** .</span><span class="sxs-lookup"><span data-stu-id="631d2-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv6, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="631d2-156">Элемент **\_ уровня КМСГ** этой структуры **всакмсгхдр** будет содержать **иппрото \_ IPv6**, член **\_ типа КМСГ** этой структуры будет содержать **IPv6 \_ пктинфо**, а элемент **\_ данных КМСГ** будет содержать структуру [**in6 \_ пктинфо**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) , используемую для хранения полученных сведений об адресе IPv6-пакета.</span><span class="sxs-lookup"><span data-stu-id="631d2-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IPV6**, the **cmsg\_type** member of this structure would contain **IPV6\_PKTINFO**, and the **cmsg\_data** member would contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received IPv6 packet address information.</span></span> <span data-ttu-id="631d2-157">IPv6-адрес в структуре **in6 \_ пктинфо** — это IPv6-адрес, с которого получен пакет.</span><span class="sxs-lookup"><span data-stu-id="631d2-157">The IPv6 address in the **in6\_pktinfo** structure is the IPv6 address from which the packet was received.</span></span>

<span data-ttu-id="631d2-158">Для сокета датаграмм с двумя стеками, если приложению требуется функция [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) , возвращающая сведения о пакете в структуре [**всамсг**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) для датаграмм, полученных по протоколу IPv4, то параметр сокета [IP \_ пктинфо](ip-pktinfo.md) должен быть установлен в значение true на сокете.</span><span class="sxs-lookup"><span data-stu-id="631d2-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then [IP\_PKTINFO](ip-pktinfo.md) socket option must be set to true on the socket.</span></span> <span data-ttu-id="631d2-159">Если только параметр IPV6 \_ пктинфо имеет значение true для сокета, сведения о пакете будут предоставлены для датаграмм, полученных по протоколу IPv6, но могут не предоставляться для датаграмм, полученных по протоколу IPv4.</span><span class="sxs-lookup"><span data-stu-id="631d2-159">If only the IPV6\_PKTINFO option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="631d2-160">Обратите внимание, что заголовочный файл *Ws2ipdef. h* автоматически включается в *Ws2tcpip. h* и никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="631d2-160">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="631d2-161">Требования</span><span class="sxs-lookup"><span data-stu-id="631d2-161">Requirements</span></span>



| <span data-ttu-id="631d2-162">Требование</span><span class="sxs-lookup"><span data-stu-id="631d2-162">Requirement</span></span> | <span data-ttu-id="631d2-163">Значение</span><span class="sxs-lookup"><span data-stu-id="631d2-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="631d2-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="631d2-164">Minimum supported client</span></span><br/> | <span data-ttu-id="631d2-165">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="631d2-165">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="631d2-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="631d2-166">Minimum supported server</span></span><br/> | <span data-ttu-id="631d2-167">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="631d2-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="631d2-168">Header</span><span class="sxs-lookup"><span data-stu-id="631d2-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="631d2-169"><dt>Ws2ipdef. h (включение Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="631d2-169"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="631d2-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="631d2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="631d2-171">Сокеты с двумя стеками</span><span class="sxs-lookup"><span data-stu-id="631d2-171">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="631d2-172">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="631d2-172">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="631d2-173">**in6 \_ пктинфо**</span><span class="sxs-lookup"><span data-stu-id="631d2-173">**in6\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[<span data-ttu-id="631d2-174">IP- \_ пктинфо</span><span class="sxs-lookup"><span data-stu-id="631d2-174">IP\_PKTINFO</span></span>](ip-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="631d2-175">**\_Параметры сокета иппрото IPv6**</span><span class="sxs-lookup"><span data-stu-id="631d2-175">**IPPROTO\_IPV6 Socket Options**</span></span>](ipproto-ipv6-socket-options.md)
</dt> <dt>

[<span data-ttu-id="631d2-176">**сетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="631d2-176">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="631d2-177">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="631d2-177">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="631d2-178">**всамсг**</span><span class="sxs-lookup"><span data-stu-id="631d2-178">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="631d2-179">**LPFN_WSARECVMSG (Всареквмсг)**</span><span class="sxs-lookup"><span data-stu-id="631d2-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
