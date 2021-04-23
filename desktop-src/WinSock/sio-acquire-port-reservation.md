---
description: Управляющий код получает резервирование во время выполнения для блока портов TCP или UDP.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: Код элемента управления SIO_ACQUIRE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719476"
---
# <a name="sio_acquire_port_reservation-control-code"></a><span data-ttu-id="b64db-103">Код элемента управления SIO_ACQUIRE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="b64db-103">SIO_ACQUIRE_PORT_RESERVATION control code</span></span>

## <a name="description"></a><span data-ttu-id="b64db-104">Описание</span><span class="sxs-lookup"><span data-stu-id="b64db-104">Description</span></span>

<span data-ttu-id="b64db-105">Контрольный код для **\_ \_ \_ резервирования порта SIO** получает резервирование во время выполнения для блока портов TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="b64db-105">The **SIO\_ACQUIRE\_PORT\_RESERVATION** control code acquires a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="b64db-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="b64db-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="b64db-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b64db-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="b64db-108">s</span><span class="sxs-lookup"><span data-stu-id="b64db-108">s</span></span>

<span data-ttu-id="b64db-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="b64db-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="b64db-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="b64db-110">dwIoControlCode</span></span>

<span data-ttu-id="b64db-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="b64db-111">The control code for the operation.</span></span>
<span data-ttu-id="b64db-112">Для этой операции используйте для **\_ получения \_ порта SIO \_ резервирование портов**  .</span><span class="sxs-lookup"><span data-stu-id="b64db-112">Use **SIO\_ACQUIRE\_PORT\_RESERVATION**  for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="b64db-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="b64db-113">lpvInBuffer</span></span>

<span data-ttu-id="b64db-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="b64db-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="b64db-115">Этот параметр содержит указатель на структуру [**\_ \_ диапазона портов inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) , которая указывает номер начальной точки и число портов для резервирования.</span><span class="sxs-lookup"><span data-stu-id="b64db-115">This parameter contains a pointer to an [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure that specifies the starting point number and the number of ports to reserve.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="b64db-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="b64db-116">cbInBuffer</span></span>

<span data-ttu-id="b64db-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="b64db-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="b64db-118">Этот параметр должен быть размером структуры [**\_ \_ диапазона портов inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) .</span><span class="sxs-lookup"><span data-stu-id="b64db-118">This parameter should be the size of the [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="b64db-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="b64db-119">lpvOutBuffer</span></span>

<span data-ttu-id="b64db-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="b64db-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="b64db-121">При успешном выходе этот параметр содержит указатель на структуру [**\_ \_ \_ экземпляра резервирования порта inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="b64db-121">On successful output, this parameter contains a pointer to an [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="b64db-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="b64db-122">cbOutBuffer</span></span>

<span data-ttu-id="b64db-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="b64db-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="b64db-124">Этот параметр должен быть не меньше размера структуры [**\_ \_ \_ экземпляра резервирования порта inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="b64db-124">This parameter must be at least the size of the [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="b64db-125">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="b64db-125">lpcbBytesReturned</span></span>

<span data-ttu-id="b64db-126">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="b64db-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="b64db-127">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="b64db-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="b64db-128">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="b64db-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="b64db-129">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="b64db-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="b64db-130">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="b64db-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="b64db-131">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="b64db-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="b64db-132">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="b64db-132">lpvOverlapped</span></span>

<span data-ttu-id="b64db-133">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b64db-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b64db-134">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b64db-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="b64db-135">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="b64db-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="b64db-136">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b64db-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b64db-137">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="b64db-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="b64db-138">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b64db-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="b64db-139">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="b64db-139">lpCompletionRoutine</span></span>

<span data-ttu-id="b64db-140">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="b64db-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="b64db-141">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="b64db-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="b64db-142">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="b64db-142">lpThreadId</span></span>

<span data-ttu-id="b64db-143">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове **впукуеуеапк**.</span><span class="sxs-lookup"><span data-stu-id="b64db-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to **WPUQueueApc**.</span></span>
<span data-ttu-id="b64db-144">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция **впукуеуеапк** не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="b64db-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the **WPUQueueApc** function returns.</span></span>

<span data-ttu-id="b64db-145">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="b64db-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="b64db-146">лперрно</span><span class="sxs-lookup"><span data-stu-id="b64db-146">lpErrno</span></span>

<span data-ttu-id="b64db-147">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b64db-147">A pointer to the error code.</span></span>

<span data-ttu-id="b64db-148">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="b64db-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b64db-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b64db-149">Return value</span></span>

<span data-ttu-id="b64db-150">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b64db-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="b64db-151">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="b64db-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="b64db-152">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b64db-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="b64db-153">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="b64db-153">Error code</span></span> | <span data-ttu-id="b64db-154">Значение</span><span class="sxs-lookup"><span data-stu-id="b64db-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="b64db-155">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="b64db-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="b64db-156">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="b64db-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="b64db-157">Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="b64db-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="b64db-158">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="b64db-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="b64db-159">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="b64db-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="b64db-160">Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="b64db-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="b64db-161">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b64db-161">**WSAEFAULT**</span></span> | <span data-ttu-id="b64db-162">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="b64db-162">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="b64db-163">Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="b64db-163">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="b64db-164">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="b64db-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="b64db-165">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="b64db-165">A blocking operation is currently executing.</span></span> <span data-ttu-id="b64db-166">Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b64db-166">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="b64db-167">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="b64db-167">**WSAEINTR**</span></span> | <span data-ttu-id="b64db-168">Операция блокировки была прервана вызовом [**всаканцелблоккингкалл**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="b64db-168">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="b64db-169">Эта ошибка возвращается в случае прерывания блокирующей операции.</span><span class="sxs-lookup"><span data-stu-id="b64db-169">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="b64db-170">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="b64db-170">**WSAEINVAL**</span></span> | <span data-ttu-id="b64db-171">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="b64db-171">An invalid argument was supplied.</span></span> <span data-ttu-id="b64db-172">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="b64db-172">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="b64db-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="b64db-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="b64db-174">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="b64db-174">A socket operation encountered a dead network.</span></span> <span data-ttu-id="b64db-175">Эта ошибка возвращается в случае сбоя сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="b64db-175">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="b64db-176">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="b64db-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="b64db-177">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="b64db-177">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="b64db-178">Эта ошибка возвращается, если дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="b64db-178">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="b64db-179">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="b64db-179">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="b64db-180">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="b64db-180">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="b64db-181">Эта ошибка возвращается, если указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b64db-181">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="b64db-182">Эта ошибка также возвращается, если поставщик транспорта не поддерживает **\_ запрос на получение \_ \_ резервирования порта SIO** .</span><span class="sxs-lookup"><span data-stu-id="b64db-182">This error is also returned if the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="b64db-183">Эта ошибка также возвращается, если попытка использовать запрос на **\_ \_ \_ зарезервированный порт суперконтроллера** ввода/вывода выполняется на сокете, отличном от UDP или TCP.</span><span class="sxs-lookup"><span data-stu-id="b64db-183">This error is also returned when an attempt to use the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b64db-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b64db-184">Remarks</span></span>

<span data-ttu-id="b64db-185">**Запрос на \_ \_ \_ зарезервированный порт SIO** поддерживается в Windows Vista и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b64db-185">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="b64db-186">Приложения и службы, которым необходимо резервировать порты, делятся на две категории.</span><span class="sxs-lookup"><span data-stu-id="b64db-186">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="b64db-187">Первая категория включает компоненты, которым требуется определенный порт в рамках своей работы.</span><span class="sxs-lookup"><span data-stu-id="b64db-187">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="b64db-188">Такие компоненты, как правило, предпочитают указывать требуемый порт во время установки (например, в манифесте приложения).</span><span class="sxs-lookup"><span data-stu-id="b64db-188">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="b64db-189">Вторая категория включает компоненты, которым требуется любой доступный порт или блок портов во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b64db-189">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="b64db-190">Эти две категории соответствуют конкретным и запросам резервирования портов с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="b64db-190">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="b64db-191">Определенные запросы на резервирование могут быть постоянными или средой выполнения, тогда как запросы резервирования портов с подстановочными знаками поддерживаются только во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b64db-191">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="b64db-192">Запрос на получение данных о **\_ \_ \_ резервировании порта SIO**  используется для запроса резервирования среды выполнения для блока портов TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="b64db-192">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="b64db-193">Для резервирования портов во время выполнения пул портов требует, чтобы резервирования использовались в процессе, для которого было предоставлено резервирование.</span><span class="sxs-lookup"><span data-stu-id="b64db-193">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="b64db-194">Количество резервирований портов среды выполнения было последним только в течение времени существования сокета, на котором был вызван **\_ запрос IOCTL \_ \_ резервирования порта**  .</span><span class="sxs-lookup"><span data-stu-id="b64db-194">Runtime port reservations last only as long as the lifetime of the socket on which the **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL was called.</span></span>
<span data-ttu-id="b64db-195">Напротив, постоянные резервирования портов, созданные с помощью функции [**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) или [**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) , могут быть использованы любым процессом с возможностью получения постоянных резервирований.</span><span class="sxs-lookup"><span data-stu-id="b64db-195">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="b64db-196">После получения резервирования порта времени выполнения TCP или UDP приложение может запрашивать назначения портов из резервирования портов, открыв сокет TCP или UDP, а затем вызывая функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) , указывающую на подключение SIO, и передав маркер резервирования перед вызовом функции Bind на сокете. [**\_ \_ \_**](sio-associate-port-reservation.md)</span><span class="sxs-lookup"><span data-stu-id="b64db-196">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the [**SIO\_ASSOCIATE\_PORT\_RESERVATION**](sio-associate-port-reservation.md) IOCTL and passing the reservation token before issuing a call to the bind function on the socket.</span></span>

<span data-ttu-id="b64db-197">Если оба параметра *лповерлаппед* и *лпкомплетионраутине* равны **null**, сокет в этой функции будет рассматриваться как сокет без перекрытия.</span><span class="sxs-lookup"><span data-stu-id="b64db-197">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="b64db-198">Для не перекрывающихся сокетов параметры *лповерлаппед* и *лпкомплетионраутине* игнорируются, за исключением того, что функция может блокироваться, *Если сокеты* находятся в блокирующем режиме.</span><span class="sxs-lookup"><span data-stu-id="b64db-198">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="b64db-199">Если *сокеты* находятся в режиме без блокировки, эта функция по-прежнему будет заблокирована, так как этот КОНКРЕТНЫЙ запрос IOCTL не поддерживает режим без блокировки.</span><span class="sxs-lookup"><span data-stu-id="b64db-199">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="b64db-200">Для перекрывающихся сокетов операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="b64db-200">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="b64db-201">Любой запрос IOCTL может блокироваться неограниченно в зависимости от реализации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="b64db-201">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="b64db-202">Если приложение не допускает блокировку в вызове функции Всаиоктл или **вспиоктл** , перекрывающиеся операции ввода-вывода будут рекомендованы для ioctl, которые, скорее всего, блокируются.</span><span class="sxs-lookup"><span data-stu-id="b64db-202">If the application cannot tolerate blocking in a WSAIoctl or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="b64db-203">Запрос IOCTL на **\_ Получение \_ порта \_ SIO**  может завершиться ошибкой, если операция **всаеинтр** или **WSA \_ \_ прервана** в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="b64db-203">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="b64db-204">Запрос отменяется диспетчером ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="b64db-204">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="b64db-205">Сокет закрыт.</span><span class="sxs-lookup"><span data-stu-id="b64db-205">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="b64db-206">Примеры</span><span class="sxs-lookup"><span data-stu-id="b64db-206">Examples</span></span>

<span data-ttu-id="b64db-207">В следующем примере запрашивается резервирование портов среды выполнения, затем создается сокет и выделяется порт из резервирования порта среды выполнения для сокета, а затем закрывается сокет и освобождается резервирование портов среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="b64db-207">The following example acquires a runtime port reservation, then creates a socket and allocates a port from the runtime port reservation for the socket, and then closes the socket and the releases the runtime port reservation.</span></span>

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

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

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

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
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

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
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

## <a name="see-also"></a><span data-ttu-id="b64db-208">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b64db-208">See also</span></span>

[<span data-ttu-id="b64db-209">**гласит**</span><span class="sxs-lookup"><span data-stu-id="b64db-209">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)

[<span data-ttu-id="b64db-210">**выполняется**</span><span class="sxs-lookup"><span data-stu-id="b64db-210">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="b64db-211">**креатеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="b64db-211">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="b64db-212">**креатеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="b64db-212">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="b64db-213">**делетеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="b64db-213">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="b64db-214">**делетеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="b64db-214">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="b64db-215">**\_диапазон портов \_ inet**</span><span class="sxs-lookup"><span data-stu-id="b64db-215">**INET\_PORT\_RANGE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[<span data-ttu-id="b64db-216">**\_ \_ экземпляр резервирования порта \_ inet**</span><span class="sxs-lookup"><span data-stu-id="b64db-216">**INET\_PORT\_RESERVATION\_INSTANCE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[<span data-ttu-id="b64db-217">**лукупперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="b64db-217">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="b64db-218">**лукупперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="b64db-218">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="b64db-219">**\_ \_ резервирование порта для сопоставления SIO \_**</span><span class="sxs-lookup"><span data-stu-id="b64db-219">**SIO\_ASSOCIATE\_PORT\_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="b64db-220">**\_ \_ резервирование портов освобождения SIO \_**</span><span class="sxs-lookup"><span data-stu-id="b64db-220">**SIO\_RELEASE\_PORT\_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="b64db-221">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="b64db-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="b64db-222">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="b64db-222">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="b64db-223">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="b64db-223">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="b64db-224">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="b64db-224">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="b64db-225">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="b64db-225">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="b64db-226">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="b64db-226">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="b64db-227">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="b64db-227">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
