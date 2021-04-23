---
description: Считывает данные из открытого файла.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Функция Нтреадфиле (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538534"
---
# <a name="ntreadfile-function"></a><span data-ttu-id="ddeaf-103">Функция Нтреадфиле</span><span class="sxs-lookup"><span data-stu-id="ddeaf-103">NtReadFile function</span></span>

<span data-ttu-id="ddeaf-104">Считывает данные из открытого файла.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-104">Reads data from an open file.</span></span>

<span data-ttu-id="ddeaf-105">Эта функция является аналогом пользовательского режима функции [**звреадфиле**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) , документированной в комплекте драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="ddeaf-105">This function is the user-mode equivalent to the [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) function documented in the Windows Driver Kit (WDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="ddeaf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddeaf-106">Syntax</span></span>


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a><span data-ttu-id="ddeaf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ddeaf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddeaf-108">*FileHandle* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-108">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-109">Обработчик для объекта File.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-109">Handle to the file object.</span></span> <span data-ttu-id="ddeaf-110">Этот маркер создается при успешном вызове [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) или [**нтопенфиле**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span><span class="sxs-lookup"><span data-stu-id="ddeaf-110">This handle is created by a successful call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) or [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-111">*Событие* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-111">*Event* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-112">При необходимости дескриптор объекта события может быть установлен в сигнальное состояние после завершения операции чтения.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-112">Optionally, a handle to an event object to set to the signaled state after the read operation completes.</span></span> <span data-ttu-id="ddeaf-113">Драйвер устройства и промежуточные драйверы должны установить этот параметр в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-113">Device and intermediate drivers should set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-114">*Апкраутине* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-114">*ApcRoutine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-115">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-115">This parameter is reserved.</span></span> <span data-ttu-id="ddeaf-116">Драйвер устройства и промежуточные драйверы должны установить этот указатель на **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-116">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-117">*Апкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-117">*ApcContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-118">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-118">This parameter is reserved.</span></span> <span data-ttu-id="ddeaf-119">Драйвер устройства и промежуточные драйверы должны установить этот указатель на **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-119">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-120">*Иостатусблокк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-120">*IoStatusBlock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-121">Указатель на структуру [**\_ \_ блока состояния ввода-вывода**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) , которая получает конечное состояние завершения и сведения о запрошенной операции чтения.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-121">Pointer to an [**IO\_STATUS\_BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) structure that receives the final completion status and information about the requested read operation.</span></span> <span data-ttu-id="ddeaf-122">**Информационный** элемент получает число байтов, фактически считанных из файла.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-122">The **Information** member receives the number of bytes actually read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-123">*Буфер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-123">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-124">Указатель на выделенный вызывающим объектом буфер, который получает данные, считанные из файла.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-124">Pointer to a caller-allocated buffer that receives the data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-125">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-125">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-126">Размер (в байтах) буфера, на который указывает *буфер*.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-126">The size, in bytes, of the buffer pointed to by *Buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-127">*ByteOffset* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-127">*ByteOffset* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-128">Указатель на переменную, которая указывает начальное смещение в байтах в файле, с которого начнется операция чтения.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-128">Pointer to a variable that specifies the starting byte offset in the file where the read operation will begin.</span></span> <span data-ttu-id="ddeaf-129">Если предпринимается попытка чтения после конца файла, **нтреадфиле** возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-129">If an attempt is made to read beyond the end of the file, **NtReadFile** returns an error.</span></span>

<span data-ttu-id="ddeaf-130">Если при вызове [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) задано одно из  \_ оповещений о синхронном вводе-выводе в файле ФЛАГов КРЕАТЕОПТИОНС \_ \_ или \_ \_ \_ неоповещение файла, диспетчер ввода-вывода сохраняет текущее расположение файла.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-130">If the call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set either of the *CreateOptions* flags FILE\_SYNCHRONOUS\_IO\_ALERT or FILE\_SYNCHRONOUS\_IO\_NONALERT, the I/O Manager maintains the current file position.</span></span> <span data-ttu-id="ddeaf-131">Если это так, вызывающий объект **нтреадфиле** может указать, что вместо явного значения *ByteOffset* должно использоваться текущее смещение позиции файла.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-131">If so, the caller of **NtReadFile** can specify that the current file position offset be used instead of an explicit *ByteOffset* value.</span></span> <span data-ttu-id="ddeaf-132">Эту спецификацию можно выполнить с помощью одного из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-132">This specification can be made by using one of the following methods:</span></span>

-   <span data-ttu-id="ddeaf-133">Укажите указатель на **большое \_ целое** значение, в котором элемент **хигхпарт** имеет значение-1, а для элемента **ловпарт** — в качестве системного файла значений \_ используется \_ \_ расположение указателя файла \_ .</span><span class="sxs-lookup"><span data-stu-id="ddeaf-133">Specify a pointer to a **LARGE\_INTEGER** value with the **HighPart** member set to -1 and the **LowPart** member set to the system-defined value FILE\_USE\_FILE\_POINTER\_POSITION.</span></span>

-   <span data-ttu-id="ddeaf-134">Передайте **пустой** указатель для *ByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-134">Pass a **NULL** pointer for *ByteOffset*.</span></span>

<span data-ttu-id="ddeaf-135">**Нтреадфиле** обновляет текущее расположение файла, добавляя число байтов, считанных при завершении операции чтения, если она использует текущее расположение файла, поддерживаемое диспетчером ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-135">**NtReadFile** updates the current file position by adding the number of bytes read when it completes the read operation, if it is using the current file position maintained by the I/O Manager.</span></span>

<span data-ttu-id="ddeaf-136">Даже если диспетчер ввода-вывода сохраняет текущую позицией в файле, вызывающий объект может сбросить эту точку, передав явное значение *ByteOffset* в **нтреадфиле**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-136">Even when the I/O Manager is maintaining the current file position, the caller can reset this position by passing an explicit *ByteOffset* value to **NtReadFile**.</span></span> <span data-ttu-id="ddeaf-137">Это автоматически изменяет текущее расположение файла на это значение *ByteOffset* , выполняет операцию чтения, а затем обновляет расположение в соответствии с числом фактически считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-137">Doing this automatically changes the current file position to that *ByteOffset* value, performs the read operation, and then updates the position according to the number of bytes actually read.</span></span> <span data-ttu-id="ddeaf-138">Этот метод предоставляет вызывающему объекту атомарную службу поиска и чтения.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-138">This technique gives the caller atomic seek-and-read service.</span></span>

</dd> <dt>

<span data-ttu-id="ddeaf-139">*Ключ* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-139">*Key* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddeaf-140">Драйвер устройства и промежуточные драйверы должны установить этот указатель на **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-140">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddeaf-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ddeaf-141">Return value</span></span>

<span data-ttu-id="ddeaf-142">**Нтреадфиле** ВОЗВРАЩАЕТ либо состояние \_ Success, либо соответствующий код ошибки NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-142">**NtReadFile** returns either STATUS\_SUCCESS or the appropriate NTSTATUS error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddeaf-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddeaf-143">Remarks</span></span>

<span data-ttu-id="ddeaf-144">Вызывающие объекты **нтреадфиле** должны уже называться [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) с ФАЙЛОМ \_ Read \_ Data или универсальным \_ чтением значения, заданным в параметре *десиредакцесс* .</span><span class="sxs-lookup"><span data-stu-id="ddeaf-144">Callers of **NtReadFile** must have already called [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) with the FILE\_READ\_DATA or GENERIC\_READ value set in the *DesiredAccess* parameter.</span></span>

<span data-ttu-id="ddeaf-145">Если предыдущий вызов [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) устанавливает \_ флаг File No \_ промежуточной \_ буферизации в параметре *креатеоптионс* в **NtCreateFile**, параметры *length* и *ByteOffset* для **нтреадфиле** должны быть кратны размеру сектора.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-145">If the preceding call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set the FILE\_NO\_INTERMEDIATE\_BUFFERING flag in the *CreateOptions* parameter to **NtCreateFile**, the *Length* and *ByteOffset* parameters to **NtReadFile** must be multiples of the sector size.</span></span> <span data-ttu-id="ddeaf-146">Дополнительные сведения см. в разделе **NtCreateFile**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-146">For more information, see **NtCreateFile**.</span></span>

<span data-ttu-id="ddeaf-147">**Нтреадфиле** начинает чтение из заданной *ByteOffset* или текущего расположения файла в заданном *буфере*.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-147">**NtReadFile** begins reading from the given *ByteOffset* or the current file position into the given *Buffer*.</span></span> <span data-ttu-id="ddeaf-148">Операция чтения завершается одним из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="ddeaf-148">It terminates the read operation under one of the following conditions:</span></span>

-   <span data-ttu-id="ddeaf-149">Буфер заполнен, так как было считано число байтов, указанное параметром *длины* .</span><span class="sxs-lookup"><span data-stu-id="ddeaf-149">The buffer is full because the number of bytes specified by the *Length* parameter has been read.</span></span> <span data-ttu-id="ddeaf-150">Таким образом, больше данных нельзя поместить в буфер без переполнения.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-150">Therefore, no more data can be placed into the buffer without an overflow.</span></span>

-   <span data-ttu-id="ddeaf-151">Конец файла достигнут во время операции чтения, поэтому в этом файле больше нет данных для передачи в буфер.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-151">The end of file is reached during the read operation, so there is no more data in the file to be transferred into the buffer.</span></span>

<span data-ttu-id="ddeaf-152">Если вызывающий объект открыл файл с флагом SYNCHRONIZE, установленным в *десиредакцесс*, вызывающий поток может синхронизироваться с завершением операции чтения, ожидая обработки файла *FileHandle*.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-152">If the caller opened the file with the SYNCHRONIZE flag set in *DesiredAccess*, the calling thread can synchronize to the completion of the read operation by waiting on the file handle, *FileHandle*.</span></span> <span data-ttu-id="ddeaf-153">Дескриптор получает сигнал каждый раз, когда завершается операция ввода-вывода, выполненная над дескриптором.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-153">The handle is signaled each time that an I/O operation that was issued on the handle completes.</span></span> <span data-ttu-id="ddeaf-154">Однако вызывающий объект не должен ждать обработчика, открытого для синхронного доступа к файлам ( \_ \_ \_ предупреждение о непредупреждении или синхронных операциях ввода-вывода файлов \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="ddeaf-154">However, the caller must not wait on a handle that was opened for synchronous file access (FILE\_SYNCHRONOUS\_IO\_NONALERT or FILE\_SYNCHRONOUS\_IO\_ALERT).</span></span> <span data-ttu-id="ddeaf-155">В этом случае **нтреадфиле** ожидает от имени вызывающего объекта и не возвращает значение до завершения операции чтения.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-155">In this case, **NtReadFile** waits on behalf of the caller and does not return until the read operation is complete.</span></span> <span data-ttu-id="ddeaf-156">Вызывающий объект может безопасно ожидать обработку файла, только если выполняются все три следующих условия.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-156">The caller can safely wait on the file handle only if all three of the following conditions are met:</span></span>

-   <span data-ttu-id="ddeaf-157">Маркер был открыт для асинхронного доступа (т. е. не \_ \_ задан флаг синхронного ввода-вывода \_ *xxx* ).</span><span class="sxs-lookup"><span data-stu-id="ddeaf-157">The handle was opened for asynchronous access (that is, neither FILE\_SYNCHRONOUS\_IO\_*XXX* flag was specified).</span></span>

-   <span data-ttu-id="ddeaf-158">Этот маркер используется только для одной операции ввода-вывода за раз.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-158">The handle is being used for only one I/O operation at a time.</span></span>

-   <span data-ttu-id="ddeaf-159">**Нтреадфиле** вернул состояние " \_ Ожидание".</span><span class="sxs-lookup"><span data-stu-id="ddeaf-159">**NtReadFile** returned STATUS\_PENDING.</span></span>

<span data-ttu-id="ddeaf-160">Драйвер должен вызывать **нтреадфиле** в контексте системного процесса, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-160">A driver should call **NtReadFile** in the context of the system process if any of the following conditions exist:</span></span>

-   <span data-ttu-id="ddeaf-161">Драйвер создал файловый обработчик, который он передает в **нтреадфиле**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-161">The driver created the file handle that it passes to **NtReadFile**.</span></span>

-   <span data-ttu-id="ddeaf-162">**Нтреадфиле** будет уведомлять драйвер о завершении ввода-вывода с помощью события, созданного драйвером.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-162">**NtReadFile** will notify the driver of I/O completion by means of an event that the driver created.</span></span>

-   <span data-ttu-id="ddeaf-163">**Нтреадфиле** будет уведомлять драйвер о завершении ввода-вывода с помощью подпрограммы обратного вызова APC, которую драйвер передает в **нтреадфиле**.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-163">**NtReadFile** will notify the driver of I/O completion by means of an APC callback routine that the driver passes to **NtReadFile**.</span></span>

<span data-ttu-id="ddeaf-164">Дескрипторы файлов и событий допустимы только в контексте процесса, где создаются дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-164">File and event handles are valid only in the process context where the handles are created.</span></span> <span data-ttu-id="ddeaf-165">Поэтому, чтобы избежать брешей в системе безопасности, драйвер должен создать любой файл или обработчик событий, который он передает в **нтреадфиле** в контексте системного процесса, а не контекста процесса, в котором находится драйвер.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-165">Therefore, to avoid security holes, the driver should create any file or event handle that it passes to **NtReadFile** in the context of the system process rather than the context of the process that the driver is in.</span></span>

<span data-ttu-id="ddeaf-166">Аналогичным образом **нтреадфиле** должен вызываться в контексте системного процесса, если он уведомляет драйвер о завершении ввода-вывода с помощью APC, поскольку APC всегда срабатывают в контексте потока, который выдает запрос ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-166">Likewise, **NtReadFile** should be called in the context of the system process if it notifies the driver of I/O completion by means of an APC, because APCs are always fired in the context of the thread that issues the I/O request.</span></span> <span data-ttu-id="ddeaf-167">Если драйвер вызывает **нтреадфиле** в контексте процесса, отличного от системы, то компания APC может быть отложена неограниченное время или вообще не сработать.</span><span class="sxs-lookup"><span data-stu-id="ddeaf-167">If the driver calls **NtReadFile** in the context of a process other than the system one, the APC could be delayed indefinitely, or it might not fire at all.</span></span>

<span data-ttu-id="ddeaf-168">Дополнительные сведения о работе с файлами см. [в разделе Использование файлов в драйвере](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span><span class="sxs-lookup"><span data-stu-id="ddeaf-168">For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span></span>

<span data-ttu-id="ddeaf-169">Вызывающие объекты **нтреадфиле** должны выполняться на уровне IRQL = пассивный \_ уровень, а также [включить специальный APC ядра](/windows-hardware/drivers/kernel/disabling-apcs).</span><span class="sxs-lookup"><span data-stu-id="ddeaf-169">Callers of **NtReadFile** must be running at IRQL = PASSIVE\_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddeaf-170">Требования</span><span class="sxs-lookup"><span data-stu-id="ddeaf-170">Requirements</span></span>



| <span data-ttu-id="ddeaf-171">Требование</span><span class="sxs-lookup"><span data-stu-id="ddeaf-171">Requirement</span></span> | <span data-ttu-id="ddeaf-172">Значение</span><span class="sxs-lookup"><span data-stu-id="ddeaf-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddeaf-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddeaf-173">Minimum supported client</span></span><br/> | <span data-ttu-id="ddeaf-174">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="ddeaf-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddeaf-175">Minimum supported server</span></span><br/> | <span data-ttu-id="ddeaf-176">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ddeaf-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="ddeaf-177">Целевая платформа</span><span class="sxs-lookup"><span data-stu-id="ddeaf-177">Target platform</span></span><br/>          | <dl> <span data-ttu-id="ddeaf-178"><dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="ddeaf-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="ddeaf-179">Header</span><span class="sxs-lookup"><span data-stu-id="ddeaf-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddeaf-180"><dt>WDM. h (включает WDM. h, Нтддк. h или Нтифс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddeaf-180"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="ddeaf-181">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ddeaf-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddeaf-182"><dt>NTDLL. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddeaf-182"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ddeaf-183">DLL</span><span class="sxs-lookup"><span data-stu-id="ddeaf-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddeaf-184"><dt>Ntdll.dll (пользовательский режим)</dt></span><span class="sxs-lookup"><span data-stu-id="ddeaf-184"><dt>Ntdll.dll (user mode)</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="ddeaf-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddeaf-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddeaf-186">**кеинитиализивент**</span><span class="sxs-lookup"><span data-stu-id="ddeaf-186">**KeInitializeEvent**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[<span data-ttu-id="ddeaf-187">**NtCreateFile**</span><span class="sxs-lookup"><span data-stu-id="ddeaf-187">**NtCreateFile**</span></span>](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[<span data-ttu-id="ddeaf-188">**нткуеринформатионфиле**</span><span class="sxs-lookup"><span data-stu-id="ddeaf-188">**NtQueryInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[<span data-ttu-id="ddeaf-189">**нтсетинформатионфиле**</span><span class="sxs-lookup"><span data-stu-id="ddeaf-189">**NtSetInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[<span data-ttu-id="ddeaf-190">**нтвритефиле**</span><span class="sxs-lookup"><span data-stu-id="ddeaf-190">**NtWriteFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
