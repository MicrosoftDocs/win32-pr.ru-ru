---
description: Управляющий код освобождает резервирование времени выполнения для блока портов TCP или UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: Код элемента управления SIO_RELEASE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57f96d0396d661eba12f9e64238c492f38e97b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719456"
---
# <a name="sio_release_port_reservation-control-code"></a><span data-ttu-id="e6ccd-103">Код элемента управления SIO_RELEASE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="e6ccd-103">SIO_RELEASE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="e6ccd-104">Описание</span><span class="sxs-lookup"><span data-stu-id="e6ccd-104">Description</span></span>

<span data-ttu-id="e6ccd-105">Код **управления \_ \_ \_ резервирования порта SIO** освобождает резервирование времени выполнения для блока портов TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-105">The **SIO\_RELEASE\_PORT\_RESERVATION** control code releases a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="e6ccd-106">Зарезервированное время выполнения должно быть получено из процесса выдачи с помощью [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-106">The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span></span>

<span data-ttu-id="e6ccd-107">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="e6ccd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6ccd-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="e6ccd-109">s</span><span class="sxs-lookup"><span data-stu-id="e6ccd-109">s</span></span>

<span data-ttu-id="e6ccd-110">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="e6ccd-111">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="e6ccd-111">dwIoControlCode</span></span>

<span data-ttu-id="e6ccd-112">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-112">The control code for the operation.</span></span>
<span data-ttu-id="e6ccd-113">Используйте для этой операции **\_ \_ \_ резервирование портов освобождения SIO** .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-113">Use **SIO\_RELEASE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="e6ccd-114">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="e6ccd-114">lpvInBuffer</span></span>

<span data-ttu-id="e6ccd-115">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="e6ccd-116">Этот параметр содержит указатель на структуру [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) с маркером резервирования порта TCP или UDP для освобождения.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-116">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to release.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="e6ccd-117">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="e6ccd-117">cbInBuffer</span></span>

<span data-ttu-id="e6ccd-118">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="e6ccd-119">Этот параметр должен быть не меньше размера структуры [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-119">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="e6ccd-120">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="e6ccd-120">lpvOutBuffer</span></span>

<span data-ttu-id="e6ccd-121">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-121">A pointer to the output buffer.</span></span>
<span data-ttu-id="e6ccd-122">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-122">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="e6ccd-123">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="e6ccd-123">cbOutBuffer</span></span>

<span data-ttu-id="e6ccd-124">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-124">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="e6ccd-125">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-125">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="e6ccd-126">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="e6ccd-126">lpcbBytesReturned</span></span>

<span data-ttu-id="e6ccd-127">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-127">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="e6ccd-128">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-128">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="e6ccd-129">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-129">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="e6ccd-130">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-130">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="e6ccd-131">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-131">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="e6ccd-132">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-132">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="e6ccd-133">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="e6ccd-133">lpvOverlapped</span></span>

<span data-ttu-id="e6ccd-134">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-134">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e6ccd-135">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-135">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="e6ccd-136">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-136">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="e6ccd-137">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-137">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e6ccd-138">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-138">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="e6ccd-139">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="e6ccd-140">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="e6ccd-140">lpCompletionRoutine</span></span>

<span data-ttu-id="e6ccd-141">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="e6ccd-141">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="e6ccd-142">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="e6ccd-142">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="e6ccd-143">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="e6ccd-143">lpThreadId</span></span>

<span data-ttu-id="e6ccd-144">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="e6ccd-144">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="e6ccd-145">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-145">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="e6ccd-146">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-146">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="e6ccd-147">лперрно</span><span class="sxs-lookup"><span data-stu-id="e6ccd-147">lpErrno</span></span>

<span data-ttu-id="e6ccd-148">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-148">A pointer to the error code.</span></span>

<span data-ttu-id="e6ccd-149">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-149">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6ccd-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6ccd-150">Return value</span></span>

<span data-ttu-id="e6ccd-151">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-151">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="e6ccd-152">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-152">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="e6ccd-153">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="e6ccd-153">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="e6ccd-154">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="e6ccd-154">Error code</span></span> | <span data-ttu-id="e6ccd-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ccd-155">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="e6ccd-156">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-156">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="e6ccd-157">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-157">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="e6ccd-158">Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-158">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="e6ccd-159">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-159">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="e6ccd-160">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-160">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="e6ccd-161">Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды **SIO_FLUSH** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-161">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="e6ccd-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-162">**WSAEFAULT**</span></span> | <span data-ttu-id="e6ccd-163">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-163">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="e6ccd-164">Эта ошибка возвращается параметром *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-164">This error is returned of the *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="e6ccd-165">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="e6ccd-166">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-166">A blocking operation is currently executing.</span></span> <span data-ttu-id="e6ccd-167">Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-167">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="e6ccd-168">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-168">**WSAEINTR**</span></span> | <span data-ttu-id="e6ccd-169">Операция блокировки была прервана вызовом **всаканцелблоккингкалл**.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-169">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="e6ccd-170">Эта ошибка возвращается в случае прерывания блокирующей операции.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-170">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="e6ccd-171">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-171">**WSAEINVAL**</span></span> | <span data-ttu-id="e6ccd-172">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-172">An invalid argument was supplied.</span></span> <span data-ttu-id="e6ccd-173">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-173">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="e6ccd-174">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-174">**WSAENETDOWN**</span></span> | <span data-ttu-id="e6ccd-175">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-175">A socket operation encountered a dead network.</span></span> <span data-ttu-id="e6ccd-176">Эта ошибка возвращается в случае сбоя сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-176">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="e6ccd-177">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-177">**WSAENOTSOCK**</span></span> | <span data-ttu-id="e6ccd-178">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-178">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="e6ccd-179">Эта ошибка возвращается, если дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-179">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="e6ccd-180">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="e6ccd-181">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-181">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="e6ccd-182">Эта ошибка возвращается, если указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-182">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="e6ccd-183">Эта ошибка также возвращается, если поставщик транспорта не поддерживает запрос на **\_ \_ \_ зарезервированный номер порта освобождения SIO** .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-183">This error is also returned if the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="e6ccd-184">Эта ошибка также возвращается, если попытка использования ioctl **\_ \_ порта \_ выпуска SIO** выполняется на сокете, отличном от UDP или TCP.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-184">This error is also returned when an attempt to use the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="e6ccd-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6ccd-185">Remarks</span></span>

<span data-ttu-id="e6ccd-186">В Windows Vista и более поздних версиях операционной системы поддерживается запрос IOCTL для **\_ \_ \_ резервирования портов** в версии SIO.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-186">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="e6ccd-187">Приложения и службы, которым необходимо резервировать порты, делятся на две категории.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-187">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="e6ccd-188">Первая категория включает компоненты, которым требуется определенный порт в рамках своей работы.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-188">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="e6ccd-189">Такие компоненты, как правило, предпочитают указывать требуемый порт во время установки (например, в манифесте приложения).</span><span class="sxs-lookup"><span data-stu-id="e6ccd-189">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="e6ccd-190">Вторая категория включает компоненты, которым требуется любой доступный порт или блок портов во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-190">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="e6ccd-191">Эти две категории соответствуют конкретным и запросам резервирования портов с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-191">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="e6ccd-192">Определенные запросы на резервирование могут быть постоянными или средой выполнения, тогда как запросы резервирования портов с подстановочными знаками поддерживаются только во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-192">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="e6ccd-193">[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl используется для запроса резервирования среды выполнения для блока портов TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-193">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="e6ccd-194">Для резервирования портов во время выполнения пул портов требует, чтобы резервирования использовались в процессе, для которого было предоставлено резервирование.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-194">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="e6ccd-195">Количество резервирований портов среды выполнения последний раз, пока время существования сокета, на котором вызывался [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-195">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="e6ccd-196">Напротив, постоянные резервирования портов, созданные с помощью функции [**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) или [**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) , могут быть использованы любым процессом с возможностью получения постоянных резервирований.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-196">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="e6ccd-197">**\_ \_ \_ Зарезервированный номер порта освобождения SIO** используется для освобождения резервирования времени выполнения для блока портов TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-197">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is used to release a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="e6ccd-198">Если оба параметра *лповерлаппед* и *лпкомплетионраутине* равны **null**, сокет в этой функции будет рассматриваться как сокет без перекрытия.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-198">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="e6ccd-199">Для не перекрывающихся сокетов параметры *лповерлаппед* и *лпкомплетионраутине* игнорируются, за исключением того, что функция может блокироваться, *Если сокеты* находятся в блокирующем режиме.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-199">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="e6ccd-200">Если *сокеты* находятся в режиме без блокировки, эта функция по-прежнему будет заблокирована, так как этот КОНКРЕТНЫЙ запрос IOCTL не поддерживает режим без блокировки.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-200">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="e6ccd-201">Для перекрывающихся сокетов операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-201">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="e6ccd-202">Любой запрос IOCTL может блокироваться неограниченно в зависимости от реализации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-202">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="e6ccd-203">Если приложение не допускает блокировку в вызове функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** , перекрывающиеся операции ввода-вывода будут рекомендованы для ioctl, которые, скорее всего, блокируются.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-203">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="e6ccd-204">В следующих случаях операция IOCTL с **\_ \_ \_ зарезервированным портом SIO** может завершиться ошибкой, так как операции **всаеинтр** или **WSA \_ \_ прерываются** .</span><span class="sxs-lookup"><span data-stu-id="e6ccd-204">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="e6ccd-205">Запрос отменяется диспетчером ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="e6ccd-206">Сокет закрыт.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-206">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="e6ccd-207">Примеры</span><span class="sxs-lookup"><span data-stu-id="e6ccd-207">Examples</span></span>

<span data-ttu-id="e6ccd-208">В следующем примере запрашивается резервирование портов среды выполнения, а затем освобождается резервирование портов среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="e6ccd-208">The following example acquires a runtime port reservation and then releases the runtime port reservation.</span></span>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a><span data-ttu-id="e6ccd-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6ccd-209">See also</span></span>

[<span data-ttu-id="e6ccd-210">**креатеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-210">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="e6ccd-211">**креатеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-211">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="e6ccd-212">**делетеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-212">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="e6ccd-213">**делетеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-213">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="e6ccd-214">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-214">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="e6ccd-215">**лукупперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-215">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="e6ccd-216">**лукупперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-216">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="e6ccd-217">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-217">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="e6ccd-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="e6ccd-219">фиксатор</span><span class="sxs-lookup"><span data-stu-id="e6ccd-219">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="e6ccd-220">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-220">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="e6ccd-221">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-221">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="e6ccd-222">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-222">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="e6ccd-223">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-223">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="e6ccd-224">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-224">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="e6ccd-225">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="e6ccd-225">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
