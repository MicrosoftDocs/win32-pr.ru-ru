---
description: Указывает зарегистрированный дескриптор буфера, используемый с зарегистрированными расширениями ввода-вывода Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Мсвсоккдеф. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080539"
---
# <a name="rio_bufferid"></a><span data-ttu-id="cca8c-103">Рио \_ BUFFERID</span><span class="sxs-lookup"><span data-stu-id="cca8c-103">RIO\_BUFFERID</span></span>

<span data-ttu-id="cca8c-104">**Рио \_ BUFFERID** typedef указывает зарегистрированный дескриптор буфера, используемый с зарегистрированными расширениями ввода-вывода Winsock.</span><span class="sxs-lookup"><span data-stu-id="cca8c-104">The **RIO\_BUFFERID** typedef specifies a registered buffer descriptor used with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

<span data-ttu-id="cca8c-105">**Рио \_ BUFFERID**</span><span class="sxs-lookup"><span data-stu-id="cca8c-105">**RIO\_BUFFERID**</span></span>
</dt> <dd>

<span data-ttu-id="cca8c-106">Тип данных, указывающий зарегистрированный дескриптор буфера, используемый для запросов send и Receive.</span><span class="sxs-lookup"><span data-stu-id="cca8c-106">A data type that specifies a registered buffer descriptor used with send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cca8c-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cca8c-107">Remarks</span></span>

<span data-ttu-id="cca8c-108">Зарегистрированные расширения ввода-вывода Winsock работают главным образом с зарегистрированными буферами с помощью объектов **Рио \_ BUFFERID** .</span><span class="sxs-lookup"><span data-stu-id="cca8c-108">The Winsock registered I/O extensions operate primarily on registered buffers using **RIO\_BUFFERID** objects.</span></span> <span data-ttu-id="cca8c-109">Приложение получает **Рио \_ BUFFERID** для существующего буфера с помощью функции [**риорегистербуффер**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cca8c-109">An application obtains a **RIO\_BUFFERID** for an existing buffer using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function.</span></span> <span data-ttu-id="cca8c-110">Приложение может освободить регистрацию с помощью функции [**риодерегистербуффер**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .</span><span class="sxs-lookup"><span data-stu-id="cca8c-110">An application can release a registration using the [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function.</span></span>

<span data-ttu-id="cca8c-111">Когда существующий буфер регистрируется в качестве объекта **Рио \_ BUFFERID** с помощью функции [**риорегистербуффер**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , определенные внутренние ресурсы выделяются из физической памяти, а существующий буфер приложения блокируется в физической памяти.</span><span class="sxs-lookup"><span data-stu-id="cca8c-111">When an existing buffer is registered as a **RIO\_BUFFERID** object using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function, certain internal resources are allocated from physical memory, and the existing application buffer will be locked into physical memory.</span></span> <span data-ttu-id="cca8c-112">Функция [**риодерегистербуффер**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) вызывается для отмены регистрации буфера, освобождения этих внутренних ресурсов и позволяет разблокировать буфер и освободить его из физической памяти.</span><span class="sxs-lookup"><span data-stu-id="cca8c-112">The [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function is called to deregister the buffer, free these internal resources, and allow the buffer to be unlocked and released from physical memory.</span></span>

<span data-ttu-id="cca8c-113">Повторная регистрация и Отмена регистрации буферов приложений с помощью зарегистрированных расширений ввода-вывода Winsock могут привести к значительному снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="cca8c-113">Repeated registration and deregistration of application buffers using the Winsock registered I/O extensions may cause significant performance degradation.</span></span> <span data-ttu-id="cca8c-114">При проектировании приложения, использующего зарегистрированные расширения ввода-вывода Winsock, необходимо учитывать следующие подходы к управлению буферами для снижения числа повторных регистраций и отмены регистрации буферов приложений:</span><span class="sxs-lookup"><span data-stu-id="cca8c-114">The following buffer management approaches should be considered when designing an application using the Winsock registered I/O extensions to minimize repeated registration and deregistration of application buffers:</span></span>

-   <span data-ttu-id="cca8c-115">• Максимальное повторное использование буферов.</span><span class="sxs-lookup"><span data-stu-id="cca8c-115">• Maximize the reuse of buffers.</span></span>
-   <span data-ttu-id="cca8c-116">• Поддержание ограниченного пула неиспользуемых зарегистрированных буферов для использования приложением.</span><span class="sxs-lookup"><span data-stu-id="cca8c-116">• Maintain a limited pool of unused registered buffers for use by the application.</span></span>
-   <span data-ttu-id="cca8c-117">• Поддержание ограниченного пула зарегистрированных буферов и выполнение буферных копий между этими зарегистрированными буферами и другими незарегистрированными буферами.</span><span class="sxs-lookup"><span data-stu-id="cca8c-117">• Maintain a limited pool of registered buffers and perform buffer copies between these registered buffers and other unregistered buffers.</span></span>

<span data-ttu-id="cca8c-118">**Рио \_ BUFFERID** typedef определяется в файле заголовка *мсвсоккдеф. h* , который автоматически включается в заголовочный файл *мсвсокк. h* .</span><span class="sxs-lookup"><span data-stu-id="cca8c-118">The **RIO\_BUFFERID** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="cca8c-119">Файл заголовка *мсвсоккдеф. h* никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="cca8c-119">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="cca8c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cca8c-120">Requirements</span></span>



| <span data-ttu-id="cca8c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cca8c-121">Requirement</span></span> | <span data-ttu-id="cca8c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cca8c-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca8c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cca8c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cca8c-124">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cca8c-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="cca8c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cca8c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cca8c-126">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cca8c-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="cca8c-127">Header</span><span class="sxs-lookup"><span data-stu-id="cca8c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cca8c-128"><dt>Мсвсоккдеф. h (включение Мсвсокк. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cca8c-128"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca8c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cca8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca8c-130">**Рио \_ buf**</span><span class="sxs-lookup"><span data-stu-id="cca8c-130">**RIO\_BUF**</span></span>](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[<span data-ttu-id="cca8c-131">**риодерегистербуффер**</span><span class="sxs-lookup"><span data-stu-id="cca8c-131">**RIODeregisterBuffer**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[<span data-ttu-id="cca8c-132">**риорецеиве**</span><span class="sxs-lookup"><span data-stu-id="cca8c-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="cca8c-133">**риорецеивикс**</span><span class="sxs-lookup"><span data-stu-id="cca8c-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="cca8c-134">[**риорегистербуффер**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cca8c-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cca8c-135">**риосенд**</span><span class="sxs-lookup"><span data-stu-id="cca8c-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="cca8c-136">[**риосендекс**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cca8c-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> </dl>

 

 
