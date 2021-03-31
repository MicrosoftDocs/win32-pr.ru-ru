---
description: Управляющий код включает или отключает параметр для каждого подключения для параметра проверки активности TCP, который указывает время ожидания и интервал проверки активности TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Код элемента управления SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155866"
---
# <a name="sio_keepalive_vals-control-code"></a><span data-ttu-id="2f49c-103">Код элемента управления SIO_KEEPALIVE_VALS</span><span class="sxs-lookup"><span data-stu-id="2f49c-103">SIO_KEEPALIVE_VALS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="2f49c-104">Описание</span><span class="sxs-lookup"><span data-stu-id="2f49c-104">Description</span></span>

<span data-ttu-id="2f49c-105">Управляющий код **\_ \_ Валс** контроля доступа SIO включает или отключает параметр для каждого подключения для параметра проверки активности TCP, который указывает время ожидания и интервал проверки активности TCP.</span><span class="sxs-lookup"><span data-stu-id="2f49c-105">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval.</span></span>

<span data-ttu-id="2f49c-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="2f49c-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="2f49c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f49c-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="2f49c-108">s</span><span class="sxs-lookup"><span data-stu-id="2f49c-108">s</span></span>

<span data-ttu-id="2f49c-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="2f49c-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="2f49c-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="2f49c-110">dwIoControlCode</span></span>

<span data-ttu-id="2f49c-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="2f49c-111">The control code for the operation.</span></span>
<span data-ttu-id="2f49c-112">Используйте **\_ \_ Валс KeepAlive** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="2f49c-112">Use **SIO\_KEEPALIVE\_VALS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="2f49c-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="2f49c-113">lpvInBuffer</span></span>

<span data-ttu-id="2f49c-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="2f49c-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="2f49c-115">Этот параметр должен указывать на структуру **TCP \_ KeepAlive** .</span><span class="sxs-lookup"><span data-stu-id="2f49c-115">This parameter should point to a **tcp\_keepalive** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="2f49c-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="2f49c-116">cbInBuffer</span></span>

<span data-ttu-id="2f49c-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="2f49c-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="2f49c-118">Этот параметр должен быть больше или равен размеру структуры **\_ KeepAlive TCP** , указанной параметром *лпвинбуффер* .</span><span class="sxs-lookup"><span data-stu-id="2f49c-118">This parameter should equal to or greater than the size of the **tcp\_keepalive** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="2f49c-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="2f49c-119">lpvOutBuffer</span></span>

<span data-ttu-id="2f49c-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="2f49c-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="2f49c-121">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="2f49c-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="2f49c-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="2f49c-122">cbOutBuffer</span></span>

<span data-ttu-id="2f49c-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="2f49c-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="2f49c-124">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="2f49c-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="2f49c-125">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="2f49c-125">lpcbBytesReturned</span></span>

<span data-ttu-id="2f49c-126">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="2f49c-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="2f49c-127">Этот возвращаемый параметр указывает на значение **DWORD** , равное нулю, для этой операции, так как выходные данные отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="2f49c-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="2f49c-128">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="2f49c-128">lpvOverlapped</span></span>

<span data-ttu-id="2f49c-129">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="2f49c-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2f49c-130">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="2f49c-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="2f49c-131">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="2f49c-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="2f49c-132">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="2f49c-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2f49c-133">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="2f49c-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="2f49c-134">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f49c-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="2f49c-135">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="2f49c-135">lpCompletionRoutine</span></span>

<span data-ttu-id="2f49c-136">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="2f49c-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="2f49c-137">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="2f49c-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="2f49c-138">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="2f49c-138">lpThreadId</span></span>

<span data-ttu-id="2f49c-139">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="2f49c-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="2f49c-140">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="2f49c-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="2f49c-141">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="2f49c-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="2f49c-142">лперрно</span><span class="sxs-lookup"><span data-stu-id="2f49c-142">lpErrno</span></span>

<span data-ttu-id="2f49c-143">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="2f49c-143">A pointer to the error code.</span></span>

<span data-ttu-id="2f49c-144">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="2f49c-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f49c-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f49c-145">Return value</span></span>

<span data-ttu-id="2f49c-146">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2f49c-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="2f49c-147">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="2f49c-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="2f49c-148">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="2f49c-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="2f49c-149">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="2f49c-149">Error code</span></span> | <span data-ttu-id="2f49c-150">Значение</span><span class="sxs-lookup"><span data-stu-id="2f49c-150">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="2f49c-151">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="2f49c-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="2f49c-152">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="2f49c-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="2f49c-153">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="2f49c-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="2f49c-154">Операция перекрытия была отменена из-за замыкания сокета или выполнения команды **IOCTL SIO_FLUSH** .</span><span class="sxs-lookup"><span data-stu-id="2f49c-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="2f49c-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="2f49c-155">**WSAEFAULT**</span></span> | <span data-ttu-id="2f49c-156">Параметр *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f49c-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="2f49c-157">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="2f49c-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="2f49c-158">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="2f49c-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="2f49c-159">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="2f49c-159">**WSAEINTR**</span></span> | <span data-ttu-id="2f49c-160">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="2f49c-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="2f49c-161">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="2f49c-161">**WSAEINVAL**</span></span> | <span data-ttu-id="2f49c-162">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="2f49c-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="2f49c-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="2f49c-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="2f49c-164">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="2f49c-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="2f49c-165">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="2f49c-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="2f49c-166">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="2f49c-166">The socket option is not supported on the specified protocol.</span></span> <span data-ttu-id="2f49c-167">Эта ошибка возвращается для сокета датаграммы.</span><span class="sxs-lookup"><span data-stu-id="2f49c-167">This error is returned for a datagram socket.</span></span> |
| <span data-ttu-id="2f49c-168">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="2f49c-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="2f49c-169">Дескриптор s не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="2f49c-169">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="2f49c-170">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="2f49c-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="2f49c-171">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2f49c-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="2f49c-172">Эта ошибка возвращается в том случае, если поставщик транспорта не поддерживает **\_ \_ Валс ioctl суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="2f49c-172">This error is returned if the **SIO\_KEEPALIVE\_VALS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2f49c-173">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f49c-173">Remarks</span></span>

<span data-ttu-id="2f49c-174">В Windows 2000 и более поздних версиях операционной системы поддерживается запрос IOCTL **\_ KeepAlive \_ Валс** .</span><span class="sxs-lookup"><span data-stu-id="2f49c-174">The **SIO\_KEEPALIVE\_VALS** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="2f49c-175">Управляющий код **\_ \_ Валс поддержки SIO** включает или отключает параметр для каждого подключения для параметра проверки активности TCP, который указывает время ожидания проверки активности TCP и интервал, используемый для пакетов поддержания активности TCP.</span><span class="sxs-lookup"><span data-stu-id="2f49c-175">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval used for TCP keep-alive packets.</span></span>
<span data-ttu-id="2f49c-176">Дополнительные сведения о параметре проверки активности см. в разделе 4.2.3.6 (требования для узлов Интернета) — уровни взаимодействия, указанные в RFC 1122, доступны на [веб-сайте IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="2f49c-176">For more information on the keep-alive option, see section 4.2.3.6 on the Requirements for Internet Hosts—Communication Layers specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="2f49c-177">(Этот ресурс может быть доступен только на английском языке.)</span><span class="sxs-lookup"><span data-stu-id="2f49c-177">(This resource may only be available in English.)</span></span>

<span data-ttu-id="2f49c-178">Параметр *лпвинбуффер* должен указывать на структуру **TCP \_ KeepAlive** , определенную в файле заголовка *мсткпип. h* .</span><span class="sxs-lookup"><span data-stu-id="2f49c-178">The *lpvInBuffer* parameter should point to a **tcp\_keepalive** structure defined in the *Mstcpip.h* header file.</span></span>
<span data-ttu-id="2f49c-179">Эта структура определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f49c-179">This structure is defined as follows:</span></span>

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

<span data-ttu-id="2f49c-180">Значение, указанное в элементе **онофф** , определяет, включена или отключена проверка активности TCP.</span><span class="sxs-lookup"><span data-stu-id="2f49c-180">The value specified in the **onoff** member determines if TCP keep-alive is enabled or disabled.</span></span>
<span data-ttu-id="2f49c-181">Если для элемента **онофф** задано ненулевое значение, то поддерживается проверка активности TCP и используются другие элементы структуры.</span><span class="sxs-lookup"><span data-stu-id="2f49c-181">If the **onoff** member is set to a nonzero value, TCP keep-alive is enabled and the other members in the structure are used.</span></span>
<span data-ttu-id="2f49c-182">Элемент **KeepAliveTime** указывает время ожидания (в миллисекундах) без активности, пока не будет отправлен первый пакет проверки активности.</span><span class="sxs-lookup"><span data-stu-id="2f49c-182">The **keepalivetime** member specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent.</span></span>
<span data-ttu-id="2f49c-183">Член **keepAliveInterval** указывает интервал (в миллисекундах) между отправкой последовательных пакетов поддержания активности, если подтверждение не получено.</span><span class="sxs-lookup"><span data-stu-id="2f49c-183">The **keepaliveinterval** member specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgement is received.</span></span>

<span data-ttu-id="2f49c-184">Параметр [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , который является одним из [**параметров сокета SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options), также может использоваться для включения или отключения проверки активности TCP в соединении, а также для запроса текущего состояния этого параметра.</span><span class="sxs-lookup"><span data-stu-id="2f49c-184">The [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option, which is one of the [**SOL_SOCKET Socket Options**](/windows/desktop/winsock/sol-socket-socket-options), can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option.</span></span>
<span data-ttu-id="2f49c-185">Чтобы запросить, включена ли поддержка TCP-активности на сокете, функцию жетсоккопт можно вызвать с параметром [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="2f49c-185">To query whether TCP keep-alive is enabled on a socket, the getsockopt function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="2f49c-186">Чтобы включить или отключить протокол TCP на активность, функцию **сетсоккопт** можно вызвать с параметром [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="2f49c-186">To enable or disable TCP keep-alive, the **setsockopt** function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="2f49c-187">Если поддержка проверки активности TCP включена с [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), то параметры TCP, используемые по умолчанию, используются для времени ожидания проверки активности и интервала, если эти значения не были изменены с помощью **SIO \_ KeepAlive \_ Валс**.</span><span class="sxs-lookup"><span data-stu-id="2f49c-187">If TCP keep-alive is enabled with [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="2f49c-188">Значение времени ожидания проверки активности по умолчанию для всей системы может быть управляемым с помощью параметра реестра [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) , который принимает значение в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="2f49c-188">The default system-wide value of the keep-alive timeout is controllable through the [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="2f49c-189">Если ключ не задан, время ожидания проверки активности по умолчанию составляет 2 часа.</span><span class="sxs-lookup"><span data-stu-id="2f49c-189">If the key is not set, the default keep-alive timeout is 2 hours.</span></span>
<span data-ttu-id="2f49c-190">Значение интервала проверки активности по умолчанию может быть управляемым с помощью параметра реестра [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) , который принимает значение в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="2f49c-190">The default system-wide value of the keep-alive interval is controllable through the [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="2f49c-191">Если ключ не задан, интервал проверки активности по умолчанию равен 1 секунде.</span><span class="sxs-lookup"><span data-stu-id="2f49c-191">If the key is not set, the default keep-alive interval is 1 second.</span></span>

<span data-ttu-id="2f49c-192">В Windows Vista и более поздних версиях количество проверок активности (повторных передач данных) устанавливается равным 10 и не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="2f49c-192">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="2f49c-193">В Windows Server 2003, Windows XP и Windows 2000 параметр по умолчанию для количества проверок активности по сроку поддержания равен 5.</span><span class="sxs-lookup"><span data-stu-id="2f49c-193">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span>
<span data-ttu-id="2f49c-194">Количество зондов проверки активности может быть управляемым с помощью параметров реестра **TcpMaxDataRetransmissions** и [**пптпткпмаксдатаретрансмиссионс**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="2f49c-194">The number of keep-alive probes is controllable through the **TcpMaxDataRetransmissions** and [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span>
<span data-ttu-id="2f49c-195">Число зондов проверки активности устанавливается равным большему из двух значений раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="2f49c-195">The number of keep-alive probes is set to the larger of the two registry key values.</span></span>
<span data-ttu-id="2f49c-196">Если это число равно 0, зонды проверки активности не будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="2f49c-196">If this number is 0, then keep-alive probes will not be sent.</span></span>
<span data-ttu-id="2f49c-197">Если это число превышает 255, то оно корректируется на 255.</span><span class="sxs-lookup"><span data-stu-id="2f49c-197">If this number is above 255, then it is adjusted to 255.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f49c-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f49c-198">See also</span></span>

<span data-ttu-id="2f49c-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2f49c-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>

<span data-ttu-id="2f49c-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2f49c-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>

<span data-ttu-id="2f49c-201">[**пптпткпмаксдатаретрансмиссионс**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="2f49c-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>

[<span data-ttu-id="2f49c-202">фиксатор</span><span class="sxs-lookup"><span data-stu-id="2f49c-202">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="2f49c-203">**SO_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="2f49c-203">**SO_KEEPALIVE**</span></span>](/windows/desktop/winsock/so-keepalive)

[<span data-ttu-id="2f49c-204">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="2f49c-204">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="2f49c-205">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="2f49c-205">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="2f49c-206">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="2f49c-206">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="2f49c-207">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="2f49c-207">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="2f49c-208">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="2f49c-208">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="2f49c-209">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="2f49c-209">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
