---
description: Управляющий код, который настраивает начальные параметры времени ожидания повторной передачи (RTO) на сокете.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: Код элемента управления SIO_TCP_INITIAL_RTO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "104488472"
---
# <a name="sio_tcp_initial_rto-control-code"></a><span data-ttu-id="7c9a6-103">Код элемента управления SIO_TCP_INITIAL_RTO</span><span class="sxs-lookup"><span data-stu-id="7c9a6-103">SIO_TCP_INITIAL_RTO control code</span></span>

## <a name="description"></a><span data-ttu-id="7c9a6-104">Описание</span><span class="sxs-lookup"><span data-stu-id="7c9a6-104">Description</span></span>

<span data-ttu-id="7c9a6-105">Код элемента управления **SIO_TCP_INITIAL_RTO** настраивает начальные параметры времени ожидания повторной передачи (RTO) на сокете.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-105">The **SIO_TCP_INITIAL_RTO** control code configures initial retransmission timeout (RTO) parameters on a socket.</span></span>

<span data-ttu-id="7c9a6-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
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
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
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

## <a name="parameters"></a><span data-ttu-id="7c9a6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c9a6-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="7c9a6-108">s</span><span class="sxs-lookup"><span data-stu-id="7c9a6-108">s</span></span>

<span data-ttu-id="7c9a6-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="7c9a6-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="7c9a6-110">dwIoControlCode</span></span>

<span data-ttu-id="7c9a6-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-111">The control code for the operation.</span></span>
<span data-ttu-id="7c9a6-112">Для этой операции используйте **SIO_TCP_INITIAL_RTO** .</span><span class="sxs-lookup"><span data-stu-id="7c9a6-112">Use **SIO_TCP_INITIAL_RTO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="7c9a6-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="7c9a6-113">lpvInBuffer</span></span>

<span data-ttu-id="7c9a6-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="7c9a6-115">Этот параметр содержит указатель на [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) , связанный с сокетом.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-115">This parameter contains a pointer to the [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="7c9a6-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="7c9a6-116">cbInBuffer</span></span>

<span data-ttu-id="7c9a6-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="7c9a6-118">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="7c9a6-118">lpvOutBuffer</span></span>

<span data-ttu-id="7c9a6-119">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="7c9a6-120">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="7c9a6-121">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="7c9a6-121">cbOutBuffer</span></span>

<span data-ttu-id="7c9a6-122">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="7c9a6-123">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="7c9a6-124">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="7c9a6-124">lpcbBytesReturned</span></span>

<span data-ttu-id="7c9a6-125">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="7c9a6-126">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="7c9a6-127">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="7c9a6-128">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="7c9a6-129">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="7c9a6-130">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="7c9a6-131">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="7c9a6-131">lpvOverlapped</span></span>

<span data-ttu-id="7c9a6-132">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="7c9a6-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7c9a6-133">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="7c9a6-134">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="7c9a6-135">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="7c9a6-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7c9a6-136">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="7c9a6-137">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="7c9a6-138">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="7c9a6-138">lpCompletionRoutine</span></span>

<span data-ttu-id="7c9a6-139">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="7c9a6-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="7c9a6-140">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="7c9a6-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="7c9a6-141">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="7c9a6-141">lpThreadId</span></span>

<span data-ttu-id="7c9a6-142">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="7c9a6-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="7c9a6-143">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="7c9a6-144">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="7c9a6-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="7c9a6-145">лперрно</span><span class="sxs-lookup"><span data-stu-id="7c9a6-145">lpErrno</span></span>

<span data-ttu-id="7c9a6-146">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-146">A pointer to the error code.</span></span>

<span data-ttu-id="7c9a6-147">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="7c9a6-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c9a6-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c9a6-148">Return value</span></span>

<span data-ttu-id="7c9a6-149">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="7c9a6-150">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="7c9a6-151">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="7c9a6-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="7c9a6-152">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="7c9a6-152">Error code</span></span> | <span data-ttu-id="7c9a6-153">Значение</span><span class="sxs-lookup"><span data-stu-id="7c9a6-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="7c9a6-154">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="7c9a6-155">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="7c9a6-156">Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="7c9a6-157">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="7c9a6-158">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="7c9a6-159">Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="7c9a6-160">**всаеакцес**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-160">**WSAEACCES**</span></span> | <span data-ttu-id="7c9a6-161">Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="7c9a6-162">Эта ошибка возникает при нескольких условиях, которые включают следующее: у пользователя отсутствуют необходимые права администратора на локальном компьютере, или приложение не работает в расширенной оболочке как встроенное администратор ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="7c9a6-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="7c9a6-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-163">**WSAEFAULT**</span></span> | <span data-ttu-id="7c9a6-164">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="7c9a6-165">Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="7c9a6-166">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="7c9a6-167">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="7c9a6-168">Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="7c9a6-169">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-169">**WSAEINTR**</span></span> | <span data-ttu-id="7c9a6-170">Операция блокировки была прервана вызовом *всаканцелблоккингкалл*.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-170">A blocking operation was interrupted by a call to *WSACancelBlockingCall*.</span></span> <span data-ttu-id="7c9a6-171">Эта ошибка возвращается в случае прерывания блокирующей операции.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="7c9a6-172">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-172">**WSAEINVAL**</span></span> | <span data-ttu-id="7c9a6-173">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-173">An invalid argument was supplied.</span></span> <span data-ttu-id="7c9a6-174">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="7c9a6-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="7c9a6-176">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="7c9a6-177">Эта ошибка возвращается в случае сбоя сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="7c9a6-178">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="7c9a6-179">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="7c9a6-180">Эта ошибка возвращается, если дескриптор s не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-180">This error is returned if the descriptor s is not a socket.</span></span> |
| <span data-ttu-id="7c9a6-181">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="7c9a6-182">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="7c9a6-183">Эта ошибка возвращается, если указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="7c9a6-184">Эта ошибка также возвращается, если **SIO_TCP_INITIAL_RTO** ioctl не поддерживается поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-184">This error is also returned if the **SIO_TCP_INITIAL_RTO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="7c9a6-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c9a6-185">Remarks</span></span>

<span data-ttu-id="7c9a6-186">Приложение может использовать **SIO_TCP_INITIAL_RTO** IOCTL для управления начальными характеристиками повторной передачи (SYN/SYN + ACK) СОКЕТа TCP, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-186">An application can use the **SIO_TCP_INITIAL_RTO** IOCTL to control the initial (SYN / SYN+ACK) retransmission characteristics of a TCP socket if required.</span></span>
<span data-ttu-id="7c9a6-187">Приложение при использовании этого параметра должно предоставлять подходящие значения перед началом попытки подключения TCP к сокету.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-187">An application, if using this option, must supply suitable values before starting a TCP connection attempt on the socket.</span></span>

<span data-ttu-id="7c9a6-188">[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) ioctl позволяет приложению настроить начальное время ожидания повторной отправки (SYN), используемое сокетом.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-188">The [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL allows an application to configure the initial (SYN) retransmission timeout (RTO) used by the socket.</span></span>

<span data-ttu-id="7c9a6-189">Указатель на структуру [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) , переданную в параметре *лпвинбуффер* , позволяет приложению настроить начальное время кругового пути (RTT), используемое для расчета времени ожидания повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-189">A pointer to a [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) structure passed in the *lpvInBuffer* parameter allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout.</span></span>
<span data-ttu-id="7c9a6-190">Кроме того, приложение может настроить число повторных передач, которые будут выполняться до сбоя попытки подключения.</span><span class="sxs-lookup"><span data-stu-id="7c9a6-190">The application can also configure the number of retransmissions that will be attempted before the connection attempt fails.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c9a6-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c9a6-191">See also</span></span>

[<span data-ttu-id="7c9a6-192">фиксатор</span><span class="sxs-lookup"><span data-stu-id="7c9a6-192">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="7c9a6-193">**TCP_INITIAL_RTO_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-193">**TCP_INITIAL_RTO_PARAMETERS**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[<span data-ttu-id="7c9a6-194">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="7c9a6-195">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="7c9a6-196">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="7c9a6-197">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="7c9a6-198">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="7c9a6-199">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="7c9a6-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
