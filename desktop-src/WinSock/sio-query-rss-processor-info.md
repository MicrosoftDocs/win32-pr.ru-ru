---
description: Управляющий код запрашивает связь между сокетом и ядром процессора RSS и узлом NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: Код элемента управления SIO_QUERY_RSS_PROCESSOR_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991108"
---
# <a name="sio_query_rss_processor_info-control-code"></a><span data-ttu-id="8a817-103">Код элемента управления SIO_QUERY_RSS_PROCESSOR_INFO</span><span class="sxs-lookup"><span data-stu-id="8a817-103">SIO_QUERY_RSS_PROCESSOR_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="8a817-104">Описание</span><span class="sxs-lookup"><span data-stu-id="8a817-104">Description</span></span>

<span data-ttu-id="8a817-105">Код **управления \_ \_ \_ \_ сведениями о обработчике SIO для запросов к RSS-каналу** запрашивает связь между сокетом и ядром процессора RSS и узлом NUMA.</span><span class="sxs-lookup"><span data-stu-id="8a817-105">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** control code queries the association between a socket and an RSS processor core and NUMA node.</span></span>

<span data-ttu-id="8a817-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="8a817-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="8a817-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a817-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="8a817-108">s</span><span class="sxs-lookup"><span data-stu-id="8a817-108">s</span></span>

<span data-ttu-id="8a817-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="8a817-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="8a817-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="8a817-110">dwIoControlCode</span></span>

<span data-ttu-id="8a817-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="8a817-111">The control code for the operation.</span></span>
<span data-ttu-id="8a817-112">Для этой операции используйте **\_ \_ \_ \_ сведения о обработчике запросов SIO** в формате RSS.</span><span class="sxs-lookup"><span data-stu-id="8a817-112">Use **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="8a817-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="8a817-113">lpvInBuffer</span></span>

<span data-ttu-id="8a817-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="8a817-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="8a817-115">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="8a817-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="8a817-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="8a817-116">cbInBuffer</span></span>

<span data-ttu-id="8a817-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="8a817-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="8a817-118">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="8a817-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="8a817-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="8a817-119">lpvOutBuffer</span></span>

<span data-ttu-id="8a817-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="8a817-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="8a817-121">Этот параметр должен указывать на структуру [**\_ \_ сходства процессоров сокетов**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) , если параметры *Лповерлаппед* и *лпкомплетионраутине* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8a817-121">This parameter should point to a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="8a817-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="8a817-122">cbOutBuffer</span></span>

<span data-ttu-id="8a817-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="8a817-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="8a817-124">Этот параметр должен быть не меньше размера структуры [**\_ \_ сходства процессора сокета**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="8a817-124">This parameter must be at least the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="8a817-125">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="8a817-125">lpcbBytesReturned</span></span>

<span data-ttu-id="8a817-126">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="8a817-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="8a817-127">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение *DWORD* , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="8a817-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a *DWORD* value of zero.</span></span>

<span data-ttu-id="8a817-128">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="8a817-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="8a817-129">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="8a817-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="8a817-130">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="8a817-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="8a817-131">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="8a817-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="8a817-132">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="8a817-132">lpvOverlapped</span></span>

<span data-ttu-id="8a817-133">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="8a817-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8a817-134">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8a817-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="8a817-135">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="8a817-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="8a817-136">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="8a817-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8a817-137">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="8a817-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="8a817-138">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="8a817-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="8a817-139">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="8a817-139">lpCompletionRoutine</span></span>

<span data-ttu-id="8a817-140">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="8a817-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="8a817-141">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="8a817-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="8a817-142">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="8a817-142">lpThreadId</span></span>

<span data-ttu-id="8a817-143">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="8a817-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="8a817-144">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="8a817-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="8a817-145">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="8a817-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="8a817-146">лперрно</span><span class="sxs-lookup"><span data-stu-id="8a817-146">lpErrno</span></span>

<span data-ttu-id="8a817-147">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="8a817-147">A pointer to the error code.</span></span>

<span data-ttu-id="8a817-148">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="8a817-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a817-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a817-149">Return value</span></span>

<span data-ttu-id="8a817-150">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8a817-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="8a817-151">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="8a817-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="8a817-152">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="8a817-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="8a817-153">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="8a817-153">Error code</span></span> | <span data-ttu-id="8a817-154">Значение</span><span class="sxs-lookup"><span data-stu-id="8a817-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="8a817-155">**Ошибка \_ недостаточного \_ буфера**</span><span class="sxs-lookup"><span data-stu-id="8a817-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="8a817-156">Область данных, переданная в системный вызов, слишком мала.</span><span class="sxs-lookup"><span data-stu-id="8a817-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="8a817-157">Эта ошибка возвращается, если буфер, на который указывает параметр *лпваутбуффер* с размером буфера, переданным в параметре *кбаутбуффер* , слишком мал.</span><span class="sxs-lookup"><span data-stu-id="8a817-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="8a817-158">Требуемый размер буфера будет возвращен в параметре *лпкббитесретурнед* .</span><span class="sxs-lookup"><span data-stu-id="8a817-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> <span data-ttu-id="8a817-159">Эта ошибка возвращается, если параметр *кбаутбуффер* меньше размера структуры [**\_ \_ сходства процессора сокета**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="8a817-159">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span> |
| <span data-ttu-id="8a817-160">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="8a817-160">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="8a817-161">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="8a817-161">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="8a817-162">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="8a817-162">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="8a817-163">Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="8a817-163">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="8a817-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8a817-164">**WSAEFAULT**</span></span> | <span data-ttu-id="8a817-165">Параметр *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="8a817-165">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="8a817-166">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="8a817-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="8a817-167">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8a817-167">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="8a817-168">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="8a817-168">**WSAEINTR**</span></span> | <span data-ttu-id="8a817-169">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="8a817-169">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="8a817-170">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="8a817-170">**WSAEINVAL**</span></span> | <span data-ttu-id="8a817-171">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="8a817-171">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="8a817-172">Эта ошибка возвращается, если параметр *кбаутбуффер* меньше размера структуры [**\_ \_ сходства процессора сокета**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="8a817-172">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>
| <span data-ttu-id="8a817-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="8a817-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="8a817-174">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="8a817-174">The network subsystem has failed.</span></span> |
| <span data-ttu-id="8a817-175">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="8a817-175">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="8a817-176">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="8a817-176">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="8a817-177">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="8a817-177">**WSAENOTCONN**</span></span> | <span data-ttu-id="8a817-178">*Сокеты не* подключены.</span><span class="sxs-lookup"><span data-stu-id="8a817-178">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="8a817-179">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="8a817-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="8a817-180">Дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="8a817-180">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="8a817-181">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="8a817-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="8a817-182">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8a817-182">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="8a817-183">Эта ошибка возвращается в том случае, если поставщик транспорта не поддерживает **\_ запрос на \_ \_ \_ сведения о процессоре SIO** в формате RSS.</span><span class="sxs-lookup"><span data-stu-id="8a817-183">This error is returned if the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="8a817-184">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a817-184">Remarks</span></span>

<span data-ttu-id="8a817-185">**\_ \_ \_ \_ Сведения о обработчике запросов SIO** в формате RSS поддерживаются в Windows 8, Windows Server 2012 и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8a817-185">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="8a817-186">**\_ \_ \_ \_ Сведения о обработчике запросов SIO** в формате RSS используются для определения связи между сокетом и ядром процессора RSS и узлом NUMA.</span><span class="sxs-lookup"><span data-stu-id="8a817-186">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node.</span></span>
<span data-ttu-id="8a817-187">Этот запрос IOCTL возвращает [**структуру \_ \_ соответствия процессоров сокетов**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) , которая содержит [**\_ номер процессора**](/windows/desktop/api/winnt/ns-winnt-processor_number) и идентификатор узла NUMA.</span><span class="sxs-lookup"><span data-stu-id="8a817-187">This IOCTL returns a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure that contains the [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) and the NUMA node ID.</span></span>
<span data-ttu-id="8a817-188">Возвращенная [**Структура \_ номеров процессоров**](/windows/desktop/api/winnt/ns-winnt-processor_number) содержит номер группы и относительный номер процессора в группе.</span><span class="sxs-lookup"><span data-stu-id="8a817-188">The returned [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) structure contains a group number and relative processor number within the group.</span></span>

<span data-ttu-id="8a817-189">Если сокет является UDP-сокетом, сокет должен быть подключен для правильной работы **\_ запроса на \_ \_ \_ сведения о процессоре SIO с запросом** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="8a817-189">If the socket is a UDP socket, the socket must be connected for the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL to work properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a817-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a817-190">See also</span></span>

[<span data-ttu-id="8a817-191">**PROCESSOR_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="8a817-191">**PROCESSOR_NUMBER**</span></span>](/windows/desktop/api/winnt/ns-winnt-processor_number)

[<span data-ttu-id="8a817-192">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="8a817-192">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="8a817-193">**SOCKET_PROCESSOR_AFFINITY**</span><span class="sxs-lookup"><span data-stu-id="8a817-193">**SOCKET_PROCESSOR_AFFINITY**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[<span data-ttu-id="8a817-194">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="8a817-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="8a817-195">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="8a817-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="8a817-196">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="8a817-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="8a817-197">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="8a817-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="8a817-198">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="8a817-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="8a817-199">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="8a817-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
