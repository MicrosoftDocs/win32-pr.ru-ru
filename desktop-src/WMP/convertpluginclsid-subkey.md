---
title: Подраздел Конвертплугинклсид
description: Подраздел Конвертплугинклсид
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Проигрыватель Windows Media, подраздел Конвертплугинклсид
- Проигрыватель Windows Media, расширения имен файлов
- Проигрыватель Windows Media, реестр
- реестр, расширения имен файлов
- реестр, подраздел Конвертплугинклсид
- реестр, параметры для проигрывателя Windows Media
- параметры реестра для расширения имени файла
- Подраздел Конвертплугинклсид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068067"
---
# <a name="convertpluginclsid-subkey"></a><span data-ttu-id="7a5ba-111">Подраздел Конвертплугинклсид</span><span class="sxs-lookup"><span data-stu-id="7a5ba-111">ConvertPluginCLSID Subkey</span></span>

<span data-ttu-id="7a5ba-112">Когда проигрыватель Windows Media 11 обнаруживает пользовательское расширение имени файла, он ищет подраздел реестра, соответствующий этому расширению.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-112">When Windows Media Player 11 encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="7a5ba-113">Подраздел описывается в [разделе Параметры реестра расширения имени файла](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7a5ba-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="7a5ba-114">В некоторых случаях подраздел расширения содержит подраздел с именем **конвертплугинклсид**.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-114">In some cases, the extension's subkey has a subkey named **ConvertPluginCLSID**.</span></span>

<span data-ttu-id="7a5ba-115">Например, предположим, что вы создали пользовательский формат файла (с расширением XYZ) и подключаемый модуль преобразования, который преобразует файлы в формат, поддерживаемый проигрывателем Windows Media, затем вы храните идентификатор класса подключаемого модуля в одном или обоих следующих подразделах.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-115">For example, suppose you have created a custom file format (with file name extension .xyz) and a conversion plug-in that converts the files to a format supported by Windows Media Player Then you would store the class ID of the plug-in in one or both of the following subkeys.</span></span>

<span data-ttu-id="7a5ba-116">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ мультимедиа \\ вмплайер \\ Extensions \\ . XYZ \\ конвертплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-116">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="7a5ba-117">**HKEY \_ текущее \_ пользовательское \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ . XYZ \\ конвертплугинклсид**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-117">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\.xyz\\ConvertPluginCLSID**</span></span>

<span data-ttu-id="7a5ba-118">Подраздел **конвертплугинклсид** указывает идентификаторы классов подключаемых модулей, которые проигрыватель Windows Media может использовать для преобразования файла мультимедиа из его пользовательского формата в формат, поддерживаемый проигрывателем.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-118">The **ConvertPluginCLSID** subkey specifies the class IDs of plug-ins that Windows Media Player can use to convert a media file from its custom format to a format supported by the Player.</span></span>

<span data-ttu-id="7a5ba-119">Подраздел **конвертплугинклсид** содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-119">The **ConvertPluginCLSID** subkey has the following entries.</span></span>

-   <span data-ttu-id="7a5ba-120">Запись по умолчанию, представляющая подключаемый модуль преобразования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-120">A default entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="7a5ba-121">Именованная запись, представляющая подключаемый модуль преобразования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-121">A named entry that represents the default conversion plug-in.</span></span>
-   <span data-ttu-id="7a5ba-122">Дополнительные именованные записи, представляющие альтернативные подключаемые модули преобразования.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-122">Additional named entries that represent alternate conversion plug-ins.</span></span>

<span data-ttu-id="7a5ba-123">Например, предположим, что пользовательский формат файла имеет подключаемый модуль преобразования по умолчанию и два альтернативных подключаемых модуля преобразования. Записи реестра в подразделе **конвертплугинклсид** будут иметь следующую форму.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-123">For example, suppose a custom file format has a default conversion plug-in and two alternate conversion plug-ins. The registry entries under the **ConvertPluginCLSID** subkey would have the following form.</span></span>



| <span data-ttu-id="7a5ba-124">Имя</span><span class="sxs-lookup"><span data-stu-id="7a5ba-124">Name</span></span>                                                                          | <span data-ttu-id="7a5ba-125">Тип</span><span class="sxs-lookup"><span data-stu-id="7a5ba-125">Type</span></span>        | <span data-ttu-id="7a5ba-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7a5ba-126">Value</span></span>                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| <span data-ttu-id="7a5ba-127">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7a5ba-127">Default</span></span>                                                                       | <span data-ttu-id="7a5ba-128">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-128">**REG\_SZ**</span></span> | <span data-ttu-id="7a5ba-129">Идентификатор класса в формате реестра подключаемого модуля преобразования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-129">The class ID, in registry format, of the default conversion plug-in.</span></span> |
| <span data-ttu-id="7a5ba-130">Идентификатор класса в формате реестра подключаемого модуля преобразования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-130">The class ID, in registry format, of the default conversion plug-in.</span></span>          | <span data-ttu-id="7a5ba-131">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-131">**REG\_SZ**</span></span> | <span data-ttu-id="7a5ba-132">Понятное имя подключаемого модуля преобразования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-132">The friendly name of the default conversion plug-in.</span></span>                 |
| <span data-ttu-id="7a5ba-133">Идентификатор класса (в формате реестра) первого альтернативного подключаемого модуля преобразования.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-133">The class ID, in registry format, of the first alternate conversion plug-in.</span></span>  | <span data-ttu-id="7a5ba-134">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-134">**REG\_SZ**</span></span> | <span data-ttu-id="7a5ba-135">Понятное имя первого альтернативного подключаемого модуля преобразования.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-135">The friendly name of the first alternate conversion plug-in.</span></span>         |
| <span data-ttu-id="7a5ba-136">Идентификатор класса в формате реестра второго дополнительного подключаемого модуля преобразования.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-136">The class ID, in registry format, of the second alternate conversion plug-in.</span></span> | <span data-ttu-id="7a5ba-137">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-137">**REG\_SZ**</span></span> | <span data-ttu-id="7a5ba-138">Понятное имя второго дополнительного подключаемого модуля преобразования.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-138">The friendly name of the second alternate conversion plug-in.</span></span>        |



 

<span data-ttu-id="7a5ba-139">Обратите внимание, что подключаемый модуль преобразования по умолчанию представлен двумя записями реестра: записью по умолчанию и именованной записью.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-139">Note that the default conversion plug-in is represented by two registry entries: the default entry and a named entry.</span></span> <span data-ttu-id="7a5ba-140">Проигрыватель Windows Media использует запись по умолчанию, чтобы определить, какой подключаемый модуль является подключаемым модулем преобразования по умолчанию (основной).</span><span class="sxs-lookup"><span data-stu-id="7a5ba-140">Windows Media Player uses the default entry to determine which plug-in is the default (primary) conversion plug-in.</span></span> <span data-ttu-id="7a5ba-141">Проигрыватель Windows Media использует именованные записи для получения понятных имен для всех подключаемых модулей преобразования, включая подключаемый модуль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-141">Windows Media Player uses the named entries to obtain friendly names for all conversion plug-ins, including the default plug-in.</span></span>

<span data-ttu-id="7a5ba-142">Понятное имя подключаемого модуля преобразования определяется компанией, которая создает подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-142">The friendly name of a conversion plug-in is determined by the company that creates the plug-in.</span></span> <span data-ttu-id="7a5ba-143">Проигрыватель Windows Media может отображать понятное имя в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-143">Windows Media Player might display the friendly name in its user interface.</span></span>

<span data-ttu-id="7a5ba-144">Когда проигрыватель Windows Media пытается преобразовать файл из пользовательского формата в стандартный формат, сначала загружается подключаемый модуль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-144">When Windows Media Player attempts to convert a file from a custom format to a standard format, it first loads the default plug-in.</span></span> <span data-ttu-id="7a5ba-145">Если подключаемому модулю по умолчанию не удается преобразовать файл и возвращается \_ \_ \_ \_ \_ неизвестный владелец файла NS E WMP Convert \_ \_ , проигрыватель загружает каждый альтернативный подключаемый модуль до тех пор, пока не будет выполнено успешное преобразование или не попытайтесь использовать подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-145">If the default plug-in fails to convert the file and returns NS\_E\_WMP\_CONVERT\_PLUGIN\_UNKNOWN\_FILE\_OWNER, the Player loads each alternate plug-in until a successful conversion happens or there are no more plug-ins to try.</span></span> <span data-ttu-id="7a5ba-146">Проигрыватель не отображает предупреждающее сообщение, если не найден подключаемый модуль преобразования для расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-146">The Player does not display a warning message if no conversion plug-in is found for the file name extension.</span></span>

<span data-ttu-id="7a5ba-147">Запись реестра **конвертплугинклсид** поддерживается проигрывателем Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="7a5ba-147">The **ConvertPluginCLSID** registry entry is supported by Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a5ba-148">См. также</span><span class="sxs-lookup"><span data-stu-id="7a5ba-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a5ba-149">**Параметры реестра для расширения имени файла**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-149">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> <dt>

[<span data-ttu-id="7a5ba-150">**Подключаемые модули преобразования проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7a5ba-150">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




