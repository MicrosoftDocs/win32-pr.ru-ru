---
description: Предназначен для того, чтобы приложение решило принимать входящие подключения через сокет прослушивания.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Параметр SO_CONDITIONAL_ACCEPT Socket (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702734"
---
# <a name="so_conditional_accept-socket-option"></a><span data-ttu-id="fe5bd-103">Поэтому \_ Условный \_ вариант принятия сокета</span><span class="sxs-lookup"><span data-stu-id="fe5bd-103">SO\_CONDITIONAL\_ACCEPT socket option</span></span>

<span data-ttu-id="fe5bd-104">Вариант **\_ условного \_ приема** сокета позволяет приложению решить, принимать ли входящее подключение через сокет прослушивания.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-104">The **SO\_CONDITIONAL\_ACCEPT** socket option is designed to allow an application to decide whether or not to accept an incoming connection on a listening socket.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="fe5bd-105">Значение параметра сокета</span><span class="sxs-lookup"><span data-stu-id="fe5bd-105">Socket option value</span></span>

<span data-ttu-id="fe5bd-106">Константа, представляющая этот параметр сокета, — 0x3002.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-106">The constant that represents this socket option is 0x3002.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe5bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe5bd-107">Syntax</span></span>


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="fe5bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe5bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe5bd-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="fe5bd-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5bd-110">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-110">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="fe5bd-111">*уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe5bd-111">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5bd-112">Уровень, на котором определен параметр.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-112">The level at which the option is defined.</span></span> <span data-ttu-id="fe5bd-113">Для выполнения этой операции используйте **\_ сокет Sol** .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-113">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe5bd-114">*optname* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fe5bd-114">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5bd-115">Параметр сокета, для которого задается значение.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-115">The socket option for which the value is to be set.</span></span> <span data-ttu-id="fe5bd-116">Используйте для этой операции **\_ условное \_ принятие** .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-116">Use **SO\_CONDITIONAL\_ACCEPT** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe5bd-117">*оптвал* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fe5bd-117">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5bd-118">Указатель на буфер, содержащий значение для устанавливаемого параметра.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-118">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="fe5bd-119">Этот параметр должен указывать на буфер, который больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-119">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="fe5bd-120">Это значение рассматривается как логическое значение с 0, которое указывает **false** (отключено), и ненулевое значение, указывающее на значение **true** (включено).</span><span class="sxs-lookup"><span data-stu-id="fe5bd-120">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="fe5bd-121">*оптлен* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fe5bd-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe5bd-122">Указатель на размер (в байтах) буфера *оптвал* .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="fe5bd-123">Этот размер должен быть больше или равен размеру значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-123">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe5bd-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe5bd-124">Return value</span></span>

<span data-ttu-id="fe5bd-125">Если операция завершается успешно, [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-125">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="fe5bd-126">Если операция завершается неудачно, возвращается значение ошибки СОКЕТа \_ и можно получить конкретный код ошибки, вызвав [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="fe5bd-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="fe5bd-127">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="fe5bd-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="fe5bd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="fe5bd-128">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe5bd-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="fe5bd-130">Перед использованием этой функции должен быть выполнен успешный вызов [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="fe5bd-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="fe5bd-132">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="fe5bd-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="fe5bd-134">Один из параметров *оптвал* или *оптлен* указывает на память, которая не находится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="fe5bd-135">Эта ошибка также возвращается, если значение, на которое указывает параметр *оптлен* , меньше, чем размер значения **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="fe5bd-136"><dt>**[всаеинпрогресс](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="fe5bd-137">Выполняется блокировка вызова Windows Sockets 1,1, или поставщик услуг все еще обрабатывает функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="fe5bd-138"><dt>**[всаеинвал](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="fe5bd-139">Неизвестный или недопустимый параметр *уровня* .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-139">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="fe5bd-140">Эта ошибка также возвращается, если сокет уже находится в состоянии прослушивания.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-140">This error is also returned if the socket was already in a listening state.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="fe5bd-141"><dt>**[всаенопротупт](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="fe5bd-142">Параметр неизвестен или не поддерживается указанным семейством протоколов.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-142">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="fe5bd-143"><dt>**[всаенотсокк](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="fe5bd-144">Дескриптор не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-144">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="fe5bd-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe5bd-145">Remarks</span></span>

<span data-ttu-id="fe5bd-146">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , вызываемая с применением **\_ условного \_** сокета Accept, позволяет приложению решить, принимать ли входящие подключения через сокет прослушивания.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-146">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to decide whether or not to accept an incoming connection on a listening socket.</span></span> <span data-ttu-id="fe5bd-147">Параметр условного принятия для сокета по умолчанию отключен (имеет значение **false**).</span><span class="sxs-lookup"><span data-stu-id="fe5bd-147">The conditional accept option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="fe5bd-148">Если этот параметр сокета включен, стек TCP не принимает подключения автоматически.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-148">When this socket option is enabled, the TCP stack does not automatically accept connections.</span></span> <span data-ttu-id="fe5bd-149">Он ожидает, когда приложение покажет, что оно принимает подключение с помощью условного обратного вызова Accept, зарегистрированного с помощью функции [**всаакцепт**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-149">It waits for the application to indicate that it accepts the connection via the conditional accept callback registered with [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function.</span></span> <span data-ttu-id="fe5bd-150">После получения запроса на подключение Winsock вызывает условный обратный вызов accept, зарегистрированный приложением.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-150">Once a connection request is received, Winsock invokes the conditional accept callback registered by the application.</span></span> <span data-ttu-id="fe5bd-151">Только если условный обратный вызов accept возвращает значение **CF \_ Accept** , будет уведомлять транспорт о необходимости полного принятия подключения.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-151">Only when the conditional accept callback returns **CF\_ACCEPT** will Winsock notify the transport to fully accept the connection.</span></span>

<span data-ttu-id="fe5bd-152">Если для параметра **so \_ условного \_ приема** сокета задано значение включено (значение **true**), это имеет несколько побочных эффектов для сокета:</span><span class="sxs-lookup"><span data-stu-id="fe5bd-152">When the **SO\_CONDITIONAL\_ACCEPT** socket option is set to enabled (set to **TRUE**), this has several side effects on the socket:</span></span>

-   <span data-ttu-id="fe5bd-153">Это приведет к отключению встроенной защиты от атак SYN стека TCP, так как теперь приложение принимает владение для приема подключений.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-153">This disables the TCP stack's built-in SYN attack protection defenses, since the application is now taking ownership of accepting connections.</span></span>
-   <span data-ttu-id="fe5bd-154">Это эффективно отключает журнал ожидания прослушивания, так как соединения не принимаются от имени прослушивающего сокета.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-154">This effectively disables the listen backlog since connections aren't accepted on behalf of a listening socket.</span></span> <span data-ttu-id="fe5bd-155">Соединение никогда не будет полностью принято до тех пор, пока приложение не полностью примет использование механизма **\_ разпринятия CF** .</span><span class="sxs-lookup"><span data-stu-id="fe5bd-155">A connection is never fully accepted until the application fully accepts using the **CF\_ACCEPT** mechanism.</span></span>
-   <span data-ttu-id="fe5bd-156">Это также означает, что приложение всегда должно находиться в состоянии, чтобы вы быстро обрабатывал обратные вызовы Accept для принятия подключения.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-156">This also means the application take care to always be in a state to readily handle the accept callbacks to accept the connection.</span></span> <span data-ttu-id="fe5bd-157">Если приложение занято выполнением другой обработки, то на стороне клиента может истекает время ожидания, прежде чем приложение действительно примет подключение.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-157">If the application is busy doing other processing, then the client side may time out before the application actually accepts the connection.</span></span> <span data-ttu-id="fe5bd-158">Это ведет к плохому интерфейсу клиента.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-158">This leads to a poor client experience.</span></span>

<span data-ttu-id="fe5bd-159">Как правило, основная причина, по которой приложения используют условное принятие, — проверка исходного IP-адреса или порта, используемого подключающимся клиентом, а затем принятие решения о принятии или отклонении подключения.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-159">Generally, the main reason applications use conditional accept is to inspect the source IP address or port used by the connecting client and then decide to accept or reject the connection.</span></span> <span data-ttu-id="fe5bd-160">Однако приложения, скорее всего, будут работать лучше, если \_ \_ не включен условный вариант принятия, и приложение разрешит работу стека TCP и невыполненной работы в ожидании.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-160">However, applications are likely to perform better if the SO\_CONDITIONAL\_ACCEPT option is not enabled and the application allows the TCP stack and the listen backlog to work as expected.</span></span> <span data-ttu-id="fe5bd-161">Затем, когда приложение обрабатывает принятое подключение, если оно имеет неверный IP-адрес или порт источника, приложение может просто закрыть сокет.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-161">Then when the application handles the accepted connection, if it is from a improper IP source address or port, the application can just close the socket.</span></span> <span data-ttu-id="fe5bd-162">Недостаток безопасности этого поведения заключается в том, что теперь клиент подтвердил, что приложение прослушивает IP-адрес и порт, так как он принудительно закрыл ранее принятое подключение.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-162">The security drawback to this behavior is that now the client has confirmation that the application is listening on an IP address and port since it forcefully closed the previously accepted connection.</span></span> <span data-ttu-id="fe5bd-163">Тем не менее недостатками является включение **\_ условного \_ принятия, что** обычно перевешивает это ограничение.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-163">However, the drawbacks to enabling **SO\_CONDITIONAL\_ACCEPT** generally outweigh this limitation.</span></span>

<span data-ttu-id="fe5bd-164">Функция [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) , вызываемая с применением **\_ условного \_** сокета Accept, позволяет приложению получить текущее состояние условного приема, хотя эта функция обычно не используется.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-164">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to retrieve the current state of the conditional accept option, although this is feature not normally used.</span></span> <span data-ttu-id="fe5bd-165">Если приложению необходимо включить условное применение в сокете, оно просто вызывает функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , чтобы включить параметр.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-165">If an application needs to enable conditional accept on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="fe5bd-166">Обратите внимание, что файл заголовка *Ws2def. h* автоматически включается в *Winsock2. h* и никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="fe5bd-166">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe5bd-167">Требования</span><span class="sxs-lookup"><span data-stu-id="fe5bd-167">Requirements</span></span>



| <span data-ttu-id="fe5bd-168">Требование</span><span class="sxs-lookup"><span data-stu-id="fe5bd-168">Requirement</span></span> | <span data-ttu-id="fe5bd-169">Значение</span><span class="sxs-lookup"><span data-stu-id="fe5bd-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe5bd-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe5bd-170">Minimum supported client</span></span><br/> | <span data-ttu-id="fe5bd-171">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe5bd-171">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe5bd-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe5bd-172">Minimum supported server</span></span><br/> | <span data-ttu-id="fe5bd-173">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe5bd-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe5bd-174">Header</span><span class="sxs-lookup"><span data-stu-id="fe5bd-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe5bd-175"><dt>Ws2def. h (включение Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe5bd-175"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe5bd-176">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe5bd-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe5bd-177">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="fe5bd-177">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="fe5bd-178">**сетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="fe5bd-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="fe5bd-179">**всаакцепт**</span><span class="sxs-lookup"><span data-stu-id="fe5bd-179">**WSAAccept**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




