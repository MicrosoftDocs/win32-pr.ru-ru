---
description: Создает порт завершения ввода-вывода и связывает его с заданным маркером файла или создает порт завершения ввода-вывода, который еще не связан с маркером файла, что позволяет выполнить сопоставление позже.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Функция CreateIoCompletionPort (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683561"
---
# <a name="createiocompletionport-function"></a><span data-ttu-id="9933d-103">Функция CreateIoCompletionPort</span><span class="sxs-lookup"><span data-stu-id="9933d-103">CreateIoCompletionPort function</span></span>

<span data-ttu-id="9933d-104">Создает порт завершения ввода-вывода и связывает его с заданным маркером файла или создает порт завершения ввода-вывода, который еще не связан с маркером файла, что позволяет выполнить сопоставление позже.</span><span class="sxs-lookup"><span data-stu-id="9933d-104">Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.</span></span>

<span data-ttu-id="9933d-105">Связывание экземпляра открытого файла с портом завершения ввода-вывода позволяет процессу получить уведомление о завершении асинхронных операций ввода-вывода с использованием этого маркера файла.</span><span class="sxs-lookup"><span data-stu-id="9933d-105">Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.</span></span>

> [!Note]
>
> <span data-ttu-id="9933d-106">Термин используемый здесь *описатель файла* означает абстракцию системы, представляющую перекрывающиеся конечные точки ввода-вывода, а не только файл на диске.</span><span class="sxs-lookup"><span data-stu-id="9933d-106">The term *file handle* as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk.</span></span> <span data-ttu-id="9933d-107">В качестве дескрипторов файлов можно использовать любые системные объекты, поддерживающие перекрывающиеся операции ввода-вывода, такие как конечные точки сети, TCP-сокеты, именованные каналы и слоты почты.</span><span class="sxs-lookup"><span data-stu-id="9933d-107">Any system objects that support overlapped I/O such as network endpoints, TCP sockets, named pipes, and mail slots can be used as file handles.</span></span> <span data-ttu-id="9933d-108">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="9933d-108">For additional information, see the Remarks section.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9933d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9933d-109">Syntax</span></span>


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a><span data-ttu-id="9933d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9933d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9933d-111">*FileHandle* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9933d-111">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9933d-112">Открытый маркер файла или **недопустимое \_ \_ значение Handle**.</span><span class="sxs-lookup"><span data-stu-id="9933d-112">An open file handle or **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="9933d-113">Этот обработчик должен быть объектом, поддерживающим перекрывающиеся операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-113">The handle must be to an object that supports overlapped I/O.</span></span>

<span data-ttu-id="9933d-114">Если указан маркер, он должен быть открыт для завершения ввода-вывода с перекрытием.</span><span class="sxs-lookup"><span data-stu-id="9933d-114">If a handle is provided, it has to have been opened for overlapped I/O completion.</span></span> <span data-ttu-id="9933d-115">Например, при использовании функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) для получения маркера необходимо указать флаг **\_ \_ OVERLAPPED для флага File** .</span><span class="sxs-lookup"><span data-stu-id="9933d-115">For example, you must specify the **FILE\_FLAG\_OVERLAPPED** flag when using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function to obtain the handle.</span></span>

<span data-ttu-id="9933d-116">Если указано **недопустимое \_ \_ значение Handle** , функция создает порт завершения ввода-вывода, не связывая его с маркером файла.</span><span class="sxs-lookup"><span data-stu-id="9933d-116">If **INVALID\_HANDLE\_VALUE** is specified, the function creates an I/O completion port without associating it with a file handle.</span></span> <span data-ttu-id="9933d-117">В этом случае параметр *ексистингкомплетионпорт* должен иметь **значение NULL** , а параметр *комплетионкэй* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="9933d-117">In this case, the *ExistingCompletionPort* parameter must be **NULL** and the *CompletionKey* parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="9933d-118">*Ексистингкомплетионпорт* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9933d-118">*ExistingCompletionPort* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9933d-119">Указатель на существующий порт завершения ввода-вывода или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9933d-119">A handle to an existing I/O completion port or **NULL**.</span></span>

<span data-ttu-id="9933d-120">Если этот параметр указывает существующий порт завершения ввода-вывода, функция связывает его с маркером, указанным параметром *FileHandle* .</span><span class="sxs-lookup"><span data-stu-id="9933d-120">If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the *FileHandle* parameter.</span></span> <span data-ttu-id="9933d-121">При успешном выполнении функция возвращает маркер существующего порта завершения ввода-вывода. Он не создает новый порт завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-121">The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.</span></span>

<span data-ttu-id="9933d-122">Если этот параметр имеет **значение NULL**, функция создает новый порт завершения ввода-вывода и, если параметр *FileHandle* является допустимым, связывает его с новым портом завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-122">If this parameter is **NULL**, the function creates a new I/O completion port and, if the *FileHandle* parameter is valid, associates it with the new I/O completion port.</span></span> <span data-ttu-id="9933d-123">В противном случае связь с обработчиком файлов не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9933d-123">Otherwise no file handle association occurs.</span></span> <span data-ttu-id="9933d-124">При успешном выполнении функция возвращает маркер в новый порт завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-124">The function returns the handle to the new I/O completion port if successful.</span></span>

</dd> <dt>

<span data-ttu-id="9933d-125">*Комплетионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9933d-125">*CompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9933d-126">Определяемый пользователем ключ завершения для каждого обработчика, включенный в каждый пакет завершения ввода-вывода для указанного маркера файла.</span><span class="sxs-lookup"><span data-stu-id="9933d-126">The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle.</span></span> <span data-ttu-id="9933d-127">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="9933d-127">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="9933d-128">*Нумберофконкуррентсреадс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9933d-128">*NumberOfConcurrentThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9933d-129">Максимальное число потоков, которые операционная система может разрешить одновременно обрабатывать пакеты завершения ввода-вывода для порта завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-129">The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port.</span></span> <span data-ttu-id="9933d-130">Этот параметр не учитывается, если параметр *ексистингкомплетионпорт* имеет **значение**, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="9933d-130">This parameter is ignored if the *ExistingCompletionPort* parameter is not **NULL**.</span></span>

<span data-ttu-id="9933d-131">Если этот параметр равен нулю, система разрешает столько параллельно выполняющихся потоков, сколько процессоров в системе.</span><span class="sxs-lookup"><span data-stu-id="9933d-131">If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9933d-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9933d-132">Return value</span></span>

<span data-ttu-id="9933d-133">Если функция выполнена успешно, возвращаемое значение является маркером для порта завершения ввода-вывода:</span><span class="sxs-lookup"><span data-stu-id="9933d-133">If the function succeeds, the return value is the handle to an I/O completion port:</span></span>

-   <span data-ttu-id="9933d-134">Если параметр *ексистингкомплетионпорт* имеет **значение NULL**, возвращаемое значение является новым маркером.</span><span class="sxs-lookup"><span data-stu-id="9933d-134">If the *ExistingCompletionPort* parameter was **NULL**, the return value is a new handle.</span></span>

-   <span data-ttu-id="9933d-135">Если параметр *ексистингкомплетионпорт* был допустимым маркером порта завершения ввода-вывода, возвращаемое значение имеет тот же маркер.</span><span class="sxs-lookup"><span data-stu-id="9933d-135">If the *ExistingCompletionPort* parameter was a valid I/O completion port handle, the return value is that same handle.</span></span>

-   <span data-ttu-id="9933d-136">Если параметр *FileHandle* является допустимым маркером, этот маркер файла теперь связан с возвращенным портом завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-136">If the *FileHandle* parameter was a valid handle, that file handle is now associated with the returned I/O completion port.</span></span>

<span data-ttu-id="9933d-137">Если функция завершается ошибкой, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="9933d-137">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="9933d-138">Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="9933d-138">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9933d-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9933d-139">Remarks</span></span>

<span data-ttu-id="9933d-140">Система ввода-вывода может дать инструкции отправить пакеты уведомлений о завершении ввода-вывода в порты завершения ввода-вывода, где они помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="9933d-140">The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued.</span></span> <span data-ttu-id="9933d-141">Функция **CreateIoCompletionPort** предоставляет эту функцию.</span><span class="sxs-lookup"><span data-stu-id="9933d-141">The **CreateIoCompletionPort** function provides this functionality.</span></span>

<span data-ttu-id="9933d-142">Порт завершения ввода-вывода и его обработчик связаны с процессом, который его создал, и не может совместно работать между процессами.</span><span class="sxs-lookup"><span data-stu-id="9933d-142">An I/O completion port and its handle are associated with the process that created it and is not sharable between processes.</span></span> <span data-ttu-id="9933d-143">Однако один и тот же обработчик может совместно работать между потоками в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="9933d-143">However, a single handle is sharable between threads in the same process.</span></span>

<span data-ttu-id="9933d-144">**CreateIoCompletionPort** можно использовать в трех различных режимах:</span><span class="sxs-lookup"><span data-stu-id="9933d-144">**CreateIoCompletionPort** can be used in three distinct modes:</span></span>

-   <span data-ttu-id="9933d-145">Создайте только порт завершения ввода-вывода, не связав его с маркером файла.</span><span class="sxs-lookup"><span data-stu-id="9933d-145">Create only an I/O completion port without associating it with a file handle.</span></span>
-   <span data-ttu-id="9933d-146">Свяжите существующий порт завершения ввода-вывода с маркером файла.</span><span class="sxs-lookup"><span data-stu-id="9933d-146">Associate an existing I/O completion port with a file handle.</span></span>
-   <span data-ttu-id="9933d-147">Создание и сопоставление в одном вызове.</span><span class="sxs-lookup"><span data-stu-id="9933d-147">Perform both creation and association in a single call.</span></span>

<span data-ttu-id="9933d-148">Чтобы создать порт завершения ввода-вывода, не связывая его, присвойте параметру *FileHandle* **неверное \_ \_ значение Handle**, параметр *ексистингкомплетионпорт* — **null**, а параметр *комплетионкэй* — нуль (который в данном случае игнорируется).</span><span class="sxs-lookup"><span data-stu-id="9933d-148">To create an I/O completion port without associating it, set the *FileHandle* parameter to **INVALID\_HANDLE\_VALUE**, the *ExistingCompletionPort* parameter to **NULL**, and the *CompletionKey* parameter to zero (which is ignored in this case).</span></span> <span data-ttu-id="9933d-149">Задайте для параметра *нумберофконкуррентсреадс* требуемое значение параллелизма для нового порта завершения ввода-вывода или нуль для значения по умолчанию (число процессоров в системе).</span><span class="sxs-lookup"><span data-stu-id="9933d-149">Set the *NumberOfConcurrentThreads* parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).</span></span>

<span data-ttu-id="9933d-150">В качестве маркера, переданного в параметре *FileHandle* , можно использовать любой обработчик, поддерживающий перекрывающиеся операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-150">The handle passed in the *FileHandle* parameter can be any handle that supports overlapped I/O.</span></span> <span data-ttu-id="9933d-151">Чаще всего это маркер, Открытый функцией [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с помощью флага **File \_ Flag \_ OVERLAPPED** (например, файлы, слоты почты и каналы).</span><span class="sxs-lookup"><span data-stu-id="9933d-151">Most commonly, this is a handle opened by the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function using the **FILE\_FLAG\_OVERLAPPED** flag (for example, files, mail slots, and pipes).</span></span> <span data-ttu-id="9933d-152">Объекты, созданные другими функциями, такими как [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) , также могут быть связаны с портом завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-152">Objects created by other functions such as [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) can also be associated with an I/O completion port.</span></span> <span data-ttu-id="9933d-153">Пример использования сокетов см. в разделе [**акцептекс**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span><span class="sxs-lookup"><span data-stu-id="9933d-153">For an example using sockets, see [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span></span> <span data-ttu-id="9933d-154">Маркер может быть связан только с одним портом завершения ввода-вывода, и после создания связи этот обработчик остается связанным с этим портом завершения ввода-вывода, пока он не будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="9933d-154">A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.</span></span>

<span data-ttu-id="9933d-155">Дополнительные сведения о теории портов завершения ввода-вывода, использовании и связанных функциях см. в разделе [порты завершения ввода-вывода](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="9933d-155">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="9933d-156">Несколько дескрипторов файлов можно связать с одним портом завершения ввода-вывода, вызвав **CreateIoCompletionPort** несколько раз с одним и тем же дескриптором порта завершения ввода-вывода в параметре *ексистингкомплетионпорт* и при каждом другом дескрипторе файла в параметре *FileHandle* .</span><span class="sxs-lookup"><span data-stu-id="9933d-156">Multiple file handles can be associated with a single I/O completion port by calling **CreateIoCompletionPort** multiple times with the same I/O completion port handle in the *ExistingCompletionPort* parameter and a different file handle in the *FileHandle* parameter each time.</span></span>

<span data-ttu-id="9933d-157">Используйте параметр *комплетионкэй* , чтобы помочь приложению определить, какие операции ввода-вывода завершены.</span><span class="sxs-lookup"><span data-stu-id="9933d-157">Use the *CompletionKey* parameter to help your application track which I/O operations have completed.</span></span> <span data-ttu-id="9933d-158">Это значение не используется **CreateIoCompletionPort** для функционального управления; Вместо этого он прикрепляется к файлу, указанному в параметре *FileHandle* во время связи с портом завершения ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-158">This value is not used by **CreateIoCompletionPort** for functional control; rather, it is attached to the file handle specified in the *FileHandle* parameter at the time of association with an I/O completion port.</span></span> <span data-ttu-id="9933d-159">Этот ключ завершения должен быть уникальным для каждого файла, и он прилагается к обработчику файлов во время внутреннего процесса очереди завершения.</span><span class="sxs-lookup"><span data-stu-id="9933d-159">This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process.</span></span> <span data-ttu-id="9933d-160">Он возвращается в вызове функции [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) при получении пакета завершения.</span><span class="sxs-lookup"><span data-stu-id="9933d-160">It is returned in the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function call when a completion packet arrives.</span></span> <span data-ttu-id="9933d-161">Параметр *комплетионкэй* также используется функцией [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) для постановки в очередь собственных пакетов завершения специального назначения.</span><span class="sxs-lookup"><span data-stu-id="9933d-161">The *CompletionKey* parameter is also used by the [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) function to queue your own special-purpose completion packets.</span></span>

<span data-ttu-id="9933d-162">После того как экземпляр открытого маркера связан с портом завершения ввода-вывода, он не может использоваться в функции [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) или [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) , поскольку эти функции имеют собственные механизмы асинхронного ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-162">After an instance of an open handle is associated with an I/O completion port, it cannot be used in the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function because these functions have their own asynchronous I/O mechanisms.</span></span>

<span data-ttu-id="9933d-163">Не рекомендуется совместно использовать один и тот же маркер файла, связанный с портом завершения ввода-вывода, с помощью наследования или вызова функции [**дупликатехандле**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="9933d-163">It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="9933d-164">Операции, выполняемые с такими повторяющимися дескрипторами, формируют уведомления о завершении.</span><span class="sxs-lookup"><span data-stu-id="9933d-164">Operations performed with such duplicate handles generate completion notifications.</span></span> <span data-ttu-id="9933d-165">Рекомендуется соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="9933d-165">Careful consideration is advised.</span></span>

<span data-ttu-id="9933d-166">Обработчик порта завершения ввода-вывода и все файлы, связанные с этим конкретным портом завершения ввода-вывода, называются *ссылками на порт завершения ввода*-вывода.</span><span class="sxs-lookup"><span data-stu-id="9933d-166">The I/O completion port handle and every file handle associated with that particular I/O completion port are known as *references to the I/O completion port*.</span></span> <span data-ttu-id="9933d-167">Порт завершения ввода-вывода освобождается при отсутствии ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="9933d-167">The I/O completion port is released when there are no more references to it.</span></span> <span data-ttu-id="9933d-168">Поэтому все эти дескрипторы должны быть должным образом закрыты, чтобы освободить порт завершения ввода-вывода и связанные с ним системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9933d-168">Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources.</span></span> <span data-ttu-id="9933d-169">После выполнения этих условий закройте обработчик порта завершения ввода-вывода, вызвав функцию [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="9933d-169">After these conditions are satisfied, close the I/O completion port handle by calling the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="9933d-170">В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.</span><span class="sxs-lookup"><span data-stu-id="9933d-170">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="9933d-171">Технология</span><span class="sxs-lookup"><span data-stu-id="9933d-171">Technology</span></span>                                           | <span data-ttu-id="9933d-172">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9933d-172">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="9933d-173">Протокол SMB 3,0</span><span class="sxs-lookup"><span data-stu-id="9933d-173">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="9933d-174">Да</span><span class="sxs-lookup"><span data-stu-id="9933d-174">Yes</span></span><br/> |
| <span data-ttu-id="9933d-175">Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)</span><span class="sxs-lookup"><span data-stu-id="9933d-175">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="9933d-176">Да</span><span class="sxs-lookup"><span data-stu-id="9933d-176">Yes</span></span><br/> |
| <span data-ttu-id="9933d-177">SMB 3,0 с масштабируемыми файловыми ресурсами (SO)</span><span class="sxs-lookup"><span data-stu-id="9933d-177">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="9933d-178">Да</span><span class="sxs-lookup"><span data-stu-id="9933d-178">Yes</span></span><br/> |
| <span data-ttu-id="9933d-179">Общий том кластераная файловая система (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="9933d-179">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="9933d-180">Да</span><span class="sxs-lookup"><span data-stu-id="9933d-180">Yes</span></span><br/> |
| <span data-ttu-id="9933d-181">Восстанавливаемая файловая система (ReFS)</span><span class="sxs-lookup"><span data-stu-id="9933d-181">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="9933d-182">Да</span><span class="sxs-lookup"><span data-stu-id="9933d-182">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9933d-183">Требования</span><span class="sxs-lookup"><span data-stu-id="9933d-183">Requirements</span></span>



| <span data-ttu-id="9933d-184">Требование</span><span class="sxs-lookup"><span data-stu-id="9933d-184">Requirement</span></span> | <span data-ttu-id="9933d-185">Значение</span><span class="sxs-lookup"><span data-stu-id="9933d-185">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9933d-186">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9933d-186">Minimum supported client</span></span><br/> | <span data-ttu-id="9933d-187">\[Приложения UWP для классических приложений Windows XP \|\]</span><span class="sxs-lookup"><span data-stu-id="9933d-187">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="9933d-188">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9933d-188">Minimum supported server</span></span><br/> | <span data-ttu-id="9933d-189">\[Приложения UWP для классических приложений Windows Server 2003 \|\]</span><span class="sxs-lookup"><span data-stu-id="9933d-189">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="9933d-190">Header</span><span class="sxs-lookup"><span data-stu-id="9933d-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="9933d-191"><dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9933d-191"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9933d-192">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9933d-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="9933d-193"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9933d-193"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="9933d-194">DLL</span><span class="sxs-lookup"><span data-stu-id="9933d-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9933d-195"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9933d-195"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="9933d-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9933d-196">See also</span></span>

<dl> <dt>

<span data-ttu-id="9933d-197">**Обзорные разделы**</span><span class="sxs-lookup"><span data-stu-id="9933d-197">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="9933d-198">Функции управления файлами</span><span class="sxs-lookup"><span data-stu-id="9933d-198">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="9933d-199">Порты завершения ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="9933d-199">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="9933d-200">Использование заголовков Windows</span><span class="sxs-lookup"><span data-stu-id="9933d-200">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[<span data-ttu-id="9933d-201">Сокеты Windows 2</span><span class="sxs-lookup"><span data-stu-id="9933d-201">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

<span data-ttu-id="9933d-202">**Функции**</span><span class="sxs-lookup"><span data-stu-id="9933d-202">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="9933d-203">**акцептекс**</span><span class="sxs-lookup"><span data-stu-id="9933d-203">**AcceptEx**</span></span>](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[<span data-ttu-id="9933d-204">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="9933d-204">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="9933d-205">**дупликатехандле**</span><span class="sxs-lookup"><span data-stu-id="9933d-205">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="9933d-206">**жеткуеуедкомплетионстатус**</span><span class="sxs-lookup"><span data-stu-id="9933d-206">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="9933d-207">**жеткуеуедкомплетионстатусекс**</span><span class="sxs-lookup"><span data-stu-id="9933d-207">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="9933d-208">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="9933d-208">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="9933d-209">**реадфиликс**</span><span class="sxs-lookup"><span data-stu-id="9933d-209">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="9933d-210">**вритефиликс**</span><span class="sxs-lookup"><span data-stu-id="9933d-210">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

