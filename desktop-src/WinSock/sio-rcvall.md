---
description: Управляющий код позволяет сокету принимать все пакеты IPv4 или IPv6, передаваемые через сетевой интерфейс.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: Код элемента управления SIO_RCVALL
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719341"
---
# <a name="sio_rcvall-control-code"></a><span data-ttu-id="669f0-103">Код элемента управления SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="669f0-103">SIO_RCVALL Control Code</span></span>

## <a name="description"></a><span data-ttu-id="669f0-104">Описание</span><span class="sxs-lookup"><span data-stu-id="669f0-104">Description</span></span>
<span data-ttu-id="669f0-105">Управляющий код **SIO \_ рквалл** позволяет сокету принимать все пакеты IPv4 или IPv6, передаваемые через сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="669f0-105">The **SIO\_RCVALL** control code enables a socket to receive all IPv4 or IPv6 packets passing through a network interface.</span></span>

<span data-ttu-id="669f0-106">Чтобы выполнить эту операцию, вызовите функцию [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="669f0-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="669f0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="669f0-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="669f0-108">s</span><span class="sxs-lookup"><span data-stu-id="669f0-108">s</span></span>

<span data-ttu-id="669f0-109">Дескриптор, идентифицирующий сокет.</span><span class="sxs-lookup"><span data-stu-id="669f0-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="669f0-110">двиоконтролкоде</span><span class="sxs-lookup"><span data-stu-id="669f0-110">dwIoControlCode</span></span>

<span data-ttu-id="669f0-111">Управляющий код для операции.</span><span class="sxs-lookup"><span data-stu-id="669f0-111">The control code for the operation.</span></span>
<span data-ttu-id="669f0-112">Для этой операции используйте **SIO \_ рквалл** .</span><span class="sxs-lookup"><span data-stu-id="669f0-112">Use **SIO\_RCVALL** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="669f0-113">лпвинбуффер</span><span class="sxs-lookup"><span data-stu-id="669f0-113">lpvInBuffer</span></span>

<span data-ttu-id="669f0-114">Указатель на входной буфер, который должен содержать значение параметра.</span><span class="sxs-lookup"><span data-stu-id="669f0-114">A pointer to the input buffer that should contain the option value.</span></span>
<span data-ttu-id="669f0-115">Возможные значения параметра **SIO \_ рквалл** ioctl указаны в перечислении **RCVALL_VALUE** , определенном в файле заголовка *мсткпип. h* .</span><span class="sxs-lookup"><span data-stu-id="669f0-115">The possible values for the **SIO\_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the *Mstcpip.h* header file.</span></span>

<span data-ttu-id="669f0-116">Ниже приведены возможные значения для **SIO \_ рквалл** .</span><span class="sxs-lookup"><span data-stu-id="669f0-116">The possible values for **SIO\_RCVALL** are as follows:</span></span>

| <span data-ttu-id="669f0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="669f0-117">Value</span></span> | <span data-ttu-id="669f0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="669f0-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="669f0-119">**РКВАЛЛ \_**</span><span class="sxs-lookup"><span data-stu-id="669f0-119">**RCVALL\_OFF**</span></span> | <span data-ttu-id="669f0-120">Отключите этот параметр, чтобы сокет не получал все пакеты IPv4 или IPv6, передаваемые через сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="669f0-120">Disable this option so a socket does not receive all IPv4 or IPv6 packets passing through a network interface.</span></span> |
| <span data-ttu-id="669f0-121">**РКВАЛЛ \_**</span><span class="sxs-lookup"><span data-stu-id="669f0-121">**RCVALL\_ON**</span></span> | <span data-ttu-id="669f0-122">Включите этот параметр, чтобы сокет получал все пакеты IPv4 или IPv6, передаваемые через сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="669f0-122">Enable this option so a socket receives all IPv4 or IPv6 packets passing through a network interface.</span></span> <span data-ttu-id="669f0-123">Этот параметр включает неизбирательный режим на плате сетевого интерфейса (NIC), если сетевой адаптер поддерживает неизбирательный режим.</span><span class="sxs-lookup"><span data-stu-id="669f0-123">This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode.</span></span> <span data-ttu-id="669f0-124">В сегменте локальной сети с сетевым концентратором сетевая карта, поддерживающая неизбирательный режим, захватывает весь трафик IPv4 или IPv6 в локальной сети, включая трафик между другими компьютерами в одном сегменте локальной сети.</span><span class="sxs-lookup"><span data-stu-id="669f0-124">On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment.</span></span> <span data-ttu-id="669f0-125">Все захваченные пакеты (IPv4 или IPv6, в зависимости от сокета) будут переданы в необработанный сокет.</span><span class="sxs-lookup"><span data-stu-id="669f0-125">All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket.</span></span> <span data-ttu-id="669f0-126">Этот параметр не будет захватывать другие пакеты (например, пакеты ARP, IPX и NetBEUI) в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="669f0-126">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span> <span data-ttu-id="669f0-127">NetMon использует тот же режим для сетевого интерфейса, но не использует этот параметр для записи трафика.</span><span class="sxs-lookup"><span data-stu-id="669f0-127">Netmon uses the same mode for the network interface, but does not use this option to capture traffic.</span></span> |
| <span data-ttu-id="669f0-128">**РКВАЛЛ \_ соккетлевелонли**</span><span class="sxs-lookup"><span data-stu-id="669f0-128">**RCVALL\_SOCKETLEVELONLY**</span></span> | <span data-ttu-id="669f0-129">Эта функция в настоящее время не реализована, поэтому установка этого параметра не влияет на.</span><span class="sxs-lookup"><span data-stu-id="669f0-129">This feature is not currently implemented, so setting this option does not have any affect.</span></span> |
| <span data-ttu-id="669f0-130">**РКВАЛЛ \_ иплевел**</span><span class="sxs-lookup"><span data-stu-id="669f0-130">**RCVALL\_IPLEVEL**</span></span> | <span data-ttu-id="669f0-131">Включите этот параметр, чтобы сокет IPv4 или IPv6 получал все пакеты на уровне IP-адресов, передаваемых через сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="669f0-131">Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level passing through a network interface.</span></span> <span data-ttu-id="669f0-132">Этот параметр не включает неизбирательный режим на плате сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="669f0-132">This option does not enable promiscuous mode on the network interface card.</span></span> <span data-ttu-id="669f0-133">Этот параметр влияет только на обработку пакетов на уровне IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="669f0-133">This option only affects packet processing at the IP level.</span></span> <span data-ttu-id="669f0-134">Сетевая карта по-прежнему получает только пакеты, направленные на настроенные адрес рассылки и адреса многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="669f0-134">The NIC still receives only packets directed to its configured unicast and multicast addresses.</span></span> <span data-ttu-id="669f0-135">Тем не менее, сокет с включенным параметром будет получать не только пакеты, направленные на определенные IP-адреса, но и все пакеты IPv4 или IPv6, получаемые сетевым адаптером.</span><span class="sxs-lookup"><span data-stu-id="669f0-135">However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.</span></span> <span data-ttu-id="669f0-136">Этот параметр не записывает другие пакеты (например, пакеты ARP, IPX и NetBEUI), полученные через интерфейс.</span><span class="sxs-lookup"><span data-stu-id="669f0-136">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.</span></span> |

### <a name="cbinbuffer"></a><span data-ttu-id="669f0-137">кбинбуффер</span><span class="sxs-lookup"><span data-stu-id="669f0-137">cbInBuffer</span></span>

<span data-ttu-id="669f0-138">Размер входного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="669f0-138">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="669f0-139">Этот параметр должен быть больше или равен размеру значения перечисления **RCVALL_VALUE** , на которое указывает параметр *лпвинбуффер* .</span><span class="sxs-lookup"><span data-stu-id="669f0-139">This parameter should be equal to or greater than the size of the **RCVALL_VALUE** enumeration value pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="669f0-140">лпваутбуффер</span><span class="sxs-lookup"><span data-stu-id="669f0-140">lpvOutBuffer</span></span>

<span data-ttu-id="669f0-141">Указатель на выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="669f0-141">A pointer to the output buffer.</span></span>
<span data-ttu-id="669f0-142">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="669f0-142">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="669f0-143">кбаутбуффер</span><span class="sxs-lookup"><span data-stu-id="669f0-143">cbOutBuffer</span></span>

<span data-ttu-id="669f0-144">Размер выходного буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="669f0-144">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="669f0-145">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="669f0-145">This parameter is unused for this operation.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="669f0-146">лпкббитесретурнед</span><span class="sxs-lookup"><span data-stu-id="669f0-146">lpcbBytesReturned</span></span>

<span data-ttu-id="669f0-147">Указатель на переменную, которая получает размер данных, хранящихся в выходном буфере, в байтах.</span><span class="sxs-lookup"><span data-stu-id="669f0-147">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="669f0-148">Этот параметр не используется для этой операции.</span><span class="sxs-lookup"><span data-stu-id="669f0-148">This parameter is unused for this operation.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="669f0-149">лпвоверлаппед</span><span class="sxs-lookup"><span data-stu-id="669f0-149">lpvOverlapped</span></span>

<span data-ttu-id="669f0-150">Указатель на структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="669f0-150">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="669f0-151">Если *сокеты были созданы* без атрибута OVERLAPPED, параметр *лповерлаппед* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="669f0-151">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="669f0-152">Если *конструктор* был открыт с атрибутом OVERLAPPED и параметр *Лповерлаппед* не равен **null**, операция выполняется как перекрытый (асинхронная) операция.</span><span class="sxs-lookup"><span data-stu-id="669f0-152">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="669f0-153">В этом случае параметр *лповерлаппед* должен указывать на допустимую структуру [**всаоверлаппед**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="669f0-153">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="669f0-154">Для операций с перекрытием функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает значение немедленно, и соответствующий метод завершения получает сигнал о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="669f0-154">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="669f0-155">В противном случае функция не возвращает значение до тех пор, пока операция не будет завершена или произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="669f0-155">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="669f0-156">лпкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="669f0-156">lpCompletionRoutine</span></span>

<span data-ttu-id="669f0-157">Тип: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="669f0-157">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="669f0-158">Указатель на подпрограммы завершения, вызываемую при завершении операции (игнорируется для сокетов без перекрытия).</span><span class="sxs-lookup"><span data-stu-id="669f0-158">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="669f0-159">лпсреадид</span><span class="sxs-lookup"><span data-stu-id="669f0-159">lpThreadId</span></span>

<span data-ttu-id="669f0-160">Указатель на структуру [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) , которая будет использоваться поставщиком при последующем вызове [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="669f0-160">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="669f0-161">Поставщик должен хранить указанную [**всасреадид**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) структуру (а не указатель на то же значение) до тех пор, пока функция [**впукуеуеапк**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="669f0-161">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="669f0-162">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="669f0-162">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="669f0-163">лперрно</span><span class="sxs-lookup"><span data-stu-id="669f0-163">lpErrno</span></span>

<span data-ttu-id="669f0-164">Указатель на код ошибки.</span><span class="sxs-lookup"><span data-stu-id="669f0-164">A pointer to the error code.</span></span>

<span data-ttu-id="669f0-165">**Примечание**  .  Этот параметр применяется только к функции **вспиоктл** .</span><span class="sxs-lookup"><span data-stu-id="669f0-165">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="669f0-166">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="669f0-166">Return value</span></span>

<span data-ttu-id="669f0-167">Если операция завершается успешно, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="669f0-167">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="669f0-168">Если операция завершается ошибкой или находится в состоянии ожидания, функция [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **Вспиоктл** возвращает **\_ ошибку сокета**.</span><span class="sxs-lookup"><span data-stu-id="669f0-168">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="669f0-169">Чтобы получить расширенные сведения об ошибке, вызовите [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="669f0-169">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="669f0-170">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="669f0-170">Error code</span></span> | <span data-ttu-id="669f0-171">Значение</span><span class="sxs-lookup"><span data-stu-id="669f0-171">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="669f0-172">**\_ожидается ввод-вывод WSA \_**</span><span class="sxs-lookup"><span data-stu-id="669f0-172">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="669f0-173">Операция перекрытия успешно инициирована, и ее завершение будет указано позже.</span><span class="sxs-lookup"><span data-stu-id="669f0-173">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="669f0-174">**\_Операция WSA \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="669f0-174">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="669f0-175">Операция перекрытия была отменена из-за замыкания сокета или выполнения команды ioctl **SIO_FLUSH** .</span><span class="sxs-lookup"><span data-stu-id="669f0-175">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="669f0-176">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="669f0-176">**WSAEFAULT**</span></span> | <span data-ttu-id="669f0-177">Параметр *лповерлаппед* или *лпкомплетионраутине* не полностью содержится в допустимой части адресного пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="669f0-177">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="669f0-178">**всаеинпрогресс**</span><span class="sxs-lookup"><span data-stu-id="669f0-178">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="669f0-179">Функция вызывается при выполнении обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="669f0-179">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="669f0-180">**всаеинтр**</span><span class="sxs-lookup"><span data-stu-id="669f0-180">**WSAEINTR**</span></span> | <span data-ttu-id="669f0-181">Операция блокирования была прервана.</span><span class="sxs-lookup"><span data-stu-id="669f0-181">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="669f0-182">**всаеинвал**</span><span class="sxs-lookup"><span data-stu-id="669f0-182">**WSAEINVAL**</span></span> | <span data-ttu-id="669f0-183">Параметр *двиоконтролкоде* не является допустимой командой, или указан недопустимый входной параметр, либо команда неприменима к указанному типу сокета.</span><span class="sxs-lookup"><span data-stu-id="669f0-183">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="669f0-184">Эта ошибка также возвращается, если параметр *кбинбуффер* меньше, чем `sizeof(UCHAR)` параметр *лпвинбуффер* или указывает на значение, которое не является значением перечисления **RCVALL_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="669f0-184">This error is also returned if the *cbInBuffer* parameter is less than the `sizeof(UCHAR)` or the *lpvInBuffer* parameter points to value that is not a **RCVALL_VALUE** enumeration value.</span></span> <span data-ttu-id="669f0-185">Эта ошибка также может возвращаться, если не удается найти сетевой интерфейс, связанный с сокетом.</span><span class="sxs-lookup"><span data-stu-id="669f0-185">This error can also be returned if the network interface associated with the socket cannot be found.</span></span> <span data-ttu-id="669f0-186">Это может произойти, если сетевой интерфейс, связанный с сокетом, удаляется или удаляется (например, удаляется сетевое устройство PCMCIA или USB).</span><span class="sxs-lookup"><span data-stu-id="669f0-186">This could occur if the network interface associated with the socket is deleted or removed (a remove PCMCIA or USB network device, for example).</span></span> |
| <span data-ttu-id="669f0-187">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="669f0-187">**WSAENETDOWN**</span></span> | <span data-ttu-id="669f0-188">Сбой сетевой подсистемы.</span><span class="sxs-lookup"><span data-stu-id="669f0-188">The network subsystem has failed.</span></span> |
| <span data-ttu-id="669f0-189">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="669f0-189">**WSAENOBUFS**</span></span> | <span data-ttu-id="669f0-190">Нет доступного места в буфере.</span><span class="sxs-lookup"><span data-stu-id="669f0-190">No buffer space available.</span></span> |
| <span data-ttu-id="669f0-191">**всаенопротупт**</span><span class="sxs-lookup"><span data-stu-id="669f0-191">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="669f0-192">Параметр сокета не поддерживается для указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="669f0-192">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="669f0-193">**всаенотсокк**</span><span class="sxs-lookup"><span data-stu-id="669f0-193">**WSAENOTSOCK**</span></span> | <span data-ttu-id="669f0-194">Дескриптор *s* не является сокетом.</span><span class="sxs-lookup"><span data-stu-id="669f0-194">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="669f0-195">**всаеопнотсупп**</span><span class="sxs-lookup"><span data-stu-id="669f0-195">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="669f0-196">Указанная команда IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="669f0-196">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="669f0-197">Эта ошибка возвращается, если поставщик транспорта не поддерживает **SIO \_ рквалл** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="669f0-197">This error is returned if the **SIO\_RCVALL** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="669f0-198">Комментарии</span><span class="sxs-lookup"><span data-stu-id="669f0-198">Remarks</span></span>

<span data-ttu-id="669f0-199">В Windows 2000 и более поздних версиях операционной системы поддерживается **SIO \_ рквалл** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="669f0-199">The **SIO\_RCVALL** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="669f0-200">**SIO \_ рквалл** ioctl позволяет сокету принимать все пакеты IPv4 или IPv6 в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="669f0-200">The **SIO\_RCVALL** IOCTL enables a socket to receive all IPv4 or IPv6 packets on a network interface.</span></span>
<span data-ttu-id="669f0-201">Маркер сокета, передаваемый функции [**всаиоктл**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) или **вспиоктл** , должен быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="669f0-201">The socket handle passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function must be one of the following:</span></span>

* <span data-ttu-id="669f0-202">Сокет IPv4, созданный с семейством адресов, равным AF_INET, тип сокета, установленный в SOCK_RAW, и протокол, для которого задано значение IPPROTO_IP.</span><span class="sxs-lookup"><span data-stu-id="669f0-202">An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.</span></span>
* <span data-ttu-id="669f0-203">Сокет IPv6, созданный с семейством адресов, равным AF_INET6, тип сокета, установленный в SOCK_RAW, и протокол, для которого задано значение IPPROTO_IPV6.</span><span class="sxs-lookup"><span data-stu-id="669f0-203">An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.</span></span>

<span data-ttu-id="669f0-204">Дополнительные сведения об необработанных сокетах см. в разделе [**необработанные сокеты TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span><span class="sxs-lookup"><span data-stu-id="669f0-204">For more information on raw sockets, see [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span></span>

<span data-ttu-id="669f0-205">Сокет также должен быть привязан к явному локальному интерфейсу IPv4 или IPv6, что означает, что вы не можете выполнить привязку к **адресу \_** или **in6addr \_ любому** из них.</span><span class="sxs-lookup"><span data-stu-id="669f0-205">The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR\_ANY** or **in6addr\_any**.</span></span>

<span data-ttu-id="669f0-206">После привязки сокета и успешного завершения функции IOCTL вызовы функций [**всарекв**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) или [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) возвращают IPv4-датаграммы, проходящие через данный интерфейс IPv4, или возвращают IPv6 датаграмм, передаваемых через данный интерфейс IPv6.</span><span class="sxs-lookup"><span data-stu-id="669f0-206">Once the socket is bound and the IOCTL completes successfully, calls to the [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) or [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions return IPv4 datagrams passing through the given IPv4 interface or return IPv6 datagrams passing through the given IPv6 interface.</span></span>
<span data-ttu-id="669f0-207">Обратите внимание, что необходимо указать достаточно большой буфер.</span><span class="sxs-lookup"><span data-stu-id="669f0-207">Note that you must supply a sufficiently large buffer.</span></span>
<span data-ttu-id="669f0-208">При настройке этого IOCTL будут записываться только пакеты IPv4 или IPv6 для заданного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="669f0-208">Setting this IOCTL will only capture IPv4 or IPv6 packets on a given interface.</span></span>
<span data-ttu-id="669f0-209">Этот запрос IOCTL не будет захватывать другие пакеты (например, пакеты ARP, IPX и NetBEUI) в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="669f0-209">This IOCTL will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span>

<span data-ttu-id="669f0-210">Сокет, привязанный к определенному локальному интерфейсу с помощью ioctl **\_ рквалл** , будет принимать только пакеты, передаваемые через этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="669f0-210">A socket bound to a specific local interface with the **SIO\_RCVALL** IOCTL will receive only packets passing through that interface.</span></span>
<span data-ttu-id="669f0-211">Он не будет получать пакеты, полученные на другом интерфейсе, и пересылаться в другом интерфейсе, отличном от сокета с подключением **SIO \_ рквалл** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="669f0-211">It will not receive packets received on another interface and getting forwarded out on another interface different from the socket bound with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="669f0-212">В Windows Server 2008 и более ранних версиях параметр **\_ Рквалл ioctl SIO** не будет записывать локальные пакеты, отправленные из сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="669f0-212">On Windows Server 2008 and earlier, the **SIO\_RCVALL** IOCTL setting would not capture local packets sent out of a network interface.</span></span>
<span data-ttu-id="669f0-213">Это включает пакеты, полученные на другом интерфейсе, и перенаправляли сетевой интерфейс, указанный для **SIO \_ рквалл** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="669f0-213">This included packets received on another interface and forwarded out the network interface specified for the **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="669f0-214">В Windows 7 и Windows Server 2008 R2 это было изменено, так что также фиксируются локальные пакеты, отправленные из сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="669f0-214">On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured.</span></span>
<span data-ttu-id="669f0-215">Это относится к пакетам, полученным в другом интерфейсе, и последующем пересылке сетевого интерфейса, привязанного к сокету, с помощью интерфейса **SIO \_ рквалл** IOCTL.</span><span class="sxs-lookup"><span data-stu-id="669f0-215">This includes packets received on another interface and then forwarded out the network interface bound to the socket with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="669f0-216">Для установки этого IOCTL требуются права администратора на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="669f0-216">Setting this IOCTL requires Administrator privilege on the local computer.</span></span>

<span data-ttu-id="669f0-217">Эта функция иногда называется неизбирательным режимом.</span><span class="sxs-lookup"><span data-stu-id="669f0-217">This feature is sometimes referred to as promiscuous mode.</span></span>
<span data-ttu-id="669f0-218">Любое прямое изменение от применения этого параметра к одному интерфейсу, а затем к другому интерфейсу с одним вызовом с помощью этого IOCTL не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="669f0-218">Any direct change from applying this option on one interface and then to another interface with a single call using this IOCTL is not supported.</span></span>
<span data-ttu-id="669f0-219">Приложение должно сначала использовать этот запрос IOCTL, чтобы отключить поведение первого интерфейса, а затем использовать этот запрос IOCTL для включения поведения в новом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="669f0-219">An application must first use this IOCTL to turn off the behavior on the first interface, and then use this IOCTL to enable the behavior on a new interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="669f0-220">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="669f0-220">See also</span></span>

[<span data-ttu-id="669f0-221">**фиксатор**</span><span class="sxs-lookup"><span data-stu-id="669f0-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="669f0-222">**Необработанные сокеты TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="669f0-222">**TCP/IP Raw Sockets**</span></span>](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[<span data-ttu-id="669f0-223">**всажетластеррор**</span><span class="sxs-lookup"><span data-stu-id="669f0-223">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="669f0-224">**всажетоверлаппедресулт**</span><span class="sxs-lookup"><span data-stu-id="669f0-224">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="669f0-225">**всаиоктл**</span><span class="sxs-lookup"><span data-stu-id="669f0-225">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="669f0-226">**всаоверлаппед**</span><span class="sxs-lookup"><span data-stu-id="669f0-226">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="669f0-227">**всасоккета**</span><span class="sxs-lookup"><span data-stu-id="669f0-227">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="669f0-228">**всасоккетв**</span><span class="sxs-lookup"><span data-stu-id="669f0-228">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
