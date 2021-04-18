---
description: Управляющий код задает запись перенаправления для нового TCP-сокета, используемого для подключения службы перенаправления.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: Код управления SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719624"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="12e07-103">Код управления SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS</span><span class="sxs-lookup"><span data-stu-id="12e07-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="12e07-104">Описание</span><span class="sxs-lookup"><span data-stu-id="12e07-104">Description</span></span>

<span data-ttu-id="12e07-105">Код управления для **\_ \_ \_ \_ \_ записи перенаправления подключения суперконтроллера** ввода-вывода устанавливает запись перенаправления на новый сокет TCP, используемый для подключения к конечному месту назначения для использования службой перенаправления платформы фильтрации Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="12e07-105">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code sets the redirect record to the new TCP socket used for connecting to the final destination for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="12e07-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="12e07-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="12e07-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="12e07-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="12e07-108">s</span><span class="sxs-lookup"><span data-stu-id="12e07-108">s</span></span>

<span data-ttu-id="12e07-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="12e07-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="12e07-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="12e07-110">dwIoControlCode</span></span>

<span data-ttu-id="12e07-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="12e07-111">The control code for the operation.</span></span>
<span data-ttu-id="12e07-112">Используйте **SIO \_ для \_ установки \_ \_ \_ записей перенаправления соединений WFP** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="12e07-112">Use **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="12e07-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="12e07-113">lpvInBuffer</span></span>

<span data-ttu-id="12e07-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="12e07-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="12e07-115">Этот параметр содержит указатель на запись перенаправления WFP, связанную с сокетом.</span><span class="sxs-lookup"><span data-stu-id="12e07-115">This parameter contains a pointer to the WFP redirect record associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="12e07-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="12e07-116">cbInBuffer</span></span>

<span data-ttu-id="12e07-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="12e07-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="12e07-118">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="12e07-118">lpvOutBuffer</span></span>

<span data-ttu-id="12e07-119">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="12e07-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="12e07-120">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="12e07-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="12e07-121">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="12e07-121">cbOutBuffer</span></span>

<span data-ttu-id="12e07-122">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="12e07-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="12e07-123">Этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="12e07-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="12e07-124">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="12e07-124">lpcbBytesReturned</span></span>

<span data-ttu-id="12e07-125">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="12e07-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="12e07-126">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="12e07-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="12e07-127">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="12e07-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="12e07-128">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="12e07-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="12e07-129">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="12e07-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="12e07-130">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="12e07-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="12e07-131">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="12e07-131">lpvOverlapped</span></span>

<span data-ttu-id="12e07-132">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="12e07-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="12e07-133">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="12e07-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="12e07-134">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="12e07-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="12e07-135">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="12e07-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="12e07-136">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="12e07-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="12e07-137">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="12e07-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="12e07-138">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="12e07-138">lpCompletionRoutine</span></span>

<span data-ttu-id="12e07-139">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="12e07-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="12e07-140">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="12e07-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="12e07-141">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="12e07-141">lpThreadId</span></span>

<span data-ttu-id="12e07-142">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="12e07-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="12e07-143">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="12e07-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="12e07-144">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="12e07-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="12e07-145">лперрно</span><span class="sxs-lookup"><span data-stu-id="12e07-145">lpErrno</span></span>

<span data-ttu-id="12e07-146">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="12e07-146">A pointer to the error code.</span></span>

<span data-ttu-id="12e07-147">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="12e07-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="12e07-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12e07-148">Return value</span></span>

<span data-ttu-id="12e07-149">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="12e07-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="12e07-150">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="12e07-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="12e07-151">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="12e07-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="12e07-152">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="12e07-152">Error code</span></span> | <span data-ttu-id="12e07-153">Значение</span><span class="sxs-lookup"><span data-stu-id="12e07-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="12e07-154">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="12e07-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="12e07-155">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="12e07-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="12e07-156">Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="12e07-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="12e07-157">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="12e07-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="12e07-158">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="12e07-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="12e07-159">Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды **SIO_FLUSH** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="12e07-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="12e07-160">**всаеакцес**</span><span class="sxs-lookup"><span data-stu-id="12e07-160">**WSAEACCES**</span></span> | <span data-ttu-id="12e07-161">Предпринята попытка доступа к сокету методом, запрещенным его разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="12e07-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="12e07-162">Эта ошибка возникает при нескольких условиях, которые включают следующее: у пользователя отсутствуют необходимые права администратора на локальном компьютере, или приложение не работает в расширенной оболочке как встроенное администратор ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="12e07-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="12e07-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="12e07-163">**WSAEFAULT**</span></span> | <span data-ttu-id="12e07-164">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="12e07-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="12e07-165">Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="12e07-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="12e07-166">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="12e07-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="12e07-167">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="12e07-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="12e07-168">Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="12e07-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="12e07-169">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="12e07-169">**WSAEINTR**</span></span> | <span data-ttu-id="12e07-170">Операция блокировки была прервана вызовом **всаканцелблоккингкалл**.</span><span class="sxs-lookup"><span data-stu-id="12e07-170">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="12e07-171">Эта ошибка возвращается в случае прерывания блокирующей операции.</span><span class="sxs-lookup"><span data-stu-id="12e07-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="12e07-172">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="12e07-172">**WSAEINVAL**</span></span> | <span data-ttu-id="12e07-173">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="12e07-173">An invalid argument was supplied.</span></span> <span data-ttu-id="12e07-174">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="12e07-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="12e07-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="12e07-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="12e07-176">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="12e07-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="12e07-177">Эта ошибка возвращается в случае сбоя сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="12e07-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="12e07-178">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="12e07-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="12e07-179">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="12e07-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="12e07-180">Эта ошибка возвращается, если дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="12e07-180">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="12e07-181">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="12e07-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="12e07-182">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="12e07-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="12e07-183">Эта ошибка возвращается, если указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="12e07-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="12e07-184">Эта ошибка также возвращается, если в поставщике транспорта не поддерживаются **\_ \_ \_ \_ \_ записи перенаправления подключения SIO** .</span><span class="sxs-lookup"><span data-stu-id="12e07-184">This error is also returned if the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="12e07-185">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12e07-185">Remarks</span></span>

<span data-ttu-id="12e07-186">**\_ \_ \_ \_ \_ Записи перенаправления подключения SIO в WFP** поддерживаются в Windows 8, Windows Server 2012 и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="12e07-186">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="12e07-187">WFP обеспечивает доступ к пути обработки пакетов TCP/IP, где входящие и исходящие пакеты могут быть проверены или изменены перед тем, как разрешить их обработку.</span><span class="sxs-lookup"><span data-stu-id="12e07-187">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="12e07-188">Коснувшись пути обработки TCP/IP, независимые поставщики программного обеспечения могут более легко создавать брандмауэры, антивирусные программы, программное обеспечение диагностики и другие типы приложений и служб.</span><span class="sxs-lookup"><span data-stu-id="12e07-188">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="12e07-189">WFP предоставляет компоненты пользовательского режима и режима ядра, позволяющие сторонним поставщикам программного обеспечения участвовать в принятии решений о фильтрации, выполняемых на нескольких уровнях стека протоколов TCP/IP и всей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="12e07-189">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="12e07-190">Функция перенаправления подключения WFP позволяет драйверу ядра вызова WFP перенаправлять подключение локально в процесс пользовательского режима, выполнять проверку содержимого в пользовательском режиме и пересылать проверенное содержимое с помощью другого подключения к исходному назначению.</span><span class="sxs-lookup"><span data-stu-id="12e07-190">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="12e07-191">**Набор SIO \_ . \_ \_ \_ \_ записи перенаправления подключения в WFP** и несколько других связанных ioctl являются компонентами пользовательского режима, которые позволяют нескольким ПРИЛОЖЕНИЯМ-посредникам подключений на основе WFP проверять одинаковый поток трафика.</span><span class="sxs-lookup"><span data-stu-id="12e07-191">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="12e07-192">Каждый агент проверки может безопасно повторно проверить сетевой трафик, который уже был проверен другим агентом проверки.</span><span class="sxs-lookup"><span data-stu-id="12e07-192">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="12e07-193">При наличии нескольких прокси-серверов (например, разработанных разными поставщиками программного обеспечения) подключение, используемое одним прокси-сервером для обмена данными с конечным местом назначения, может быть перенаправлено вторым прокси-сервером, а новое соединение снова будет перенаправлено исходным прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="12e07-193">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="12e07-194">Без отслеживания подключений исходное соединение может никогда не достичь конечного места назначения, так как оно зависает в бесконечном цикле прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="12e07-194">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="12e07-195">**\_ \_ \_ \_ \_ Записи перенаправления подключения суперконтроллера** ввода-вывода по протоколу ioctl используются для обеспечения отслеживания подключений через посредника при перенаправленных соединениях сокетов.</span><span class="sxs-lookup"><span data-stu-id="12e07-195">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="12e07-196">Эта функция WFP упрощает отслеживание записей перенаправления из первоначального перенаправления соединения к конечному подключению.</span><span class="sxs-lookup"><span data-stu-id="12e07-196">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="12e07-197">[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) ioctl используется службой перенаправления на основе WFP для получения записи перенаправления из принятого соединения пакетов TCP/IP (например, подключенный сокет для сокета TCP или UDP-сокета), перенаправленный на **него в режиме \_ \_** ядра.</span><span class="sxs-lookup"><span data-stu-id="12e07-197">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at  **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="12e07-198">[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) ioctl получает контекст перенаправления для записи перенаправления, которая используется.</span><span class="sxs-lookup"><span data-stu-id="12e07-198">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL retrieves the redirect context for a redirect record, which is used.</span></span>
<span data-ttu-id="12e07-199">Контекст перенаправления является необязательным и используется, если текущее состояние перенаправления соединения заключается в том, что подключение было перенаправлено вызывающей службой перенаправления или если соединение было ранее перенаправлено вызывающей службой перенаправления, но позднее перенаправлено другой службой перенаправления. Служба перенаправления передает полученную запись перенаправления в сокет TCP, который используется для прокси-сервера с исходным содержимым, используя **\_ \_ \_ \_ \_ записи перенаправления подключения** с помощью SIO.</span><span class="sxs-lookup"><span data-stu-id="12e07-199">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="12e07-200">Приложение, вызывающее **\_ \_ \_ \_ \_ записи перенаправления подключения суперконтроллера** ввода/вывода, не нуждается в понимании большого двоичного объекта, содержащего заданную запись перенаправления.</span><span class="sxs-lookup"><span data-stu-id="12e07-200">The application calling the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect record being set.</span></span>
<span data-ttu-id="12e07-201">Это непрозрачный большой двоичный объект данных, который приложение должно передать обратно в новый сокет.</span><span class="sxs-lookup"><span data-stu-id="12e07-201">This is an opaque blob of data that the application needs to pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="12e07-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12e07-202">See also</span></span>

[<span data-ttu-id="12e07-203">**Параметры сокета IPPROTO_IP**</span><span class="sxs-lookup"><span data-stu-id="12e07-203">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="12e07-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="12e07-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="12e07-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="12e07-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="12e07-206">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="12e07-206">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="12e07-207">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="12e07-207">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="12e07-208">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="12e07-208">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="12e07-209">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="12e07-209">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="12e07-210">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="12e07-210">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="12e07-211">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="12e07-211">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="12e07-212">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="12e07-212">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
