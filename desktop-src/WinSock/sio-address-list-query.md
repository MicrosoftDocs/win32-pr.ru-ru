---
description: Код элемента управления получает список локальных транспортных адресов семейства протоколов сокета, к которому может быть привязано приложение.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Код элемента управления SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719629"
---
# <a name="sio_address_list_query-control-code"></a><span data-ttu-id="022ed-103">Код элемента управления SIO_ADDRESS_LIST_QUERY</span><span class="sxs-lookup"><span data-stu-id="022ed-103">SIO_ADDRESS_LIST_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="022ed-104">Описание</span><span class="sxs-lookup"><span data-stu-id="022ed-104">Description</span></span>

<span data-ttu-id="022ed-105">Код элемента управления **\_ \_ \_ запросом списка адресов SIO** получает список локальных транспортных адресов семейства протоколов сокетов, к которым может быть привязано приложение.</span><span class="sxs-lookup"><span data-stu-id="022ed-105">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="022ed-106">Список адресов зависит от семейства адресов, а некоторые адреса исключаются из списка.</span><span class="sxs-lookup"><span data-stu-id="022ed-106">The list of addresses varies based on address family and some addresses are excluded from the list.</span></span>

<span data-ttu-id="022ed-107">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="022ed-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="022ed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="022ed-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="022ed-109">s</span><span class="sxs-lookup"><span data-stu-id="022ed-109">s</span></span>

<span data-ttu-id="022ed-110">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="022ed-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="022ed-111">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="022ed-111">dwIoControlCode</span></span>

<span data-ttu-id="022ed-112">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="022ed-112">The control code for the operation.</span></span>
<span data-ttu-id="022ed-113">Используйте **\_ \_ \_ запрос списка адресов SIO** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="022ed-113">Use **SIO\_ADDRESS\_LIST\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="022ed-114">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="022ed-114">lpvInBuffer</span></span>

<span data-ttu-id="022ed-115">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="022ed-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="022ed-116">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="022ed-116">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="022ed-117">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="022ed-117">cbInBuffer</span></span>

<span data-ttu-id="022ed-118">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="022ed-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="022ed-119">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="022ed-119">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="022ed-120">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="022ed-120">lpvOutBuffer</span></span>

<span data-ttu-id="022ed-121">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="022ed-121">A pointer to the output buffer.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="022ed-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="022ed-122">cbOutBuffer</span></span>

<span data-ttu-id="022ed-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="022ed-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="022ed-124">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="022ed-124">lpcbBytesReturned</span></span>

<span data-ttu-id="022ed-125">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="022ed-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="022ed-126">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="022ed-126">lpvOverlapped</span></span>

<span data-ttu-id="022ed-127">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="022ed-127">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="022ed-128">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="022ed-128">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="022ed-129">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="022ed-129">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="022ed-130">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="022ed-130">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="022ed-131">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="022ed-131">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="022ed-132">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="022ed-132">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="022ed-133">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="022ed-133">lpCompletionRoutine</span></span>

<span data-ttu-id="022ed-134">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="022ed-134">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="022ed-135">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="022ed-135">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="022ed-136">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="022ed-136">lpThreadId</span></span>

<span data-ttu-id="022ed-137">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="022ed-137">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="022ed-138">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="022ed-138">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="022ed-139">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="022ed-139">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="022ed-140">лперрно</span><span class="sxs-lookup"><span data-stu-id="022ed-140">lpErrno</span></span>

<span data-ttu-id="022ed-141">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="022ed-141">A pointer to the error code.</span></span>

<span data-ttu-id="022ed-142">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="022ed-142">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="022ed-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="022ed-143">Return value</span></span>

<span data-ttu-id="022ed-144">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="022ed-144">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="022ed-145">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="022ed-145">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="022ed-146">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="022ed-146">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="022ed-147">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="022ed-147">Error code</span></span> | <span data-ttu-id="022ed-148">Значение</span><span class="sxs-lookup"><span data-stu-id="022ed-148">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="022ed-149">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="022ed-149">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="022ed-150">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="022ed-150">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="022ed-151">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="022ed-151">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="022ed-152">Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="022ed-152">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="022ed-153">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="022ed-153">**WSAEFAULT**</span></span> | <span data-ttu-id="022ed-154">Параметр *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="022ed-154">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="022ed-155">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="022ed-155">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="022ed-156">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="022ed-156">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="022ed-157">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="022ed-157">**WSAEINTR**</span></span> | <span data-ttu-id="022ed-158">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="022ed-158">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="022ed-159">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="022ed-159">**WSAEINVAL**</span></span> | <span data-ttu-id="022ed-160">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="022ed-160">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="022ed-161">Эта ошибка возвращается, если параметр *кбинбуффер* не имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="022ed-161">This error is returned if the *cbInBuffer* parameter is not set to **NULL**.</span></span> |
| <span data-ttu-id="022ed-162">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="022ed-162">**WSAENETDOWN**</span></span> | <span data-ttu-id="022ed-163">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="022ed-163">The network subsystem has failed.</span></span> |
| <span data-ttu-id="022ed-164">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="022ed-164">**WSAENOBUFS**</span></span> | <span data-ttu-id="022ed-165">Нет доступного места в буфере.</span><span class="sxs-lookup"><span data-stu-id="022ed-165">No buffer space available.</span></span> |
| <span data-ttu-id="022ed-166">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="022ed-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="022ed-167">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="022ed-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="022ed-168">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="022ed-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="022ed-169">Дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="022ed-169">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="022ed-170">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="022ed-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="022ed-171">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="022ed-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="022ed-172">Эта ошибка возвращается, если поставщик транспорта не поддерживает **\_ \_ \_ запрос списка адресов SIO** .</span><span class="sxs-lookup"><span data-stu-id="022ed-172">This error is returned if the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="022ed-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="022ed-173">Remarks</span></span>

<span data-ttu-id="022ed-174">**Запрос IOCTL \_ \_ списка адресов \_ SIO** поддерживается в Windows 2000 и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="022ed-174">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="022ed-175">Код элемента управления **\_ \_ \_ запросом списка адресов SIO** получает список локальных транспортных адресов семейства протоколов сокетов, к которым может быть привязано приложение.</span><span class="sxs-lookup"><span data-stu-id="022ed-175">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="022ed-176">Список адресов зависит от семейства адресов.</span><span class="sxs-lookup"><span data-stu-id="022ed-176">The list of addresses varies based on address family.</span></span>

<span data-ttu-id="022ed-177">Для \_ семейства адресов AF INET6 все адреса возвращаются, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="022ed-177">For the AF\_INET6 address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="022ed-178">Любой IP-адрес, в котором состояние обнаружения повторяющихся адресов (отец) не Ипдадстатепреферред.</span><span class="sxs-lookup"><span data-stu-id="022ed-178">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="022ed-179">Любой IP-адрес с уровнем области ниже Скопелевелсубнет в интерфейсе, где тип интерфейса — это **\_ тип \_ \_ замыкания на себя программного обеспечения**.</span><span class="sxs-lookup"><span data-stu-id="022ed-179">Any IP address with a scope level lower than ScopeLevelSubnet on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK**.</span></span>
<span data-ttu-id="022ed-180">Это означает, что локальные ссылки (FE80: \*) и замыкание (:: 1) используются в интерфейсах, **Если тип \_ \_ \_ замыкания на себя** не исключается, но не в том случае, если эти адреса находятся в интерфейсе с другим типом.</span><span class="sxs-lookup"><span data-stu-id="022ed-180">This means link-local (fe80:\*) and loopback (::1) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="022ed-181">Для семейства адресов **AF \_ inet** все адреса возвращаются, за исключением следующих:</span><span class="sxs-lookup"><span data-stu-id="022ed-181">For the **AF\_INET** address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="022ed-182">Любой IP-адрес, в котором состояние обнаружения повторяющихся адресов (отец) не Ипдадстатепреферред.</span><span class="sxs-lookup"><span data-stu-id="022ed-182">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="022ed-183">Любой IP-адрес в интерфейсе с типом интерфейса, **Если \_ тип \_ " \_ замыкание на себя** " и "ссылка" является локальным.</span><span class="sxs-lookup"><span data-stu-id="022ed-183">Any IP address on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK** and link is local.</span></span>
<span data-ttu-id="022ed-184">Это означает, что локальные адреса (169,254.*) и замыкание на себя (127.*) используются в интерфейсах, **Если тип \_ \_ \_ замыкания на себя** не исключается, но не в том случае, если эти адреса находятся в интерфейсе с другим типом.</span><span class="sxs-lookup"><span data-stu-id="022ed-184">This means link-local (169.254.*) and loopback (127.*) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="022ed-185">Дополнительные сведения о состоянии "отец" см. в документации вспомогательной функции IP в разделе Перечисление [**\_ \_ состояния IP**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) -адресов и [**\_ \_ \_ адрес одноадресной рассылки IP-адаптера**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) и в документации MIB по структуре [**\_ \_ строк MIB уникастипаддресс**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .</span><span class="sxs-lookup"><span data-stu-id="022ed-185">For more information on DAD state, see the IP Helper documentation on the [**IP\_DAD\_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) enumeration and [**IP\_ADAPTER\_UNICAST\_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) structure and the MIB documentation on the [**MIB\_UNICASTIPADDRESS\_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) structure.</span></span>
<span data-ttu-id="022ed-186">Дополнительные сведения о типе интерфейса см. в документации вспомогательной функции IP на странице Структура [**\_ \_ адресов IP-адаптеров**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) , а также в разделе [**жетадаптерсаддрессес**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) и документации MIB по структуре [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) .</span><span class="sxs-lookup"><span data-stu-id="022ed-186">For more information on interface type, see the IP Helper documentation on the [**IP\_ADAPTER\_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the MIB documentation on [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span></span>
<span data-ttu-id="022ed-187">Дополнительные сведения об уровне области см. в документации вспомогательной функции IP на [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) структуре и перечислении [**\_ уровня области**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .</span><span class="sxs-lookup"><span data-stu-id="022ed-187">For more information on the scope level, see the IP Helper documentation on the [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**SCOPE\_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) enumeration.</span></span>

<span data-ttu-id="022ed-188">Список, возвращенный в выходном буфере, на который указывает параметр *лпваутбуффер* , представлен в виде [**структуры \_ \_ списка адресов сокета**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .</span><span class="sxs-lookup"><span data-stu-id="022ed-188">The list returned in the output buffer pointed to by the *lpvOutBuffer* parameter is in the form of a [**SOCKET\_ADDRESS\_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) structure.</span></span>

<span data-ttu-id="022ed-189">Если выходной буфер, указанный в параметре *лпваутбуффер* , недостаточно велик для хранения списка адресов, то в результате выполнения этого ioctl возвращается **\_ Ошибка сокета** , а [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [всаефаулт](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="022ed-189">If the output buffer specified in the *lpvOutBuffer* parameter is not large enough to contain the address list, **SOCKET\_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [WSAEFAULT](windows-sockets-error-codes-2.md).</span></span>
<span data-ttu-id="022ed-190">Необходимый размер (в байтах) выходного буфера возвращается в параметре *лпкббитесретурнед* в этом случае.</span><span class="sxs-lookup"><span data-stu-id="022ed-190">The required size, in bytes, for the output buffer is returned in the *lpcbBytesReturned* parameter in this case.</span></span>
<span data-ttu-id="022ed-191">Примечание. код ошибки [всаефаулт](windows-sockets-error-codes-2.md) также возвращается, если параметр *лпвинбуффер*, *лпваутбуффер* или *лпкббитесретурнед* не полностью содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="022ed-191">Note the [WSAEFAULT](windows-sockets-error-codes-2.md) error code is also returned if the *lpvInBuffer*, *lpvOutBuffer*, or *lpcbBytesReturned* parameter is not completely contained in a valid part of the user address space.</span></span>

<span data-ttu-id="022ed-192">**\_ \_ \_ Запрос списка адресов SIO** обычно вызывается синхронно с параметром *лпвоверлаппед* , имеющим значение **null**, так как список адресов возвращается немедленно.</span><span class="sxs-lookup"><span data-stu-id="022ed-192">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is normally called synchronously with the *lpvOverlapped* parameter set to **NULL**, since the list of addresses is returned immediately.</span></span>

<span data-ttu-id="022ed-193">**Примечание**  .  В средах Windows Plug-n-Play адреса можно добавлять и удалять динамически.</span><span class="sxs-lookup"><span data-stu-id="022ed-193">**Note**  In Windows Plug-n-Play environments, addresses can be added and removed dynamically.</span></span>
<span data-ttu-id="022ed-194">Поэтому приложения не могут полагаться на сведения, возвращаемые **\_ \_ \_ запросом списка адресов SIO** , как постоянные.</span><span class="sxs-lookup"><span data-stu-id="022ed-194">Therefore, applications cannot rely on the information returned by **SIO\_ADDRESS\_LIST\_QUERY** to be persistent.</span></span>
<span data-ttu-id="022ed-195">Приложения могут регистрироваться для получения уведомлений об изменении адреса через **\_ список адресов SIO \_ \_ изменение** ioctl, который обеспечивает уведомление с помощью перекрывающихся операций ввода-вывода или события **\_ \_ \_ изменения списка адресов** .</span><span class="sxs-lookup"><span data-stu-id="022ed-195">Applications may register for address change notifications through the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL which provides for notification through either overlapped I/O or **FD\_ADDRESS\_LIST\_CHANGE** event.</span></span>
<span data-ttu-id="022ed-196">Чтобы гарантировать, что приложение всегда имеет текущие сведения о списке адресов, можно использовать следующую последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="022ed-196">The following sequence of actions can be used to guarantee that the application always has current address list information:</span></span>

* <span data-ttu-id="022ed-197">Выдача IOCTL с **\_ \_ \_ изменением списка адресов SIO**</span><span class="sxs-lookup"><span data-stu-id="022ed-197">Issue the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL</span></span>
* <span data-ttu-id="022ed-198">Выдача **\_ запроса IOCTL \_ списка \_ адресов SIO**</span><span class="sxs-lookup"><span data-stu-id="022ed-198">Issue the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL</span></span>
* <span data-ttu-id="022ed-199">Всякий раз, когда вызов IOCTL на **\_ \_ \_ изменение списка адресов SIO** уведомляет приложение об изменении списка адресов (через перекрывающиеся операции ввода-вывода или с помощью сигнализации о событии **\_ \_ \_ изменения списка адресов** ), должна повторяться вся последовательность действий.</span><span class="sxs-lookup"><span data-stu-id="022ed-199">Whenever the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL call notifies the application of an address list change (either through overlapped I/O or by signaling **FD\_ADDRESS\_LIST\_CHANGE** event), the whole sequence of actions should be repeated.</span></span>

<span data-ttu-id="022ed-200">В пакете средств разработки программного обеспечения Microsoft Windows (SDK), выпущенном для Windows Vista и более поздних версий, изменилась Организация файлов заголовков, а в файле заголовка *Ws2def. h* определен код контроля **\_ \_ \_ запросов SIO** .</span><span class="sxs-lookup"><span data-stu-id="022ed-200">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the **SIO\_ADDRESS\_LIST\_QUERY** control code is defined in the *Ws2def.h* header file.</span></span>
<span data-ttu-id="022ed-201">Обратите внимание, что файл заголовка *Ws2def. h* автоматически включается в *Winsock2. h* и никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="022ed-201">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="022ed-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="022ed-202">See also</span></span>

[<span data-ttu-id="022ed-203">**жетадаптерсаддрессес**</span><span class="sxs-lookup"><span data-stu-id="022ed-203">**GetAdaptersAddresses**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[<span data-ttu-id="022ed-204">**IP_ADAPTER_ADDRESSES**</span><span class="sxs-lookup"><span data-stu-id="022ed-204">**IP_ADAPTER_ADDRESSES**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[<span data-ttu-id="022ed-205">**IP_ADAPTER_UNICAST_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="022ed-205">**IP_ADAPTER_UNICAST_ADDRESS**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[<span data-ttu-id="022ed-206">**IP_DAD_STATE**</span><span class="sxs-lookup"><span data-stu-id="022ed-206">**IP_DAD_STATE**</span></span>](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[<span data-ttu-id="022ed-207">**MIB_IF_ROW2**</span><span class="sxs-lookup"><span data-stu-id="022ed-207">**MIB_IF_ROW2**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[<span data-ttu-id="022ed-208">**MIB_UNICASTIPADDRESS_ROW**</span><span class="sxs-lookup"><span data-stu-id="022ed-208">**MIB_UNICASTIPADDRESS_ROW**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[<span data-ttu-id="022ed-209">**SCOPE_LEVEL**</span><span class="sxs-lookup"><span data-stu-id="022ed-209">**SCOPE_LEVEL**</span></span>](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[<span data-ttu-id="022ed-210">**SOCKET_ADDRESS_LIST**</span><span class="sxs-lookup"><span data-stu-id="022ed-210">**SOCKET_ADDRESS_LIST**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[<span data-ttu-id="022ed-211">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="022ed-211">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="022ed-212">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="022ed-212">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="022ed-213">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="022ed-213">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="022ed-214">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="022ed-214">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="022ed-215">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="022ed-215">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="022ed-216">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="022ed-216">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="022ed-217">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="022ed-217">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
