---
description: Код элемента управления извлекает оптимальное значение невыполненной работы по отправке для базового соединения.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: Код элемента управления SIO_IDEAL_SEND_BACKLOG_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719626"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a><span data-ttu-id="c3a28-103">Код элемента управления SIO_IDEAL_SEND_BACKLOG_QUERY</span><span class="sxs-lookup"><span data-stu-id="c3a28-103">SIO_IDEAL_SEND_BACKLOG_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="c3a28-104">Описание</span><span class="sxs-lookup"><span data-stu-id="c3a28-104">Description</span></span>

<span data-ttu-id="c3a28-105">Управляющий код для **\_ \_ \_ \_ запроса невыполненной работы SIO** получает оптимальное значение невыполненной отправки (ISB) для базового соединения.</span><span class="sxs-lookup"><span data-stu-id="c3a28-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** control code retrieves the ideal send backlog (ISB) value for the underlying connection.</span></span>

<span data-ttu-id="c3a28-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="c3a28-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="c3a28-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3a28-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="c3a28-108">s</span><span class="sxs-lookup"><span data-stu-id="c3a28-108">s</span></span>

<span data-ttu-id="c3a28-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="c3a28-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="c3a28-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="c3a28-110">dwIoControlCode</span></span>

<span data-ttu-id="c3a28-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="c3a28-111">The control code for the operation.</span></span>
<span data-ttu-id="c3a28-112">Используйте **оптимальный для этой операции \_ \_ \_ \_ запрос на отработку невыполненной работы по SIO** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="c3a28-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="c3a28-113">lpvInBuffer</span></span>

<span data-ttu-id="c3a28-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="c3a28-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="c3a28-115">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="c3a28-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="c3a28-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="c3a28-116">cbInBuffer</span></span>

<span data-ttu-id="c3a28-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="c3a28-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="c3a28-118">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="c3a28-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="c3a28-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="c3a28-119">lpvOutBuffer</span></span>

<span data-ttu-id="c3a28-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="c3a28-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="c3a28-121">Этот параметр должен указывать на тип данных **ulong** , если параметры *лповерлаппед* и *лпкомплетионраутине* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3a28-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="c3a28-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="c3a28-122">cbOutBuffer</span></span>

<span data-ttu-id="c3a28-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="c3a28-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="c3a28-124">Этот параметр должен быть не меньше размера типа данных **ulong** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="c3a28-125">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="c3a28-125">lpcbBytesReturned</span></span>

<span data-ttu-id="c3a28-126">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="c3a28-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="c3a28-127">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="c3a28-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="c3a28-128">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="c3a28-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="c3a28-129">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="c3a28-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="c3a28-130">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="c3a28-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="c3a28-131">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="c3a28-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="c3a28-132">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="c3a28-132">lpvOverlapped</span></span>

<span data-ttu-id="c3a28-133">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="c3a28-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="c3a28-134">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c3a28-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="c3a28-135">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="c3a28-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="c3a28-136">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="c3a28-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="c3a28-137">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="c3a28-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="c3a28-138">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="c3a28-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="c3a28-139">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="c3a28-139">lpCompletionRoutine</span></span>

<span data-ttu-id="c3a28-140">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="c3a28-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="c3a28-141">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="c3a28-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="c3a28-142">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="c3a28-142">lpThreadId</span></span>

<span data-ttu-id="c3a28-143">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="c3a28-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="c3a28-144">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="c3a28-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="c3a28-145">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="c3a28-146">лперрно</span><span class="sxs-lookup"><span data-stu-id="c3a28-146">lpErrno</span></span>

<span data-ttu-id="c3a28-147">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="c3a28-147">A pointer to the error code.</span></span>

<span data-ttu-id="c3a28-148">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3a28-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3a28-149">Return value</span></span>

<span data-ttu-id="c3a28-150">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c3a28-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="c3a28-151">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="c3a28-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="c3a28-152">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="c3a28-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="c3a28-153">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="c3a28-153">Error code</span></span> | <span data-ttu-id="c3a28-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c3a28-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="c3a28-155">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="c3a28-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="c3a28-156">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="c3a28-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="c3a28-157">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="c3a28-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="c3a28-158">Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="c3a28-158">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="c3a28-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c3a28-159">**WSAEFAULT**</span></span> | <span data-ttu-id="c3a28-160">Параметр *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3a28-160">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="c3a28-161">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="c3a28-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="c3a28-162">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="c3a28-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="c3a28-163">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="c3a28-163">**WSAEINTR**</span></span> | <span data-ttu-id="c3a28-164">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="c3a28-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="c3a28-165">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="c3a28-165">**WSAEINVAL**</span></span> | <span data-ttu-id="c3a28-166">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="c3a28-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="c3a28-167">Эта ошибка возвращается, если параметр *кбаутбуффер* меньше, чем размер типа данных **ulong** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span>
| <span data-ttu-id="c3a28-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="c3a28-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="c3a28-169">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="c3a28-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="c3a28-170">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="c3a28-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="c3a28-171">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="c3a28-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="c3a28-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="c3a28-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="c3a28-173">Сокеты не подключены.</span><span class="sxs-lookup"><span data-stu-id="c3a28-173">The socket s is not connected.</span></span> |
| <span data-ttu-id="c3a28-174">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="c3a28-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="c3a28-175">Дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="c3a28-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="c3a28-176">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="c3a28-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="c3a28-177">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c3a28-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="c3a28-178">Эта ошибка возникает, если поставщик транспорта не поддерживает запрос IOCTL для **\_ \_ \_ невыполненной работы \_ SIO** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-178">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="c3a28-179">Эта ошибка также возвращается при попытке использовать запрос IOCTL для **\_ оптимального \_ \_ \_ запроса невыполненной работы по отправке** через сокет датаграмм.</span><span class="sxs-lookup"><span data-stu-id="c3a28-179">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="c3a28-180">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3a28-180">Remarks</span></span>

<span data-ttu-id="c3a28-181">В Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы поддерживается запрос IOCTL для **\_ оптимального использования \_ \_ \_ запросов на отработку SIO** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="c3a28-182">При отправке данных через TCP-соединение с помощью сокетов Windows важно обеспечить достаточное количество необработанных данных (отправленных, но еще не подтвержденных) в TCP для достижения максимальной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="c3a28-182">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="c3a28-183">Оптимальное значение объема данных, необходимых для достижения наилучшей пропускной способности для подключения TCP, называется идеальным размером невыполненной отправки (ISB).</span><span class="sxs-lookup"><span data-stu-id="c3a28-183">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="c3a28-184">Значение ISB является функцией произведения задержки пропускной способности подключения TCP и полученного окна приема получателя (а также частично перегрузки в сети).</span><span class="sxs-lookup"><span data-stu-id="c3a28-184">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="c3a28-185">Значение ISB для каждого подключения доступно в реализации протокола TCP в Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c3a28-185">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="c3a28-186">**\_ Оптимальный \_ \_ \_ запрос на отработку невыполненной работы по отправке SIO** может использоваться приложением для получения уведомления при динамическом изменении значения ISB для соединения.</span><span class="sxs-lookup"><span data-stu-id="c3a28-186">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="c3a28-187">В Windows Server 2008, Windows Vista с пакетом обновления 1 (SP1) и более поздних версиях операционной системы для ориентированных на поток сокетов, находящихся в подключенном состоянии, поддерживается [**\_ \_ \_ \_ изменение невыполненной работы SIO**](sio-ideal-send-backlog-change.md) и **\_ оптимальный \_ \_ \_ запрос на отработку невыполненной** работы.</span><span class="sxs-lookup"><span data-stu-id="c3a28-187">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="c3a28-188">Диапазон значений ISB для TCP-соединения теоретически может иметь размер от 0 до 16 мегабайт.</span><span class="sxs-lookup"><span data-stu-id="c3a28-188">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="c3a28-189">Обычное [**\_ \_ \_ \_ изменение невыполненной работы суперконтроллера**](sio-ideal-send-backlog-change.md) ввода-вывода **и \_ оптимальный \_ \_ запрос на отработку невыполненной работы по \_ запросу** ioctl основаны на методе Send, используемом приложениями.</span><span class="sxs-lookup"><span data-stu-id="c3a28-189">The typical usage of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs is based on the send method used by the applications.</span></span>
<span data-ttu-id="c3a28-190">Обсуждаются два распространенных варианта.</span><span class="sxs-lookup"><span data-stu-id="c3a28-190">Two common cases are discussed.</span></span>

<span data-ttu-id="c3a28-191">Приложения, выполняющие один блокирующий или неблокирующий запрос на отправку, обычно полагаются на внутреннюю буферизацию отправки через Winsock для достижения достаточной пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="c3a28-191">Applications that perform one blocking or non-blocking send request at a time typically rely on internal send buffering by Winsock to achieve decent throughput.</span></span>
<span data-ttu-id="c3a28-192">Ограничение буфера отправки для данного соединения управляется параметром **\_ сндбуф** Socket.</span><span class="sxs-lookup"><span data-stu-id="c3a28-192">The send buffer limit for a given connection is controlled by the **SO\_SNDBUF** socket option.</span></span>
<span data-ttu-id="c3a28-193">Для блокирующего и неблокирующего метода Send ограничение буфера отправки определяет, сколько данных остается в TCP.</span><span class="sxs-lookup"><span data-stu-id="c3a28-193">For the blocking and non-blocking send method, the send buffer limit determines how much data is kept outstanding in TCP.</span></span>
<span data-ttu-id="c3a28-194">Если значение ISB для соединения превышает предел буфера отправки, то пропускная способность соединения не будет оптимальной.</span><span class="sxs-lookup"><span data-stu-id="c3a28-194">If the ISB value for the connection is larger than the send buffer limit, then the throughput achieved on the connection will not be optimal.</span></span>
<span data-ttu-id="c3a28-195">Чтобы повысить пропускную способность, приложения могут установить ограничение буфера отправки на основе результата запроса ISB, так как в соединении происходят уведомления об изменениях ISB.</span><span class="sxs-lookup"><span data-stu-id="c3a28-195">In order to achieve better throughput, the applications can set the send buffer limit based on the result of the ISB query as ISB change notifications occur on the connection.</span></span>

<span data-ttu-id="c3a28-196">Для приложений, использующих перекрывающиеся методы отправки с несколькими ожидающими запросами на отправку, объем данных, оставшихся в TCP, определяется ограничением буфера отправки в Winsock и общим объемом данных, содержащихся в необработанных перекрывающихся запросах Send.</span><span class="sxs-lookup"><span data-stu-id="c3a28-196">For applications that use the overlapped send method with multiple send requests outstanding, the amount of data kept outstanding in TCP is determined by the send buffer limit in Winsock and the total amount of data contained in the outstanding overlapped send requests.</span></span>
<span data-ttu-id="c3a28-197">В этом случае приложения должны использовать значение ISB, чтобы определить, сколько необработанных запросов на отправку следует хранить, и каков размер данных для каждого запроса на отправку.</span><span class="sxs-lookup"><span data-stu-id="c3a28-197">In this case, applications should use the ISB value to determine how many outstanding send requests they should keep and what the data size for each send request should be.</span></span>
<span data-ttu-id="c3a28-198">В идеале приложение должно попытаться удовлетворить следующее уравнение:</span><span class="sxs-lookup"><span data-stu-id="c3a28-198">Ideally, the application should try to keep the following equation satisfied:</span></span>

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

<span data-ttu-id="c3a28-199">Обратите внимание на то, что использование функции ISB IOCTL через TCP-сокеты в приведенном выше случае может привести к увеличению использования памяти в Exchange для повышения пропускной способности при подключении с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="c3a28-199">Note that using the ISB IOCTLs over TCP sockets in the above fashion can lead to increased memory usage in exchange for increased throughput on connections with a high bandwidth-delay product.</span></span>
<span data-ttu-id="c3a28-200">Реализация TCP в Windows будет регулировать значения ISB по мере необходимости на основе общего использования системной памяти.</span><span class="sxs-lookup"><span data-stu-id="c3a28-200">The TCP implementation in Windows will throttle ISB values as necessary based on overall system memory usage.</span></span>

<span data-ttu-id="c3a28-201">**\_ Оптимальный \_ \_ \_ запрос на отработку невыполненной работы по отправке суперконтроллера** ввода-вывода разрешен только для сокета потока, который находится в подключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c3a28-201">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="c3a28-202">В противном случае функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** завершится с ошибкой **всаенотконн**.</span><span class="sxs-lookup"><span data-stu-id="c3a28-202">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="c3a28-203">Любой запрос IOCTL может блокироваться неограниченно в зависимости от реализации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="c3a28-203">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="c3a28-204">Если приложение не допускает блокировку в вызове функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** , перекрывающиеся операции ввода-вывода будут рекомендованы для ioctl, которые, скорее всего, блокируются.</span><span class="sxs-lookup"><span data-stu-id="c3a28-204">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="c3a28-205">**\_ Наилучший \_ \_ \_ запрос на отработку невыполненной работы по отправке SIO** , скорее всего, не блокируется, поэтому он обычно вызывается синхронно с параметрами *Лповерлаппед* и *лпкомплетионраутине* , установленными в **null**.</span><span class="sxs-lookup"><span data-stu-id="c3a28-205">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not likely to block so it is normally called synchronously with the *lpOverlapped* and *lpCompletionRoutine* parameters set to **NULL**.</span></span>

<span data-ttu-id="c3a28-206">**\_ Наилучший \_ запрос на \_ \_ отработку отказа при отправке запросов** ioctl может завершиться сбоем, если операция **всаеинтр** или **WSA \_ \_ прервана** в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c3a28-206">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

<span data-ttu-id="c3a28-207">Подключение TCP корректно отключается в направлении отправки.</span><span class="sxs-lookup"><span data-stu-id="c3a28-207">The TCP connection is gracefully disconnected in the send direction.</span></span>
<span data-ttu-id="c3a28-208">Это может произойти в результате вызова функции Shutdown с тем, как для параметра установлено значение **SD \_ Send**, вызов функции **Дисконнектекс** или вызов функции **TransmitFile** или **трансмитпаккетс** с параметром *DwFlags* , для которого задано значение **tf \_ Disconnect** или **tf \_ reмногократного использования**.</span><span class="sxs-lookup"><span data-stu-id="c3a28-208">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
<span data-ttu-id="c3a28-209">Подключение TCP сброшено или прервано.</span><span class="sxs-lookup"><span data-stu-id="c3a28-209">The TCP connection has been reset or aborted.</span></span>
<span data-ttu-id="c3a28-210">Запрос отменяется диспетчером ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="c3a28-210">The request is canceled by the I/O Manager.</span></span>

<span data-ttu-id="c3a28-211">Две встроенные функции-оболочки для этих IOCTL определены в файле заголовка *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="c3a28-211">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="c3a28-212">Рекомендуется использовать эти встроенные функции вместо того, чтобы использовать [**\_ оптимальное \_ \_ \_ изменение невыполненной работы SIO**](sio-ideal-send-backlog-change.md) и **\_ \_ \_ невыполненную \_** работу по запросу IOCTL.</span><span class="sxs-lookup"><span data-stu-id="c3a28-212">It is recommended that these inline functions be used instead of using the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs directly.</span></span>

<span data-ttu-id="c3a28-213">Встроенная функция-оболочка для [**\_ идеального \_ \_ \_ изменения невыполненной работы по отправке SIO**](sio-ideal-send-backlog-change.md) — функция **идеалсендбакклогнотифи** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-213">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="c3a28-214">Встроенная функция-оболочка для **\_ \_ \_ \_ запроса на отработку невыполненной работы суперконтроллера** ввода-вывода с помощью ioctl — это функция **идеалсендбакклогкуери** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-214">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is the **idealsendbacklogquery** function.</span></span>

<span data-ttu-id="c3a28-215">Динамическая отправка буфера для протокола TCP была добавлена в Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c3a28-215">Dynamic send buffering for TCP was added on Windows 7 and Windows Server 2008 R2.</span></span>
<span data-ttu-id="c3a28-216">По умолчанию динамическая буферизация отправки для TCP включена, если только приложение не задает для сокета потока параметр **so \_ сндбуф** .</span><span class="sxs-lookup"><span data-stu-id="c3a28-216">By default, dynamic send buffering for TCP is enabled unless an application sets the **SO\_SNDBUF** socket option on the stream socket.</span></span>

<span data-ttu-id="c3a28-217">Использование Netsh — это рекомендуемый метод для запроса или настройки динамической буферизации отправки для TCP.</span><span class="sxs-lookup"><span data-stu-id="c3a28-217">Using netsh is the recommended method to query or set dynamic send buffering for TCP.</span></span>

<span data-ttu-id="c3a28-218">Текущее значение для динамической буферизации отправки для TCP можно получить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="c3a28-218">The current value for dynamic send buffering for TCP can be retrieved using the following command:</span></span>

`netsh winsock show autotuning`

<span data-ttu-id="c3a28-219">Динамическую буферизацию отправки для TCP можно отключить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="c3a28-219">Dynamic send buffering for TCP can be disabled using the following command:</span></span>

`netsh winsock set autotuning off`

<span data-ttu-id="c3a28-220">Динамическую буферизацию отправки для TCP можно включить с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="c3a28-220">Dynamic send buffering for TCP can be enabled using the following command:</span></span>

`netsh winsock set autotuning on`

<span data-ttu-id="c3a28-221">Хотя это не рекомендуется, можно отключить буферизацию динамической отправки из приложения, задав для следующего параметра реестра значение 0:</span><span class="sxs-lookup"><span data-stu-id="c3a28-221">While it is discouraged, dynamic send buffering can be disabled from an application by setting the following registry value to zero:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

<span data-ttu-id="c3a28-222">При изменении значения для динамической буферизации отправки с помощью NetSh.exe или изменения значения реестра компьютер должен быть перезагружен, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="c3a28-222">When changing the value for dynamic send buffering using NetSh.exe or changing the registry value, the computer must be restarted for the change to take effect.</span></span>

<span data-ttu-id="c3a28-223">Благодаря динамической буферизации отправки в Windows 7 и Windows Server 2008 R2 использование оптимальных запросов на [**\_ \_ \_ отработку невыполненной работы \_**](sio-ideal-send-backlog-change.md) и **\_ \_ \_ \_ запроса на отработку невыполненной работы** SIO требуется только в особых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="c3a28-223">With dynamic send buffering on Windows 7 and Windows Server 2008 R2, the use of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are needed only in special circumstances.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3a28-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3a28-224">See also</span></span>

[<span data-ttu-id="c3a28-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="c3a28-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span></span>](sio-ideal-send-backlog-change.md)

[<span data-ttu-id="c3a28-226">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="c3a28-226">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="c3a28-227">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="c3a28-227">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="c3a28-228">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="c3a28-228">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="c3a28-229">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="c3a28-229">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="c3a28-230">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="c3a28-230">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="c3a28-231">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="c3a28-231">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="c3a28-232">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="c3a28-232">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
