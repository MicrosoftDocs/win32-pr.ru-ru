---
title: IStream — реализация составного файла
description: Интерфейс IStream поддерживает чтение и запись данных в объекты Stream. В структурированном объекте хранилища объекты-потоки содержат данные и хранилища, которые предоставляют структуру.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105664785"
---
# <a name="istream---compound-file-implementation"></a><span data-ttu-id="92558-105">IStream — реализация составного файла</span><span class="sxs-lookup"><span data-stu-id="92558-105">IStream - Compound File Implementation</span></span>

<span data-ttu-id="92558-106">Интерфейс [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) поддерживает чтение и запись данных в объекты Stream.</span><span class="sxs-lookup"><span data-stu-id="92558-106">The [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface supports reading and writing data to stream objects.</span></span> <span data-ttu-id="92558-107">В структурированном объекте хранилища объекты-потоки содержат данные и хранилища, которые предоставляют структуру.</span><span class="sxs-lookup"><span data-stu-id="92558-107">In a structured storage object, stream objects contain the data and storages provide the structure.</span></span> <span data-ttu-id="92558-108">Простые данные можно записывать непосредственно в поток, но чаще потоки — это элементы, вложенные в объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="92558-108">Simple data can be written directly to a stream, but more frequently, streams are elements nested within a storage object.</span></span> <span data-ttu-id="92558-109">Они похожи на стандартные файлы.</span><span class="sxs-lookup"><span data-stu-id="92558-109">They are similar to standard files.</span></span>

<span data-ttu-id="92558-110">Спецификация [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) определяет больше функций, чем поддерживается реализацией com.</span><span class="sxs-lookup"><span data-stu-id="92558-110">The specification of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) defines more functionality than the COM implementation supports.</span></span> <span data-ttu-id="92558-111">Например, интерфейс **IStream** определяет потоки длиной до 2 ⁶ ⁴ байт, что требует 64-разрядный указатель поиска.</span><span class="sxs-lookup"><span data-stu-id="92558-111">For example, the **IStream** interface defines streams up to 2⁶⁴ bytes in length requiring a 64-bit seek pointer.</span></span> <span data-ttu-id="92558-112">Однако реализация COM поддерживает только потоки длиной до 2 ³ ² байт (4 ГБ), а операции чтения и записи всегда ограничены 2 ³ ² байтами.</span><span class="sxs-lookup"><span data-stu-id="92558-112">However, the COM implementation only supports streams up to 2³² bytes in length (4 GB) and read and write operations are always limited to 2³² bytes at a time.</span></span> <span data-ttu-id="92558-113">Реализация COM также не поддерживает транзакционную блокировку в потоках или в области.</span><span class="sxs-lookup"><span data-stu-id="92558-113">The COM implementation also does not support stream transactioning or region locking.</span></span>

<span data-ttu-id="92558-114">Чтобы создать простой поток на основе глобальной памяти, получите указатель [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , вызвав функцию API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span><span class="sxs-lookup"><span data-stu-id="92558-114">To create a simple stream based on global memory, get an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer by calling the API function [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span></span> <span data-ttu-id="92558-115">Чтобы получить указатель **IStream** внутри объекта составного файла, вызовите либо [**Стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , либо [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span><span class="sxs-lookup"><span data-stu-id="92558-115">To get an **IStream** pointer within a compound file object, call either [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) or [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span></span> <span data-ttu-id="92558-116">Эти функции извлекают указатель [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , с помощью которого можно вызвать [**креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) или [**опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) для указателя **IStream** .</span><span class="sxs-lookup"><span data-stu-id="92558-116">These functions retrieve an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer, with which you can then call [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) for an **IStream** pointer.</span></span> <span data-ttu-id="92558-117">В любом случае используется один и тот же код реализации **IStream** .</span><span class="sxs-lookup"><span data-stu-id="92558-117">In either case, the same **IStream** implementation code is used.</span></span>

> [!Note]  
> <span data-ttu-id="92558-118">Реализация составного файла в структурированном хранилище не выполняется в методе [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), но включает методы [**чтения**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) и [**записи**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) через указатель интерфейса [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="92558-118">The compound file implementation of structured storage does not succeed on a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method for [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), but it includes the [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) and [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) methods through the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer.</span></span>

 

## <a name="when-to-use"></a><span data-ttu-id="92558-119">Назначение</span><span class="sxs-lookup"><span data-stu-id="92558-119">When to Use</span></span>

<span data-ttu-id="92558-120">Вызывайте методы [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для чтения и записи данных в поток.</span><span class="sxs-lookup"><span data-stu-id="92558-120">Call the methods of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) to read and write data to a stream.</span></span>

<span data-ttu-id="92558-121">Поскольку объекты потока могут быть упакованы в другие процессы, приложения могут совместно использовать данные в объектах хранилища, не используя глобальную память.</span><span class="sxs-lookup"><span data-stu-id="92558-121">Because stream objects can be marshaled to other processes, applications can share the data in storage objects without having to use global memory.</span></span> <span data-ttu-id="92558-122">В реализации составного файла COM для объектов потоков пользовательская функция упаковки в COM создает удаленную версию исходного объекта в новом процессе, когда два процесса имеют доступ к общей памяти.</span><span class="sxs-lookup"><span data-stu-id="92558-122">In the COM compound file implementation of stream objects, the custom marshaling facilities in COM create a remote version of the original object in the new process when the two processes have shared-memory access.</span></span> <span data-ttu-id="92558-123">Таким же удаленная версия не должна взаимодействовать с исходным процессом для выполнения своих функций.</span><span class="sxs-lookup"><span data-stu-id="92558-123">Thus, the remote version does not need to communicate with the original process to carry out its functions.</span></span>

<span data-ttu-id="92558-124">Удаленная версия объекта Stream использует тот же указатель поиска, что и исходный поток.</span><span class="sxs-lookup"><span data-stu-id="92558-124">The remote version of the stream object shares the same seek pointer as the original stream.</span></span> <span data-ttu-id="92558-125">Если вы не хотите совместно использовать указатель поиска, используйте метод [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) , чтобы предоставить копию объекта потока для удаленного процесса.</span><span class="sxs-lookup"><span data-stu-id="92558-125">If you do not want to share the seek pointer, use the [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) method to provide a copy of the stream object for the remote process.</span></span>

> [!Note]
> <span data-ttu-id="92558-126">Если создается объект потока, превышающий кучу в памяти компьютера, и вы используете обработчик **хглобал** для объекта глобальной памяти, объект Stream вызывает метод [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) внутренне вхе он требует больше памяти.</span><span class="sxs-lookup"><span data-stu-id="92558-126">If creating a stream object that is larger than the heap in your computer's memory and you are using an **HGLOBAL** handle to a global memory object, the stream object calls the [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) method internally whe it requires more memory.</span></span> <span data-ttu-id="92558-127">Поскольку **LocalLock** всегда копирует данные из источника в место назначения, увеличение объекта потока с 20 МБ до 25 МБ, например, требует большого количества времени.</span><span class="sxs-lookup"><span data-stu-id="92558-127">Because **GlobalRealloc** always copies data from the source to the destination, increasing a stream object from 20 MB to 25 MB, for example, requires large amounts of time.</span></span> <span data-ttu-id="92558-128">Это связано с размером скопированных приращений и усугубить, если на компьютере установлено менее 45 МБ памяти из-за переключения дисков.</span><span class="sxs-lookup"><span data-stu-id="92558-128">This is due to the size of the increments copied and is worsened if there is less than 45 MB of memory on the computer because of disk swapping.</span></span>
>
> <span data-ttu-id="92558-129">Предпочтительным решением является реализация метода [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , который использует память, выделенную [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) , а не [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="92558-129">The preferred solution is to implement an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) method that uses memory allocated by [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) instead of [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span></span> <span data-ttu-id="92558-130">Это может зарезервировать большой фрагмент виртуального адресного пространства, а затем зафиксировать память в этом адресном пространстве по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="92558-130">This can reserve a large chunk of virtual address space and then commit memory within that address space as required.</span></span> <span data-ttu-id="92558-131">Копирование данных не происходит, и память зафиксирована только по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="92558-131">No data copying occurs and memory is committed only as it is required.</span></span>
>
> <span data-ttu-id="92558-132">Альтернативой [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) является вызов метода [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) объекта Stream для увеличения объема выделяемой памяти заранее.</span><span class="sxs-lookup"><span data-stu-id="92558-132">An alternative to [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) is to call the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method on the stream object to increase the memory allocation in advance.</span></span> <span data-ttu-id="92558-133">Однако это не так эффективно, как использование [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), как описано выше.</span><span class="sxs-lookup"><span data-stu-id="92558-133">This is not, however, as efficient as using [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), as described above.</span></span>

 

## <a name="methods"></a><span data-ttu-id="92558-134">Методы</span><span class="sxs-lookup"><span data-stu-id="92558-134">Methods</span></span>

<dl> <dt>

<span data-ttu-id="92558-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span><span class="sxs-lookup"><span data-stu-id="92558-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span></span>
</dt> <dd>

<span data-ttu-id="92558-136">Считывает указанное число байтов из объекта потока в память, начиная с текущего указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="92558-136">Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</span></span> <span data-ttu-id="92558-137">Эта реализация возвращает значение \_ ОК, если конец потока был достигнут во время чтения.</span><span class="sxs-lookup"><span data-stu-id="92558-137">This implementation returns S\_OK if the end of the stream was reached during the read.</span></span> <span data-ttu-id="92558-138">(Это аналогично поведению "конец файла", обнаруженному в файловой системе MS-DOS FAT).</span><span class="sxs-lookup"><span data-stu-id="92558-138">(This is the same as the "end of file" behavior found in the MS-DOS FAT file system.)</span></span>

</dd> <dt>

<span data-ttu-id="92558-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span><span class="sxs-lookup"><span data-stu-id="92558-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span></span>
</dt> <dd>

<span data-ttu-id="92558-140">Записывает указанное число из байтов в объект потока, начиная с текущего указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="92558-140">Writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span> <span data-ttu-id="92558-141">В этой реализации объекты потока не имеют разреженных объектов.</span><span class="sxs-lookup"><span data-stu-id="92558-141">In this implementation, stream objects are not sparse.</span></span> <span data-ttu-id="92558-142">Все байты заполнения в конечном итоге выделяются на диске и назначаются потоку.</span><span class="sxs-lookup"><span data-stu-id="92558-142">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

</dd> <dt>

<span data-ttu-id="92558-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span><span class="sxs-lookup"><span data-stu-id="92558-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span></span>
</dt> <dd>

<span data-ttu-id="92558-144">Изменяет указатель поиска на новое расположение относительно начала потока до конца потока или текущего положения поиска.</span><span class="sxs-lookup"><span data-stu-id="92558-144">Changes the seek pointer to a new location relative to the beginning of the stream, to the end of the stream, or to the current seek pointer.</span></span>

</dd> <dt>

<span data-ttu-id="92558-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span><span class="sxs-lookup"><span data-stu-id="92558-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span></span>
</dt> <dd>

<span data-ttu-id="92558-146">Изменяет размер объекта-потока.</span><span class="sxs-lookup"><span data-stu-id="92558-146">Changes the size of the stream object.</span></span> <span data-ttu-id="92558-147">В этой реализации нет никакой гарантии, что выделенное пространство будет непрерывным.</span><span class="sxs-lookup"><span data-stu-id="92558-147">In this implementation, there is no guarantee that the space allocated will be contiguous.</span></span>

</dd> <dt>

<span data-ttu-id="92558-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span><span class="sxs-lookup"><span data-stu-id="92558-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="92558-149">Копирует указанное число байтов из текущего указателя поиска в потоке до текущего указателя поиска в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="92558-149">Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.</span></span>

</dd> <dt>

<span data-ttu-id="92558-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span><span class="sxs-lookup"><span data-stu-id="92558-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span></span>
</dt> <dd>

<span data-ttu-id="92558-151">Реализация составного файла для [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) поддерживает открытие потоков только в режиме Direct, а не в режиме транзакций.</span><span class="sxs-lookup"><span data-stu-id="92558-151">The compound file implementation of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supports opening streams only in direct mode, not transacted mode.</span></span> <span data-ttu-id="92558-152">Поэтому метод не действует при вызове, отличном от сброса всех буферов памяти до следующего уровня хранилища.</span><span class="sxs-lookup"><span data-stu-id="92558-152">Therefore, the method has no effect when called other than to flush all memory buffers to the next storage level.</span></span>

<span data-ttu-id="92558-153">В этой реализации не имеет значения, следует ли зафиксировать изменения в потоках, необходимо только внести изменения в объекты хранилища.</span><span class="sxs-lookup"><span data-stu-id="92558-153">In this implementation, it does not matter if you commit changes to streams, you need only commit changes for storage objects.</span></span>

</dd> <dt>

<span data-ttu-id="92558-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span><span class="sxs-lookup"><span data-stu-id="92558-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span></span>
</dt> <dd>

<span data-ttu-id="92558-155">Эта реализация не поддерживает транзакционные потоки, поэтому вызов этого метода не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="92558-155">This implementation does not support transacted streams, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="92558-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span><span class="sxs-lookup"><span data-stu-id="92558-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span></span>
</dt> <dd>

<span data-ttu-id="92558-157">Блокировка диапазона не поддерживается этой реализацией, поэтому вызов этого метода не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="92558-157">Range-locking is not supported by this implementation, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="92558-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span><span class="sxs-lookup"><span data-stu-id="92558-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span></span>
</dt> <dd>

<span data-ttu-id="92558-159">Удаляет ограничение доступа для диапазона байтов, которые ранее были ограничены с помощью [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span><span class="sxs-lookup"><span data-stu-id="92558-159">Removes the access restriction on a range of bytes previously restricted with [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="92558-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span><span class="sxs-lookup"><span data-stu-id="92558-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span></span>
</dt> <dd>

<span data-ttu-id="92558-161">Получает структуру [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) для этого потока</span><span class="sxs-lookup"><span data-stu-id="92558-161">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this stream</span></span>

</dd> <dt>

<span data-ttu-id="92558-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span><span class="sxs-lookup"><span data-stu-id="92558-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span></span>
</dt> <dd>

<span data-ttu-id="92558-163">Создает новый объект потока с собственным указателем, который ссылается на те же байты, что и исходный поток.</span><span class="sxs-lookup"><span data-stu-id="92558-163">Creates a new stream object with its own seek pointer that references the same bytes as the original stream.</span></span>

</dd> </dl>

<span data-ttu-id="92558-164">Для простого режима [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) действуют следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="92558-164">A simple-mode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is subject to the following constraints.</span></span>

-   <span data-ttu-id="92558-165">Поток является простым режимом, если он был создан или открыт из хранилища в простом режиме.</span><span class="sxs-lookup"><span data-stu-id="92558-165">A stream is simple mode if it was created or opened from a simple-mode storage.</span></span> <span data-ttu-id="92558-166">Хранилище имеет простой режим, если он создан или открыт с помощью \_ простого флага стгм, установленного в параметре *грфмоде* .</span><span class="sxs-lookup"><span data-stu-id="92558-166">A storage is simple mode if it is created or opened with the STGM\_SIMPLE flag set in the *grfMode* parameter.</span></span>
-   <span data-ttu-id="92558-167">Методы [**clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) и [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="92558-167">The [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) and [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) methods are not supported.</span></span>
-   <span data-ttu-id="92558-168">Поддерживается метод [**stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , однако \_ должно быть указано значение статфлаг.</span><span class="sxs-lookup"><span data-stu-id="92558-168">The [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method is supported, but the STATFLAG\_NONAME value must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92558-169">См. также</span><span class="sxs-lookup"><span data-stu-id="92558-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92558-170">**IStream**</span><span class="sxs-lookup"><span data-stu-id="92558-170">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="92558-171">**Метод IStorage**</span><span class="sxs-lookup"><span data-stu-id="92558-171">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="92558-172">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="92558-172">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[<span data-ttu-id="92558-173">**стгкреатедокфиле**</span><span class="sxs-lookup"><span data-stu-id="92558-173">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="92558-174">**стгопенстораже**</span><span class="sxs-lookup"><span data-stu-id="92558-174">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 