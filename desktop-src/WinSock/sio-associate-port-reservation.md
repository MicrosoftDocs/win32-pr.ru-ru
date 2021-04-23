---
description: Управляющий код связывает сокет с постоянным или резервным резервированием для блока TCP или UDP, идентифицируемого маркером резервирования портов.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: Код элемента управления SIO_ASSOCIATE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265766"
---
# <a name="sio_associate_port_reservation-control-code"></a><span data-ttu-id="26843-103">Код элемента управления SIO_ASSOCIATE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="26843-103">SIO_ASSOCIATE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="26843-104">Описание</span><span class="sxs-lookup"><span data-stu-id="26843-104">Description</span></span>

<span data-ttu-id="26843-105">Управляющий код для **\_ \_ \_ резервирования порта SIO** связывает сокет с постоянным или резервным резервированием для блока TCP или UDP, идентифицируемого маркером резервирования портов.</span><span class="sxs-lookup"><span data-stu-id="26843-105">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** control code associates a socket with a persistent or runtime reservation for a block of TCP or UDP identified by the port reservation token.</span></span>
<span data-ttu-id="26843-106">Этот запрос IOCTL должен быть выдан перед привязкой к сокету.</span><span class="sxs-lookup"><span data-stu-id="26843-106">This IOCTL must be issued before the socket is bound.</span></span>
<span data-ttu-id="26843-107">Если и при привязке сокета, назначенный ему порт будет выбран из резервирования портов, определенного данным токеном.</span><span class="sxs-lookup"><span data-stu-id="26843-107">If and when the socket is bound, the port assigned to it will be selected from the port reservation identified by the given token.</span></span>
<span data-ttu-id="26843-108">Если из указанного резервирования нет доступных портов, вызов функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="26843-108">If no ports are available from the specified reservation, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function call will fail.</span></span>

<span data-ttu-id="26843-109">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="26843-109">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
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

## <a name="parameters"></a><span data-ttu-id="26843-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="26843-110">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="26843-111">s</span><span class="sxs-lookup"><span data-stu-id="26843-111">s</span></span>

<span data-ttu-id="26843-112">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="26843-112">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="26843-113">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="26843-113">dwIoControlCode</span></span>

<span data-ttu-id="26843-114">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="26843-114">The control code for the operation.</span></span>
<span data-ttu-id="26843-115">Для этой операции используйте **\_ \_ \_ резервирование порта для сопоставления SIO** .</span><span class="sxs-lookup"><span data-stu-id="26843-115">Use **SIO\_ASSOCIATE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="26843-116">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="26843-116">lpvInBuffer</span></span>

<span data-ttu-id="26843-117">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="26843-117">A pointer to the input buffer.</span></span>
<span data-ttu-id="26843-118">Этот параметр содержит указатель на структуру [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) с маркером резервирования портов TCP или UDP для связи с сокетом.</span><span class="sxs-lookup"><span data-stu-id="26843-118">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to associate with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="26843-119">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="26843-119">cbInBuffer</span></span>

<span data-ttu-id="26843-120">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="26843-120">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="26843-121">Этот параметр должен быть не меньше размера структуры [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="26843-121">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="26843-122">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="26843-122">lpvOutBuffer</span></span>

<span data-ttu-id="26843-123">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="26843-123">A pointer to the output buffer.</span></span>
<span data-ttu-id="26843-124">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="26843-124">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="26843-125">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="26843-125">cbOutBuffer</span></span>

<span data-ttu-id="26843-126">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="26843-126">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="26843-127">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="26843-127">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="26843-128">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="26843-128">lpcbBytesReturned</span></span>

<span data-ttu-id="26843-129">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="26843-129">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="26843-130">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="26843-130">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="26843-131">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="26843-131">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="26843-132">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="26843-132">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="26843-133">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="26843-133">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="26843-134">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="26843-134">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="26843-135">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="26843-135">lpvOverlapped</span></span>

<span data-ttu-id="26843-136">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="26843-136">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="26843-137">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="26843-137">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="26843-138">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="26843-138">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="26843-139">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="26843-139">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="26843-140">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="26843-140">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="26843-141">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="26843-141">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="26843-142">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="26843-142">lpCompletionRoutine</span></span>

<span data-ttu-id="26843-143">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="26843-143">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="26843-144">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="26843-144">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="26843-145">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="26843-145">lpThreadId</span></span>

<span data-ttu-id="26843-146">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="26843-146">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="26843-147">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="26843-147">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="26843-148">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="26843-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="26843-149">лперрно</span><span class="sxs-lookup"><span data-stu-id="26843-149">lpErrno</span></span>

<span data-ttu-id="26843-150">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="26843-150">A pointer to the error code.</span></span>

<span data-ttu-id="26843-151">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="26843-151">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="26843-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26843-152">Return value</span></span>

<span data-ttu-id="26843-153">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="26843-153">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="26843-154">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="26843-154">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="26843-155">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="26843-155">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="26843-156">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="26843-156">Error code</span></span> | <span data-ttu-id="26843-157">Значение</span><span class="sxs-lookup"><span data-stu-id="26843-157">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="26843-158">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="26843-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="26843-159">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="26843-159">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="26843-160">Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="26843-160">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="26843-161">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="26843-161">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="26843-162">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="26843-162">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="26843-163">Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды **\_ ioctl Flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="26843-163">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="26843-164">**всаеакцес**</span><span class="sxs-lookup"><span data-stu-id="26843-164">**WSAEACCES**</span></span> | <span data-ttu-id="26843-165">Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="26843-165">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="26843-166">Эта ошибка возникает при нескольких условиях для постоянных резервирований портов, которые включают следующее: у пользователя отсутствуют необходимые права администратора на локальном компьютере, или приложение не работает в расширенной оболочке как встроенное администратор ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="26843-166">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="26843-167">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="26843-167">**WSAEFAULT**</span></span> | <span data-ttu-id="26843-168">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="26843-168">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="26843-169">Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="26843-169">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="26843-170">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="26843-170">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="26843-171">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="26843-171">A blocking operation is currently executing.</span></span> <span data-ttu-id="26843-172">Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="26843-172">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="26843-173">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="26843-173">**WSAEINTR**</span></span> | <span data-ttu-id="26843-174">Операция блокировки была прервана вызовом [**всаканцелблоккингкалл**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="26843-174">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="26843-175">Эта ошибка возвращается в случае прерывания блокирующей операции.</span><span class="sxs-lookup"><span data-stu-id="26843-175">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="26843-176">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="26843-176">**WSAEINVAL**</span></span> | <span data-ttu-id="26843-177">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="26843-177">An invalid argument was supplied.</span></span> <span data-ttu-id="26843-178">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="26843-178">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="26843-179">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="26843-179">**WSAENETDOWN**</span></span> | <span data-ttu-id="26843-180">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="26843-180">A socket operation encountered a dead network.</span></span> <span data-ttu-id="26843-181">Эта ошибка возвращается в случае сбоя сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="26843-181">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="26843-182">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="26843-182">**WSAENOTSOCK**</span></span> | <span data-ttu-id="26843-183">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="26843-183">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="26843-184">Эта ошибка возвращается, если дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="26843-184">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="26843-185">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="26843-185">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="26843-186">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="26843-186">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="26843-187">Эта ошибка возвращается, если указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26843-187">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="26843-188">Эта ошибка также возвращается, если поставщик транспорта не поддерживает запрос IOCTL для **\_ \_ \_ резервирования порта SIO** .</span><span class="sxs-lookup"><span data-stu-id="26843-188">This error is also returned if the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="26843-189">Эта ошибка также возвращается, если попытка использовать запрос на **\_ \_ \_ зарезервированный номер порта** для подключения SIO выполняется на сокете, отличном от UDP или TCP.</span><span class="sxs-lookup"><span data-stu-id="26843-189">This error is also returned when an attempt to use the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="26843-190">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26843-190">Remarks</span></span>

<span data-ttu-id="26843-191">В Windows Vista и более поздних версиях операционной системы поддерживается запрос IOCTL для **\_ сопоставления \_ порта \_ SIO** .</span><span class="sxs-lookup"><span data-stu-id="26843-191">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="26843-192">Приложения и службы, которым необходимо резервировать порты, делятся на две категории.</span><span class="sxs-lookup"><span data-stu-id="26843-192">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="26843-193">Первая категория включает компоненты, которым требуется определенный порт в рамках своей работы.</span><span class="sxs-lookup"><span data-stu-id="26843-193">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="26843-194">Такие компоненты, как правило, предпочитают указывать требуемый порт во время установки (например, в манифесте приложения).</span><span class="sxs-lookup"><span data-stu-id="26843-194">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="26843-195">Вторая категория включает компоненты, которым требуется любой доступный порт или блок портов во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="26843-195">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="26843-196">Эти две категории соответствуют конкретным и запросам резервирования портов с подстановочными знаками.</span><span class="sxs-lookup"><span data-stu-id="26843-196">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="26843-197">Определенные запросы на резервирование могут быть постоянными или средой выполнения, тогда как запросы резервирования портов с подстановочными знаками поддерживаются только во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="26843-197">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="26843-198">Для сопоставления резервирования портов TCP или UDP с постоянным резервированием или резервированиями времени выполнения используется запрос IOCTL **\_ \_ \_ резервирования порта SIO** .</span><span class="sxs-lookup"><span data-stu-id="26843-198">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used to associate a TCP or UDP port reservation with either a persistent or runtime reservation.</span></span>

<span data-ttu-id="26843-199">Функция [**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) или [**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) предоставляет приложению или службе возможность зарезервировать постоянный блок портов TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="26843-199">The [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function provides the ability for an application or service to reserve a persistent block of TCP or UDP ports.</span></span>
<span data-ttu-id="26843-200">Постоянные резервирования портов записываются в постоянном хранилище для модуля TCP или UDP в Windows.</span><span class="sxs-lookup"><span data-stu-id="26843-200">Persistent port reservations are recorded in a persistent store for the TCP or UDP module in Windows.</span></span>
<span data-ttu-id="26843-201">Обратите внимание, что маркер для заданной постоянного резервирования портов может изменяться при каждом перезапуске системы.</span><span class="sxs-lookup"><span data-stu-id="26843-201">Note that the token for a given persistent port reservation may change each time the system is restarted.</span></span>

<span data-ttu-id="26843-202">После получения постоянного резервирования порта TCP или UDP приложение может запрашивать назначения портов из резервирования портов, открывая сокет TCP или UDP, а затем вызывая функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) , указывающую на подключение суперконтроллера ввода/вывода, и передав маркер резервирования перед вызовом функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) на сокете. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26843-202">Once a persistent TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="26843-203">[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl можно использовать для запроса резервирования времени выполнения для блока портов TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="26843-203">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL can be used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="26843-204">Для резервирования портов во время выполнения пул портов требует, чтобы резервирования использовались в процессе, для которого было предоставлено резервирование.</span><span class="sxs-lookup"><span data-stu-id="26843-204">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="26843-205">Количество резервирований портов среды выполнения последний раз, пока время существования сокета, на котором вызывался [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="26843-205">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="26843-206">Напротив, постоянные резервирования портов, созданные с помощью функции [**креатеперсистентткппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) или [**креатеперсистентудппортресерватион**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) , могут быть использованы любым процессом с возможностью получения постоянных резервирований.</span><span class="sxs-lookup"><span data-stu-id="26843-206">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="26843-207">После получения резервирования порта времени выполнения TCP или UDP приложение может запрашивать назначения портов из резервирования портов, открыв сокет TCP или UDP, а затем вызывая функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) , указывающую на подключение SIO, и передав маркер резервирования перед вызовом функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) на сокете. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26843-207">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL and passing the reservation token before issuing a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function on the socket.</span></span>

<span data-ttu-id="26843-208">Если оба параметра *лповерлаппед* и *лпкомплетионраутине* равны NULL, сокет в этой функции будет рассматриваться как сокет без перекрытия.</span><span class="sxs-lookup"><span data-stu-id="26843-208">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="26843-209">Для не перекрывающихся сокетов параметры *лповерлаппед* и *лпкомплетионраутине* игнорируются, за исключением того, что функция может блокироваться, *Если сокеты* находятся в блокирующем режиме.</span><span class="sxs-lookup"><span data-stu-id="26843-209">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="26843-210">Если *сокеты* находятся в режиме без блокировки, эта функция по-прежнему будет заблокирована, так как этот КОНКРЕТНЫЙ запрос IOCTL не поддерживает режим без блокировки.</span><span class="sxs-lookup"><span data-stu-id="26843-210">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="26843-211">Для перекрывающихся сокетов операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="26843-211">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="26843-212">Любой запрос IOCTL может блокироваться неограниченно в зависимости от реализации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="26843-212">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="26843-213">Если приложение не допускает блокировку в вызове функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** , перекрывающиеся операции ввода-вывода будут рекомендованы для ioctl, которые, скорее всего, блокируются.</span><span class="sxs-lookup"><span data-stu-id="26843-213">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="26843-214">Запрос IOCTL для **\_ \_ \_ резервирования порта SIO** может завершиться ошибкой с **всаеинтр** или **WSA_OPERATION_ABORTED** в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="26843-214">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA_OPERATION_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="26843-215">Запрос отменяется диспетчером ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="26843-215">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="26843-216">Сокет закрыт.</span><span class="sxs-lookup"><span data-stu-id="26843-216">The socket is closed.</span></span>

<span data-ttu-id="26843-217">Запрос IOCTL для **\_ \_ \_ резервирования порта** , переданный функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** для постоянного резервирования портов, может использоваться в приложении только в том случае, если пользователь вошел в систему как член группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="26843-217">The **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function for a persistent port reservation can only be used in an application when the user is logged on as a member of the Administrators group.</span></span>
<span data-ttu-id="26843-218">Если в приложении используется запрос на **\_ \_ \_ зарезервированный номер порта** (IOCTL), если пользователь не является членом группы "Администраторы", вызов функции завершится неудачей и возвращается **всаеакцес** .</span><span class="sxs-lookup"><span data-stu-id="26843-218">If **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL is used in an application when the user is not a member of the Administrators group, the function call will fail and **WSAEACCES** is returned.</span></span>
<span data-ttu-id="26843-219">Использование функции IOCTL для **\_ \_ \_ резервирования порта SIO** также может завершиться сбоем из-за контроля учетных записей (UAC) в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="26843-219">The use of the **SIO\_ASSOCIATE\_PORT\_RESERVATION** IOCTL can also fail because of user account control (UAC) on Windows Vista and later.</span></span>
<span data-ttu-id="26843-220">Если приложение, использующее этот запрос IOCTL с постоянным резервированием портов, выполняется пользователем, который вошел в систему в качестве члена группы администраторов, отличной от встроенного администратора, этот вызов завершится ошибкой, если приложение не будет помечено в файле манифеста с параметром **requestedExecutionLevel** , равным *requireAdministrator*.</span><span class="sxs-lookup"><span data-stu-id="26843-220">If an application that uses this IOCTL with a persistent port reservation is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a **requestedExecutionLevel** set to *requireAdministrator*.</span></span>
<span data-ttu-id="26843-221">Если в приложении отсутствует этот файл манифеста, пользователь, вошедший в систему в качестве члена группы администраторов, кроме встроенного администратора, должен запустить приложение в расширенной оболочке как встроенное администратор ( `RunAs administrator` ) для выполнения этой функции.</span><span class="sxs-lookup"><span data-stu-id="26843-221">If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (`RunAs administrator`) for this function to succeed.</span></span>

## <a name="see-also"></a><span data-ttu-id="26843-222">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26843-222">See also</span></span>

[<span data-ttu-id="26843-223">**выполняется**</span><span class="sxs-lookup"><span data-stu-id="26843-223">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="26843-224">**креатеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="26843-224">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="26843-225">**креатеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="26843-225">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="26843-226">**делетеперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="26843-226">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="26843-227">**делетеперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="26843-227">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="26843-228">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="26843-228">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="26843-229">**лукупперсистентткппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="26843-229">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="26843-230">**лукупперсистентудппортресерватион**</span><span class="sxs-lookup"><span data-stu-id="26843-230">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="26843-231">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="26843-231">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="26843-232">**SIO_RELEASE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="26843-232">**SIO_RELEASE_PORT_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="26843-233">фиксатор</span><span class="sxs-lookup"><span data-stu-id="26843-233">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="26843-234">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="26843-234">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="26843-235">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="26843-235">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="26843-236">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="26843-236">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="26843-237">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="26843-237">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="26843-238">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="26843-238">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="26843-239">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="26843-239">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
