---
description: Управляющий код получает статистику протокола TCP для указанного сокета.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: Код элемента управления SIO_TCP_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: cea9a2d31654d1263f285ee9967b24700fe25138
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105720833"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="36571-103">Код элемента управления SIO_TCP_INFO</span><span class="sxs-lookup"><span data-stu-id="36571-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="36571-104">Описание</span><span class="sxs-lookup"><span data-stu-id="36571-104">Description</span></span>

<span data-ttu-id="36571-105">Код **управления \_ \_ сведениями TCP SIO** получает статистику протокола TCP для указанного сокета.</span><span class="sxs-lookup"><span data-stu-id="36571-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="36571-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="36571-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="36571-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="36571-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="36571-108">s</span><span class="sxs-lookup"><span data-stu-id="36571-108">s</span></span>

<span data-ttu-id="36571-109">Дескриптор, определяющий сокет.</span><span class="sxs-lookup"><span data-stu-id="36571-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="36571-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="36571-110">dwIoControlCode</span></span>

<span data-ttu-id="36571-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="36571-111">The control code for the operation.</span></span>
<span data-ttu-id="36571-112">Для этой операции используйте **\_ \_ сведения TCP SIO** .</span><span class="sxs-lookup"><span data-stu-id="36571-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="36571-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="36571-113">lpvInBuffer</span></span>

<span data-ttu-id="36571-114">Указатель на входной буфер.</span><span class="sxs-lookup"><span data-stu-id="36571-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="36571-115">Этот параметр содержит указатель на **DWORD** , указывающий версию управляющего кода **\_ TCP \_ SIO** .</span><span class="sxs-lookup"><span data-stu-id="36571-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="36571-116">Укажите 0, чтобы использовать [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span><span class="sxs-lookup"><span data-stu-id="36571-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="36571-117">Укажите 1, чтобы использовать [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), повидес больше полей.</span><span class="sxs-lookup"><span data-stu-id="36571-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which povides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="36571-118">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="36571-118">cbInBuffer</span></span>

<span data-ttu-id="36571-119">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="36571-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="36571-120">Этот параметр должен иметь размер типа данных **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="36571-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="36571-121">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="36571-121">lpvOutBuffer</span></span>

<span data-ttu-id="36571-122">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="36571-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="36571-123">При успешном выходе этот параметр содержит указатель на структуру [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) , СОДЕРЖАЩУЮ статистику TCP для указанного сокета.</span><span class="sxs-lookup"><span data-stu-id="36571-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="36571-124">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="36571-124">cbOutBuffer</span></span>

<span data-ttu-id="36571-125">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="36571-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="36571-126">Этот параметр должен быть не меньше размера структуры [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) .</span><span class="sxs-lookup"><span data-stu-id="36571-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="36571-127">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="36571-127">lpcbBytesReturned</span></span>

<span data-ttu-id="36571-128">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="36571-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="36571-129">Если выходной буфер слишком мал, вызов завершается ошибкой, [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает [**всаеинвал**](windows-sockets-error-codes-2.md), а параметр *лпкббитесретурнед* указывает на значение **DWORD** , равное нулю.</span><span class="sxs-lookup"><span data-stu-id="36571-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="36571-130">Если *лповерлаппед* имеет значение **null**, то значение **DWORD** , на которое указывает параметр *лпкббитесретурнед* , возвращаемое при успешном вызове, не может быть нулевым.</span><span class="sxs-lookup"><span data-stu-id="36571-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="36571-131">Если параметр *лповерлаппед* имеет значение, отличное от **null** , для перекрывающихся сокетов, то операции, которые не могут быть выполнены немедленно, будут инициированы, а завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="36571-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="36571-132">Значение **DWORD** , на которое указывает возвращаемый параметр *лпкббитесретурнед* , может быть равно нулю, так как размер хранимых данных не может быть определен до завершения операции перекрытия.</span><span class="sxs-lookup"><span data-stu-id="36571-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="36571-133">Окончательное состояние завершения можно получить, если при выполнении операции будет получен сигнал о соответствующем методе завершения.</span><span class="sxs-lookup"><span data-stu-id="36571-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="36571-134">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="36571-134">lpvOverlapped</span></span>

<span data-ttu-id="36571-135">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="36571-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="36571-136">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="36571-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="36571-137">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="36571-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="36571-138">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="36571-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="36571-139">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="36571-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="36571-140">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="36571-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="36571-141">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="36571-141">lpCompletionRoutine</span></span>

<span data-ttu-id="36571-142">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="36571-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="36571-143">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="36571-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="36571-144">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="36571-144">lpThreadId</span></span>

<span data-ttu-id="36571-145">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="36571-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="36571-146">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="36571-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="36571-147">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="36571-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="36571-148">лперрно</span><span class="sxs-lookup"><span data-stu-id="36571-148">lpErrno</span></span>

<span data-ttu-id="36571-149">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="36571-149">A pointer to the error code.</span></span>

<span data-ttu-id="36571-150">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="36571-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="36571-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36571-151">Return value</span></span>

<span data-ttu-id="36571-152">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="36571-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="36571-153">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="36571-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="36571-154">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="36571-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="36571-155">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="36571-155">Error code</span></span> | <span data-ttu-id="36571-156">Значение</span><span class="sxs-lookup"><span data-stu-id="36571-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="36571-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="36571-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="36571-158">Указатель на входной буфер имел **значение NULL** или указан неправильный размер входного буфера.</span><span class="sxs-lookup"><span data-stu-id="36571-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="36571-159">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="36571-159">**WSAEINVAL**</span></span> | <span data-ttu-id="36571-160">Указан недопустимый аргумент.</span><span class="sxs-lookup"><span data-stu-id="36571-160">An invalid argument was supplied.</span></span> <span data-ttu-id="36571-161">Эта ошибка возвращается, если параметр *двиоконтролкоде* не является допустимой командой или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="36571-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="36571-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36571-162">Remarks</span></span>

<span data-ttu-id="36571-163">В отличие от получения статистики TCP с помощью функции [**жетперткпконнектионестатс**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) , получение статистики TCP с помощью этого управляющего кода не требует от пользовательского кода загрузки, хранения и фильтрации таблицы соединений TCP, а также не требует повышенных привилегий для использования.</span><span class="sxs-lookup"><span data-stu-id="36571-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="36571-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36571-164">See also</span></span>

[<span data-ttu-id="36571-165">фиксатор</span><span class="sxs-lookup"><span data-stu-id="36571-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="36571-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="36571-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="36571-167">**жетперткпконнектионестатс**</span><span class="sxs-lookup"><span data-stu-id="36571-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="36571-168">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="36571-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="36571-169">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="36571-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="36571-170">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="36571-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="36571-171">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="36571-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="36571-172">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="36571-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="36571-173">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="36571-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
