---
description: Управляющий код настраивает сокет TCP для более низкой задержки и более быстрых операций в интерфейсе замыкания на себя.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: Код элемента управления SIO_LOOPBACK_FAST_PATH
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719625"
---
# <a name="sio_loopback_fast_path-control-code"></a><span data-ttu-id="3ba5f-103">Код элемента управления SIO_LOOPBACK_FAST_PATH</span><span class="sxs-lookup"><span data-stu-id="3ba5f-103">SIO_LOOPBACK_FAST_PATH Control Code</span></span>

## <a name="description"></a><span data-ttu-id="3ba5f-104">Описание</span><span class="sxs-lookup"><span data-stu-id="3ba5f-104">Description</span></span>

<span data-ttu-id="3ba5f-105">Код **управления \_ \_ быстрым \_ путем замыкания на себя SIO** настраивает TCP-сокет для более низкой задержки и более быстрые операции в интерфейсе замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-105">The **SIO\_LOOPBACK\_FAST\_PATH** control code configures a TCP socket for lower latency and faster operations on the loopback interface.</span></span>

<span data-ttu-id="3ba5f-106">**Важно!**  **\_ \_ Быстрый \_ путь обратной связи SIO** является устаревшим и не рекомендуется использовать в коде.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-106">**Important**  The **SIO\_LOOPBACK\_FAST\_PATH** is deprecated and is not recommended to be used in your code.</span></span>

<span data-ttu-id="3ba5f-107">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="3ba5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ba5f-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="3ba5f-109">s</span><span class="sxs-lookup"><span data-stu-id="3ba5f-109">s</span></span>

<span data-ttu-id="3ba5f-110">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="3ba5f-111">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="3ba5f-111">dwIoControlCode</span></span>

<span data-ttu-id="3ba5f-112">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-112">The control code for the operation.</span></span>
<span data-ttu-id="3ba5f-113">Используйте **\_ \_ Быстрый \_ путь замыкания на себя SIO** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-113">Use **SIO\_LOOPBACK\_FAST\_PATH** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="3ba5f-114">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="3ba5f-114">lpvInBuffer</span></span>

<span data-ttu-id="3ba5f-115">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="3ba5f-116">Этот параметр содержит указатель на логическое значение, указывающее, следует ли настроить сокет для выполнения операций быстрого замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-116">This parameter contains a pointer to a Boolean value that indicates if the socket should be configured for fast loopback operations.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="3ba5f-117">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="3ba5f-117">cbInBuffer</span></span>

<span data-ttu-id="3ba5f-118">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-118">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="3ba5f-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="3ba5f-119">lpvOutBuffer</span></span>

<span data-ttu-id="3ba5f-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="3ba5f-121">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="3ba5f-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="3ba5f-122">cbOutBuffer</span></span>

<span data-ttu-id="3ba5f-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="3ba5f-124">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="3ba5f-125">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="3ba5f-125">lpcbBytesReturned</span></span>

<span data-ttu-id="3ba5f-126">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="3ba5f-127">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="3ba5f-128">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="3ba5f-129">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="3ba5f-130">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="3ba5f-131">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="3ba5f-132">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="3ba5f-132">lpvOverlapped</span></span>

<span data-ttu-id="3ba5f-133">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="3ba5f-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="3ba5f-134">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="3ba5f-135">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="3ba5f-136">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="3ba5f-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="3ba5f-137">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="3ba5f-138">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="3ba5f-139">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="3ba5f-139">lpCompletionRoutine</span></span>

<span data-ttu-id="3ba5f-140">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="3ba5f-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="3ba5f-141">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="3ba5f-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="3ba5f-142">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="3ba5f-142">lpThreadId</span></span>

<span data-ttu-id="3ba5f-143">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="3ba5f-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="3ba5f-144">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="3ba5f-145">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="3ba5f-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="3ba5f-146">лперрно</span><span class="sxs-lookup"><span data-stu-id="3ba5f-146">lpErrno</span></span>

<span data-ttu-id="3ba5f-147">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-147">A pointer to the error code.</span></span>

<span data-ttu-id="3ba5f-148">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="3ba5f-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ba5f-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ba5f-149">Return value</span></span>

<span data-ttu-id="3ba5f-150">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="3ba5f-151">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="3ba5f-152">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="3ba5f-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="3ba5f-153">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="3ba5f-153">Error code</span></span> | <span data-ttu-id="3ba5f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3ba5f-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="3ba5f-155">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="3ba5f-156">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="3ba5f-157">Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="3ba5f-158">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="3ba5f-159">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="3ba5f-160">Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды **\_ ioctl Flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="3ba5f-161">**всаеакцес**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-161">**WSAEACCES**</span></span> | <span data-ttu-id="3ba5f-162">Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-162">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="3ba5f-163">Эта ошибка возникает при нескольких условиях для постоянных резервирований портов, которые включают следующее: у пользователя отсутствуют необходимые права администратора на локальном компьютере, или приложение не работает в расширенной оболочке как встроенное администратор ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="3ba5f-163">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="3ba5f-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-164">**WSAEFAULT**</span></span> | <span data-ttu-id="3ba5f-165">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-165">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="3ba5f-166">Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-166">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="3ba5f-167">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-167">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="3ba5f-168">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-168">A blocking operation is currently executing.</span></span> <span data-ttu-id="3ba5f-169">Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-169">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="3ba5f-170">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-170">**WSAEINTR**</span></span> | <span data-ttu-id="3ba5f-171">Операция блокировки была прервана вызовом [**всаканцелблоккингкалл**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="3ba5f-171">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="3ba5f-172">Эта ошибка возвращается в случае прерывания блокирующей операции.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-172">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="3ba5f-173">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-173">**WSAEINVAL**</span></span> | <span data-ttu-id="3ba5f-174">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-174">An invalid argument was supplied.</span></span> <span data-ttu-id="3ba5f-175">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-175">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="3ba5f-176">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-176">**WSAENETDOWN**</span></span> | <span data-ttu-id="3ba5f-177">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-177">A socket operation encountered a dead network.</span></span> <span data-ttu-id="3ba5f-178">Эта ошибка возвращается в случае сбоя сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-178">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="3ba5f-179">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="3ba5f-180">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-180">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="3ba5f-181">Эта ошибка возвращается, если дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-181">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="3ba5f-182">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-182">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="3ba5f-183">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-183">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="3ba5f-184">Эта ошибка возвращается, если указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-184">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="3ba5f-185">Эта ошибка также возвращается, если в поставщике транспорта не поддерживается функция IOCTL с **\_ \_ быстрым \_ путем обратной связи SIO** .</span><span class="sxs-lookup"><span data-stu-id="3ba5f-185">This error is also returned if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="3ba5f-186">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ba5f-186">Remarks</span></span>

<span data-ttu-id="3ba5f-187">Приложение может использовать запрос IOCTL **с \_ \_ быстрым \_ путем замыкания на себя** , чтобы уменьшить задержку и повысить производительность операций замыкания на себя на сокете TCP.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-187">An application can use the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL to reduce the latency and improve the performance of loopback operations on a TCP socket.</span></span>
<span data-ttu-id="3ba5f-188">Этот запрос IOCTL запрашивает использование в стеке TCP/IP специального быстрого пути для операций замыкания на себя на этом сокете.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-188">This IOCTL requests that the TCP/IP stack uses a special fast path for loopback operations on this socket.</span></span>
<span data-ttu-id="3ba5f-189">IOCTL **с \_ \_ быстрым \_ путем замыкания на себя** можно использовать только с сокетами TCP.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-189">The **SIO\_LOOPBACK\_FAST\_PATH** IOCTL can be used only with TCP sockets.</span></span>
<span data-ttu-id="3ba5f-190">Этот запрос IOCTL должен использоваться на обеих сторонах сеанса замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-190">This IOCTL must be used on both sides of the loopback session.</span></span>
<span data-ttu-id="3ba5f-191">Быстрый путь TCP замыкания на себя поддерживается с помощью интерфейса замыкания на себя IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-191">The TCP loopback fast path is supported using either the IPv4 or IPv6 loopback interface.</span></span>

<span data-ttu-id="3ba5f-192">Сокет, который планирует инициировать запрос на соединение, должен применить этот IOCTL перед выполнением запроса на соединение.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-192">The socket that plans to initiate the connection request must apply this IOCTL before making the connection request.</span></span>
<span data-ttu-id="3ba5f-193">Поэтому сокет, используемый функцией [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**коннектекс**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**всаконнект**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**всаконнектбилист**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)или [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) для инициации подключения, должен применить этот запрос IOCTL, чтобы использовать быстрый путь для операций замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-193">So the socket used by the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) function to initiate the connection must apply this IOCTL to use the fast path for loopback operations.</span></span>

<span data-ttu-id="3ba5f-194">Сокет, прослушивающий запрос на соединение, должен применить этот IOCTL перед принятием подключения.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-194">The socket that is listening for the connection request must apply this IOCTL before accepting the connection.</span></span>
<span data-ttu-id="3ba5f-195">Поэтому сокет, используемый функцией Listen, должен применить этот запрос IOCTL, чтобы все принимаемые сокеты использовали быстрый путь для замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-195">So the socket used by the listen function must apply this IOCTL so any sockets that are accepted will use the fast path for loopback.</span></span>
<span data-ttu-id="3ba5f-196">Все сокеты, возвращаемые функцией Listen и передаваемые функции [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**акцептекс**](/windows/desktop/api/winsock/nf-winsock-acceptex)или [**всаакцепт**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) , будут помечены для использования специального быстрого пути для операций замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-196">Any sockets returned by the listen function and passed to the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex), or [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) function will be marked to use the special fast path for loopback operations.</span></span>

<span data-ttu-id="3ba5f-197">Когда приложение устанавливает подключение через интерфейс замыкания на себя, используя быстрый путь, все пакеты во время существования соединения должны использовать быстрый путь.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-197">Once an application establishes the connection on a loopback interface using the fast path, all packets for the lifetime of the connection must use the fast path.</span></span>

<span data-ttu-id="3ba5f-198">Применение **\_ \_ быстрого \_ пути замыкания контроллера SIO** к сокету, который будет подключен к незамыканию, не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-198">Applying **SIO\_LOOPBACK\_FAST\_PATH** to a socket which will be connected to a non-loopback path will have no effect.</span></span>

<span data-ttu-id="3ba5f-199">Эта оптимизация замыкания на себя TCP приводит к передаче пакетов через транспортный уровень (TL) вместо традиционных замыканий на себя через сетевой уровень.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-199">This TCP loopback optimization results in packets that flow through the Transport Layer (TL) instead of the traditional loopback through the Network Layer.</span></span>
<span data-ttu-id="3ba5f-200">Эта оптимизация повышает задержку для пакетов замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-200">This optimization improves the latency for loopback packets.</span></span>
<span data-ttu-id="3ba5f-201">После того как приложение перейдет в режим подключения, чтобы использовать быстрый путь замыкания на себя, все пакеты будут следовать пути замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-201">Once an application opts in for a connection level setting to use the loopback fast path, all packets will follow the loopback path.</span></span>
<span data-ttu-id="3ba5f-202">Для обратной связи, перегрузка и удаление пакетов не ожидаются.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-202">For loopback communications, congestion and packet drop are not expected.</span></span>
<span data-ttu-id="3ba5f-203">Понятие контроля перегрузки и надежной доставки в TCP будет ненужным.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-203">The notion of congestion control and reliable delivery in TCP will be unnecessary.</span></span>
<span data-ttu-id="3ba5f-204">Однако это не верно для управления потоком.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-204">This, however, is not true for flow control.</span></span>
<span data-ttu-id="3ba5f-205">Без управления потоком отправитель может перегрузить буфер приема, что приведет к ошибочному поведению TCP-сигнала.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-205">Without flow control, the sender can overwhelm the receive buffer, leading to erroneous TCP loopback behavior.</span></span>
<span data-ttu-id="3ba5f-206">Управление потоком в пути оптимизации замыкания на себя TCP осуществляется путем размещения запросов send в очереди.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-206">The flow control in the TCP optimized loopback path is maintained by placing send requests in a queue.</span></span>
<span data-ttu-id="3ba5f-207">Когда буфер Receive заполнен, стек TCP/IP гарантирует, что отправка не будет завершена до тех пор, пока очередь не будет обслуживать управление потоком.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-207">When receive buffer is full, the TCP/IP stack guarantees that the sends won't complete until the queue is serviced maintaining flow control.</span></span>

<span data-ttu-id="3ba5f-208">Для соединений с быстрым путем замыкания на себя по протоколу TCP при наличии вызова платформы фильтрации Windows (WFP) для данных подключения необходимо использовать неоптимизированный медленный путь для замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-208">TCP fast path loopback connections in the presence of a Windows Filtering Platform (WFP) callout for connection data must take the un-optimized slow path for loopback.</span></span>
<span data-ttu-id="3ba5f-209">Поэтому фильтры WFP не будут использовать этот новый быстрый путь замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-209">So WFP filters will prevent this new loopback fast path from being used.</span></span>
<span data-ttu-id="3ba5f-210">Если фильтр WFP включен, система будет использовать медленный путь, даже если был установлен быстрый запрос IOCTL на **\_ замыкание \_ \_ SIO** .</span><span class="sxs-lookup"><span data-stu-id="3ba5f-210">When a WFP filter is enabled, the system we will use the slow path even if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL was set.</span></span>
<span data-ttu-id="3ba5f-211">Это гарантирует, что приложения пользовательского режима обладают полными возможностями безопасности WFP.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-211">This ensures that user-mode applications have the full WFP security capability.</span></span>

<span data-ttu-id="3ba5f-212">По умолчанию **\_ Быстрый режим замыкания на себя на петлевой \_ \_ адрес** отключен.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-212">By default, **SIO\_LOOPBACK\_FAST\_PATH** is disabled.</span></span>

<span data-ttu-id="3ba5f-213">Только подмножество параметров сокета TCP/IP поддерживается в том случае, если для быстрого замыкания на сокет используется быстрый замыкание на себя через порт **SIO \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="3ba5f-213">Only a subset of the TCP/IP socket options are supported when the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is used to enable the loopback fast path on a socket.</span></span>
<span data-ttu-id="3ba5f-214">В список поддерживаемых параметров входят следующие.</span><span class="sxs-lookup"><span data-stu-id="3ba5f-214">The list of supported options includes the following:</span></span>

* <span data-ttu-id="3ba5f-215">**\_срок жизни IP**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-215">**IP\_TTL**</span></span>
* <span data-ttu-id="3ba5f-216">**IP- \_ адрес рассылки, \_ Если**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-216">**IP\_UNICAST\_IF**</span></span>
* <span data-ttu-id="3ba5f-217">**\_Одноадресные \_ ПРЫЖКи IPv6**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-217">**IPV6\_UNICAST\_HOPS**</span></span>
* <span data-ttu-id="3ba5f-218">**\_Одноадресная рассылка IPv6, \_ Если**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-218">**IPV6\_UNICAST\_IF**</span></span>
* <span data-ttu-id="3ba5f-219">**\_V6ONLY IPv6**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-219">**IPV6\_V6ONLY**</span></span>
* <span data-ttu-id="3ba5f-220">**Поэтому \_ условное \_ принятие**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-220">**SO\_CONDITIONAL\_ACCEPT**</span></span>
* <span data-ttu-id="3ba5f-221">**Итак, \_ ексклусивеаддрусе**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-221">**SO\_EXCLUSIVEADDRUSE**</span></span>
* <span data-ttu-id="3ba5f-222">**Итак \_ , \_ масштабируемость портов**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-222">**SO\_PORT\_SCALABILITY**</span></span>
* <span data-ttu-id="3ba5f-223">**Итак, \_ рквбуф**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-223">**SO\_RCVBUF**</span></span>
* <span data-ttu-id="3ba5f-224">**Итак, \_ реусеаддр**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-224">**SO\_REUSEADDR**</span></span>
* <span data-ttu-id="3ba5f-225">**\_БСДУРЖЕНТ TCP**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-225">**TCP\_BSDURGENT**</span></span>

## <a name="see-also"></a><span data-ttu-id="3ba5f-226">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ba5f-226">See also</span></span>

[<span data-ttu-id="3ba5f-227">**Параметры сокета IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-227">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="3ba5f-228">**Параметры сокета IPPROTO_IPV6**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-228">**IPPROTO_IPV6 Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[<span data-ttu-id="3ba5f-229">**Параметры сокета IPPROTO_TCP**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-229">**IPPROTO_TCP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-tcp-socket-options)

[<span data-ttu-id="3ba5f-230">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-230">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="3ba5f-231">**Параметры сокета SOL_SOCKET**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-231">**SOL_SOCKET Socket Options**</span></span>](/windows/desktop/winsock/sol-socket-socket-options)

[<span data-ttu-id="3ba5f-232">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-232">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="3ba5f-233">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-233">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="3ba5f-234">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-234">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="3ba5f-235">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-235">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="3ba5f-236">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-236">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="3ba5f-237">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="3ba5f-237">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
