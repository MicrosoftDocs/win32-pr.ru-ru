---
description: В этом разделе приведены ссылки на записи, которые можно использовать в файле autorun. INF. Запись состоит из ключа и значения.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Записи autorun. INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262921"
---
# <a name="autoruninf-entries"></a><span data-ttu-id="f70be-104">Записи autorun. INF</span><span class="sxs-lookup"><span data-stu-id="f70be-104">Autorun.inf Entries</span></span>

<span data-ttu-id="f70be-105">В этом разделе приведены ссылки на записи, которые можно использовать в файле autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="f70be-105">This topic is a reference for the entries that can be used in an Autorun.inf file.</span></span> <span data-ttu-id="f70be-106">Запись состоит из ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="f70be-106">An entry consists of a key and a value.</span></span>

-   <span data-ttu-id="f70be-107">[\[Ключи автозапуска \]](#autorun-keys)</span><span class="sxs-lookup"><span data-stu-id="f70be-107">[\[AutoRun\] Keys](#autorun-keys)</span></span>
    -   [<span data-ttu-id="f70be-108">action</span><span class="sxs-lookup"><span data-stu-id="f70be-108">action</span></span>](#parameters)
    -   [<span data-ttu-id="f70be-109">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="f70be-109">CustomEvent</span></span>](#customevent)
    -   [<span data-ttu-id="f70be-110">значок</span><span class="sxs-lookup"><span data-stu-id="f70be-110">icon</span></span>](#parameters)
    -   [<span data-ttu-id="f70be-111">label</span><span class="sxs-lookup"><span data-stu-id="f70be-111">label</span></span>](#parameters)
    -   [<span data-ttu-id="f70be-112">open</span><span class="sxs-lookup"><span data-stu-id="f70be-112">open</span></span>](#parameters)
    -   [<span data-ttu-id="f70be-113">усеаутоплай</span><span class="sxs-lookup"><span data-stu-id="f70be-113">UseAutoPlay</span></span>](#parameters)
    -   [<span data-ttu-id="f70be-114">вызов</span><span class="sxs-lookup"><span data-stu-id="f70be-114">shellexecute</span></span>](#shellexecute)
    -   [<span data-ttu-id="f70be-115">консоль</span><span class="sxs-lookup"><span data-stu-id="f70be-115">shell</span></span>](#autoruninf-entries)
    -   [<span data-ttu-id="f70be-116">\\команда оболочки</span><span class="sxs-lookup"><span data-stu-id="f70be-116">shell\\verb</span></span>](#shellverb)
-   <span data-ttu-id="f70be-117">[\[\]Ключи содержимого](#content-keys)</span><span class="sxs-lookup"><span data-stu-id="f70be-117">[\[Content\] Keys](#content-keys)</span></span>
-   <span data-ttu-id="f70be-118">[\[\]Ключи ексклусивеконтентпасс](#exclusivecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="f70be-118">[\[ExclusiveContentPaths\] Keys](#exclusivecontentpaths-keys)</span></span>
-   <span data-ttu-id="f70be-119">[\[\]Ключи игнореконтентпасс](#ignorecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="f70be-119">[\[IgnoreContentPaths\] Keys](#ignorecontentpaths-keys)</span></span>
-   <span data-ttu-id="f70be-120">[\[\]Ключи девицеинсталл](#deviceinstall-keys)</span><span class="sxs-lookup"><span data-stu-id="f70be-120">[\[DeviceInstall\] Keys](#deviceinstall-keys)</span></span>
    -   [<span data-ttu-id="f70be-121">DriverPath</span><span class="sxs-lookup"><span data-stu-id="f70be-121">DriverPath</span></span>](#driverpath)

## <a name="autorun-keys"></a><span data-ttu-id="f70be-122">\[Ключи автозапуска \]</span><span class="sxs-lookup"><span data-stu-id="f70be-122">\[AutoRun\] Keys</span></span>

-   [<span data-ttu-id="f70be-123">action</span><span class="sxs-lookup"><span data-stu-id="f70be-123">action</span></span>](#parameters)
-   [<span data-ttu-id="f70be-124">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="f70be-124">CustomEvent</span></span>](#customevent)
-   [<span data-ttu-id="f70be-125">значок</span><span class="sxs-lookup"><span data-stu-id="f70be-125">icon</span></span>](#parameters)
-   [<span data-ttu-id="f70be-126">label</span><span class="sxs-lookup"><span data-stu-id="f70be-126">label</span></span>](#parameters)
-   [<span data-ttu-id="f70be-127">open</span><span class="sxs-lookup"><span data-stu-id="f70be-127">open</span></span>](#parameters)
-   [<span data-ttu-id="f70be-128">усеаутоплай</span><span class="sxs-lookup"><span data-stu-id="f70be-128">UseAutoPlay</span></span>](#parameters)
-   [<span data-ttu-id="f70be-129">вызов</span><span class="sxs-lookup"><span data-stu-id="f70be-129">shellexecute</span></span>](#shellexecute)
-   [<span data-ttu-id="f70be-130">консоль</span><span class="sxs-lookup"><span data-stu-id="f70be-130">shell</span></span>](#autoruninf-entries)
-   [<span data-ttu-id="f70be-131">\\команда оболочки</span><span class="sxs-lookup"><span data-stu-id="f70be-131">shell\\verb</span></span>](#shellverb)

### <a name="action"></a><span data-ttu-id="f70be-132">action</span><span class="sxs-lookup"><span data-stu-id="f70be-132">action</span></span>

<span data-ttu-id="f70be-133">Запись **действия** указывает текст, используемый в диалоговом окне автозапуска для обработчика, представляющего программу, указанную в записи [Open](#parameters) или [ShellExecute](#shellexecute) в файле autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="f70be-133">The **action** entry specifies the text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span> <span data-ttu-id="f70be-134">Значение может быть выражено как текст или как ресурс, хранящийся в двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="f70be-134">The value can be expressed as either text or as a resource stored in a binary.</span></span>


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a><span data-ttu-id="f70be-135">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-135">Parameters</span></span>

-   <span data-ttu-id="f70be-136">*актионтекст*</span><span class="sxs-lookup"><span data-stu-id="f70be-136">*ActionText*</span></span>

    <span data-ttu-id="f70be-137">Текст, который используется в диалоговом окне автозапуска для обработчика, представляющего программу, указанную в записи [Open](#parameters) или [ShellExecute](#shellexecute) в файле autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="f70be-137">Text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span>

-   <span data-ttu-id="f70be-138">*равно*</span><span class="sxs-lookup"><span data-stu-id="f70be-138">*filepath*</span></span>

    <span data-ttu-id="f70be-139">Строка, содержащая полный путь к каталогу, содержащему двоичный файл, содержащий строку.</span><span class="sxs-lookup"><span data-stu-id="f70be-139">A string that contains the fully qualified path of the directory that contains the binary file containing the string.</span></span> <span data-ttu-id="f70be-140">Если путь не указан, файл должен находиться в корневом каталоге диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-140">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="f70be-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="f70be-141">*filename*</span></span>

    <span data-ttu-id="f70be-142">Строка, содержащая имя двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="f70be-142">A string that contains the binary file's name.</span></span>

-   <span data-ttu-id="f70be-143">*Идентификатора*</span><span class="sxs-lookup"><span data-stu-id="f70be-143">*resourceID*</span></span>

    <span data-ttu-id="f70be-144">Идентификатор строки в двоичном файле.</span><span class="sxs-lookup"><span data-stu-id="f70be-144">The ID of the string within the binary file.</span></span>

### <a name="remarks"></a><span data-ttu-id="f70be-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-145">Remarks</span></span>

<span data-ttu-id="f70be-146">Ключ **действия** используется только в Windows XP с пакетом обновления 2 (SP2) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="f70be-146">The **action** key is only used in Windows XP Service Pack 2 (SP2) or later.</span></span> <span data-ttu-id="f70be-147">Поддерживается только для дисков типа " \_ съемный диск" и " \_ ФИКСИРОВАНный диск".</span><span class="sxs-lookup"><span data-stu-id="f70be-147">It is only supported for drives of type DRIVE\_REMOVABLE and DRIVE\_FIXED.</span></span> <span data-ttu-id="f70be-148">В случае \_ съемного диска требуется ключ **действия** .</span><span class="sxs-lookup"><span data-stu-id="f70be-148">In the case of DRIVE\_REMOVABLE, the **action** key is required.</span></span> <span data-ttu-id="f70be-149">Команда **действия** в файле autorun. INF звукового компакт-диска или фильма DVD пропускается, и эти носители продолжают работать как в Windows XP с пакетом обновления 1 (SP1) и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="f70be-149">An **action** command in the Autorun.inf file of an audio CD or movie DVD is ignored, and these media continue to behave as in Windows XP Service Pack 1 (SP1) and earlier.</span></span>

<span data-ttu-id="f70be-150">Строка, отображаемая в диалоговом окне автозапуска, создается путем объединения текста, указанного в записи **действия** , с жестко заданным именем поставщика, предоставленным оболочкой.</span><span class="sxs-lookup"><span data-stu-id="f70be-150">The string displayed in the Autoplay dialog is constructed by combining the text specified in the **action** entry with hard-coded text naming the provider, provided by the Shell.</span></span> <span data-ttu-id="f70be-151">Рядом с ним отображается [значок](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="f70be-151">The [icon](#parameters) is displayed next to it.</span></span> <span data-ttu-id="f70be-152">Эта запись всегда отображается как первый параметр в диалоговом окне Автозапуск и выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f70be-152">This entry always appears as the first option in the Autoplay dialog and is selected by default.</span></span> <span data-ttu-id="f70be-153">Если пользователь принимает параметр, запускается приложение, указанное в записи [Open](#parameters) или [ShellExecute](#shellexecute) файла autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="f70be-153">If the user accepts the option, the application specified by the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file is launched.</span></span> <span data-ttu-id="f70be-154">Параметр **всегда выполнять выбранное действие** недоступен в этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="f70be-154">The **Always do the selected action** option is not available in this situation.</span></span>

<span data-ttu-id="f70be-155">Сочетание клавиш [действия](#parameters) и [значка](#parameters) определяет представление приложения, видимое для конечного пользователя в диалоговом окне автозапуска.</span><span class="sxs-lookup"><span data-stu-id="f70be-155">The [action](#parameters) and [icon](#parameters) keys together define the representation of the application that is seen by the end user in the Autoplay dialog.</span></span> <span data-ttu-id="f70be-156">Они должны составляться таким образом, чтобы пользователи могли легко их определять.</span><span class="sxs-lookup"><span data-stu-id="f70be-156">They should be composed in such a way that users can easily identify them.</span></span> <span data-ttu-id="f70be-157">Они должны указывать приложение для выполнения, компанию, создавшую его, и все связанные фирменные символики.</span><span class="sxs-lookup"><span data-stu-id="f70be-157">They should indicate the application to be run, the company that created it, and any associated branding.</span></span>

<span data-ttu-id="f70be-158">Для обеспечения обратной совместимости запись **действия** является необязательной для устройств типа \_ фиксированное устройство.</span><span class="sxs-lookup"><span data-stu-id="f70be-158">For backward compatibility, the **action** entry is optional for devices of type DRIVE\_FIXED.</span></span> <span data-ttu-id="f70be-159">Для этого типа в диалоговом окне автозапуска используется запись по умолчанию, если в файле autorun. INF отсутствует запись **действия** .</span><span class="sxs-lookup"><span data-stu-id="f70be-159">For this type, a default entry is used in the Autoplay dialog if no **action** entry is present in the Autorun.inf file.</span></span>

<span data-ttu-id="f70be-160">Запись **действия** является обязательной для устройств типа " \_ съемный диск", до тех пор пока не будет добавлена поддержка autorun. INF.</span><span class="sxs-lookup"><span data-stu-id="f70be-160">The **action** entry is mandatory for devices of type DRIVE\_REMOVABLE, which until now did not have Autorun.inf support.</span></span> <span data-ttu-id="f70be-161">Если запись **действия** отсутствует, диалоговое окно автозапуска отображается, но не имеет параметра для запуска дополнительного содержимого.</span><span class="sxs-lookup"><span data-stu-id="f70be-161">If no **action** entry is present, the Autoplay dialog is displayed but with no option to launch the additional content.</span></span>

### <a name="customevent"></a><span data-ttu-id="f70be-162">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="f70be-162">CustomEvent</span></span>

<span data-ttu-id="f70be-163">Запись **CustomEvent** указывает событие пользовательского содержимого автозапуска.</span><span class="sxs-lookup"><span data-stu-id="f70be-163">The **CustomEvent** entry specifies a custom AutoPlay content event.</span></span>


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a><span data-ttu-id="f70be-164">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-164">Parameters</span></span>

-   <span data-ttu-id="f70be-165">*CustomEventName*</span><span class="sxs-lookup"><span data-stu-id="f70be-165">*CustomEventName*</span></span>

    <span data-ttu-id="f70be-166">Текстовая строка, содержащая имя события автозапуска содержимого.</span><span class="sxs-lookup"><span data-stu-id="f70be-166">A text string containing the name of the AutoPlay content event.</span></span> <span data-ttu-id="f70be-167">Имя должно содержать не более 100 алфавитно-цифровых символов.</span><span class="sxs-lookup"><span data-stu-id="f70be-167">The name must be no more than 100 alphanumeric characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="f70be-168">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-168">Remarks</span></span>

<span data-ttu-id="f70be-169">В файл autorun. INF тома можно включить имя пользовательского события.</span><span class="sxs-lookup"><span data-stu-id="f70be-169">You can include a custom event name in the Autorun.inf file of a volume.</span></span> <span data-ttu-id="f70be-170">Когда программа автозапуска запрашивает у пользователя приложение для использования с томом, оно отображает только те приложения, которые зарегистрированы для указанного имени пользовательского события.</span><span class="sxs-lookup"><span data-stu-id="f70be-170">When AutoPlay prompts the user for an application to use with the volume, it displays only applications that have registered for the specified custom event name.</span></span> <span data-ttu-id="f70be-171">Сведения о том, как зарегистрировать приложение в качестве обработчика для события пользовательского содержимого автозапуска, см. в разделе [Автоматический запуск с помощью](/previous-versions/windows/apps/hh452731(v=win.10)) автозапуска или [Регистрация обработчика событий](how-to-register-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="f70be-171">For information on how you can register an application as a handler for your custom AutoPlay content event, see [Auto-launching with AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) or [How to Register an Event Handler](how-to-register-an-event-handler.md).</span></span>

<span data-ttu-id="f70be-172">В следующем примере задается значение «Миконтентонарривал» в качестве нового события автоматического содержимого.</span><span class="sxs-lookup"><span data-stu-id="f70be-172">The following example specifies the value "MyContentOnArrival" as a new AutoPlay content event.</span></span>


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a><span data-ttu-id="f70be-173">icon</span><span class="sxs-lookup"><span data-stu-id="f70be-173">icon</span></span>

<span data-ttu-id="f70be-174">Запись **Icon** указывает значок, представляющий диск с поддержкой автозапуска в пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="f70be-174">The **icon** entry specifies an icon which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
icon=iconfilename[,index]
```



### <a name="parameters"></a><span data-ttu-id="f70be-175">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-175">Parameters</span></span>

-   <span data-ttu-id="f70be-176">*иконфиленаме*</span><span class="sxs-lookup"><span data-stu-id="f70be-176">*iconfilename*</span></span>

    <span data-ttu-id="f70be-177">Имя файла ICO, BMP, exe или DLL, содержащего сведения о значке.</span><span class="sxs-lookup"><span data-stu-id="f70be-177">Name of an .ico, .bmp, .exe, or .dll file containing the icon information.</span></span> <span data-ttu-id="f70be-178">Если файл содержит более одного значка, необходимо также указать Отсчитываемый от нуля индекс значка.</span><span class="sxs-lookup"><span data-stu-id="f70be-178">If a file contains more than one icon, you must also specify zero-based index of the icon.</span></span>

### <a name="remarks"></a><span data-ttu-id="f70be-179">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-179">Remarks</span></span>

<span data-ttu-id="f70be-180">Значок вместе с меткой представляет диск с поддержкой автозапуска в пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="f70be-180">The icon, together with the label, represents the AutoRun-enabled drive in the Windows user interface.</span></span> <span data-ttu-id="f70be-181">Например, в проводнике Windows диск представляется этим значком вместо стандартного значка диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-181">For instance, in Windows Explorer, the drive is represented by this icon instead of the standard drive icon.</span></span> <span data-ttu-id="f70be-182">Файл значка должен находиться в том же каталоге, что и файл, заданный командой [Open](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="f70be-182">The icon's file must be in the same directory as the file specified by the [open](#parameters) command.</span></span>

<span data-ttu-id="f70be-183">В следующем примере задается второй значок в файле MyProg.exe.</span><span class="sxs-lookup"><span data-stu-id="f70be-183">The following example specifies the second icon in the MyProg.exe file.</span></span>


```
icon=MyProg.exe,1
```



### <a name="label"></a><span data-ttu-id="f70be-184">метка</span><span class="sxs-lookup"><span data-stu-id="f70be-184">label</span></span>

<span data-ttu-id="f70be-185">В записи **метки** указывается текстовая метка, представляющая диск с поддержкой автозапуска в пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="f70be-185">The **label** entry specifies a text label which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
label=LabelText
```



### <a name="parameters"></a><span data-ttu-id="f70be-186">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-186">Parameters</span></span>

-   <span data-ttu-id="f70be-187">*LabelText*</span><span class="sxs-lookup"><span data-stu-id="f70be-187">*LabelText*</span></span>

    <span data-ttu-id="f70be-188">Текстовая строка, содержащая метку.</span><span class="sxs-lookup"><span data-stu-id="f70be-188">A text string containing the label.</span></span> <span data-ttu-id="f70be-189">Оно может содержать пробелы и не должно быть длиннее 32 символов.</span><span class="sxs-lookup"><span data-stu-id="f70be-189">It can contain spaces and should be no longer than 32 characters.</span></span>

> [!Note]  
> <span data-ttu-id="f70be-190">Можно указать значение в параметре **LabelText** , который превышает 32 символов и не получает сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f70be-190">It is possible to put a value in the **LabelText** parameter which exceeds 32 characters and receive no error message.</span></span> <span data-ttu-id="f70be-191">Однако система отображает только первые 32 символов.</span><span class="sxs-lookup"><span data-stu-id="f70be-191">However, the system only displays the first 32 characters.</span></span> <span data-ttu-id="f70be-192">Все символы после 32-го усекаются и не отображаются.</span><span class="sxs-lookup"><span data-stu-id="f70be-192">Any characters after the 32nd are truncated and not displayed.</span></span> <span data-ttu-id="f70be-193">Например, если **LabelText** имеет следующий вид: метка = "Этот компакт-диск предназначен для конечного музыкального компакт-диска".</span><span class="sxs-lookup"><span data-stu-id="f70be-193">For example, if the **LabelText** is as follows: label="This CD is designed to be the ultimate music CD."</span></span> <span data-ttu-id="f70be-194">появится следующее: "Этот компакт-диск рассчитан на UL".</span><span class="sxs-lookup"><span data-stu-id="f70be-194">the following will be displayed, "This CD is designed to be the ul".</span></span>

 

### <a name="remarks"></a><span data-ttu-id="f70be-195">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-195">Remarks</span></span>

<span data-ttu-id="f70be-196">Метка вместе со значком представляет диск с поддержкой автозапуска в пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="f70be-196">The label, together with an icon, represents the AutoRun-enabled drive in the Windows user interface.</span></span>

<span data-ttu-id="f70be-197">В следующем примере в качестве метки диска задается значение "моя метка диска".</span><span class="sxs-lookup"><span data-stu-id="f70be-197">The following example specifies the value "My Drive Label" as the drive's label.</span></span>


```
label=My Drive Label
```



### <a name="open"></a><span data-ttu-id="f70be-198">open</span><span class="sxs-lookup"><span data-stu-id="f70be-198">open</span></span>

<span data-ttu-id="f70be-199">**Открытая** запись указывает путь и имя файла приложения, которое запускается при вставке диска в дисковод.</span><span class="sxs-lookup"><span data-stu-id="f70be-199">The **open** entry specifies the path and file name of the application that AutoRun launches when a user inserts a disc in the drive.</span></span>


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a><span data-ttu-id="f70be-200">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-200">Parameters</span></span>

-   <span data-ttu-id="f70be-201">*exefile*</span><span class="sxs-lookup"><span data-stu-id="f70be-201">*exefile*</span></span>

    <span data-ttu-id="f70be-202">Полный путь к исполняемому файлу, запускаемому при вставке компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-202">Fully qualified path of an executable file that runs when the CD is inserted.</span></span> <span data-ttu-id="f70be-203">Если указано только имя файла, оно должно находиться в корневом каталоге диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-203">If only a file name is specified, it must be in drive's root directory.</span></span> <span data-ttu-id="f70be-204">Чтобы определить расположение файла в подкаталоге, необходимо указать путь.</span><span class="sxs-lookup"><span data-stu-id="f70be-204">To locate the file in a subdirectory, you must specify a path.</span></span> <span data-ttu-id="f70be-205">Можно также включить один или несколько параметров командной строки для передачи в запускаемое приложение.</span><span class="sxs-lookup"><span data-stu-id="f70be-205">You can also include one or more command-line parameters to pass to the startup application.</span></span>

### <a name="useautoplay"></a><span data-ttu-id="f70be-206">усеаутоплай</span><span class="sxs-lookup"><span data-stu-id="f70be-206">UseAutoPlay</span></span>

<span data-ttu-id="f70be-207">В Windows XP запись **усеаутоплай** указывает, что вместо автозапуска следует использовать автозапуск.</span><span class="sxs-lookup"><span data-stu-id="f70be-207">On Windows XP, the **UseAutoPlay** entry specifies that AutoPlay should be used instead of AutoRun.</span></span>

<span data-ttu-id="f70be-208">В Windows Vista и более поздних версиях эта запись приводит к подавлению каких-либо действий, заданных для автозапуска (с помощью записей **Open** или **ShellExecute** ), из диалогового окна автозапуска.</span><span class="sxs-lookup"><span data-stu-id="f70be-208">On Windows Vista and later, this entry causes any actions specified for AutoRun (by using either the **open** or **shellexecute** entries) to be suppressed from the AutoPlay dialog.</span></span> <span data-ttu-id="f70be-209">Эта запись не влияет на версии Windows, предшествующие Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f70be-209">This entry has no effect on versions of Windows earlier than Windows XP.</span></span>

<span data-ttu-id="f70be-210">В Windows 8 и более поздних версиях при указании значения 0 автозапуск для этого устройства будет отключен.</span><span class="sxs-lookup"><span data-stu-id="f70be-210">On Windows 8 and later, specifying a value of 0 will disable autoplay for this device.</span></span>

### <a name="parameters"></a><span data-ttu-id="f70be-211">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-211">Parameters</span></span>

<span data-ttu-id="f70be-212">Чтобы использовать этот параметр, добавьте запись для **усеаутоплай** в файл autorun. INF и установите запись равную 1.</span><span class="sxs-lookup"><span data-stu-id="f70be-212">To use this option, add an entry for **UseAutoPlay** to the Autorun.inf file and set the entry equal to 1.</span></span> <span data-ttu-id="f70be-213">Другие значения не поддерживаются в версиях Windows, предшествующих Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f70be-213">No other value is supported on versions of Windows earlier than Windows 8.</span></span>

<span data-ttu-id="f70be-214">В Windows 8 и более поздних версиях укажите значение 0, чтобы отключить автозапуск для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="f70be-214">On Windows 8 and later, specify a value of 0 to disable autoplay for this device.</span></span>


```
UseAutoPlay=1
```



### <a name="remarks"></a><span data-ttu-id="f70be-215">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-215">Remarks</span></span>

<span data-ttu-id="f70be-216">В настоящее время **усеаутоплай** применимо только в Windows XP или более поздних версиях и только на том диске, на котором [**Жетдриветипе**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) определяет тип **устройства \_ CDROM**.</span><span class="sxs-lookup"><span data-stu-id="f70be-216">Currently, **UseAutoPlay** is applicable only on Windows XP or later and only on a drive that [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determines to be of type **DRIVE\_CDROM**.</span></span>

<span data-ttu-id="f70be-217">При использовании **усеаутоплай** любое действие, заданное записями **Open** или **ShellExecute** в файле autorun. INF, не учитывается в Windows XP и пропускается из диалогового окна автозапуска в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f70be-217">When **UseAutoPlay** is used, any action specified by the **open** or **shellexecute** entries in Autorun.inf is ignored on Windows XP and omitted from the AutoPlay dialog on Windows Vista.</span></span>

<span data-ttu-id="f70be-218">Автозапуск обычно используется для автоматического запуска или загрузки объекта, содержащегося на вставленном носителе, в то время как автозапуск представляет собой диалоговое окно, содержащее список соответствующих действий, которые могут быть предприняты, и позволяет пользователю выбрать нужное действие.</span><span class="sxs-lookup"><span data-stu-id="f70be-218">AutoRun is typically used to automatically run or load something contained on the inserted media, whereas AutoPlay presents a dialog that includes a list of relevant actions that may be taken and enables the user to choose which action to take.</span></span> <span data-ttu-id="f70be-219">Дополнительные сведения о разнице между автозапуском и автозапуском см. в статьях [Создание приложения для чтения компакт-дисков с поддержкой автозапуска](autoplay.md) и [использование и настройка автозапуска](autoplay2k-using.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="f70be-219">For more information about the difference between AutoRun and AutoPlay, see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md) and [Using and Configuring AutoPlay](autoplay2k-using.md), respectively.</span></span>

### <a name="usage-example"></a><span data-ttu-id="f70be-220">Пример использования</span><span class="sxs-lookup"><span data-stu-id="f70be-220">Usage Example</span></span>

<span data-ttu-id="f70be-221">Компакт-диск содержит три файла: autorun. INF, Readme.txt и Music. WMA.</span><span class="sxs-lookup"><span data-stu-id="f70be-221">A CD contains three files: Autorun.inf, Readme.txt, and Music.wma.</span></span> <span data-ttu-id="f70be-222">В зависимости от используемой версии Windows и параметров, указанных в файле autorun. INF, компакт-диск может обрабатываться при вставке (при условии, что для диска, на который вставлен компакт-диск, включена функция автозапуска или автозапуска).</span><span class="sxs-lookup"><span data-stu-id="f70be-222">Depending on the version of Windows in use and options specified in Autorun.inf, the CD may be handled by either AutoRun or AutoPlay when it is inserted (assuming AutoRun/AutoPlay is enabled for the drive into which the CD is inserted).</span></span>

<span data-ttu-id="f70be-223">Во-первых, рассмотрим файл autorun. inf со следующим содержимым, указывая, что **усеаутоплай = 1** не указан:</span><span class="sxs-lookup"><span data-stu-id="f70be-223">First, consider an Autorun.inf file with the following contents, noting that **UseAutoPlay=1** is not specified:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
```



<span data-ttu-id="f70be-224">Действие, выполняемое оболочкой при вставке этого компакт-диска, зависит от используемой версии Windows:</span><span class="sxs-lookup"><span data-stu-id="f70be-224">The action taken by the Shell when this CD is inserted depends on the version of Windows in use:</span></span>

-   <span data-ttu-id="f70be-225">В Windows XP и более ранних версиях этот компакт-диск обрабатывается при вставке.</span><span class="sxs-lookup"><span data-stu-id="f70be-225">On Windows XP or earlier, this CD is handled by AutoRun when it is inserted.</span></span> <span data-ttu-id="f70be-226">В этом случае запись **ShellExecute** считывается, и оболочка вызывает обработчик файлов, связанный с TXT-файлами. Обычно это открывается Readme.txt в блокноте.</span><span class="sxs-lookup"><span data-stu-id="f70be-226">In this case, the **shellexecute** entry is read, and the Shell invokes the file handler associated with .txt files; typically this would open Readme.txt in Notepad.</span></span>
-   <span data-ttu-id="f70be-227">В Windows Vista присутствие файла autorun. INF с записью **ShellExecute** приводит к тому, что носитель будет опознан как тип автозапуска "программное обеспечение и игры".</span><span class="sxs-lookup"><span data-stu-id="f70be-227">On Windows Vista, the presence of an Autorun.inf file with a **shellexecute** entry causes the media to be identified as AutoPlay type "Software and games".</span></span> <span data-ttu-id="f70be-228">В этом случае пользователю предлагается диалоговое окно автозапуска, которое включает действие, заданное записью **ShellExecute** (в диалоговом окне как "Load Readme.txt"), а также действия по умолчанию, связанные с носителями типа "программное обеспечение и игры".</span><span class="sxs-lookup"><span data-stu-id="f70be-228">In this case the user is presented with an AutoPlay dialog that includes the action specified by the **shellexecute** entry (presented as "Load Readme.txt" in the dialog), along with default actions associated with media of type "Software and games".</span></span>

<span data-ttu-id="f70be-229">Чтобы указать, что автозапуск следует использовать вместо автозапуска в Windows XP, и что действие, заданное записью AutoRun ShellExecute, должно быть подавлено в диалоговом окне автозапуска в Windows Vista, вставьте **усеаутоплай** в файл autorun. INF следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f70be-229">To indicate that AutoPlay should be used rather than AutoRun on Windows XP, and that the action specified by the AutoRun shellexecute entry should be suppressed from the AutoPlay dialog on Windows Vista, insert **UseAutoPlay** into the Autorun.inf file as follows:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



<span data-ttu-id="f70be-230">Опять же, действие, выполняемое оболочкой при вставке компакт-диска, зависит от используемой версии Windows.</span><span class="sxs-lookup"><span data-stu-id="f70be-230">Once again, the action taken by the Shell when this CD is inserted depends on the version of Windows in use.</span></span>

-   <span data-ttu-id="f70be-231">В версиях Windows, предшествующих Windows XP, по-прежнему используется автозапуск и выполняется действие, указанное в **ShellExecute** , как описано выше.</span><span class="sxs-lookup"><span data-stu-id="f70be-231">On versions of Windows earlier than Windows XP, AutoRun is still used and the action specified by **shellexecute** is performed, as described previously.</span></span> <span data-ttu-id="f70be-232">(Обратите внимание, что только Автозапуск доступен в версиях Windows, предшествующих Windows XP.)</span><span class="sxs-lookup"><span data-stu-id="f70be-232">(Note that only AutoRun is available on versions of Windows earlier than Windows XP.)</span></span>
-   <span data-ttu-id="f70be-233">В Windows XP запись **усеаутоплай** приводит к тому, что вместо автозапуска используется автозапуск.</span><span class="sxs-lookup"><span data-stu-id="f70be-233">On Windows XP, the **UseAutoPlay** entry causes AutoPlay to be used in place of AutoRun.</span></span> <span data-ttu-id="f70be-234">В этом случае Автозапуск определяет, что носитель содержит аудио-файл Windows Media (WMA), и распределяет содержимое по категориям "музыкальные файлы".</span><span class="sxs-lookup"><span data-stu-id="f70be-234">In this case, AutoPlay determines that the media contains a Windows Media Audio (.wma) file and categorizes the content as "Music files".</span></span> <span data-ttu-id="f70be-235">Пользователю предоставляется диалоговое окно автозапуска, содержащее зарегистрированные обработчики для типа автозапуска "музыкальные файлы". запись ShellExecute AutoRun игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f70be-235">The user is presented with an AutoPlay dialog containing registered handlers for the "Music files" AutoPlay media type; the AutoRun shellexecute entry is ignored.</span></span>

### <a name="shellexecute"></a><span data-ttu-id="f70be-236">вызов</span><span class="sxs-lookup"><span data-stu-id="f70be-236">shellexecute</span></span>

[<span data-ttu-id="f70be-237">Версия 5,0.</span><span class="sxs-lookup"><span data-stu-id="f70be-237">Version 5.0.</span></span>](versions.md) <span data-ttu-id="f70be-238">Запись **ShellExecute** Указывает приложение или файл данных, которые функция autorun будет использовать для вызова [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="f70be-238">The **shellexecute** entry specifies an application or data file that AutoRun will use to call [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a><span data-ttu-id="f70be-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-239">Parameters</span></span>

-   <span data-ttu-id="f70be-240">*равно*</span><span class="sxs-lookup"><span data-stu-id="f70be-240">*filepath*</span></span>

    <span data-ttu-id="f70be-241">Строка, содержащая полный путь к каталогу, содержащему данные или исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="f70be-241">A string that contains the fully qualified path of the directory that contains the data or executable file.</span></span> <span data-ttu-id="f70be-242">Если путь не указан, файл должен находиться в корневом каталоге диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-242">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="f70be-243">*filename*</span><span class="sxs-lookup"><span data-stu-id="f70be-243">*filename*</span></span>

    <span data-ttu-id="f70be-244">Строка, содержащая имя файла.</span><span class="sxs-lookup"><span data-stu-id="f70be-244">A string that contains the file's name.</span></span> <span data-ttu-id="f70be-245">Если это исполняемый файл, он запускается.</span><span class="sxs-lookup"><span data-stu-id="f70be-245">If it is an executable file, it is launched.</span></span> <span data-ttu-id="f70be-246">Если это файл данных, то он должен быть членом [типа файла](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f70be-246">If it is a data file, it must be a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="f70be-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) запускает команду по умолчанию, связанную с типом файла.</span><span class="sxs-lookup"><span data-stu-id="f70be-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) launches the default command associated with the file type.</span></span>

-   <span data-ttu-id="f70be-248">*парамкс*</span><span class="sxs-lookup"><span data-stu-id="f70be-248">*paramx*</span></span>

    <span data-ttu-id="f70be-249">Содержит любые дополнительные параметры, которые должны быть переданы в [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="f70be-249">Contains any additional parameters that should be passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

### <a name="remarks"></a><span data-ttu-id="f70be-250">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-250">Remarks</span></span>

<span data-ttu-id="f70be-251">Эта запись аналогична [открытой](#parameters), но позволяет использовать сведения о [сопоставлении файлов](fa-intro.md) для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="f70be-251">This entry is similar to [open](#parameters), but it allows you to use [file association](fa-intro.md) information to run the application.</span></span>

### <a name="shell"></a><span data-ttu-id="f70be-252">оболочка</span><span class="sxs-lookup"><span data-stu-id="f70be-252">shell</span></span>

<span data-ttu-id="f70be-253">Запись **Shell** указывает команду по умолчанию для контекстного меню диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-253">The **shell** entry specifies a default command for the drive's shortcut menu.</span></span>


```
shell=verb
```



### <a name="parameters"></a><span data-ttu-id="f70be-254">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-254">Parameters</span></span>

-   <span data-ttu-id="f70be-255">*Команда*</span><span class="sxs-lookup"><span data-stu-id="f70be-255">*verb*</span></span>

    <span data-ttu-id="f70be-256">Команда, соответствующая команде меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-256">The verb that corresponds to the menu command.</span></span> <span data-ttu-id="f70be-257">Команда и связанная с ней команда меню должны быть определены в файле autorun. INF с записью [ \\ команды оболочки](#shellverb) .</span><span class="sxs-lookup"><span data-stu-id="f70be-257">The verb and its associated menu command must be defined in the Autorun.inf file with a [shell\\verb](#shellverb) entry.</span></span>

### <a name="remarks"></a><span data-ttu-id="f70be-258">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-258">Remarks</span></span>

<span data-ttu-id="f70be-259">Когда пользователь щелкает правой кнопкой мыши значок диска, появляется контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-259">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="f70be-260">При наличии файла autorun. inf из него берется команда контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f70be-260">If an Autorun.inf file is present, the default shortcut menu command is taken from it.</span></span> <span data-ttu-id="f70be-261">Эта команда также выполняется, когда пользователь дважды щелкает значок диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-261">This command also executes when the user double-clicks the drive's icon.</span></span>

<span data-ttu-id="f70be-262">Чтобы указать команду контекстного меню по умолчанию, сначала определите ее глагол, командную строку и текст меню с помощью [ \\ команды оболочки](#shellverb).</span><span class="sxs-lookup"><span data-stu-id="f70be-262">To specify the default shortcut menu command, first define its verb, command string, and menu text with [shell\\verb](#shellverb).</span></span> <span data-ttu-id="f70be-263">Затем используйте оболочку, чтобы сделать ее командой контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f70be-263">Then use shell to make it the default shortcut menu command.</span></span> <span data-ttu-id="f70be-264">В противном случае текст пункта меню по умолчанию будет "Автозапуск", который запускает приложение, указанное в [открытом](#parameters) элементе.</span><span class="sxs-lookup"><span data-stu-id="f70be-264">Otherwise, the default menu item text will be "AutoPlay", which launches the application specified by the [open](#parameters) entry.</span></span>

### <a name="shellverb"></a><span data-ttu-id="f70be-265">\\команда оболочки</span><span class="sxs-lookup"><span data-stu-id="f70be-265">shell\\verb</span></span>

<span data-ttu-id="f70be-266">Запись **\\ команды оболочки** добавляет пользовательскую команду в контекстное меню диска.</span><span class="sxs-lookup"><span data-stu-id="f70be-266">The **shell\\verb** entry adds a custom command to the drive's shortcut menu.</span></span>


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a><span data-ttu-id="f70be-267">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-267">Parameters</span></span>

-   <span data-ttu-id="f70be-268">*Команда*</span><span class="sxs-lookup"><span data-stu-id="f70be-268">*verb*</span></span>

    <span data-ttu-id="f70be-269">Команда меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-269">The menu command's verb.</span></span> <span data-ttu-id="f70be-270">*_\\ Командная запись команды_* **оболочки \\**_связывает команду с_ исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="f70be-270">The **shell\\**_verb_*_\\command_* entry associates the verb with an executable file.</span></span> <span data-ttu-id="f70be-271">Глаголы не должны содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="f70be-271">Verbs must not contain embedded spaces.</span></span> <span data-ttu-id="f70be-272">По умолчанию *команда* — это текст, отображаемый в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-272">By default, *verb* is the text that is displayed in the shortcut menu.</span></span>

-   <span data-ttu-id="f70be-273">*Filename.exe*</span><span class="sxs-lookup"><span data-stu-id="f70be-273">*Filename.exe*</span></span>

    <span data-ttu-id="f70be-274">Путь и имя файла приложения, которое выполняет действие.</span><span class="sxs-lookup"><span data-stu-id="f70be-274">The path and file name of the application that performs the action.</span></span>

-   <span data-ttu-id="f70be-275">*менутекст*</span><span class="sxs-lookup"><span data-stu-id="f70be-275">*MenuText*</span></span>

    <span data-ttu-id="f70be-276">Этот параметр задает текст, отображаемый в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-276">This parameter specifies the text that is displayed in the shortcut menu.</span></span> <span data-ttu-id="f70be-277">Если он не указан, *команда* отображается.</span><span class="sxs-lookup"><span data-stu-id="f70be-277">If it is omitted, *verb* is displayed.</span></span> <span data-ttu-id="f70be-278">*Менутекст* может быть в смешанном регистре и может содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="f70be-278">*MenuText* can be mixed-case and can contain spaces.</span></span> <span data-ttu-id="f70be-279">Для пункта меню можно задать сочетание клавиш, поместив амперсанд (&) перед буквой.</span><span class="sxs-lookup"><span data-stu-id="f70be-279">You can set a shortcut key for the menu item by putting an ampersand (&) in front of the letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="f70be-280">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-280">Remarks</span></span>

<span data-ttu-id="f70be-281">Когда пользователь щелкает правой кнопкой мыши значок диска, появляется контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-281">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="f70be-282">Добавление **записей \\ команд оболочки** в файл autorun. INF позволяет добавлять команды в это контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-282">Adding **shell\\verb** entries to the drive's Autorun.inf file allows you to add commands to this shortcut menu.</span></span>

<span data-ttu-id="f70be-283">Эта запись состоит из двух частей, которые должны находиться в разных строках.</span><span class="sxs-lookup"><span data-stu-id="f70be-283">There are two parts to this entry, which must be on separate lines.</span></span> <span data-ttu-id="f70be-284">Первая часть —*_\\ команда_* **оболочки \\**.</span><span class="sxs-lookup"><span data-stu-id="f70be-284">The first part is **shell\\**_verb_*_\\command_*.</span></span> <span data-ttu-id="f70be-285">Оно должно указываться обязательно.</span><span class="sxs-lookup"><span data-stu-id="f70be-285">It is required.</span></span> <span data-ttu-id="f70be-286">Он связывает строку, называемую *глаголом*, с приложением, которое запускается при выполнении команды.</span><span class="sxs-lookup"><span data-stu-id="f70be-286">It associates a string, called a *verb*, with the application to launch when the command runs.</span></span> <span data-ttu-id="f70be-287">Вторая часть — это запись _команды_ **оболочки \\**.</span><span class="sxs-lookup"><span data-stu-id="f70be-287">The second part is the **shell\\**_verb_ entry.</span></span> <span data-ttu-id="f70be-288">Этот параметр необязателен.</span><span class="sxs-lookup"><span data-stu-id="f70be-288">It is optional.</span></span> <span data-ttu-id="f70be-289">Его можно включить, чтобы указать текст, отображаемый в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="f70be-289">You can include it to specify the text that displays in the shortcut menu.</span></span>

<span data-ttu-id="f70be-290">Чтобы указать команду контекстного меню по умолчанию, определите команду с помощью **\\ команды оболочки** и сделайте ее командой по умолчанию с записью [оболочки](#autoruninf-entries) .</span><span class="sxs-lookup"><span data-stu-id="f70be-290">To specify a default shortcut menu command, define the verb with **shell\\verb**, and make it the default command with the [shell](#autoruninf-entries) entry.</span></span>

<span data-ttu-id="f70be-291">Следующий пример фрагмента кода autorun. INF связывает *команду с командой со* строкой "Notepad ABC \\readme.txt".</span><span class="sxs-lookup"><span data-stu-id="f70be-291">The following sample Autorun.inf fragment associates the *readit* verb with the command string "Notepad abc\\readme.txt".</span></span> <span data-ttu-id="f70be-292">Текст меню — «Read Me», а «m» определен как клавиша быстрого доступа к элементу.</span><span class="sxs-lookup"><span data-stu-id="f70be-292">The menu text is "Read Me", and 'M' is defined as the item's shortcut key.</span></span> <span data-ttu-id="f70be-293">Когда пользователь выбирает эту команду, \\ открывается файл abcreadme.txt на диске с блокнотом Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="f70be-293">When the user selects this command, the drive's abc\\readme.txt file opens with Microsoft Notepad.</span></span>


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a><span data-ttu-id="f70be-294">\[\]Ключи содержимого</span><span class="sxs-lookup"><span data-stu-id="f70be-294">\[Content\] Keys</span></span>

<span data-ttu-id="f70be-295">Существует три ключа типа файла: **мусикфилес**, **пиктурефилес** и **видеофилес**.</span><span class="sxs-lookup"><span data-stu-id="f70be-295">There are three file type keys: **MusicFiles**, **PictureFiles**, and **VideoFiles**.</span></span>

<span data-ttu-id="f70be-296">Если одно из этих значений имеет значение true с учетом значения 1, y, Yes, t или true, Пользовательский интерфейс автозапуска отображает обработчики, связанные с этим типом содержимого, независимо от того, существует ли на носителе содержимое этого типа.</span><span class="sxs-lookup"><span data-stu-id="f70be-296">If one of these contents is set to true through one the case-insensitive values 1, y, yes, t, or true, the Autoplay UI displays the handlers associated with that content type regardless of whether content of that type exists on the media.</span></span>

<span data-ttu-id="f70be-297">Если одно из этих значений имеет значение false с учетом значения 0, n, No, f или false, то пользовательский интерфейс автозапуска не отображает обработчики, связанные с этим типом содержимого, даже если на носителе обнаружено содержимое этого типа.</span><span class="sxs-lookup"><span data-stu-id="f70be-297">If one of these contents is set to false through one the case-insensitive values 0, n, no, f, or false, the Autoplay UI does not display the handlers associated with that content type even if content of that type is detected on the media.</span></span>

<span data-ttu-id="f70be-298">Использование этого раздела предназначено для того, чтобы позволить авторам содержимого передавать данные для автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="f70be-298">Use of this section is intended to allow content authors to communicate the intent of content to Autoplay.</span></span> <span data-ttu-id="f70be-299">Например, компакт-диск можно классифицировать как содержащий только музыкальное содержимое, даже если у него есть изображения и видеоролики, и в противном случае они будут отображаться как смешанное содержимое.</span><span class="sxs-lookup"><span data-stu-id="f70be-299">For instance, a CD can be categorized as containing only music content even though it also has pictures and videos and would otherwise be seen as having mixed content.</span></span>

<span data-ttu-id="f70be-300">Раздел **\[ содержимого \]** поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="f70be-300">The **\[Content\]** section is only supported under Windows Vista and later.</span></span>


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a><span data-ttu-id="f70be-301">\[\]Ключи ексклусивеконтентпасс</span><span class="sxs-lookup"><span data-stu-id="f70be-301">\[ExclusiveContentPaths\] Keys</span></span>

<span data-ttu-id="f70be-302">Папки, перечисленные в этом разделе, ограничивают автозапуск для поиска содержимого только в тех папках и вложенных папках.</span><span class="sxs-lookup"><span data-stu-id="f70be-302">Folders listed in this section limit Autoplay to searching only those folders and their subfolders for content.</span></span> <span data-ttu-id="f70be-303">Они могут быть заданы с предшествующей обратной косой чертой () или без нее \\ .</span><span class="sxs-lookup"><span data-stu-id="f70be-303">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="f70be-304">В любом случае они берутся в виде абсолютных путей из корневого каталога носителя.</span><span class="sxs-lookup"><span data-stu-id="f70be-304">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="f70be-305">В случае с папками, в именах которых есть пробелы, не заключайте их в кавычки, так как кавычки берутся буквально как часть пути.</span><span class="sxs-lookup"><span data-stu-id="f70be-305">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="f70be-306">Использование этого раздела предназначено для того, чтобы авторы содержимого могли сообщать о намерениях к автозапуску и сокращать время проверки, ограничивая проверку на определенные значительные участки носителя.</span><span class="sxs-lookup"><span data-stu-id="f70be-306">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="f70be-307">Ниже приведены все допустимые пути.</span><span class="sxs-lookup"><span data-stu-id="f70be-307">The following are all valid paths</span></span>


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="f70be-308">Раздел **\[ ексклусивеконтентпасс \]** поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="f70be-308">The **\[ExclusiveContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="ignorecontentpaths-keys"></a><span data-ttu-id="f70be-309">\[\]Ключи игнореконтентпасс</span><span class="sxs-lookup"><span data-stu-id="f70be-309">\[IgnoreContentPaths\] Keys</span></span>

<span data-ttu-id="f70be-310">Папки, перечисленные в этом разделе, и их вложенные папки игнорируются автозапуском при поиске содержимого на носителе.</span><span class="sxs-lookup"><span data-stu-id="f70be-310">Folders listed in this section, and their subfolders, are ignored by Autoplay when searching a media for content.</span></span> <span data-ttu-id="f70be-311">Они могут быть заданы с предшествующей обратной косой чертой () или без нее \\ .</span><span class="sxs-lookup"><span data-stu-id="f70be-311">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="f70be-312">В любом случае они берутся в виде абсолютных путей из корневого каталога носителя.</span><span class="sxs-lookup"><span data-stu-id="f70be-312">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="f70be-313">В случае с папками, в именах которых есть пробелы, не заключайте их в кавычки, так как кавычки берутся буквально как часть пути.</span><span class="sxs-lookup"><span data-stu-id="f70be-313">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="f70be-314">Пути в этом разделе имеют приоритет над путями в разделе **\[ ексклусивеконтентпасс \]** .</span><span class="sxs-lookup"><span data-stu-id="f70be-314">Paths in this section take precedence over paths in the **\[ExclusiveContentPaths\]** section.</span></span> <span data-ttu-id="f70be-315">Если путь, указанный в **\[ игнореконтентпасс \]** , является вложенной папкой пути, заданной в **\[ ексклусивеконтентпасс \]**, он по-прежнему игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f70be-315">If a path given in **\[IgnoreContentPaths\]** is a subfolder of a path given in **\[ExclusiveContentPaths\]**, it is still ignored.</span></span>

<span data-ttu-id="f70be-316">Использование этого раздела предназначено для того, чтобы авторы содержимого могли сообщать о намерениях к автозапуску и сокращать время проверки, ограничивая проверку на определенные значительные участки носителя.</span><span class="sxs-lookup"><span data-stu-id="f70be-316">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="f70be-317">Ниже приведены все допустимые пути.</span><span class="sxs-lookup"><span data-stu-id="f70be-317">The following are all valid paths</span></span>


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="f70be-318">Раздел **\[ игнореконтентпасс \]** поддерживается только в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="f70be-318">The **\[IgnoreContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="deviceinstall-keys"></a><span data-ttu-id="f70be-319">\[\]Ключи девицеинсталл</span><span class="sxs-lookup"><span data-stu-id="f70be-319">\[DeviceInstall\] Keys</span></span>

### <a name="driverpath"></a><span data-ttu-id="f70be-320">DriverPath</span><span class="sxs-lookup"><span data-stu-id="f70be-320">DriverPath</span></span>

<span data-ttu-id="f70be-321">Запись **DriverPath** указывает каталог для рекурсивного поиска файлов драйверов.</span><span class="sxs-lookup"><span data-stu-id="f70be-321">The **DriverPath** entry specifies a directory to search recursively for driver files.</span></span> <span data-ttu-id="f70be-322">Эта команда используется во время установки драйвера и не является частью операции автозапуска.</span><span class="sxs-lookup"><span data-stu-id="f70be-322">This command is used during a driver installation and is not part of an AutoRun operation.</span></span> <span data-ttu-id="f70be-323">Раздел **\[ девицеинсталл \]** поддерживается только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f70be-323">The **\[DeviceInstall\]** section is only supported under Windows XP.</span></span>


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a><span data-ttu-id="f70be-324">Параметры</span><span class="sxs-lookup"><span data-stu-id="f70be-324">Parameters</span></span>

-   <span data-ttu-id="f70be-325">*DirectoryPath*</span><span class="sxs-lookup"><span data-stu-id="f70be-325">*directorypath*</span></span>

    <span data-ttu-id="f70be-326">Путь к каталогу, в котором Windows ищет файлы драйверов вместе со всеми его подкаталогами.</span><span class="sxs-lookup"><span data-stu-id="f70be-326">A path to a directory that Windows searches for driver files, along with all of its subdirectories.</span></span>

### <a name="remarks"></a><span data-ttu-id="f70be-327">Примечания</span><span class="sxs-lookup"><span data-stu-id="f70be-327">Remarks</span></span>

<span data-ttu-id="f70be-328">Не используйте буквы дисков в *DirectoryPath* , так как они меняются с одного компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="f70be-328">Do not use drive letters in *directorypath* as they change from one computer to the next.</span></span>

<span data-ttu-id="f70be-329">Для поиска в нескольких каталогах добавьте запись **DriverPath** для каждого каталога, как в этом примере.</span><span class="sxs-lookup"><span data-stu-id="f70be-329">To search multiple directories, add a **DriverPath** entry for each directory as in this example.</span></span>


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



<span data-ttu-id="f70be-330">Если в разделе **\[ девицеинсталл \]** нет записи **DriverPath** или в записи **DriverPath** не задано значение, этот диск пропускается во время поиска файлов драйверов.</span><span class="sxs-lookup"><span data-stu-id="f70be-330">If no **DriverPath** entry is provided in the **\[DeviceInstall\]** section or the **DriverPath** entry has no value, then that drive is skipped during a search for driver files.</span></span>

 

 
