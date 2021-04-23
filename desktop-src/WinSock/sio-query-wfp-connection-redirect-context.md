---
description: Управляющий код получает контекст перенаправления для записи перенаправления, используемой службой перенаправления платформы фильтрации Windows.
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: Код элемента управления SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 1e5e5f6c56411ada1e87e8cdf240a89f9c293e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144968"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a><span data-ttu-id="1c64a-103">Код элемента управления SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="1c64a-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Control Code</span></span>

## <a name="description"></a><span data-ttu-id="1c64a-104">Описание</span><span class="sxs-lookup"><span data-stu-id="1c64a-104">Description</span></span>

<span data-ttu-id="1c64a-105">Код **управления \_ \_ \_ \_ \_ контекстом перенаправления подключения к службе SIO** получает контекст перенаправления для записи перенаправления, используемой службой перенаправления платформы фильтрации Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="1c64a-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** control code retrieves the redirect context for a redirect record used by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="1c64a-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="1c64a-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="1c64a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c64a-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="1c64a-108">s</span><span class="sxs-lookup"><span data-stu-id="1c64a-108">s</span></span>

<span data-ttu-id="1c64a-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="1c64a-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="1c64a-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="1c64a-110">dwIoControlCode</span></span>

<span data-ttu-id="1c64a-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="1c64a-111">The control code for the operation.</span></span>
<span data-ttu-id="1c64a-112">Для этой операции используйте для **\_ запроса SIO \_ \_ \_ \_ контекст перенаправления подключения WFP** .</span><span class="sxs-lookup"><span data-stu-id="1c64a-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="1c64a-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="1c64a-113">lpvInBuffer</span></span>

<span data-ttu-id="1c64a-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="1c64a-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="1c64a-115">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="1c64a-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="1c64a-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="1c64a-116">cbInBuffer</span></span>

<span data-ttu-id="1c64a-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="1c64a-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="1c64a-118">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="1c64a-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="1c64a-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="1c64a-119">lpvOutBuffer</span></span>

<span data-ttu-id="1c64a-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="1c64a-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="1c64a-121">Этот параметр должен указывать на тип данных **ulong** , если параметры *лповерлаппед* и *лпкомплетионраутине* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c64a-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="1c64a-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="1c64a-122">cbOutBuffer</span></span>

<span data-ttu-id="1c64a-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="1c64a-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="1c64a-124">Этот параметр должен быть не меньше размера типа данных **ulong** .</span><span class="sxs-lookup"><span data-stu-id="1c64a-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="1c64a-125">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="1c64a-125">lpcbBytesReturned</span></span>

<span data-ttu-id="1c64a-126">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="1c64a-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="1c64a-127">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="1c64a-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="1c64a-128">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="1c64a-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="1c64a-129">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="1c64a-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="1c64a-130">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="1c64a-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="1c64a-131">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="1c64a-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="1c64a-132">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="1c64a-132">lpvOverlapped</span></span>

<span data-ttu-id="1c64a-133">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="1c64a-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1c64a-134">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1c64a-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="1c64a-135">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="1c64a-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="1c64a-136">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="1c64a-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1c64a-137">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="1c64a-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="1c64a-138">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="1c64a-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="1c64a-139">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="1c64a-139">lpCompletionRoutine</span></span>

<span data-ttu-id="1c64a-140">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="1c64a-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="1c64a-141">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="1c64a-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="1c64a-142">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="1c64a-142">lpThreadId</span></span>

<span data-ttu-id="1c64a-143">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="1c64a-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="1c64a-144">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="1c64a-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="1c64a-145">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="1c64a-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="1c64a-146">лперрно</span><span class="sxs-lookup"><span data-stu-id="1c64a-146">lpErrno</span></span>

<span data-ttu-id="1c64a-147">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="1c64a-147">A pointer to the error code.</span></span>

<span data-ttu-id="1c64a-148">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="1c64a-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c64a-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c64a-149">Return value</span></span>

<span data-ttu-id="1c64a-150">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="1c64a-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="1c64a-151">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="1c64a-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="1c64a-152">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="1c64a-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="1c64a-153">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="1c64a-153">Error code</span></span> | <span data-ttu-id="1c64a-154">Значение</span><span class="sxs-lookup"><span data-stu-id="1c64a-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="1c64a-155">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="1c64a-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="1c64a-156">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="1c64a-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="1c64a-157">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="1c64a-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="1c64a-158">Операция перекрытия была отменена из-за замыкания сокета или выполнения команды IOCTL SIO_FLUSH.</span><span class="sxs-lookup"><span data-stu-id="1c64a-158">An overlapped operation was canceled due to the closure of the socket or the execution of the SIO_FLUSH IOCTL command.</span></span> |
| <span data-ttu-id="1c64a-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1c64a-159">**WSAEFAULT**</span></span> | <span data-ttu-id="1c64a-160">Параметр *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c64a-160">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="1c64a-161">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="1c64a-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="1c64a-162">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="1c64a-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="1c64a-163">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="1c64a-163">**WSAEINTR**</span></span> | <span data-ttu-id="1c64a-164">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="1c64a-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="1c64a-165">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="1c64a-165">**WSAEINVAL**</span></span> | <span data-ttu-id="1c64a-166">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="1c64a-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="1c64a-167">Эта ошибка возвращается, если параметр *кбаутбуффер* меньше, чем размер типа данных **ulong** .</span><span class="sxs-lookup"><span data-stu-id="1c64a-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="1c64a-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="1c64a-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="1c64a-169">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="1c64a-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="1c64a-170">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="1c64a-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="1c64a-171">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="1c64a-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="1c64a-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="1c64a-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="1c64a-173">*Сокеты не* подключены.</span><span class="sxs-lookup"><span data-stu-id="1c64a-173">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="1c64a-174">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="1c64a-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="1c64a-175">Дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="1c64a-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="1c64a-176">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="1c64a-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="1c64a-177">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1c64a-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="1c64a-178">Эта ошибка возвращается в том случае, если поставщик транспорта не поддерживает **\_ запрос на \_ \_ \_ \_ Перенаправление подключения для запроса SIO** .</span><span class="sxs-lookup"><span data-stu-id="1c64a-178">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="1c64a-179">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c64a-179">Remarks</span></span>

<span data-ttu-id="1c64a-180">В Windows 8, Windows Server 2012 и более поздних версиях операционной системы поддерживается **\_ запрос на \_ \_ \_ Перенаправление \_ подключения SIO** .</span><span class="sxs-lookup"><span data-stu-id="1c64a-180">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="1c64a-181">WFP обеспечивает доступ к пути обработки пакетов TCP/IP, где входящие и исходящие пакеты могут быть проверены или изменены перед тем, как разрешить их обработку.</span><span class="sxs-lookup"><span data-stu-id="1c64a-181">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="1c64a-182">Коснувшись пути обработки TCP/IP, независимые поставщики программного обеспечения могут более легко создавать брандмауэры, антивирусные программы, программное обеспечение диагностики и другие типы приложений и служб.</span><span class="sxs-lookup"><span data-stu-id="1c64a-182">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="1c64a-183">WFP предоставляет компоненты пользовательского режима и режима ядра, позволяющие сторонним поставщикам программного обеспечения участвовать в принятии решений о фильтрации, выполняемых на нескольких уровнях стека протоколов TCP/IP и всей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1c64a-183">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="1c64a-184">Функция перенаправления подключения WFP позволяет драйверу ядра вызова WFP перенаправлять подключение локально в процесс пользовательского режима, выполнять проверку содержимого в пользовательском режиме и пересылать проверенное содержимое с помощью другого подключения к исходному назначению.</span><span class="sxs-lookup"><span data-stu-id="1c64a-184">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="1c64a-185">**Запрос SIO \_ \_ \_ \_ \_ контекста перенаправления подключения WFP** и несколько других связанных запросов ioctl являются компонентами пользовательского режима, которые позволяют нескольким ПРИЛОЖЕНИЯМ-посредникам подключений на основе WFP проверять один и тот же поток трафика в совместном режиме.</span><span class="sxs-lookup"><span data-stu-id="1c64a-185">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="1c64a-186">Каждый агент проверки может безопасно повторно проверить сетевой трафик, который уже был проверен другим агентом проверки.</span><span class="sxs-lookup"><span data-stu-id="1c64a-186">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="1c64a-187">При наличии нескольких прокси-серверов (например, разработанных разными поставщиками программного обеспечения) подключение, используемое одним прокси-сервером для обмена данными с конечным местом назначения, может быть перенаправлено вторым прокси-сервером, а новое соединение снова будет перенаправлено исходным прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="1c64a-187">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="1c64a-188">Без отслеживания подключений исходное соединение может никогда не достичь конечного места назначения, так как оно зависает в бесконечном цикле прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="1c64a-188">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="1c64a-189">В **\_ запросе SIO \_ \_ \_ \_ контекста перенаправления подключения WFP** используется несколько приложений прокси-сервера подключений на основе WFP для совместной проверки того же потока трафика.</span><span class="sxs-lookup"><span data-stu-id="1c64a-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="1c64a-190">Каждый агент проверки может безопасно повторно проверить сетевой трафик, который уже был проверен другим агентом проверки.</span><span class="sxs-lookup"><span data-stu-id="1c64a-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="1c64a-191">При наличии нескольких прокси-серверов (например, разработанных разными поставщиками программного обеспечения) подключение, используемое одним прокси-сервером для обмена данными с конечным местом назначения, может быть перенаправлено вторым прокси-сервером, а новое соединение снова будет перенаправлено исходным прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="1c64a-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="1c64a-192">Без отслеживания подключений исходное соединение может никогда не достичь конечного места назначения, так как оно зависает в бесконечном цикле прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="1c64a-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>
<span data-ttu-id="1c64a-193">В **\_ запросе SIO \_ \_ \_ \_ контекст перенаправления подключения WFP** используется для обеспечения отслеживания подключений через посредника при перенаправленных соединениях сокетов.</span><span class="sxs-lookup"><span data-stu-id="1c64a-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="1c64a-194">Эта функция WFP упрощает отслеживание записей перенаправления из первоначального перенаправления соединения к конечному подключению.</span><span class="sxs-lookup"><span data-stu-id="1c64a-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="1c64a-195">Служба перенаправления **\_ запросов WFP запрашивает незащищенное \_ \_ подключение \_ \_** с помощью WFP. она используется для получения записи перенаправления из принятого соединения пакетов TCP/IP (например, подключенного сокета для TCP-сокета или UDP-сокета), перенаправления на него по сопутствующей вызываемому режиму ядра, зарегистрированному на уровнях **ALE \_ Connect \_ redirect** в драйвере режима ядра.</span><span class="sxs-lookup"><span data-stu-id="1c64a-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="1c64a-196">**Запрос SIO \_ \_ \_ \_ \_ контекста перенаправления подключения WFP** используется службой перенаправления на основе WFP для получения контекста перенаправления для записи перенаправления из принятого соединения TCP/IP (например, подключенный сокет для сокета TCP или UDP-сокета), перенаправленный на него вспомогательная выноска, зарегистрированная на **ALE_CONNECT_REDIRECT** уровнях.</span><span class="sxs-lookup"><span data-stu-id="1c64a-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE_CONNECT_REDIRECT** layers.</span></span>
<span data-ttu-id="1c64a-197">Контекст перенаправления является необязательным и используется, если текущее состояние перенаправления соединения заключается в том, что подключение было перенаправлено вызывающей службой перенаправления или если соединение было ранее перенаправлено вызывающей службой перенаправления, но позднее перенаправлено другой службой перенаправления.</span><span class="sxs-lookup"><span data-stu-id="1c64a-197">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="1c64a-198">Служба перенаправления передает полученную запись перенаправления в сокет TCP, который используется для прокси-сервера с исходным содержимым, используя **\_ \_ \_ \_ \_ записи перенаправления подключения** с помощью SIO.</span><span class="sxs-lookup"><span data-stu-id="1c64a-198">The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="1c64a-199">Так как контекст перенаправления WFP является BLOB-объектом данных переменной длины, заданным службой перенаправления, вызывающий объект может предоставить большой выходной буфер (например, буфер 1000, на который указывает параметр *лпваутбуффер* ) или передать его в качестве размера выходного буфера в параметре *кбаутбуффер* , равном 0, чтобы запросить размер буфера, необходимый для хранения возвращенного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="1c64a-199">Since the WFP redirect context is a variable length data blob set by the redirect service, the caller can either supply a large output buffer (a 1K buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass as an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="1c64a-200">Если размер выходного буфера недостаточно для хранения данных, функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращают **ошибку, \_ недостаточную для \_ буфера** , и требуемый размер буфера будет возвращен в значение, на которое указывает параметр *лпкббитесретурнед* .</span><span class="sxs-lookup"><span data-stu-id="1c64a-200">If the output buffer size is not sufficient the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="1c64a-201">Приложение, вызывающее **запрос SIO, \_ \_ WF \ P_CONNECTION \_ перенаправления \_ записей** ioctl не нуждается в понимании большого двоичного объекта, содержащего извлеченные записи перенаправления.</span><span class="sxs-lookup"><span data-stu-id="1c64a-201">The application calling the **SIO\_QUERY\_WF\P_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect records retrieved.</span></span>
<span data-ttu-id="1c64a-202">Это непрозрачный большой двоичный объект данных, которые приложению необходимо извлечь и передать обратно в новый сокет.</span><span class="sxs-lookup"><span data-stu-id="1c64a-202">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c64a-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c64a-203">See also</span></span>

[<span data-ttu-id="1c64a-204">**Параметры сокета IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="1c64a-204">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="1c64a-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="1c64a-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="1c64a-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="1c64a-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-set-wfp-connection-redirect-records.md)

[<span data-ttu-id="1c64a-207">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="1c64a-207">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="1c64a-208">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="1c64a-208">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="1c64a-209">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="1c64a-209">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="1c64a-210">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="1c64a-210">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="1c64a-211">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="1c64a-211">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="1c64a-212">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="1c64a-212">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="1c64a-213">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="1c64a-213">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
