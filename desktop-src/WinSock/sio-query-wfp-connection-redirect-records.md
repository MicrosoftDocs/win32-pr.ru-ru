---
description: Управляющий код получает запись перенаправления для принятого подключения TCP/IP для использования службой перенаправления платформы фильтрации Windows.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: Код элемента управления SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719457"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="b3d0d-103">Код элемента управления SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS</span><span class="sxs-lookup"><span data-stu-id="b3d0d-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="b3d0d-104">Описание</span><span class="sxs-lookup"><span data-stu-id="b3d0d-104">Description</span></span>

<span data-ttu-id="b3d0d-105">Управляющий **запрос SIO для \_ запроса на \_ \_ \_ Перенаправление подключения \_ WFP** получает запись перенаправления для принятого подключения TCP/IP для использования службой перенаправления платформы фильтрации Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="b3d0d-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code retrieves the redirect record for the accepted TCP/IP connection for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="b3d0d-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="b3d0d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3d0d-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="b3d0d-108">s</span><span class="sxs-lookup"><span data-stu-id="b3d0d-108">s</span></span>

<span data-ttu-id="b3d0d-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="b3d0d-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="b3d0d-110">dwIoControlCode</span></span>

<span data-ttu-id="b3d0d-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-111">The control code for the operation.</span></span>
<span data-ttu-id="b3d0d-112">Используйте **SIO \_ для \_ запроса \_ \_ \_ записей перенаправления подключения WFP** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="b3d0d-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="b3d0d-113">lpvInBuffer</span></span>

<span data-ttu-id="b3d0d-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="b3d0d-115">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="b3d0d-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="b3d0d-116">cbInBuffer</span></span>

<span data-ttu-id="b3d0d-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="b3d0d-118">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="b3d0d-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="b3d0d-119">lpvOutBuffer</span></span>

<span data-ttu-id="b3d0d-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="b3d0d-121">Этот параметр должен указывать на тип данных **ulong** , если параметры *лповерлаппед* и *лпкомплетионраутине* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="b3d0d-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="b3d0d-122">cbOutBuffer</span></span>

<span data-ttu-id="b3d0d-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="b3d0d-124">Этот параметр должен быть не меньше размера типа данных **ulong** .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="b3d0d-125">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="b3d0d-125">lpcbBytesReturned</span></span>

<span data-ttu-id="b3d0d-126">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="b3d0d-127">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="b3d0d-128">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="b3d0d-129">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="b3d0d-130">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="b3d0d-131">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="b3d0d-132">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="b3d0d-132">lpvOverlapped</span></span>

<span data-ttu-id="b3d0d-133">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b3d0d-134">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="b3d0d-135">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="b3d0d-136">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b3d0d-137">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="b3d0d-138">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="b3d0d-139">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="b3d0d-139">lpCompletionRoutine</span></span>

<span data-ttu-id="b3d0d-140">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="b3d0d-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="b3d0d-141">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="b3d0d-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="b3d0d-142">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="b3d0d-142">lpThreadId</span></span>

<span data-ttu-id="b3d0d-143">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="b3d0d-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="b3d0d-144">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="b3d0d-145">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="b3d0d-146">лперрно</span><span class="sxs-lookup"><span data-stu-id="b3d0d-146">lpErrno</span></span>

<span data-ttu-id="b3d0d-147">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-147">A pointer to the error code.</span></span>

<span data-ttu-id="b3d0d-148">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3d0d-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3d0d-149">Return value</span></span>

<span data-ttu-id="b3d0d-150">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="b3d0d-151">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="b3d0d-152">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b3d0d-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="b3d0d-153">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="b3d0d-153">Error code</span></span> | <span data-ttu-id="b3d0d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="b3d0d-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="b3d0d-155">**Ошибка \_ недостаточного \_ буфера**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="b3d0d-156">Область данных, переданная в системный вызов, слишком мала.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="b3d0d-157">Эта ошибка возвращается, если буфер, на который указывает параметр *лпваутбуффер* с размером буфера, переданным в параметре *кбаутбуффер* , слишком мал.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="b3d0d-158">Требуемый размер буфера будет возвращен в параметре *лпкббитесретурнед* .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="b3d0d-159">**WSA_IO_PENDING**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-159">**WSA_IO_PENDING**</span></span> | <span data-ttu-id="b3d0d-160">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-160">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="b3d0d-161">**WSA_OPERATION_ABORTED**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-161">**WSA_OPERATION_ABORTED**</span></span> | <span data-ttu-id="b3d0d-162">Операция перекрытия была отменена из-за замыкания сокета или выполнения команды ioctl **SIO_FLUSH** .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-162">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="b3d0d-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-163">**WSAEFAULT**</span></span> | <span data-ttu-id="b3d0d-164">Параметр *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-164">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="b3d0d-165">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="b3d0d-166">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-166">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="b3d0d-167">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-167">**WSAEINTR**</span></span> | <span data-ttu-id="b3d0d-168">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-168">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="b3d0d-169">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-169">**WSAEINVAL**</span></span> | <span data-ttu-id="b3d0d-170">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-170">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="b3d0d-171">Эта ошибка возвращается, если параметр *кбаутбуффер* меньше, чем размер типа данных **ulong** .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-171">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="b3d0d-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="b3d0d-173">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-173">The network subsystem has failed.</span></span> |
| <span data-ttu-id="b3d0d-174">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-174">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="b3d0d-175">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-175">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="b3d0d-176">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-176">**WSAENOTCONN**</span></span> | <span data-ttu-id="b3d0d-177">*Сокеты не* подключены.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-177">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="b3d0d-178">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="b3d0d-179">Дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-179">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="b3d0d-180">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="b3d0d-181">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-181">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="b3d0d-182">Эта ошибка возвращается в том случае, если поставщик транспорта не поддерживает **\_ запросы \_ перенаправления запросов WFP на \_ \_ Перенаправление \_ запроса** в службе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-182">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b3d0d-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3d0d-183">Remarks</span></span>

<span data-ttu-id="b3d0d-184">**Запросы SIO \_ на \_ \_ \_ Перенаправление соединений \_ WFP** поддерживаются в Windows 8, Windows Server 2012 и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-184">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="b3d0d-185">WFP обеспечивает доступ к пути обработки пакетов TCP/IP, где входящие и исходящие пакеты могут быть проверены или изменены перед тем, как разрешить их обработку.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-185">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="b3d0d-186">Коснувшись пути обработки TCP/IP, независимые поставщики программного обеспечения могут более легко создавать брандмауэры, антивирусные программы, программное обеспечение диагностики и другие типы приложений и служб.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-186">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="b3d0d-187">WFP предоставляет компоненты пользовательского режима и режима ядра, позволяющие сторонним поставщикам программного обеспечения участвовать в принятии решений о фильтрации, выполняемых на нескольких уровнях стека протоколов TCP/IP и всей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-187">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="b3d0d-188">Функция перенаправления подключения WFP позволяет драйверу ядра вызова WFP перенаправлять подключение локально в процесс пользовательского режима, выполнять проверку содержимого в пользовательском режиме и пересылать проверенное содержимое с помощью другого подключения к исходному назначению.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-188">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="b3d0d-189">**Запросы SIO \_ на \_ \_ \_ Перенаправление подключений \_ WFP запрашивают записи** , а несколько других связанных запросов ioctl являются компонентами пользовательского режима, которые позволяют нескольким ПРИЛОЖЕНИЯМ-посредникам подключений на основе WFP проверять один и тот же поток трафика в совместном режиме.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="b3d0d-190">Каждый агент проверки может безопасно повторно проверить сетевой трафик, который уже был проверен другим агентом проверки.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="b3d0d-191">При наличии нескольких прокси-серверов (например, разработанных разными поставщиками программного обеспечения) подключение, используемое одним прокси-сервером для обмена данными с конечным местом назначения, может быть перенаправлено вторым прокси-сервером, а новое соединение снова будет перенаправлено исходным прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="b3d0d-192">Без отслеживания подключений исходное соединение может никогда не достичь конечного места назначения, так как оно зависает в бесконечном цикле прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="b3d0d-193">**Записи о перенаправлении подключений в протоколе SIO используют запросы на \_ \_ \_ \_ \_ перенаправление запросов WFP** , чтобы обеспечить отслеживание подключений через посредника при перенаправленных соединениях сокетов.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="b3d0d-194">Эта функция WFP упрощает отслеживание записей перенаправления из первоначального перенаправления соединения к конечному подключению.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="b3d0d-195">Служба перенаправления запросов с помощью **запроса суперконтроллера ввода-вывода по \_ запросу \_ WFP \_ \_ \_** использует протокол IOCTL, чтобы получить запись перенаправления из принятого соединения пакетов TCP/IP (например, подключенный сокет для сокета TCP или UDP-сокета), перенаправленный на него в режиме ядра, зарегистрированном на **ALE_CONNECT_REDIRECT** уровнях в драйвере режима ядра.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE_CONNECT_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="b3d0d-196">**Запрос SIO \_ \_ \_ \_ \_ контекста перенаправления подключения WFP** используется службой перенаправления на основе WFP для получения контекста перенаправления для записи перенаправления из принятого соединения TCP/IP (например, подключенный сокет для сокета TCP или UDP-сокета), перенаправленный в него вспомогательной выноской, зарегистрированной на уровнях **\_ \_ перенаправления подключения ALE** .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE\_CONNECT\_REDIRECT** layers.</span></span>
<span data-ttu-id="b3d0d-197">Контекст перенаправления — это необязательный контекст, выделенный драйвером, который используется, если текущее состояние перенаправления соединения заключается в том, что соединение было перенаправлено вызывающей службой перенаправления или если соединение было ранее перенаправлено вызывающей службой перенаправления, но позднее перенаправлено другой службой перенаправления.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-197">The redirect context is an optional driver-allocated context used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="b3d0d-198">Для соединения с прокси-сервером TCP служба перенаправления передает полученную запись перенаправления в сокет TCP, который используется для прокси-сервера с исходным содержимым, используя **\_ \_ \_ \_ \_ записи перенаправления подключения** с помощью SIO.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-198">For a TCP proxy connection, the redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="b3d0d-199">Когда служба перенаправления перенаправляет сокет, отличный от TCP (например, UDP), записи перенаправления, возвращаемые **\_ \_ \_ \_ \_ записями перенаправления подключения к** службе "SIO", указывают на службу перенаправления, используя структуру [**Всамсг**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) , используемую с функцией [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-199">When the redirect service is redirecting a non-TCP socket (UDP, for example), the redirect records returned by the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL indicate this to the redirect service using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure used with the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>
<span data-ttu-id="b3d0d-200">Элемент управления структуры [**всамсг**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) будет иметь cmsg_type в структуре **всакмсгхдр** , для которой задано значение **\_ \_ перенаправления \_ IP-соединения**.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-200">The Control member of the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure would have a cmsg_type in the **WSACMSGHDR** structure set to **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="b3d0d-201">При принятии перенаправлений, отличных от TCP, параметр [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) должен быть предоставлен службой перенаправления.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-201">The [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) parameter must be supplied by the redirect service when accepting non-TCP redirects.</span></span>

<span data-ttu-id="b3d0d-202">Для трафика, отличного от TCP, запись перенаправления перенаправляется с помощью структуры [**всамсг**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) с функцией [**всасендмсг**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-202">For non-TCP traffic, the redirect record is forwarded using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure with the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) function.</span></span>

<span data-ttu-id="b3d0d-203">Обратите внимание, что для трафика, отличного от TCP, только пакет, создающий поток, будет содержать **\_ \_ \_ запись перенаправления IP-подключения**.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-203">Note that for non-TCP traffic, only the flow-creating packet will carry the **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="b3d0d-204">В результате, только первый пакет с прокси-сервером должен включить эти сведения с помощью функции [**LPFN_WSARECVMSG (всареквмсг)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-204">As a result, only the first proxied packet needs to include this information using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>

<span data-ttu-id="b3d0d-205">Так как запись перенаправления WFP является BLOB-объектом данных переменной длины, вызывающий объект может либо предоставить большой выходной буфер (байтовый буфер 1 024, на который указывает параметр *лпваутбуффер* ), либо передать размер буфера вывода в параметре *кбаутбуффер* , равном 0, чтобы запросить размер буфера, необходимый для хранения возвращенного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-205">Since the WFP redirect record is a variable length data blob, the caller can either supply a large output buffer (a 1,024 byte buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="b3d0d-206">Если размер выходного буфера недостаточно для хранения данных, функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращают **ошибку, \_ недостаточную для \_ буфера** , и требуемый размер буфера будет возвращен в значение, на которое указывает параметр *лпкббитесретурнед* .</span><span class="sxs-lookup"><span data-stu-id="b3d0d-206">If the output buffer size is not sufficient to the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="b3d0d-207">Приложению, вызывающему [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) , не нужно понимать большой двоичный объект, содержащий полученный контекст перенаправления.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-207">The application calling the [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) does not need to understand the blob containing the redirect context retrieved.</span></span>
<span data-ttu-id="b3d0d-208">Это непрозрачный большой двоичный объект данных, которые приложению необходимо извлечь и передать обратно в новый сокет.</span><span class="sxs-lookup"><span data-stu-id="b3d0d-208">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3d0d-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3d0d-209">See also</span></span>

[<span data-ttu-id="b3d0d-210">**Параметры сокета IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-210">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="b3d0d-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="b3d0d-212">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-212">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="b3d0d-213">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-213">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="b3d0d-214">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-214">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="b3d0d-215">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-215">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="b3d0d-216">**всамсг**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-216">**WSAMSG**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[<span data-ttu-id="b3d0d-217">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="b3d0d-218">**LPFN_WSARECVMSG (Всареквмсг)**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[<span data-ttu-id="b3d0d-219">**всасендмсг**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-219">**WSASendMsg**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[<span data-ttu-id="b3d0d-220">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-220">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="b3d0d-221">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="b3d0d-221">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
