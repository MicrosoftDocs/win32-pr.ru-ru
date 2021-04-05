---
description: Возвращает локальный адрес, локальный порт, удаленный адрес, удаленный порт, тип сокета и протокол, используемые сокетом.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Параметр SO_BSP_STATE Socket (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812443"
---
# <a name="so_bsp_state-socket-option"></a><span data-ttu-id="f1de8-103">Поэтому \_ \_ параметр сокета состояния BSP</span><span class="sxs-lookup"><span data-stu-id="f1de8-103">SO\_BSP\_STATE socket option</span></span>

<span data-ttu-id="f1de8-104">Параметр сокета **\_ \_ состояния BSP** Возвращает локальный адрес, локальный порт, удаленный адрес, удаленный порт, тип сокета и протокол, используемые сокетом.</span><span class="sxs-lookup"><span data-stu-id="f1de8-104">The **SO\_BSP\_STATE** socket option returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span>

<span data-ttu-id="f1de8-105">Чтобы выполнить эту операцию, вызовите функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="f1de8-105">To perform this operation, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="f1de8-106">Значение параметра сокета</span><span class="sxs-lookup"><span data-stu-id="f1de8-106">Socket option value</span></span>

<span data-ttu-id="f1de8-107">Константа, представляющая этот параметр сокета, — 0x1009.</span><span class="sxs-lookup"><span data-stu-id="f1de8-107">The constant that represents this socket option is 0x1009.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1de8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1de8-108">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a><span data-ttu-id="f1de8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1de8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1de8-110">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f1de8-110">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1de8-111">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="f1de8-111">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="f1de8-112">*уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1de8-112">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1de8-113">Уровень, на котором определен параметр.</span><span class="sxs-lookup"><span data-stu-id="f1de8-113">The level at which the option is defined.</span></span> <span data-ttu-id="f1de8-114">Для выполнения этой операции используйте **\_ сокет Sol** .</span><span class="sxs-lookup"><span data-stu-id="f1de8-114">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f1de8-115">*optname* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1de8-115">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1de8-116">Параметр сокета, для которого должно быть получено значение.</span><span class="sxs-lookup"><span data-stu-id="f1de8-116">The socket option for which the value is to be retrieved.</span></span> <span data-ttu-id="f1de8-117">Используйте для этой операции **\_ \_ состояние BSP** .</span><span class="sxs-lookup"><span data-stu-id="f1de8-117">Use **SO\_BSP\_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f1de8-118">*оптвал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1de8-118">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1de8-119">Указатель на буфер, в котором возвращается значение запрошенного параметра.</span><span class="sxs-lookup"><span data-stu-id="f1de8-119">A pointer to the buffer in which the value for the requested option is to be returned.</span></span> <span data-ttu-id="f1de8-120">Этот параметр должен указывать на буфер, который больше или равен размеру структуры [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="f1de8-120">This parameter should point to buffer equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f1de8-121">*оптлен* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f1de8-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1de8-122">Указатель на размер (в байтах) буфера *оптвал* .</span><span class="sxs-lookup"><span data-stu-id="f1de8-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="f1de8-123">Этот размер должен быть больше или равен размеру структуры [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="f1de8-123">This size must be equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1de8-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1de8-124">Return value</span></span>

<span data-ttu-id="f1de8-125">Если операция завершается успешно, [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f1de8-125">If the operation completes successfully, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) returns zero.</span></span>

<span data-ttu-id="f1de8-126">Если операция завершается неудачно, возвращается значение ошибки СОКЕТа \_ и можно получить конкретный код ошибки, вызвав [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="f1de8-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="f1de8-127">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="f1de8-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="f1de8-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f1de8-128">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1de8-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="f1de8-130">Перед использованием этой функции должен быть выполнен успешный вызов [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="f1de8-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f1de8-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="f1de8-132">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="f1de8-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="f1de8-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="f1de8-134">Один из параметров *оптвал* или *оптлен* указывает на память, которая не находится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="f1de8-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="f1de8-135">Эта ошибка также возвращается, если значение, на которое указывает параметр *оптлен* , меньше размера структуры [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="f1de8-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span><br/> |
| <dl> <span data-ttu-id="f1de8-136"><dt>**[всаеинпрогресс](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="f1de8-137">Выполняется блокировка вызова Windows Sockets 1,1, или поставщик услуг все еще обрабатывает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f1de8-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="f1de8-138"><dt>**[всаеинвал](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="f1de8-139">Неизвестный или недопустимый параметр *уровня* .</span><span class="sxs-lookup"><span data-stu-id="f1de8-139">The *level* parameter is unknown or invalid.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="f1de8-140"><dt>**[всаенопротупт](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="f1de8-141">Параметр неизвестен или не поддерживается указанным семейством протоколов.</span><span class="sxs-lookup"><span data-stu-id="f1de8-141">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="f1de8-142"><dt>**[всаенотсокк](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="f1de8-143">Дескриптор не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="f1de8-143">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f1de8-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1de8-144">Remarks</span></span>

<span data-ttu-id="f1de8-145">Функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , вызываемая со следующим параметром сокета **\_ \_ состояния BSP** , получает локальный адрес, локальный порт, удаленный адрес, удаленный порт, тип сокета и протокол, используемые сокетом.</span><span class="sxs-lookup"><span data-stu-id="f1de8-145">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_BSP\_STATE** socket option retrieves the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span> <span data-ttu-id="f1de8-146">Так как параметр сокета **\_ \_ состояния BSP** работает с сокетами IPv6 или IPv4 (для семейств адресов **AF \_ INET6** и **AF \_ inet** ).</span><span class="sxs-lookup"><span data-stu-id="f1de8-146">The **SO\_BSP\_STATE** socket option works with IPv6 or IPv4 sockets (the **AF\_INET6** and **AF\_INET** address families).</span></span>

<span data-ttu-id="f1de8-147">Если функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) выполнена успешно, сведения возвращаются в структуре [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) в буфере, на который указывает параметр *оптвал* .</span><span class="sxs-lookup"><span data-stu-id="f1de8-147">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function is successful, the information is returned in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure in the buffer pointed to by the *optval* parameter.</span></span> <span data-ttu-id="f1de8-148">Целое число, на которое указывает *оптлен* , должно первоначально содержать размер этого буфера; При возврате он будет установлен в значение длины в байтах для значения, возвращаемого в параметре *оптвал* .</span><span class="sxs-lookup"><span data-stu-id="f1de8-148">The integer pointed to by *optlen* should originally contain the size of this buffer; on return, it will be set to the length, in bytes, of the value returned in the *optval* parameter.</span></span>

<span data-ttu-id="f1de8-149">Члены **исоккеттипе** и **ипротокол** в возвращенной структуре [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) заполняются для дескриптора сокета в параметре *s* .</span><span class="sxs-lookup"><span data-stu-id="f1de8-149">The **iSocketType** and **iProtocol** members in the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure are filled in for the socket descriptor in the *s* parameter.</span></span>

<span data-ttu-id="f1de8-150">Если сокет находится в подключенном или связанном состоянии, то элементу **локаладдр** в возвращенной структуре [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) будет присвоена структура [SOCKADDR](sockaddr-2.md) , представляющая локальный адрес и порт.</span><span class="sxs-lookup"><span data-stu-id="f1de8-150">If the socket is in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure will be set to a [SOCKADDR](sockaddr-2.md) structure representing the local address and port.</span></span> <span data-ttu-id="f1de8-151">Если сокет находится в подключенном состоянии, то элементу **ремотеаддр** в возвращенной структуре **ксаддр \_ info** будет присвоена структура SOCKADDR, представляющая удаленный адрес и порт.</span><span class="sxs-lookup"><span data-stu-id="f1de8-151">If the socket is in a connected state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure will be set to a SOCKADDR structure representing the remote address and port.</span></span>

<span data-ttu-id="f1de8-152">Если сокет не находится в подключенном или привязанном состоянии, то элемент **локаладдр** в возвращенной структуре [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) возвращается с **пустым** указателем в элементе **лпсоккаддр** , а элемент **исоккаддрленгс** — с нулевым значением.</span><span class="sxs-lookup"><span data-stu-id="f1de8-152">If the socket is not in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span> <span data-ttu-id="f1de8-153">Если сокет не находится в состоянии привязки, то член **ремотеаддр** возвращенной структуры **ксаддр \_ info** возвращается с **пустым** указателем в элементе **лпсоккаддр** , а элемент **исоккаддрленгс** — с нулевым значением.</span><span class="sxs-lookup"><span data-stu-id="f1de8-153">If the socket is not in a bound state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span>

<span data-ttu-id="f1de8-154">Если функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) завершается ошибкой, параметры *оптвал* и *оптлен* остаются неизменными, а параметр *Оптвал* не указывает на возвращаемую структуру [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="f1de8-154">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function fails, the *optval* and *optlen* parameters are left unchanged and the *optval* parameter does not point to a returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

<span data-ttu-id="f1de8-155">Обратите внимание, что файл заголовка *Ws2def. h* автоматически включается в *Winsock2. h* и никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="f1de8-155">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1de8-156">Требования</span><span class="sxs-lookup"><span data-stu-id="f1de8-156">Requirements</span></span>



| <span data-ttu-id="f1de8-157">Требование</span><span class="sxs-lookup"><span data-stu-id="f1de8-157">Requirement</span></span> | <span data-ttu-id="f1de8-158">Значение</span><span class="sxs-lookup"><span data-stu-id="f1de8-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1de8-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1de8-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f1de8-160">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1de8-160">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1de8-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1de8-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f1de8-162">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1de8-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1de8-163">Header</span><span class="sxs-lookup"><span data-stu-id="f1de8-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1de8-164"><dt>Ws2def. h (включение Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1de8-164"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1de8-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1de8-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1de8-166">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="f1de8-166">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="f1de8-167">**\_сведения о ксаддр**</span><span class="sxs-lookup"><span data-stu-id="f1de8-167">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="f1de8-168">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="f1de8-168">SOCKADDR</span></span>](sockaddr-2.md)
</dt> </dl>

 

 
