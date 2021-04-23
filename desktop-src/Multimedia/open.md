---
title: команда Open (Корекрт \_ IO. h)
description: Команда Open инициализирует устройство. Все устройства MCI распознают эту команду.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- Открытие команды мультимедиа Windows
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802224"
---
# <a name="open-command"></a><span data-ttu-id="c751a-105">Открыть команду</span><span class="sxs-lookup"><span data-stu-id="c751a-105">open command</span></span>

<span data-ttu-id="c751a-106">Команда Open инициализирует устройство.</span><span class="sxs-lookup"><span data-stu-id="c751a-106">The open command initializes a device.</span></span> <span data-ttu-id="c751a-107">Все устройства MCI распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="c751a-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="c751a-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="c751a-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="c751a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c751a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c751a-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*лпсздевице*</span><span class="sxs-lookup"><span data-stu-id="c751a-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span></span>
</dt> <dd>

<span data-ttu-id="c751a-111">Идентификатор устройства MCI или драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="c751a-111">Identifier of an MCI device or device driver.</span></span> <span data-ttu-id="c751a-112">Это может быть имя устройства (как указано в реестре или файле SYSTEM.INI) или имя файла драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="c751a-112">This can be either a device name (as given in the registry or the SYSTEM.INI file) or the filename of the device driver.</span></span> <span data-ttu-id="c751a-113">Если указать имя файла драйвера устройства, можно дополнительно включить. Расширение DRV, но не следует включать путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="c751a-113">If you specify the filename of the device driver, you can optionally include the .DRV extension, but you should not include the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="c751a-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*лпсзопенфлагс*</span><span class="sxs-lookup"><span data-stu-id="c751a-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c751a-115">Флаг, определяющий инициализацию.</span><span class="sxs-lookup"><span data-stu-id="c751a-115">Flag that identifies what to initialize.</span></span> <span data-ttu-id="c751a-116">В следующей таблице перечислены типы устройств, которые распознают команду **Open** и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="c751a-116">The following table lists device types that recognize the **open** command and the flags used by each type.</span></span>



| <span data-ttu-id="c751a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c751a-117">Value</span></span>        | <span data-ttu-id="c751a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c751a-118">Meaning</span></span>                                                        | <span data-ttu-id="c751a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c751a-119">Meaning</span></span>                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c751a-120">кдаудио</span><span class="sxs-lookup"><span data-stu-id="c751a-120">cdaudio</span></span>      | <span data-ttu-id="c751a-121">псевдоним *\_ псевдонима устройства*, который является общим</span><span class="sxs-lookup"><span data-stu-id="c751a-121">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="c751a-122">Тип *устройства \_* типа</span><span class="sxs-lookup"><span data-stu-id="c751a-122">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="c751a-123">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="c751a-123">digitalvideo</span></span> | <span data-ttu-id="c751a-124">псевдоним *устройства \_ алиаселементнаме* нестатический родительский *дескриптор HWND* с общим родителем</span><span class="sxs-lookup"><span data-stu-id="c751a-124">alias *device\_aliaselementname* nostatic parent *hwnd* sharable</span></span> | <span data-ttu-id="c751a-125">стиль стиль всплывающего окна стиля дочернего стиля стилей *тип \_ устройства* тип *\_*</span><span class="sxs-lookup"><span data-stu-id="c751a-125">style child style overlapped style popup style *style\_type* type *device\_type*</span></span> |
| <span data-ttu-id="c751a-126">overlay</span><span class="sxs-lookup"><span data-stu-id="c751a-126">overlay</span></span>      | <span data-ttu-id="c751a-127">псевдоним родительского устройства. дочерний элемент типа *HWND* с общим родителем *\_*</span><span class="sxs-lookup"><span data-stu-id="c751a-127">alias *device\_alias* parent *hwnd* sharable style child</span></span>         | <span data-ttu-id="c751a-128">стиль стиля всплывающего окна стиля *с \_* перекрытием стилей тип *устройства \_* тип</span><span class="sxs-lookup"><span data-stu-id="c751a-128">style overlapped style popup style *style\_type* type *device\_type*</span></span>             |
| <span data-ttu-id="c751a-129">sequencer</span><span class="sxs-lookup"><span data-stu-id="c751a-129">sequencer</span></span>    | <span data-ttu-id="c751a-130">псевдоним *\_ псевдонима устройства* , который является общим</span><span class="sxs-lookup"><span data-stu-id="c751a-130">alias *device\_alias* sharable</span></span>                                 | <span data-ttu-id="c751a-131">Тип *устройства \_* типа</span><span class="sxs-lookup"><span data-stu-id="c751a-131">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="c751a-132">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="c751a-132">vcr</span></span>          | <span data-ttu-id="c751a-133">псевдоним *\_ псевдонима устройства*, который является общим</span><span class="sxs-lookup"><span data-stu-id="c751a-133">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="c751a-134">Тип *устройства \_* типа</span><span class="sxs-lookup"><span data-stu-id="c751a-134">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="c751a-135">видеодиск</span><span class="sxs-lookup"><span data-stu-id="c751a-135">videodisk</span></span>    | <span data-ttu-id="c751a-136">псевдоним *\_ псевдонима устройства*, который является общим</span><span class="sxs-lookup"><span data-stu-id="c751a-136">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="c751a-137">Тип *устройства \_* типа</span><span class="sxs-lookup"><span data-stu-id="c751a-137">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="c751a-138">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="c751a-138">waveaudio</span></span>    | <span data-ttu-id="c751a-139">псевдоним *для \_ псевдонима устройства* *\_ Размер буфера*</span><span class="sxs-lookup"><span data-stu-id="c751a-139">alias *device\_alias* buffer *buffer\_size*</span></span>                     | <span data-ttu-id="c751a-140">*\_ тип устройства* совместного типа</span><span class="sxs-lookup"><span data-stu-id="c751a-140">sharable type *device\_type*</span></span>                                                    |



 

<span data-ttu-id="c751a-141">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзопенфлагс** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="c751a-141">The following table lists the flags that can be specified in the **lpszOpenFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="c751a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c751a-142">Value</span></span>                 | <span data-ttu-id="c751a-143">Значение</span><span class="sxs-lookup"><span data-stu-id="c751a-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c751a-144">псевдоним *устройства \_* псевдонима</span><span class="sxs-lookup"><span data-stu-id="c751a-144">alias *device\_alias*</span></span> | <span data-ttu-id="c751a-145">Указывает альтернативное имя для данного устройства.</span><span class="sxs-lookup"><span data-stu-id="c751a-145">Specifies an alternate name for the given device.</span></span> <span data-ttu-id="c751a-146">Если этот параметр указан, он должен использоваться в *качестве \_ идентификатора устройства* в последующих командах.</span><span class="sxs-lookup"><span data-stu-id="c751a-146">If specified, it must be used as the *device\_id* in subsequent commands.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="c751a-147">*ElementName*</span><span class="sxs-lookup"><span data-stu-id="c751a-147">*elementname*</span></span>         | <span data-ttu-id="c751a-148">Указывает имя элемента устройства (файла), загружаемого при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="c751a-148">Specifies the name of the device element (file) loaded when the device opens.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c751a-149">*\_ Размер буфера* буфера</span><span class="sxs-lookup"><span data-stu-id="c751a-149">buffer *buffer\_size*</span></span> | <span data-ttu-id="c751a-150">Задает размер (в секундах) буфера, используемого устройством аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="c751a-150">Sets the size, in seconds, of the buffer used by the waveform-audio device.</span></span> <span data-ttu-id="c751a-151">Размер буфера по умолчанию задается при установке или настройке устройства аудио-аудио.</span><span class="sxs-lookup"><span data-stu-id="c751a-151">The default size of the buffer is set when the waveform-audio device is installed or configured.</span></span> <span data-ttu-id="c751a-152">Обычно размер буфера устанавливается равным 4 секундам.</span><span class="sxs-lookup"><span data-stu-id="c751a-152">Typically the buffer size is set to 4 seconds.</span></span> <span data-ttu-id="c751a-153">При использовании устройства МЦИВАВЕ минимальный размер составляет 2 секунды, а максимальный размер — 9 секунд.</span><span class="sxs-lookup"><span data-stu-id="c751a-153">With the MCIWAVE device, the minimum size is 2 seconds and the maximum size is 9 seconds.</span></span>                                                |
| <span data-ttu-id="c751a-154">Родительский *HWND*</span><span class="sxs-lookup"><span data-stu-id="c751a-154">parent *hwnd*</span></span>         | <span data-ttu-id="c751a-155">Задает маркер окна родительского окна.</span><span class="sxs-lookup"><span data-stu-id="c751a-155">Specifies the window handle of the parent window.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="c751a-156">общим</span><span class="sxs-lookup"><span data-stu-id="c751a-156">sharable</span></span>              | <span data-ttu-id="c751a-157">Инициализирует устройство или файл как совместно используемый.</span><span class="sxs-lookup"><span data-stu-id="c751a-157">Initializes the device or file as sharable.</span></span> <span data-ttu-id="c751a-158">Последующие попытки открыть устройство или файл завершатся ошибкой, если не указать параметр "совместное с общим" как в исходной, так и в последующих **открытых** командах.</span><span class="sxs-lookup"><span data-stu-id="c751a-158">Subsequent attempts to open the device or file fail unless you specify "sharable" in both the original and subsequent **open** commands.</span></span> <span data-ttu-id="c751a-159">MCI возвращает недопустимую ошибку устройства, если устройство уже открыто и не является общим.</span><span class="sxs-lookup"><span data-stu-id="c751a-159">MCI returns an invalid device error if the device is already open and not sharable.</span></span><br/> <span data-ttu-id="c751a-160">Устройства Sequencer и МЦИВАВЕ МЦИСЕК не поддерживают общие файлы.</span><span class="sxs-lookup"><span data-stu-id="c751a-160">The MCISEQ sequencer and MCIWAVE devices do not support shared files.</span></span><br/> |
| <span data-ttu-id="c751a-161">дочерний стиль</span><span class="sxs-lookup"><span data-stu-id="c751a-161">style child</span></span>           | <span data-ttu-id="c751a-162">Открывает окно с стилем дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="c751a-162">Opens a window with a child window style.</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="c751a-163">перекрытие стилей</span><span class="sxs-lookup"><span data-stu-id="c751a-163">style overlapped</span></span>      | <span data-ttu-id="c751a-164">Открывает окно с перекрывающейся стилем окна.</span><span class="sxs-lookup"><span data-stu-id="c751a-164">Opens a window with an overlapped window style.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c751a-165">всплывающее окно стиля</span><span class="sxs-lookup"><span data-stu-id="c751a-165">style popup</span></span>           | <span data-ttu-id="c751a-166">Открывает окно со стилем всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="c751a-166">Opens a window with a pop-up window style.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c751a-167">*\_ тип стиля* стиля</span><span class="sxs-lookup"><span data-stu-id="c751a-167">style *style\_type*</span></span>   | <span data-ttu-id="c751a-168">Указывает стиль окна.</span><span class="sxs-lookup"><span data-stu-id="c751a-168">Indicates a window style.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="c751a-169">Тип *устройства \_* типа</span><span class="sxs-lookup"><span data-stu-id="c751a-169">type *device\_type*</span></span>   | <span data-ttu-id="c751a-170">Указывает тип устройства для файла.</span><span class="sxs-lookup"><span data-stu-id="c751a-170">Specifies the device type of a file.</span></span>                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="c751a-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="c751a-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="c751a-172">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="c751a-172">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="c751a-173">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c751a-173">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c751a-174">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c751a-174">Return Value</span></span>

<span data-ttu-id="c751a-175">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c751a-175">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c751a-176">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c751a-176">Remarks</span></span>

<span data-ttu-id="c751a-177">MCI резервирует "кдаудио" для типа устройства CD Audio, "видеодиск" для типа устройства "видеодиск", "Sequencer" для типа устройства "устройство Sequencer", "Авивидео" для типа устройства "цифровое видео" и "вавеаудио" для типа устройства аудио-Audio.</span><span class="sxs-lookup"><span data-stu-id="c751a-177">MCI reserves "cdaudio" for the CD audio device type, "videodisc" for the videodisc device type, "sequencer" for the MIDI sequencer device type, "AVIVideo" for the digital-video device type, and "waveaudio" for the waveform-audio device type.</span></span>

<span data-ttu-id="c751a-178">В качестве альтернативы флагу "тип" MCI может выбрать устройство на основе расширения, используемого файлом, как записано в реестре или в \[ разделе расширения MCI \] файла SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="c751a-178">As an alternative to the "type" flag, MCI can select the device based on the extension used by the file, as recorded in the registry or the \[mci extension\] section of the SYSTEM.INI file.</span></span>

<span data-ttu-id="c751a-179">MCI может открывать AVI-файлы с помощью указателя на файловый интерфейс или указателя на потоковый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c751a-179">MCI can open AVI files by using a file-interface pointer or a stream-interface pointer.</span></span> <span data-ttu-id="c751a-180">Чтобы открыть файл с помощью любого типа указателя интерфейса, укажите символ @, за которым следует указатель интерфейса вместо имени файла или устройства для параметра *лпсздевице* .</span><span class="sxs-lookup"><span data-stu-id="c751a-180">To open a file by using either type of interface pointer, specify an at sign (@) followed by the interface pointer in place of the file or device name for the *lpszDevice* parameter.</span></span> <span data-ttu-id="c751a-181">Дополнительные сведения об интерфейсах файлов и потоков см. в разделе " [функции и макросы авифиле](avifile-functions-and-macros.md)".</span><span class="sxs-lookup"><span data-stu-id="c751a-181">For more information about the file and stream interfaces, see " [AVIFile Functions and Macros](avifile-functions-and-macros.md)."</span></span>

<span data-ttu-id="c751a-182">Следующая команда открывает устройство "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="c751a-182">The following command opens the "mysound" device.</span></span>

``` syntax
open new type waveaudio alias mysound buffer 6
```

<span data-ttu-id="c751a-183">С именем устройства "New" драйвер аудио подготавливает новый ресурс волны.</span><span class="sxs-lookup"><span data-stu-id="c751a-183">With device name "new", the waveform driver prepares a new waveform resource.</span></span> <span data-ttu-id="c751a-184">Команда назначает псевдоним устройства "мисаунд" и задает 6-секундный буфер.</span><span class="sxs-lookup"><span data-stu-id="c751a-184">The command assigns the device alias "mysound" and specifies a 6-second buffer.</span></span>

<span data-ttu-id="c751a-185">Можно удалить флаг "тип", если имя устройства сопоставлено с именем файла.</span><span class="sxs-lookup"><span data-stu-id="c751a-185">You can eliminate the "type" flag if you combine the device name with the filename.</span></span> <span data-ttu-id="c751a-186">MCI распознает это сочетание при использовании следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="c751a-186">MCI recognizes this combination when you use the following syntax:</span></span>

<span data-ttu-id="c751a-187">*\_ имя устройства*</span><span class="sxs-lookup"><span data-stu-id="c751a-187">*device\_name* !</span></span> <span data-ttu-id="c751a-188">*\_имя элемента*</span><span class="sxs-lookup"><span data-stu-id="c751a-188">*element\_name*</span></span>

<span data-ttu-id="c751a-189">Восклицательный знак отделяет имя устройства от имени файла.</span><span class="sxs-lookup"><span data-stu-id="c751a-189">The exclamation point separates the device name from the filename.</span></span> <span data-ttu-id="c751a-190">Восклицательный знак не должен разделяться пробелами.</span><span class="sxs-lookup"><span data-stu-id="c751a-190">The exclamation point should not be delimited by white spaces.</span></span>

<span data-ttu-id="c751a-191">В следующем примере открывается право. WAV файл с помощью устройства "вавеаудио".</span><span class="sxs-lookup"><span data-stu-id="c751a-191">The following example opens the RIGHT.WAV file using the "waveaudio" device.</span></span>

``` syntax
open waveaudio!right.wav
```

<span data-ttu-id="c751a-192">Драйвер МЦИВАВЕ требует наличия асинхронного устройства аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="c751a-192">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="c751a-193">Требования</span><span class="sxs-lookup"><span data-stu-id="c751a-193">Requirements</span></span>



| <span data-ttu-id="c751a-194">Требование</span><span class="sxs-lookup"><span data-stu-id="c751a-194">Requirement</span></span> | <span data-ttu-id="c751a-195">Значение</span><span class="sxs-lookup"><span data-stu-id="c751a-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c751a-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c751a-196">Minimum supported client</span></span><br/> | <span data-ttu-id="c751a-197">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c751a-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c751a-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c751a-198">Minimum supported server</span></span><br/> | <span data-ttu-id="c751a-199">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c751a-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c751a-200">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c751a-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="c751a-201"><dt>Корекрт \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="c751a-201"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c751a-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c751a-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c751a-203">MCI</span><span class="sxs-lookup"><span data-stu-id="c751a-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c751a-204">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="c751a-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

