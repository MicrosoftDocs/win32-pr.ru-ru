---
description: Разрабатывается, чтобы приложение позволяло использовать пакеты проверки активности для подключения через сокет.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Параметр SO_KEEPALIVE Socket (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702733"
---
# <a name="so_keepalive-socket-option"></a><span data-ttu-id="ad145-103">SO, \_ параметр сокета KeepAlive</span><span class="sxs-lookup"><span data-stu-id="ad145-103">SO\_KEEPALIVE socket option</span></span>

<span data-ttu-id="ad145-104">**Таким образом \_** , параметр сокета KeepAlive позволяет приложению включить пакеты проверки активности для подключения через сокет.</span><span class="sxs-lookup"><span data-stu-id="ad145-104">The **SO\_KEEPALIVE** socket option is designed to allow an application to enable keep-alive packets for a socket connection.</span></span>

<span data-ttu-id="ad145-105">Чтобы запросить состояние этого параметра сокета, вызовите функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="ad145-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="ad145-106">Чтобы установить этот параметр, вызовите функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ad145-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="ad145-107">Значение параметра сокета</span><span class="sxs-lookup"><span data-stu-id="ad145-107">Socket option value</span></span>

<span data-ttu-id="ad145-108">Константа, представляющая этот параметр сокета, — 0x0008.</span><span class="sxs-lookup"><span data-stu-id="ad145-108">The constant that represents this socket option is 0x0008.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad145-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad145-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="ad145-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad145-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad145-111">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ad145-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad145-112">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="ad145-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="ad145-113">*уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad145-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad145-114">Уровень, на котором определен параметр.</span><span class="sxs-lookup"><span data-stu-id="ad145-114">The level at which the option is defined.</span></span> <span data-ttu-id="ad145-115">Для выполнения этой операции используйте **\_ сокет Sol** .</span><span class="sxs-lookup"><span data-stu-id="ad145-115">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad145-116">*optname* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad145-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad145-117">Параметр сокета, для которого задается значение.</span><span class="sxs-lookup"><span data-stu-id="ad145-117">The socket option for which the value is to be set.</span></span> <span data-ttu-id="ad145-118">Используйте для этой операции **\_ KeepAlive** .</span><span class="sxs-lookup"><span data-stu-id="ad145-118">Use **SO\_KEEPALIVE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad145-119">*оптвал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ad145-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad145-120">Указатель на буфер, содержащий значение для устанавливаемого параметра.</span><span class="sxs-lookup"><span data-stu-id="ad145-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="ad145-121">Этот параметр должен указывать на буфер, который больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ad145-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="ad145-122">Это значение рассматривается как логическое значение с 0, которое указывает **false** (отключено), и ненулевое значение, указывающее на значение **true** (включено).</span><span class="sxs-lookup"><span data-stu-id="ad145-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="ad145-123">*оптлен* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ad145-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad145-124">Указатель на размер (в байтах) буфера *оптвал* .</span><span class="sxs-lookup"><span data-stu-id="ad145-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="ad145-125">Этот размер должен быть больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ad145-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad145-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad145-126">Return value</span></span>

<span data-ttu-id="ad145-127">Если операция завершается успешно, [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ad145-127">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="ad145-128">Если операция завершается неудачно, возвращается значение ошибки СОКЕТа \_ и можно получить конкретный код ошибки, вызвав [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="ad145-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="ad145-129">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="ad145-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="ad145-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ad145-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad145-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="ad145-132">Перед использованием этой функции должен быть выполнен успешный вызов [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="ad145-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="ad145-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="ad145-134">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="ad145-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="ad145-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="ad145-136">Один из параметров *оптвал* или *оптлен* указывает на память, которая не находится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad145-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="ad145-137">Эта ошибка также возвращается, если значение, на которое указывает параметр *оптлен* , меньше, чем размер значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ad145-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="ad145-138"><dt>**[всаеинпрогресс](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="ad145-139">Выполняется блокировка вызова Windows Sockets 1,1, или поставщик услуг все еще обрабатывает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ad145-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="ad145-140"><dt>**[всаеинвал](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="ad145-141">Неизвестный или недопустимый параметр *уровня* .</span><span class="sxs-lookup"><span data-stu-id="ad145-141">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="ad145-142">В Windows Vista и более поздних версиях эта ошибка также возвращается, если сокет находился в переходном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ad145-142">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="ad145-143"><dt>**[всаенопротупт](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="ad145-144">Параметр неизвестен или не поддерживается указанным семейством протоколов.</span><span class="sxs-lookup"><span data-stu-id="ad145-144">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="ad145-145">Эта ошибка возвращается, если дескриптор сокета, переданный в параметре *s* , был для сокета датаграммы.</span><span class="sxs-lookup"><span data-stu-id="ad145-145">This error is returned if the socket descriptor passed in the *s* parameter was for a datagram socket.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="ad145-146"><dt>**[всаенотсокк](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="ad145-147">Дескриптор не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="ad145-147">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ad145-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad145-148">Remarks</span></span>

<span data-ttu-id="ad145-149">Функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , вызываемая с поддержкой протокола **so \_** , позволяет приложению получить текущее состояние параметра KeepAlive, хотя эта функция обычно не используется.</span><span class="sxs-lookup"><span data-stu-id="ad145-149">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to retrieve the current state of the keepalive option, although this is feature not normally used.</span></span> <span data-ttu-id="ad145-150">Если приложению необходимо включить пакеты KeepAlive на сокете, оно просто вызывает функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , чтобы включить параметр.</span><span class="sxs-lookup"><span data-stu-id="ad145-150">If an application needs to enable keepalive packets on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="ad145-151">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , вызванная с параметром сокета **\_ KeepAlive** , позволяет приложению включить пакеты поддержания активности для подключения через сокет.</span><span class="sxs-lookup"><span data-stu-id="ad145-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to enable keep-alive packets for a socket connection.</span></span> <span data-ttu-id="ad145-152">Параметр **so \_ KeepAlive** для сокета по умолчанию отключен (имеет значение **false**).</span><span class="sxs-lookup"><span data-stu-id="ad145-152">The **SO\_KEEPALIVE** option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="ad145-153">Если этот параметр сокета включен, стек TCP отправляет пакеты проверки активности, когда для подключения не были получены пакеты данных или подтверждения в течение интервала.</span><span class="sxs-lookup"><span data-stu-id="ad145-153">When this socket option is enabled, the TCP stack sends keep-alive packets when no data or acknowledgement packets have been received for the connection within an interval.</span></span> <span data-ttu-id="ad145-154">Дополнительные сведения о параметре проверки активности см. в разделе 4.2.3.6 ( *требования для узлов Интернета) — уровни взаимодействия* , указанные в RFC 1122, доступны на [веб-сайте IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="ad145-154">For more information on the keep-alive option, see section 4.2.3.6 on the *Requirements for Internet Hosts—Communication Layers* specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span> <span data-ttu-id="ad145-155">(Этот ресурс может быть доступен только на английском языке.)</span><span class="sxs-lookup"><span data-stu-id="ad145-155">(This resource may only be available in English.)</span></span>

<span data-ttu-id="ad145-156">Поэтому параметр сокета **\_ KeepAlive** действителен только для протоколов, которые поддерживают понятие поддержания активности (протоколы, ориентированные на подключение).</span><span class="sxs-lookup"><span data-stu-id="ad145-156">The **SO\_KEEPALIVE** socket option is valid only for protocols that support the notion of keep-alive (connection-oriented protocols).</span></span> <span data-ttu-id="ad145-157">Для TCP время ожидания проверки активности по умолчанию составляет 2 часа, а интервал проверки активности равен 1 секунде.</span><span class="sxs-lookup"><span data-stu-id="ad145-157">For TCP, the default keep-alive timeout is 2 hours and the keep-alive interval is 1 second.</span></span> <span data-ttu-id="ad145-158">Количество зондов проверки активности по умолчанию зависит от версии Windows.</span><span class="sxs-lookup"><span data-stu-id="ad145-158">The default number of keep-alive probes varies based on the version of Windows.</span></span>

<span data-ttu-id="ad145-159">Управляющий код [**\_ \_ Валс поддержки SIO**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) может использоваться для включения или отключения проверки активности и настройки времени ожидания и интервала для одного соединения.</span><span class="sxs-lookup"><span data-stu-id="ad145-159">The [**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control code can be used to enable or disable keep-alive, and adjust the timeout and interval, for a single connection.</span></span> <span data-ttu-id="ad145-160">Если для проверки активности включена поддержка поддержания **активности \_ , то** параметры TCP по умолчанию используются для времени ожидания проверки активности и интервала, если эти значения не были изменены с помощью **SIO \_ KeepAlive \_ Валс**.</span><span class="sxs-lookup"><span data-stu-id="ad145-160">If keep-alive is enabled with **SO\_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="ad145-161">Значение времени ожидания проверки активности по умолчанию для всей системы может быть управляемым с помощью параметра реестра [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) , который принимает значение в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="ad145-161">The default system-wide value of the keep-alive timeout is controllable through the [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="ad145-162">Значение интервала проверки активности по умолчанию может быть управляемым с помощью параметра реестра [keepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , который принимает значение в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="ad145-162">The default system-wide value of the keep-alive interval is controllable through the [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span>

<span data-ttu-id="ad145-163">В Windows Vista и более поздних версиях количество проверок активности (повторных передач данных) устанавливается равным 10 и не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="ad145-163">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="ad145-164">В Windows Server 2003, Windows XP и Windows 2000 параметр по умолчанию для количества проверок активности по сроку поддержания равен 5.</span><span class="sxs-lookup"><span data-stu-id="ad145-164">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span> <span data-ttu-id="ad145-165">Количество зондов проверки активности может быть управляемым с помощью параметров реестра [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) и [пптпткпмаксдатаретрансмиссионс](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="ad145-165">The number of keep-alive probes is controllable through the [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) and [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span> <span data-ttu-id="ad145-166">Число зондов проверки активности устанавливается равным большему из двух значений раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="ad145-166">The number of keep-alive probes is set to the larger of the two registry key values.</span></span> <span data-ttu-id="ad145-167">Если это число равно 0, зонды проверки активности не будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="ad145-167">If this number is 0, then keep-alive probes will not be sent.</span></span> <span data-ttu-id="ad145-168">Если это число превышает 255, то оно корректируется на 255.</span><span class="sxs-lookup"><span data-stu-id="ad145-168">If this number is above 255, then it is adjusted to 255.</span></span>

<span data-ttu-id="ad145-169">В Windows Vista и более поздних версиях параметр **so \_ KeepAlive** Socket можно задать только с помощью функции [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , если сокет находится в известном состоянии, а не в переходном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ad145-169">On Windows Vista and later, the **SO\_KEEPALIVE** socket option can only be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is in a well-known state not a transitional state.</span></span> <span data-ttu-id="ad145-170">Для протокола TCP значение параметра сокета **\_ KeepAlive** должно быть установлено перед вызовом функции Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**Коннектекс**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**всаконнект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)или [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) или после фактического завершения запроса на подключение.</span><span class="sxs-lookup"><span data-stu-id="ad145-170">For TCP, the **SO\_KEEPALIVE** socket option should be set either before the connect function ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) is called, or after the connection request is actually completed.</span></span> <span data-ttu-id="ad145-171">Если функция Connect была вызвана асинхронно, это требует ожидания завершения соединения, прежде чем пытаться установить параметр **so для протокола \_ KeepAlive** .</span><span class="sxs-lookup"><span data-stu-id="ad145-171">If the connect function was called asynchronously, then this requires waiting for the connection completion before trying to set the **SO\_KEEPALIVE** socket option.</span></span> <span data-ttu-id="ad145-172">Если приложение пытается установить параметр " **таким \_ образом** сокета KeepAlive", когда запрос на подключение все еще обрабатывается, функция **сетсоккопт** завершится ошибкой и возвратит [всаеинвал](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="ad145-172">If an application attempts to set the **SO\_KEEPALIVE** socket option when a connection request is still in process, the **setsockopt** function will fail and return [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="ad145-173">В Windows Server 2003, Windows XP и Windows 2000 параметр **so \_ KeepAlive** Socket можно задать с помощью функции [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , если сокет является переходным состоянием (запрос на соединение все еще выполняется), а также как известное состояние.</span><span class="sxs-lookup"><span data-stu-id="ad145-173">On Windows Server 2003, Windows XP, and Windows 2000, the **SO\_KEEPALIVE** socket option can be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is a transitional state (a connection request is still in progress) as well as a well-known state.</span></span>

<span data-ttu-id="ad145-174">Обратите внимание, что файл заголовка *Ws2def. h* автоматически включается в *Winsock2. h* и никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="ad145-174">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad145-175">Требования</span><span class="sxs-lookup"><span data-stu-id="ad145-175">Requirements</span></span>



| <span data-ttu-id="ad145-176">Требование</span><span class="sxs-lookup"><span data-stu-id="ad145-176">Requirement</span></span> | <span data-ttu-id="ad145-177">Значение</span><span class="sxs-lookup"><span data-stu-id="ad145-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad145-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad145-178">Minimum supported client</span></span><br/> | <span data-ttu-id="ad145-179">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad145-179">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad145-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad145-180">Minimum supported server</span></span><br/> | <span data-ttu-id="ad145-181">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ad145-181">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad145-182">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ad145-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad145-183"><dt>Ws2def. h (включение Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad145-183"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad145-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad145-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad145-185">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="ad145-185">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="ad145-186">**сетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="ad145-186">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

<span data-ttu-id="ad145-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="ad145-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="ad145-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="ad145-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="ad145-189">[пптпткпмаксдатаретрансмиссионс](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="ad145-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="ad145-190">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="ad145-190">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

<span data-ttu-id="ad145-191">[**\_Валс KeepAlive для проверки SIO \_**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad145-191">[**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ad145-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="ad145-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="ad145-193">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="ad145-193">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
