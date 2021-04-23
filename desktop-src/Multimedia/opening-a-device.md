---
title: Открытие устройства
description: Открытие устройства
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- Команда MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069853"
---
# <a name="opening-a-device"></a><span data-ttu-id="fe186-104">Открытие устройства</span><span class="sxs-lookup"><span data-stu-id="fe186-104">Opening a Device</span></span>

<span data-ttu-id="fe186-105">Перед использованием устройства его необходимо инициализировать с помощью команды [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="fe186-105">Before using a device, you must initialize it by using the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="fe186-106">Эта команда загружает драйвер в память (если он еще не загружен) и получает идентификатор устройства, который будет использоваться для идентификации устройства в последующих командах MCI.</span><span class="sxs-lookup"><span data-stu-id="fe186-106">This command loads the driver into memory (if it isn't already loaded) and retrieves the device identifier you will use to identify the device in subsequent MCI commands.</span></span> <span data-ttu-id="fe186-107">Необходимо проверить возвращаемое значение функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) или [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) перед использованием нового идентификатора устройства, чтобы убедиться, что идентификатор является допустимым.</span><span class="sxs-lookup"><span data-stu-id="fe186-107">You should check the return value of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function before using a new device identifier to ensure that the identifier is valid.</span></span> <span data-ttu-id="fe186-108">(Идентификатор устройства можно также получить с помощью функции [**мЦижетдевицеид**](/previous-versions//dd757156(v=vs.85)) .)</span><span class="sxs-lookup"><span data-stu-id="fe186-108">(You can also retrieve a device identifier by using the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.)</span></span>

<span data-ttu-id="fe186-109">Как и все сообщения команды MCI, у **MCI \_ открыта** связанная структура.</span><span class="sxs-lookup"><span data-stu-id="fe186-109">Like all MCI command messages, **MCI\_OPEN** has an associated structure.</span></span> <span data-ttu-id="fe186-110">Эти структуры иногда называются *блоками параметров*.</span><span class="sxs-lookup"><span data-stu-id="fe186-110">These structures are sometimes called *parameter blocks*.</span></span> <span data-ttu-id="fe186-111">Структура по умолчанию для **MCI \_ открыта** — [**MCI \_ Open \_ пармс**](mci-open-parms.md).</span><span class="sxs-lookup"><span data-stu-id="fe186-111">The default structure for **MCI\_OPEN** is [**MCI\_OPEN\_PARMS**](mci-open-parms.md).</span></span> <span data-ttu-id="fe186-112">Некоторые устройства ( *например,* звуковая волна и *наложение*) имеют расширенные структуры (такие как [**MCI \_ Wave \_ Open \_ пармс**](mci-wave-open-parms.md) и [**MCI \_ овли \_ Open \_ пармс**](mci-ovly-open-parms.md)) для размещения дополнительных необязательных параметров.</span><span class="sxs-lookup"><span data-stu-id="fe186-112">Certain devices (such as *waveform* and *overlay*) have extended structures (such as [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) and [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md)) to accommodate additional optional parameters.</span></span> <span data-ttu-id="fe186-113">Если вы не хотите использовать эти дополнительные параметры, можно использовать структуру **MCI \_ Open \_ пармс** с любым устройством MCI.</span><span class="sxs-lookup"><span data-stu-id="fe186-113">Unless you need to use these additional parameters, you can use the **MCI\_OPEN\_PARMS** structure with any MCI device.</span></span>

<span data-ttu-id="fe186-114">Число открытых устройств ограничено только объемом доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="fe186-114">The number of devices you can have open is limited only by the amount of available memory.</span></span>

## <a name="using-an-alias"></a><span data-ttu-id="fe186-115">Использование псевдонима</span><span class="sxs-lookup"><span data-stu-id="fe186-115">Using an Alias</span></span>

<span data-ttu-id="fe186-116">При открытии устройства можно использовать флаг "псевдоним", чтобы указать идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-116">When you open a device, you can use the "alias" flag to specify a device identifier for the device.</span></span> <span data-ttu-id="fe186-117">Этот флаг позволяет назначить короткий идентификатор устройства для составных устройств с длинными именами файлов и позволяет открыть несколько экземпляров одного и того же файла или устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-117">This flag lets you assign a short device identifier for compound devices with lengthy filenames, and it lets you open multiple instances of the same file or device.</span></span>

<span data-ttu-id="fe186-118">Например, следующая команда присваивает идентификатору устройства "бирдкалл" длинное имя файла C: \\ набирдс \\ Sounds \\ моккмтнг. ОБЪЕМ</span><span class="sxs-lookup"><span data-stu-id="fe186-118">For example, the following command assigns the device identifier "birdcall" to the lengthy filename C:\\NABIRDS\\SOUNDS\\MOCKMTNG.WAV:</span></span>


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="fe186-119">В интерфейсе сообщения командной строки псевдоним указывается с помощью элемента **лпстралиас** структуры [**MCI \_ Open \_ пармс**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="fe186-119">In the command-message interface, you specify an alias by using the **lpstrAlias** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="specifying-a-device-type"></a><span data-ttu-id="fe186-120">Указание типа устройства</span><span class="sxs-lookup"><span data-stu-id="fe186-120">Specifying a Device Type</span></span>

<span data-ttu-id="fe186-121">При открытии устройства можно использовать флаг "тип" для ссылки на тип устройства, а не на конкретный драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-121">When you open a device, you can use the "type" flag to refer to a device type, rather than to a specific device driver.</span></span> <span data-ttu-id="fe186-122">В следующем примере открывается файл волнового аудио C: \\ Windows \\ чимес. WAV (с помощью флага "тип" укажите тип устройства **вавеаудио** ) и назначает псевдоним "чимес":</span><span class="sxs-lookup"><span data-stu-id="fe186-122">The following example opens the waveform-audio file C:\\WINDOWS\\CHIMES.WAV (using the "type" flag to specify the **waveaudio** device type) and assigns the alias "chimes":</span></span>


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="fe186-123">В интерфейсе командного сообщения функциональность флага "Type" предоставляется членом **лпстрдевицетипе** структуры [**\_ \_ пармс, открытой в MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="fe186-123">In the command-message interface, the functionality of the "type" flag is supplied by the **lpstrDeviceType** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="simple-and-compound-devices"></a><span data-ttu-id="fe186-124">Простые и составные устройства</span><span class="sxs-lookup"><span data-stu-id="fe186-124">Simple and Compound Devices</span></span>

<span data-ttu-id="fe186-125">MCI классифицирует драйверы устройств как *Составные* или *простые*.</span><span class="sxs-lookup"><span data-stu-id="fe186-125">MCI classifies device drivers as *compound* or *simple*.</span></span> <span data-ttu-id="fe186-126">Драйверам для составных устройств требуется имя файла данных для воспроизведения. драйверы для простых устройств не имеют.</span><span class="sxs-lookup"><span data-stu-id="fe186-126">Drivers for compound devices require the name of a data file for playback; drivers for simple devices do not.</span></span>

<span data-ttu-id="fe186-127">К простым устройствам относятся устройства **кдаудио** и **видеодиск** .</span><span class="sxs-lookup"><span data-stu-id="fe186-127">Simple devices include **cdaudio** and **videodisc** devices.</span></span> <span data-ttu-id="fe186-128">Существует два способа открытия простых устройств:</span><span class="sxs-lookup"><span data-stu-id="fe186-128">There are two ways to open simple devices:</span></span>

-   <span data-ttu-id="fe186-129">Укажите указатель на строку, заканчивающуюся нулем, которая содержит имя устройства из реестра или файла SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="fe186-129">Specify a pointer to a null-terminated string containing the device name from the registry or the SYSTEM.INI file.</span></span>

    <span data-ttu-id="fe186-130">Например, можно открыть устройство **видеодиск** с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="fe186-130">For example, you can open a **videodisc** device by using the following command:</span></span>


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="fe186-131">В этом случае "видеодиск" — это имя устройства из реестра или \[ \] раздела MCI SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="fe186-131">In this case, "videodisc" is the device name from the registry or the \[mci\] section of SYSTEM.INI.</span></span>

-   <span data-ttu-id="fe186-132">Укажите фактическое имя драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-132">Specify the actual name of the device driver.</span></span> <span data-ttu-id="fe186-133">Тем не менее, при открытии устройства с помощью имени файла драйвера устройства приложение будет зависят от устройства и может препятствовать его запуску при изменении конфигурации системы.</span><span class="sxs-lookup"><span data-stu-id="fe186-133">Opening a device using the device-driver filename, however, makes the application device-specific and can prevent the application from running if the system configuration changes.</span></span> <span data-ttu-id="fe186-134">Если используется имя файла, указывать полный путь или расширение имени файла не требуется. MCI предполагает, что драйверы расположены в системном каталоге и имеют. Расширение имени файла DRV.</span><span class="sxs-lookup"><span data-stu-id="fe186-134">If you use a filename, you do not need to specify the complete path or the filename extension; MCI assumes drivers are located in a system directory and have the .DRV filename extension.</span></span>

<span data-ttu-id="fe186-135">Составные устройства включают устройства **вавеаудио** и **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="fe186-135">Compound devices include **waveaudio** and **sequencer** devices.</span></span> <span data-ttu-id="fe186-136">Данные для составного устройства иногда называются *элементом устройства*.</span><span class="sxs-lookup"><span data-stu-id="fe186-136">The data for a compound device is sometimes called a *device element*.</span></span> <span data-ttu-id="fe186-137">Этот документ, однако, обычно относится к этим данным как к файлу, хотя в некоторых случаях данные могут не храниться в виде файла.</span><span class="sxs-lookup"><span data-stu-id="fe186-137">This document, however, generally refers to this data as a file, even though in some cases the data might not be stored as a file.</span></span>

<span data-ttu-id="fe186-138">Существует три способа открытия составного устройства:</span><span class="sxs-lookup"><span data-stu-id="fe186-138">There are three ways to open a compound device:</span></span>

-   <span data-ttu-id="fe186-139">Укажите только имя устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-139">Specify only the device name.</span></span> <span data-ttu-id="fe186-140">Это позволяет открыть составное устройство без сопоставления имени файла.</span><span class="sxs-lookup"><span data-stu-id="fe186-140">This lets you open a compound device without associating a filename.</span></span> <span data-ttu-id="fe186-141">Большинство составных устройств обрабатывают только команды [**( \_ MCI жетдевкапс**](mci-getdevcaps.md)) и [**Close**](close.md) ([**MCI \_ Close**](mci-close.md) [**), если**](capability.md) они открыты таким образом.</span><span class="sxs-lookup"><span data-stu-id="fe186-141">Most compound devices process only the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) commands when they are opened this way.</span></span>
-   <span data-ttu-id="fe186-142">Укажите только имя файла.</span><span class="sxs-lookup"><span data-stu-id="fe186-142">Specify only the filename.</span></span> <span data-ttu-id="fe186-143">Имя устройства определяется из сопоставлений в реестре.</span><span class="sxs-lookup"><span data-stu-id="fe186-143">The device name is determined from the associations in the registry.</span></span>
-   <span data-ttu-id="fe186-144">Укажите имя файла и название устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-144">Specify the filename and the device name.</span></span> <span data-ttu-id="fe186-145">MCI игнорирует записи в реестре и открывает указанное имя устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-145">MCI ignores the entries in the registry and opens the specified device name.</span></span>

<span data-ttu-id="fe186-146">Чтобы связать файл данных с определенным устройством, можно указать имя файла и название устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-146">To associate a data file with a particular device, you can specify the filename and device name.</span></span> <span data-ttu-id="fe186-147">Например, следующая команда открывает устройство **вавеаудио** с именем файла мивоице. SND</span><span class="sxs-lookup"><span data-stu-id="fe186-147">For example, the following command opens the **waveaudio** device with the filename MYVOICE.SND:</span></span>


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="fe186-148">В интерфейсе командной строки можно также сократить спецификацию имени устройства, используя альтернативный формат восклицательного знака, как описано в команде [**Open**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="fe186-148">In the command-string interface, you can also abbreviate the device name specification by using the alternative exclamation-point format, as documented with the [**open**](open.md) command.</span></span>

## <a name="opening-a-device-using-the-filename-extension"></a><span data-ttu-id="fe186-149">Открытие устройства с помощью расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="fe186-149">Opening a Device Using the Filename Extension</span></span>

<span data-ttu-id="fe186-150">Если команда [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) указывает только имя файла, MCI использует расширение имени файла, чтобы выбрать соответствующее устройство из списка в реестре или в \[ разделе расширения MCI \] файла SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="fe186-150">If the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command specifies only the filename, MCI uses the filename extension to select the appropriate device from the list in the registry or the \[mci extensions\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="fe186-151">Записи в \[ разделе расширения MCI \] используют следующую форму:</span><span class="sxs-lookup"><span data-stu-id="fe186-151">The entries in the \[mci extensions\] section use the following form:</span></span>

<span data-ttu-id="fe186-152">имя *файла \_ расширение*  =  *\_ имени устройства*</span><span class="sxs-lookup"><span data-stu-id="fe186-152">*filename\_extension* = *device\_name*</span></span>

<span data-ttu-id="fe186-153">MCI неявно использует *\_ имя устройства* , если расширение найдено, и если имя устройства не указано в команде **Open** .</span><span class="sxs-lookup"><span data-stu-id="fe186-153">MCI implicitly uses *device\_name* if the extension is found and if a device name has not been specified in the **open** command.</span></span>

<span data-ttu-id="fe186-154">В следующем примере показан типичный \[ раздел модулей MCI \] .</span><span class="sxs-lookup"><span data-stu-id="fe186-154">The following example shows a typical \[mci extensions\] section:</span></span>


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



<span data-ttu-id="fe186-155">С помощью этих определений MCI открывает устройство **вавеаудио** , если выдана следующая команда:</span><span class="sxs-lookup"><span data-stu-id="fe186-155">Using these definitions, MCI opens the **waveaudio** device if the following command is issued:</span></span>


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a><span data-ttu-id="fe186-156">Новые файлы данных</span><span class="sxs-lookup"><span data-stu-id="fe186-156">New Data Files</span></span>

<span data-ttu-id="fe186-157">Чтобы создать новый файл данных, просто укажите пустое имя файла.</span><span class="sxs-lookup"><span data-stu-id="fe186-157">To create a new data file, simply specify a blank filename.</span></span> <span data-ttu-id="fe186-158">MCI не сохраняет новый файл, пока вы не сохраните его с помощью команды [**сохранить**](save.md) ([**MCI \_ Save**](mci-save.md)).</span><span class="sxs-lookup"><span data-stu-id="fe186-158">MCI does not save a new file until you save it by using the [**save**](save.md) ([**MCI\_SAVE**](mci-save.md)) command.</span></span> <span data-ttu-id="fe186-159">При создании нового файла необходимо включить псевдоним устройства с помощью команды [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="fe186-159">When creating a new file, you must include a device alias with the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="fe186-160">В следующем примере открывается новый файл **вавеаудио** , запускается и останавливается запись, затем сохраняется и закрывается файл:</span><span class="sxs-lookup"><span data-stu-id="fe186-160">The following example opens a new **waveaudio** file, starts and stops recording, then saves and closes the file:</span></span>


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a><span data-ttu-id="fe186-161">Устройства, которые совместное с общим</span><span class="sxs-lookup"><span data-stu-id="fe186-161">Sharable Devices</span></span>

<span data-ttu-id="fe186-162">Флаг "общий доступ" (с возможностью совместной \_ \_ работы в виде MCI) команды [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) позволяет нескольким приложениям одновременно обращаться к одному устройству (или файлу) и экземпляру устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-162">The "sharable" (MCI\_OPEN\_SHAREABLE) flag of the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command lets multiple applications access the same device (or file) and device instance simultaneously.</span></span> <span data-ttu-id="fe186-163">Если приложение открывает устройство или файл в качестве совместного доступа, другие приложения также могут получить к нему доступ, открыв его как совместное применение.</span><span class="sxs-lookup"><span data-stu-id="fe186-163">If your application opens a device or file as sharable, other applications can also access it by opening it as sharable.</span></span> <span data-ttu-id="fe186-164">Общее устройство или файл предоставляет каждому приложению возможность изменять параметры, управляющие его состоянием работы.</span><span class="sxs-lookup"><span data-stu-id="fe186-164">The shared device or file gives each application the ability to change the parameters governing its operating state.</span></span> <span data-ttu-id="fe186-165">При каждом открытии устройства или файла как доступного для совместного выполнения MCI Возвращает уникальный идентификатор устройства, даже если идентификаторы ссылаются на один и тот же экземпляр.</span><span class="sxs-lookup"><span data-stu-id="fe186-165">Each time a device or file is opened as sharable, MCI returns a unique device identifier, even though the identifiers refer to the same instance.</span></span>

<span data-ttu-id="fe186-166">Если приложение открывает устройство или файл без указания возможности совместного использования, другие приложения не смогут получить к нему доступ, пока приложение не закроет его.</span><span class="sxs-lookup"><span data-stu-id="fe186-166">If your application opens a device or file without specifying that it is sharable, no other application can access it until your application closes it.</span></span> <span data-ttu-id="fe186-167">Кроме того, если устройство поддерживает только один открытый экземпляр, команда **Open** завершится ошибкой, если указать флаг с общим состоянием.</span><span class="sxs-lookup"><span data-stu-id="fe186-167">Also, if a device supports only one open instance, the **open** command will fail if you specify the sharable flag.</span></span>

<span data-ttu-id="fe186-168">Если приложение открывает устройство и указывает, что оно доступно для совместного использования, приложение не должно делать никаких предположений о состоянии этого устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-168">If your application opens a device and specifies that it is sharable, your application should not make any assumptions about the state of this device.</span></span> <span data-ttu-id="fe186-169">Приложению может потребоваться компенсировать изменения, внесенные другими приложениями, обращающимися к устройству.</span><span class="sxs-lookup"><span data-stu-id="fe186-169">Your application might need to compensate for changes made by other applications accessing the device.</span></span>

<span data-ttu-id="fe186-170">Большинство составных файлов не могут совместно быть объединены. Однако можно открыть несколько файлов или несколько раз открыть один файл.</span><span class="sxs-lookup"><span data-stu-id="fe186-170">Most compound files are not sharable; however, you can open multiple files, or you can open a single file multiple times.</span></span> <span data-ttu-id="fe186-171">Если один файл открывается несколько раз, MCI создает независимый экземпляр для каждого экземпляра с уникальным состоянием операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fe186-171">If you open a single file multiple times, MCI creates an independent instance for each, with each instance having a unique operating status.</span></span>

<span data-ttu-id="fe186-172">При открытии нескольких экземпляров файла необходимо назначить каждому из них уникальный идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="fe186-172">If you open multiple instances of a file, you must assign a unique device identifier to each.</span></span> <span data-ttu-id="fe186-173">Можно использовать псевдоним, как описано в следующем разделе, чтобы назначить уникальное имя для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="fe186-173">You can use an alias, as described in the following section, to assign a unique name for each file.</span></span>

 

 