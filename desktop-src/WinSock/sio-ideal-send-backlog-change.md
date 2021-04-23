---
description: Управляющий код уведомляет приложение при изменении идеального значения невыполненной работы при отправке для соединения.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: Код элемента управления SIO_IDEAL_SEND_BACKLOG_CHANGE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812454"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a><span data-ttu-id="74f34-103">Код элемента управления SIO_IDEAL_SEND_BACKLOG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="74f34-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="74f34-104">Описание</span><span class="sxs-lookup"><span data-stu-id="74f34-104">Description</span></span>

<span data-ttu-id="74f34-105">Код **управления \_ \_ \_ \_ изменениями невыполненной работы суперконтроллера** ввода-вывода уведомляет приложение о том, что для соединения было изменено значение невыполненной работы (ISB) отправки.</span><span class="sxs-lookup"><span data-stu-id="74f34-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** control code notifies an application when the ideal send backlog (ISB) value changes for the connection.</span></span>

<span data-ttu-id="74f34-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="74f34-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="74f34-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="74f34-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="74f34-108">s</span><span class="sxs-lookup"><span data-stu-id="74f34-108">s</span></span>

<span data-ttu-id="74f34-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="74f34-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="74f34-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="74f34-110">dwIoControlCode</span></span>

<span data-ttu-id="74f34-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="74f34-111">The control code for the operation.</span></span>
<span data-ttu-id="74f34-112">Используйте **\_ оптимальное \_ \_ \_ изменение невыполненной работы SIO** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="74f34-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="74f34-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="74f34-113">lpvInBuffer</span></span>

<span data-ttu-id="74f34-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="74f34-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="74f34-115">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="74f34-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="74f34-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="74f34-116">cbInBuffer</span></span>

<span data-ttu-id="74f34-117">Размер входного буфера в байтах. Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="74f34-117">The size, in bytes, of the input buffer.This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="74f34-118">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="74f34-118">lpvOutBuffer</span></span>

<span data-ttu-id="74f34-119">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="74f34-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="74f34-120">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="74f34-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="74f34-121">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="74f34-121">cbOutBuffer</span></span>

<span data-ttu-id="74f34-122">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="74f34-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="74f34-123">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="74f34-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="74f34-124">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="74f34-124">lpcbBytesReturned</span></span>

<span data-ttu-id="74f34-125">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="74f34-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="74f34-126">Этот возвращаемый параметр указывает на значение **DWORD** , равное нулю, для этой операции, так как выходные данные отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="74f34-126">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="74f34-127">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="74f34-127">lpvOverlapped</span></span>

<span data-ttu-id="74f34-128">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="74f34-128">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="74f34-129">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="74f34-129">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="74f34-130">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="74f34-130">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="74f34-131">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="74f34-131">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="74f34-132">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="74f34-132">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="74f34-133">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="74f34-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="74f34-134">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="74f34-134">lpCompletionRoutine</span></span>

<span data-ttu-id="74f34-135">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="74f34-135">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="74f34-136">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="74f34-136">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="74f34-137">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="74f34-137">lpThreadId</span></span>

<span data-ttu-id="74f34-138">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="74f34-138">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="74f34-139">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="74f34-139">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="74f34-140">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="74f34-140">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="74f34-141">лперрно</span><span class="sxs-lookup"><span data-stu-id="74f34-141">lpErrno</span></span>

<span data-ttu-id="74f34-142">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="74f34-142">A pointer to the error code.</span></span>

<span data-ttu-id="74f34-143">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="74f34-143">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="74f34-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74f34-144">Return value</span></span>

<span data-ttu-id="74f34-145">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="74f34-145">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="74f34-146">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="74f34-146">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="74f34-147">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="74f34-147">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="74f34-148">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="74f34-148">Error code</span></span> | <span data-ttu-id="74f34-149">Значение</span><span class="sxs-lookup"><span data-stu-id="74f34-149">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="74f34-150">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="74f34-150">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="74f34-151">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="74f34-151">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="74f34-152">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="74f34-152">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="74f34-153">Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="74f34-153">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="74f34-154">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="74f34-154">**WSAEFAULT**</span></span> | <span data-ttu-id="74f34-155">Параметр *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="74f34-155">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="74f34-156">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="74f34-156">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="74f34-157">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="74f34-157">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="74f34-158">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="74f34-158">**WSAEINTR**</span></span> | <span data-ttu-id="74f34-159">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="74f34-159">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="74f34-160">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="74f34-160">**WSAEINVAL**</span></span> | <span data-ttu-id="74f34-161">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="74f34-161">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="74f34-162">Эта ошибка возвращается, если параметр *кбаутбуффер* не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="74f34-162">This error is returned if the *cbOutBuffer* parameter is not zero.</span></span> |
| <span data-ttu-id="74f34-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="74f34-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="74f34-164">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="74f34-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="74f34-165">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="74f34-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="74f34-166">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="74f34-166">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="74f34-167">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="74f34-167">**WSAENOTCONN**</span></span> | <span data-ttu-id="74f34-168">*Сокеты не* подключены.</span><span class="sxs-lookup"><span data-stu-id="74f34-168">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="74f34-169">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="74f34-169">**WSAENOTSOCK**</span></span> | <span data-ttu-id="74f34-170">Дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="74f34-170">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="74f34-171">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="74f34-171">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="74f34-172">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="74f34-172">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="74f34-173">Эта ошибка возвращается, если поставщик транспорта не поддерживает запрос IOCTL **\_ \_ \_ невыполненной работы \_ по отправке SIO** .</span><span class="sxs-lookup"><span data-stu-id="74f34-173">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="74f34-174">Эта ошибка также возвращается, когда попытка использовать оптимальный запрос IOCTL для **\_ \_ отправки \_ невыполненной работы \_ SIO** на сокете датаграмм.</span><span class="sxs-lookup"><span data-stu-id="74f34-174">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="74f34-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74f34-175">Remarks</span></span>

<span data-ttu-id="74f34-176">В Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы поддерживается протокол IOCTL для **\_ оптимальной \_ отправки \_ невыполненной работы \_** .</span><span class="sxs-lookup"><span data-stu-id="74f34-176">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="74f34-177">При отправке данных через TCP-соединение с помощью сокетов Windows важно обеспечить достаточное количество необработанных данных (отправленных, но еще не подтвержденных) в TCP для достижения максимальной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="74f34-177">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="74f34-178">Оптимальное значение объема данных, необходимых для достижения наилучшей пропускной способности для подключения TCP, называется идеальным размером невыполненной отправки (ISB).</span><span class="sxs-lookup"><span data-stu-id="74f34-178">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="74f34-179">Значение ISB является функцией произведения задержки пропускной способности подключения TCP и полученного окна приема получателя (а также частично перегрузки в сети).</span><span class="sxs-lookup"><span data-stu-id="74f34-179">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="74f34-180">Значение ISB для каждого подключения доступно в реализации протокола TCP в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="74f34-180">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="74f34-181">**\_ Оптимальный запрос \_ на \_ отработку невыполненной работы \_ по отправке SIO** может использоваться приложением для получения уведомления при динамическом изменении значения ISB для соединения.</span><span class="sxs-lookup"><span data-stu-id="74f34-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="74f34-182">В Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы для ориентированных на поток сокетов, находящихся в подключенном состоянии, поддерживается **\_ \_ \_ \_ изменение невыполненной работы SIO** и [**\_ оптимальный \_ \_ \_ запрос на отработку невыполненной**](sio-ideal-send-backlog-query.md) работы.</span><span class="sxs-lookup"><span data-stu-id="74f34-182">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="74f34-183">Диапазон значений ISB для TCP-соединения теоретически может иметь размер от 0 до 16 мегабайт.</span><span class="sxs-lookup"><span data-stu-id="74f34-183">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="74f34-184">См. страницу справки по запросу IOCTL для [**\_ \_ \_ \_ запроса на отработку**](sio-ideal-send-backlog-query.md) отказа от суперконтроллера ввода-вывода для типичного использования механизма ISB, обеспечивающего лучшую пропускную способность для подключений к продуктам с высокой</span><span class="sxs-lookup"><span data-stu-id="74f34-184">See the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL reference page for typical usage of the ISB mechanism for achieving better throughput over high bandwidth-delay product connections.</span></span>

<span data-ttu-id="74f34-185">**\_ Оптимальный запрос \_ на \_ отработку невыполненной работы \_ по отправке SIO** разрешен только для сокета потока, который находится в подключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="74f34-185">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="74f34-186">В противном случае функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** завершится с ошибкой **всаенотконн**.</span><span class="sxs-lookup"><span data-stu-id="74f34-186">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="74f34-187">**\_ Оптимальный запрос \_ на \_ отработку невыполненной работы \_ по отправке SIO** не использует буферы ввода или вывода, а также пендс или блоки, пока в базовом соединении не произойдет изменение ISB.</span><span class="sxs-lookup"><span data-stu-id="74f34-187">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL uses no input or output buffers and pends or blocks until an ISB change occurs on the underlying connection.</span></span>
<span data-ttu-id="74f34-188">После завершения этого запроса IOCTL приложение Winsock может использовать запрос IOCTL с [**\_ идеальными \_ для \_ отправки \_ невыполненной работы**](sio-ideal-send-backlog-query.md) по протоколу SIO для получения нового значения ISB в соединении.</span><span class="sxs-lookup"><span data-stu-id="74f34-188">When this IOCTL is completed, a Winsock application can use the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL to retrieve the new ISB value on the connection.</span></span>

<span data-ttu-id="74f34-189">**\_ Оптимальный запрос \_ на \_ отработку невыполненной работы \_ по отправке SIO** не поддерживает режим без блокировки.</span><span class="sxs-lookup"><span data-stu-id="74f34-189">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL does not support non-blocking mode.</span></span>
<span data-ttu-id="74f34-190">Приложению разрешено выдавать этот запрос IOCTL на неблокирующем сокете, но запрос IOCTL просто блокируется или откладывается до тех пор, пока значение ISB не изменится.</span><span class="sxs-lookup"><span data-stu-id="74f34-190">An application is allowed to issue this IOCTL on a non-blocking socket, but the IOCTL will simply block or pend until the ISB value changes.</span></span>

<span data-ttu-id="74f34-191">Если оба параметра *лповерлаппед* и *лпкомплетионраутине* равны NULL, сокет в этой функции будет рассматриваться как сокет без перекрытия.</span><span class="sxs-lookup"><span data-stu-id="74f34-191">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="74f34-192">Для не перекрывающихся сокетов параметры *лповерлаппед* и *лпкомплетионраутине* игнорируются, за исключением того, что функция может блокироваться, *Если сокеты* находятся в блокирующем режиме.</span><span class="sxs-lookup"><span data-stu-id="74f34-192">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="74f34-193">Если *сокеты* находятся в режиме без блокировки, эта функция по-прежнему будет заблокирована, так как этот КОНКРЕТНЫЙ запрос IOCTL не поддерживает режим без блокировки.</span><span class="sxs-lookup"><span data-stu-id="74f34-193">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="74f34-194">Для перекрывающихся сокетов операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="74f34-194">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="74f34-195">Любой запрос IOCTL может блокироваться неограниченно в зависимости от реализации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="74f34-195">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="74f34-196">Если приложение не допускает блокировку в вызове функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** , перекрывающиеся операции ввода-вывода будут рекомендованы для ioctl, которые, скорее всего, блокируются.</span><span class="sxs-lookup"><span data-stu-id="74f34-196">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="74f34-197">**\_ Оптимальный запрос \_ на \_ отработку невыполненной работы \_ по отправке через Суперконтроллер** ввода-вывода предоставляет уведомление и должно блокироваться, пока значение ISB не изменится.</span><span class="sxs-lookup"><span data-stu-id="74f34-197">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL provides a notification and is expected to block or pend until the ISB value changes.</span></span>
<span data-ttu-id="74f34-198">Поэтому он обычно вызывается асинхронно с параметром *лповерлаппед* , для которого задана допустимая структура всаоверлаппед.</span><span class="sxs-lookup"><span data-stu-id="74f34-198">So it would commonly be called asynchronously with the *lpOverlapped* parameter set to a valid WSAOVERLAPPED structure.</span></span>

<span data-ttu-id="74f34-199">**\_ Оптимальный запрос \_ на \_ отработку \_** отказа отправки через Суперконтроллер ввода/вывода может завершиться ошибкой, если операция **всаеинтр** или **WSA \_ \_ прервана** в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="74f34-199">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="74f34-200">Подключение TCP корректно отключается в направлении отправки.</span><span class="sxs-lookup"><span data-stu-id="74f34-200">The TCP connection is gracefully disconnected in the send direction.</span></span> <span data-ttu-id="74f34-201">Это может произойти в результате вызова функции Shutdown с тем, как для параметра установлено значение **SD \_ Send**, вызов функции **Дисконнектекс** или вызов функции **TransmitFile** или **трансмитпаккетс** с параметром *DwFlags* , для которого задано значение **tf \_ Disconnect** или **tf \_ reмногократного использования**.</span><span class="sxs-lookup"><span data-stu-id="74f34-201">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
* <span data-ttu-id="74f34-202">Подключение TCP сброшено или прервано.</span><span class="sxs-lookup"><span data-stu-id="74f34-202">The TCP connection has been reset or aborted.</span></span>
* <span data-ttu-id="74f34-203">Приложение выдает запрос IOCTL для **\_ оптимального \_ \_ \_ изменения невыполненной работы при отправке** запроса на уведомление.</span><span class="sxs-lookup"><span data-stu-id="74f34-203">The application issues a **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL when there is already a pended notification request.</span></span> <span data-ttu-id="74f34-204">В каждый момент времени допускается только 1 1 ожидающих запросов на **\_ \_ \_ \_ изменение невыполненной работы** .</span><span class="sxs-lookup"><span data-stu-id="74f34-204">Only one one pended **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** request is allowed at a time.</span></span>
* <span data-ttu-id="74f34-205">Запрос отменяется диспетчером ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="74f34-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="74f34-206">Сокет закрыт.</span><span class="sxs-lookup"><span data-stu-id="74f34-206">The socket is closed.</span></span>

<span data-ttu-id="74f34-207">Две встроенные функции-оболочки для этих IOCTL определены в файле заголовка *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="74f34-207">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="74f34-208">Рекомендуется использовать эти встроенные функции вместо того, чтобы использовать **\_ оптимальное \_ \_ \_ изменение невыполненной работы SIO** и [**\_ \_ \_ невыполненную \_**](sio-ideal-send-backlog-query.md) работу по запросу IOCTL.</span><span class="sxs-lookup"><span data-stu-id="74f34-208">It is recommended that these inline functions be used instead of using the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs directly.</span></span>

<span data-ttu-id="74f34-209">Встроенная функция-оболочка для **\_ идеального \_ \_ \_ изменения невыполненной работы по отправке SIO** — функция **идеалсендбакклогнотифи** .</span><span class="sxs-lookup"><span data-stu-id="74f34-209">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="74f34-210">Встроенная функция-оболочка для [**\_ \_ \_ \_ запроса на отработку невыполненной работы суперконтроллера**](sio-ideal-send-backlog-query.md) ввода-вывода с помощью ioctl — это функция **идеалсендбакклогкуери** .</span><span class="sxs-lookup"><span data-stu-id="74f34-210">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL is the **idealsendbacklogquery** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="74f34-211">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74f34-211">See also</span></span>

[<span data-ttu-id="74f34-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span><span class="sxs-lookup"><span data-stu-id="74f34-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span></span>](sio-ideal-send-backlog-query.md)

[<span data-ttu-id="74f34-213">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="74f34-213">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="74f34-214">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="74f34-214">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="74f34-215">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="74f34-215">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="74f34-216">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="74f34-216">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="74f34-217">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="74f34-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="74f34-218">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="74f34-218">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="74f34-219">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="74f34-219">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
