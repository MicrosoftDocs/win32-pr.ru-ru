---
description: Управляющий код применяет один или несколько параметров транспорта к сокету.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: Код элемента управления SIO_APPLY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719460"
---
# <a name="sio_apply_transport_setting-control-code"></a><span data-ttu-id="0c240-103">Код элемента управления SIO_APPLY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="0c240-103">SIO_APPLY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="0c240-104">Описание</span><span class="sxs-lookup"><span data-stu-id="0c240-104">Description</span></span>

<span data-ttu-id="0c240-105">Контрольный код для **\_ применения \_ \_ параметров транспорта** применяет один или несколько параметров транспорта к сокету.</span><span class="sxs-lookup"><span data-stu-id="0c240-105">The **SIO\_APPLY\_TRANSPORT\_SETTING** control code applies one or more transport settings to a socket.</span></span>

<span data-ttu-id="0c240-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="0c240-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="0c240-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c240-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="0c240-108">s</span><span class="sxs-lookup"><span data-stu-id="0c240-108">s</span></span>

<span data-ttu-id="0c240-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="0c240-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="0c240-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="0c240-110">dwIoControlCode</span></span>

<span data-ttu-id="0c240-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="0c240-111">The control code for the operation.</span></span>
<span data-ttu-id="0c240-112">Используйте для этой операции **\_ \_ \_ параметр транспорта, применяемый SIO** .</span><span class="sxs-lookup"><span data-stu-id="0c240-112">Use **SIO\_APPLY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="0c240-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="0c240-113">lpvInBuffer</span></span>

<span data-ttu-id="0c240-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="0c240-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="0c240-115">Этот параметр содержит указатель на структуру, в которой первый элемент структуры является [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) структурой, определяющей, какой параметр транспорта применяется.</span><span class="sxs-lookup"><span data-stu-id="0c240-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being applied.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="0c240-116">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="0c240-116">cbInBuffer</span></span>

<span data-ttu-id="0c240-117">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="0c240-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="0c240-118">Этот параметр зависит от применяемого параметра транспорта.</span><span class="sxs-lookup"><span data-stu-id="0c240-118">This parameter depends on the transport setting being applied.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="0c240-119">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="0c240-119">lpvOutBuffer</span></span>

<span data-ttu-id="0c240-120">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="0c240-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="0c240-121">Этот параметр зависит от применяемого параметра транспорта.</span><span class="sxs-lookup"><span data-stu-id="0c240-121">This parameter depends on the transport setting being applied.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="0c240-122">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="0c240-122">cbOutBuffer</span></span>

<span data-ttu-id="0c240-123">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="0c240-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="0c240-124">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="0c240-124">lpcbBytesReturned</span></span>

<span data-ttu-id="0c240-125">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="0c240-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="0c240-126">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="0c240-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="0c240-127">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="0c240-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="0c240-128">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="0c240-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="0c240-129">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="0c240-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="0c240-130">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="0c240-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="0c240-131">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="0c240-131">lpvOverlapped</span></span>

<span data-ttu-id="0c240-132">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="0c240-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="0c240-133">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0c240-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="0c240-134">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="0c240-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="0c240-135">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="0c240-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="0c240-136">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="0c240-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="0c240-137">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="0c240-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="0c240-138">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="0c240-138">lpCompletionRoutine</span></span>

<span data-ttu-id="0c240-139">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="0c240-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="0c240-140">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="0c240-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="0c240-141">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="0c240-141">lpThreadId</span></span>

<span data-ttu-id="0c240-142">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="0c240-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="0c240-143">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="0c240-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="0c240-144">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="0c240-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="0c240-145">лперрно</span><span class="sxs-lookup"><span data-stu-id="0c240-145">lpErrno</span></span>

<span data-ttu-id="0c240-146">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0c240-146">A pointer to the error code.</span></span>

<span data-ttu-id="0c240-147">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="0c240-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c240-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c240-148">Return value</span></span>

<span data-ttu-id="0c240-149">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="0c240-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="0c240-150">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="0c240-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="0c240-151">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="0c240-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="0c240-152">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="0c240-152">Error code</span></span> | <span data-ttu-id="0c240-153">Значение</span><span class="sxs-lookup"><span data-stu-id="0c240-153">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="0c240-154">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="0c240-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="0c240-155">Выполняется перекрывающаяся операция ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="0c240-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="0c240-156">Это значение возвращается в том случае, если операция перекрытия была успешно инициирована и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="0c240-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="0c240-157">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="0c240-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="0c240-158">Операция ввода-вывода прервана из-за завершения потока или запроса приложения.</span><span class="sxs-lookup"><span data-stu-id="0c240-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="0c240-159">Эта ошибка возвращается, если перекрывающаяся операция была отменена из-за закрытия сокета или выполнения команды ioctl **\_ flush суперконтроллера** ввода/вывода.</span><span class="sxs-lookup"><span data-stu-id="0c240-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="0c240-160">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0c240-160">**WSAEFAULT**</span></span> | <span data-ttu-id="0c240-161">Система обнаружила недопустимый адрес указателя при попытке использовать аргумент указателя в вызове.</span><span class="sxs-lookup"><span data-stu-id="0c240-161">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="0c240-162">Эта ошибка возвращается параметром *лпвинбуффер*, *лпваутбуффер*, *лпкббитесретурнед*, *лповерлаппед* или *лпкомплетионраутине* , который полностью не содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c240-162">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="0c240-163">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="0c240-163">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="0c240-164">В данный момент выполняется блокирующая операция.</span><span class="sxs-lookup"><span data-stu-id="0c240-164">A blocking operation is currently executing.</span></span> <span data-ttu-id="0c240-165">Эта ошибка возвращается, если функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0c240-165">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="0c240-166">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="0c240-166">**WSAEINTR**</span></span> | <span data-ttu-id="0c240-167">Операция блокировки была прервана вызовом [**всаканцелблоккингкалл**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="0c240-167">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="0c240-168">Эта ошибка возвращается в случае прерывания блокирующей операции.</span><span class="sxs-lookup"><span data-stu-id="0c240-168">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="0c240-169">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="0c240-169">**WSAEINVAL**</span></span> | <span data-ttu-id="0c240-170">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="0c240-170">An invalid argument was supplied.</span></span> <span data-ttu-id="0c240-171">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="0c240-171">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="0c240-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="0c240-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="0c240-173">Операция на сокете обнаружила отключение сети.</span><span class="sxs-lookup"><span data-stu-id="0c240-173">A socket operation encountered a dead network.</span></span> <span data-ttu-id="0c240-174">Эта ошибка возвращается в случае сбоя сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="0c240-174">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="0c240-175">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="0c240-175">**WSAENOTSOCK**</span></span> | <span data-ttu-id="0c240-176">Предпринята попытка выполнить операцию для объекта, который не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="0c240-176">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="0c240-177">Эта ошибка возвращается, если дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="0c240-177">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="0c240-178">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="0c240-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="0c240-179">Предпринятая операция не поддерживается для типа объекта, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="0c240-179">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="0c240-180">Эта ошибка возвращается, если указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0c240-180">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="0c240-181">Эта ошибка также возвращается в том случае, если **\_ \_ \_ Параметры транспорта, применяемые SIO** , не поддерживаются поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="0c240-181">This error is also returned if the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="0c240-182">Эта ошибка также возвращается, если попытка использовать **\_ \_ \_ параметр транспорта, применяемого через SIO** , выполняется на сокете, отличном от UDP или TCP.</span><span class="sxs-lookup"><span data-stu-id="0c240-182">This error is also returned when an attempt to use the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="0c240-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c240-183">Remarks</span></span>

<span data-ttu-id="0c240-184">**\_ \_ \_ Параметры транспорта, применяемые SIO** , поддерживаются в windows 8, Windows Server 2012 и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0c240-184">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="0c240-185">**\_ \_ \_ Параметры транспорта, применяемые SIO** , — это универсальный запрос IOCTL, используемый для применения параметра транспорта к сокету.</span><span class="sxs-lookup"><span data-stu-id="0c240-185">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to apply transport setting to socket.</span></span>
<span data-ttu-id="0c240-186">Применяемый параметр транспорта основан на [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре *лпвинбуффер* .</span><span class="sxs-lookup"><span data-stu-id="0c240-186">The transport setting being applied is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="0c240-187">Начиная с Windows 8 и Windows Server 2012, система определяет **REAL_TIME_NOTIFICATION_CAPABILITYную** возможность на сокете TCP.</span><span class="sxs-lookup"><span data-stu-id="0c240-187">Starting with Windows 8 and Windows Server 2012, the system defines the **REAL_TIME_NOTIFICATION_CAPABILITY** capability on a TCP socket.</span></span>
<span data-ttu-id="0c240-188">Начиная с Windows 10 и Windows Server 2016, также определяется **\_ \_ контекст связывания намерес** .</span><span class="sxs-lookup"><span data-stu-id="0c240-188">Starting with Windows 10 and Windows Server 2016, **ASSOCIATE\_NAMERES\_CONTEXT** is also defined.</span></span>
<span data-ttu-id="0c240-189">Дополнительные сведения см. в разделе [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span><span class="sxs-lookup"><span data-stu-id="0c240-189">For more information, see [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span></span>

<span data-ttu-id="0c240-190">Если в [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , переданном в параметре лпвинбуффер, для элемента GUID задана **\_ \_ \_ возможность уведомления в режиме реального времени**, это запрос на применение параметров уведомлений в режиме реального времени для сокета TCP, используемого вместе с [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) для получения уведомлений в фоновом режиме в приложении Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="0c240-190">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the lpvInBuffer parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to apply real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="0c240-191">Параметр *лпвинбуффер* должен указывать на структуру **REAL_TIME_NOTIFICATION_SETTING_INPUT** .</span><span class="sxs-lookup"><span data-stu-id="0c240-191">The *lpvInBuffer* parameter should point to a **REAL_TIME_NOTIFICATION_SETTING_INPUT** structure.</span></span>
<span data-ttu-id="0c240-192">Параметр *лпваутбуффер* не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="0c240-192">The *lpvOutBuffer* parameter is unused for this operation.</span></span>
<span data-ttu-id="0c240-193">Этот параметр транспорта применяется только к сокетам TCP.</span><span class="sxs-lookup"><span data-stu-id="0c240-193">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="0c240-194">Этот параметр транспорта позволяет WinInet или подобным сетевым службам пометить заданный сокет TCP как включенный [**контролчаннелтригжер**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .</span><span class="sxs-lookup"><span data-stu-id="0c240-194">This transport setting provides a way for WinInet or similar network services to mark a given TCP socket as [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) enabled.</span></span>
<span data-ttu-id="0c240-195">Windows пометит соответствующий сокет TCP и настроит соответствующие параметры оборудования и программного обеспечения при вызове этого параметра.</span><span class="sxs-lookup"><span data-stu-id="0c240-195">Windows will mark the corresponding TCP socket and configure appropriate hardware and software settings when this option is called.</span></span>
<span data-ttu-id="0c240-196">Приложение Магазина Windows не будет вызывать этот запрос IOCTL напрямую.</span><span class="sxs-lookup"><span data-stu-id="0c240-196">A Windows Store app will not call this IOCTL directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c240-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c240-197">See also</span></span>

[<span data-ttu-id="0c240-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="0c240-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="0c240-199">фиксатор</span><span class="sxs-lookup"><span data-stu-id="0c240-199">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="0c240-200">**SIO_QUERY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="0c240-200">**SIO_QUERY_TRANSPORT_SETTING**</span></span>](sio-query-transport-setting.md)

[<span data-ttu-id="0c240-201">**TRANSPORT_SETTING_ID**</span><span class="sxs-lookup"><span data-stu-id="0c240-201">**TRANSPORT_SETTING_ID**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[<span data-ttu-id="0c240-202">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="0c240-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="0c240-203">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="0c240-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="0c240-204">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="0c240-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="0c240-205">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="0c240-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="0c240-206">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="0c240-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="0c240-207">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="0c240-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
