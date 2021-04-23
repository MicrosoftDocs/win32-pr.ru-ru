---
description: Управляющий код запрашивает параметры транспорта на сокете.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: Код элемента управления SIO_QUERY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898573"
---
# <a name="sio_query_transport_setting-control-code"></a><span data-ttu-id="fa985-103">Код элемента управления SIO_QUERY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="fa985-103">SIO_QUERY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="fa985-104">Описание</span><span class="sxs-lookup"><span data-stu-id="fa985-104">Description</span></span>

<span data-ttu-id="fa985-105">Управляющий код **\_ \_ \_ параметров транспорта запросов SIO** запрашивает параметры транспорта на сокете.</span><span class="sxs-lookup"><span data-stu-id="fa985-105">The **SIO\_QUERY\_TRANSPORT\_SETTING** control code queries the transport settings on a socket.</span></span>

<span data-ttu-id="fa985-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="fa985-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="fa985-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa985-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="fa985-108">s</span><span class="sxs-lookup"><span data-stu-id="fa985-108">s</span></span>

<span data-ttu-id="fa985-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="fa985-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="fa985-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="fa985-110">dwIoControlCode</span></span>

<span data-ttu-id="fa985-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="fa985-111">The control code for the operation.</span></span>
<span data-ttu-id="fa985-112">Используйте **\_ \_ \_ параметр транспорта запросов SIO** для этой операции.</span><span class="sxs-lookup"><span data-stu-id="fa985-112">Use **SIO\_QUERY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="fa985-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="fa985-113">lpvInBuffer</span></span>

<span data-ttu-id="fa985-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="fa985-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="fa985-115">Этот параметр содержит указатель на структуру, в которой первый элемент структуры является [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) структурой, определяющей, какой параметр транспорта запрашивается.</span><span class="sxs-lookup"><span data-stu-id="fa985-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being queried.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="fa985-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="fa985-116">cbInBuffer</span></span>

<span data-ttu-id="fa985-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="fa985-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="fa985-118">Этот параметр зависит от параметра транспорта, к которому выполняется запрос.</span><span class="sxs-lookup"><span data-stu-id="fa985-118">This parameter depends on the transport setting being queried.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="fa985-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="fa985-119">lpvOutBuffer</span></span>

<span data-ttu-id="fa985-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="fa985-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="fa985-121">Этот параметр зависит от параметра транспорта, который запрашивается, если параметры *лповерлаппед* и *Лпкомплетионраутине* имеют **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="fa985-121">This parameter depends on the transport setting being queried if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="fa985-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="fa985-122">cbOutBuffer</span></span>

<span data-ttu-id="fa985-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="fa985-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="fa985-124">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="fa985-124">lpcbBytesReturned</span></span>

<span data-ttu-id="fa985-125">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="fa985-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="fa985-126">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="fa985-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="fa985-127">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="fa985-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="fa985-128">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="fa985-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="fa985-129">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="fa985-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="fa985-130">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="fa985-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="fa985-131">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="fa985-131">lpvOverlapped</span></span>

<span data-ttu-id="fa985-132">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="fa985-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="fa985-133">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fa985-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="fa985-134">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="fa985-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="fa985-135">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="fa985-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="fa985-136">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="fa985-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="fa985-137">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="fa985-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="fa985-138">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="fa985-138">lpCompletionRoutine</span></span>

<span data-ttu-id="fa985-139">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="fa985-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="fa985-140">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="fa985-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="fa985-141">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="fa985-141">lpThreadId</span></span>

<span data-ttu-id="fa985-142">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="fa985-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="fa985-143">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="fa985-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="fa985-144">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="fa985-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="fa985-145">лперрно</span><span class="sxs-lookup"><span data-stu-id="fa985-145">lpErrno</span></span>

<span data-ttu-id="fa985-146">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="fa985-146">A pointer to the error code.</span></span>

<span data-ttu-id="fa985-147">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="fa985-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa985-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa985-148">Return value</span></span>

<span data-ttu-id="fa985-149">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="fa985-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="fa985-150">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="fa985-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="fa985-151">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="fa985-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="fa985-152">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="fa985-152">Error code</span></span> | <span data-ttu-id="fa985-153">Значение</span><span class="sxs-lookup"><span data-stu-id="fa985-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="fa985-154">**Ошибка \_ недостаточного \_ буфера**</span><span class="sxs-lookup"><span data-stu-id="fa985-154">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="fa985-155">Область данных, переданная в системный вызов, слишком мала.</span><span class="sxs-lookup"><span data-stu-id="fa985-155">The data area passed to a system call is too small.</span></span> <span data-ttu-id="fa985-156">Эта ошибка возвращается, если буфер, на который указывает параметр *лпваутбуффер* с размером буфера, переданным в параметре *кбаутбуффер* , слишком мал.</span><span class="sxs-lookup"><span data-stu-id="fa985-156">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="fa985-157">Требуемый размер буфера будет возвращен в параметре *лпкббитесретурнед* .</span><span class="sxs-lookup"><span data-stu-id="fa985-157">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="fa985-158">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="fa985-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="fa985-159">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="fa985-159">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="fa985-160">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="fa985-160">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="fa985-161">Перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="fa985-161">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="fa985-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fa985-162">**WSAEFAULT**</span></span> | <span data-ttu-id="fa985-163">Параметр *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="fa985-163">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="fa985-164">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="fa985-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="fa985-165">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fa985-165">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="fa985-166">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="fa985-166">**WSAEINTR**</span></span> | <span data-ttu-id="fa985-167">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="fa985-167">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="fa985-168">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="fa985-168">**WSAEINVAL**</span></span> | <span data-ttu-id="fa985-169">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="fa985-169">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="fa985-170">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="fa985-170">**WSAENETDOWN**</span></span> | <span data-ttu-id="fa985-171">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="fa985-171">The network subsystem has failed.</span></span> |
| <span data-ttu-id="fa985-172">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="fa985-172">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="fa985-173">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="fa985-173">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="fa985-174">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="fa985-174">**WSAENOTCONN**</span></span> | <span data-ttu-id="fa985-175">Сокеты не подключены.</span><span class="sxs-lookup"><span data-stu-id="fa985-175">The socket s is not connected.</span></span> |
| <span data-ttu-id="fa985-176">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="fa985-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="fa985-177">Дескриптор s не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="fa985-177">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="fa985-178">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="fa985-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="fa985-179">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fa985-179">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="fa985-180">Эта ошибка возвращается, если **\_ \_ \_ параметр транспорта запросов SIO** не поддерживается поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="fa985-180">This error is returned if the **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="fa985-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa985-181">Remarks</span></span>

<span data-ttu-id="fa985-182">**\_ \_ \_ Параметр транспорта запросов SIO** поддерживается в windows 8, Windows Server 2012 и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fa985-182">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="fa985-183">**\_ \_ \_ Параметр передачи запросов SIO** — это универсальный запрос IOCTL, используемый для запроса параметров транспорта на сокете.</span><span class="sxs-lookup"><span data-stu-id="fa985-183">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to query the transport settings on a socket.</span></span>
<span data-ttu-id="fa985-184">Запрашиваемый параметр транспорта основан на [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре *лпвинбуффер* .</span><span class="sxs-lookup"><span data-stu-id="fa985-184">The transport setting being queried is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="fa985-185">Единственным параметром транспорта, который сейчас определяет, является возможность получения **\_ \_ уведомлений \_ в режиме реального времени** на сокете TCP.</span><span class="sxs-lookup"><span data-stu-id="fa985-185">The only transport setting currently defines is for the **REAL\_TIME\_NOTIFICATION\_CAPABILITY** capability on a TCP socket.</span></span>

<span data-ttu-id="fa985-186">Если в [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре *лпвинбуффер* , для элемента GUID задана **\_ \_ \_ возможность уведомления в режиме реального времени**, это запрос на запрос параметров уведомлений в режиме реального времени для сокета TCP, используемого с [**Контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) , для получения фоновых сетевых уведомлений в приложении Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="fa985-186">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to query the real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="fa985-187">Параметр *лпвинбуффер* должен указывать на структуру [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) .</span><span class="sxs-lookup"><span data-stu-id="fa985-187">The *lpvInBuffer* parameter should point to a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure.</span></span>
<span data-ttu-id="fa985-188">Параметр *лпваутбуффер* должен указывать на **\_ \_ \_ \_ выходную структуру параметра уведомления в режиме реального времени** .</span><span class="sxs-lookup"><span data-stu-id="fa985-188">The *lpvOutBuffer* parameter should point to a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure.</span></span>
<span data-ttu-id="fa985-189">Этот параметр транспорта применяется только к сокетам TCP.</span><span class="sxs-lookup"><span data-stu-id="fa985-189">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="fa985-190">Этот параметр транспорта предоставляет WinInet или подобным сетевым службам запрос на заданный TCP-сокет для определения состояния [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .</span><span class="sxs-lookup"><span data-stu-id="fa985-190">This transport setting provides a way for WinInet or similar network services to query a given TCP socket to determine the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) status.</span></span>
<span data-ttu-id="fa985-191">Приложение Магазина Windows не будет вызывать этот запрос IOCTL напрямую.</span><span class="sxs-lookup"><span data-stu-id="fa985-191">A Windows Store app will not call this IOCTL directly.</span></span>
<span data-ttu-id="fa985-192">При успешном вызове [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **ВСПИОКТЛ** этот запрос IOCTL возвращает **\_ \_ \_ \_ выходную структуру параметра уведомления в режиме реального времени** с текущим состоянием.</span><span class="sxs-lookup"><span data-stu-id="fa985-192">If the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** call is successful, this IOCTL returns a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure with the current status.</span></span>

<span data-ttu-id="fa985-193">**\_ \_ \_ Параметр передачи запросов SIO** позволяет службе WinInet или подобным сетевым службам запрашивать состояние параметра транспорта для данного TCP-сокета, чтобы определить, включен ли [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) на сокете.</span><span class="sxs-lookup"><span data-stu-id="fa985-193">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL provides a way for WinInet or similar network services to query for the transport setting status for a given TCP socket to determine if [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) is enabled on the socket.</span></span>
<span data-ttu-id="fa985-194">Приложение Магазина Windows не будет вызывать этот запрос IOCTL напрямую.</span><span class="sxs-lookup"><span data-stu-id="fa985-194">A Windows Store app will not call this IOCTL directly.</span></span>

<span data-ttu-id="fa985-195">Этот запрос IOCTL применяется только к сокетам TCP.</span><span class="sxs-lookup"><span data-stu-id="fa985-195">This IOCTL applies only to TCP sockets.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa985-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa985-196">See also</span></span>

[<span data-ttu-id="fa985-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="fa985-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span></span>](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[<span data-ttu-id="fa985-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="fa985-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="fa985-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span><span class="sxs-lookup"><span data-stu-id="fa985-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[<span data-ttu-id="fa985-200">**SIO_APPLY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="fa985-200">**SIO_APPLY_TRANSPORT_SETTING**</span></span>](sio-apply-transport-setting.md)

[<span data-ttu-id="fa985-201">фиксатор</span><span class="sxs-lookup"><span data-stu-id="fa985-201">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="fa985-202">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="fa985-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="fa985-203">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="fa985-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="fa985-204">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="fa985-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="fa985-205">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="fa985-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="fa985-206">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="fa985-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="fa985-207">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="fa985-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
