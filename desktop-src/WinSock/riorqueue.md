---
description: Указывает дескриптор сокета, используемый запросами Send и Receive с зарегистрированными расширениями ввода-вывода Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Мсвсоккдеф. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344742"
---
# <a name="rio_rq"></a><span data-ttu-id="f1260-103">Рио \_ РК</span><span class="sxs-lookup"><span data-stu-id="f1260-103">RIO\_RQ</span></span>

<span data-ttu-id="f1260-104">**Рио \_ РК** typedef указывает дескриптор сокета, используемый запросами Send и Receive с зарегистрированными расширениями ввода-вывода Winsock.</span><span class="sxs-lookup"><span data-stu-id="f1260-104">The **RIO\_RQ** typedef specifies a socket descriptor used by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

<span data-ttu-id="f1260-105">**Рио \_ РК**</span><span class="sxs-lookup"><span data-stu-id="f1260-105">**RIO\_RQ**</span></span>
</dt> <dd>

<span data-ttu-id="f1260-106">Тип данных, указывающий дескриптор сокета, используемый для запросов send и Receive.</span><span class="sxs-lookup"><span data-stu-id="f1260-106">A data type that specifies a socket descriptor used by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1260-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1260-107">Remarks</span></span>

<span data-ttu-id="f1260-108">Зарегистрированные расширения ввода-вывода Winsock работают главным образом с объектом **Рио \_ РК** , а не с сокетом.</span><span class="sxs-lookup"><span data-stu-id="f1260-108">The Winsock registered I/O extensions operate primarily on a **RIO\_RQ** object rather than a socket.</span></span> <span data-ttu-id="f1260-109">Приложение получает **Рио \_ РК** для существующего сокета с помощью функции [**риокреатерекуесткуеуе**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) .</span><span class="sxs-lookup"><span data-stu-id="f1260-109">An application obtains a **RIO\_RQ** for an existing socket using the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function.</span></span> <span data-ttu-id="f1260-110">Входной сокет должен быть создан путем вызова функции [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) с флагом **WSA \_ \_ Рио** , установленным в параметре *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="f1260-110">The input socket must have been created by calling the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function with the **WSA\_FLAG\_RIO** flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="f1260-111">После получения объекта **\_ РК Рио** базовый дескриптор сокета остается действительным.</span><span class="sxs-lookup"><span data-stu-id="f1260-111">After obtaining a **RIO\_RQ** object, the underlying socket descriptor remains valid.</span></span> <span data-ttu-id="f1260-112">Приложение может продолжать использовать базовый сокет для установки и запроса параметров сокета, выдавать запросы IOCTL и в конечном итоге закрывать сокет.</span><span class="sxs-lookup"><span data-stu-id="f1260-112">An application may continue to use the underlying socket to set and query socket options, issue IOCTLs and ultimately close the socket.</span></span>

> [!Note]  
> <span data-ttu-id="f1260-113">В целях повышения эффективности доступ к очередям завершения (структурам [**Рио \_ КК**](riocqueue.md) ) и очередям запросов (**Рио \_ РК** структуры) не защищается примитивами синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f1260-113">For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues (**RIO\_RQ** structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="f1260-114">Если необходимо получить доступ к очереди завершения или запросов из нескольких потоков, доступ должен координироваться критическим разделом, упрощенной блокировкой записи чтения или аналогичным механизмом.</span><span class="sxs-lookup"><span data-stu-id="f1260-114">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="f1260-115">Эта блокировка не требуется для доступа в одном потоке.</span><span class="sxs-lookup"><span data-stu-id="f1260-115">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="f1260-116">Различные потоки могут обращаться к отдельным запросам или очередям завершения без блокировок.</span><span class="sxs-lookup"><span data-stu-id="f1260-116">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="f1260-117">Необходимость в синхронизации происходит только в том случае, если несколько потоков пытаются получить доступ к одной и той же очереди.</span><span class="sxs-lookup"><span data-stu-id="f1260-117">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="f1260-118">Синхронизация также необходима, если несколько потоков отправляют и получают на одном сокете, так как операции отправки и получения используют очередь запросов сокета.</span><span class="sxs-lookup"><span data-stu-id="f1260-118">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="f1260-119">[**Рио \_ РК**](riocqueue.md) typedef определяется в файле заголовка *мсвсоккдеф. h* , который автоматически включается в заголовочный файл *мсвсокк. h* .</span><span class="sxs-lookup"><span data-stu-id="f1260-119">The [**RIO\_RQ**](riocqueue.md) typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="f1260-120">Файл заголовка *мсвсоккдеф. h* никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="f1260-120">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1260-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f1260-121">Requirements</span></span>



| <span data-ttu-id="f1260-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f1260-122">Requirement</span></span> | <span data-ttu-id="f1260-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f1260-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1260-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1260-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f1260-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f1260-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="f1260-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1260-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f1260-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f1260-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="f1260-128">Header</span><span class="sxs-lookup"><span data-stu-id="f1260-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1260-129"><dt>Мсвсоккдеф. h (включение Мсвсокк. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1260-129"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1260-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1260-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1260-131">**риокреатерекуесткуеуе**</span><span class="sxs-lookup"><span data-stu-id="f1260-131">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="f1260-132">**риорецеиве**</span><span class="sxs-lookup"><span data-stu-id="f1260-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="f1260-133">**риорецеивикс**</span><span class="sxs-lookup"><span data-stu-id="f1260-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="f1260-134">[**риоресизерекуесткуеуе**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1260-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f1260-135">**риосенд**</span><span class="sxs-lookup"><span data-stu-id="f1260-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="f1260-136">[**риосендекс**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1260-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f1260-137">**всасоккет**</span><span class="sxs-lookup"><span data-stu-id="f1260-137">**WSASocket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
