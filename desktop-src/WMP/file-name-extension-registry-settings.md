---
title: Параметры реестра для расширения имени файла
description: Параметры реестра для расширения имени файла
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Проигрыватель Windows Media, реестр
- Проигрыватель Windows Media, расширения имен файлов
- реестр, расширения имен файлов
- реестр, параметры для проигрывателя Windows Media
- параметры реестра для расширения имени файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778488"
---
# <a name="file-name-extension-registry-settings"></a><span data-ttu-id="4d96e-108">Параметры реестра для расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="4d96e-108">File Name Extension Registry Settings</span></span>

<span data-ttu-id="4d96e-109">Если файлы цифрового мультимедиа имеют пользовательский формат, можно предоставить проигрывателю Windows Media сведения о пользовательском формате, разместив записи в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d96e-109">If your digital media files have a custom format, you can provide Windows Media Player with information about your custom format by placing entries in the registry on the user's computer.</span></span> <span data-ttu-id="4d96e-110">Проигрыватель Windows Media проверяет записи реестра, чтобы определить, как она должна управлять файлами.</span><span class="sxs-lookup"><span data-stu-id="4d96e-110">Windows Media Player inspects your registry entries to determine how it should handle your files.</span></span> <span data-ttu-id="4d96e-111">В следующем списке показано несколько действий, которые можно выполнить путем создания записей реестра, относящихся к пользовательскому формату файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4d96e-111">The following list shows several of the things you can do by creating registry entries that pertain to your custom media file format.</span></span>

-   <span data-ttu-id="4d96e-112">Предоставьте проигрывателю разрешение на воспроизведение, копирование и перекодировать файлы.</span><span class="sxs-lookup"><span data-stu-id="4d96e-112">Grant permission for the Player to play, copy, or transcode your files.</span></span>
-   <span data-ttu-id="4d96e-113">Укажите базовую технологию, которую проигрыватель будет использовать для воспроизведения файлов.</span><span class="sxs-lookup"><span data-stu-id="4d96e-113">Specify the underlying technology that the Player should use to play your files.</span></span>
-   <span data-ttu-id="4d96e-114">Укажите, где проигрыватель должен отображать файлы в представлении библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4d96e-114">Specify where the Player should display your files in its library view.</span></span>
-   <span data-ttu-id="4d96e-115">Укажите подключаемый модуль, который должен использоваться проигрывателем для преобразования файлов в стандартный формат.</span><span class="sxs-lookup"><span data-stu-id="4d96e-115">Specify a plug-in that the Player should use to convert your files to a standard format.</span></span>
-   <span data-ttu-id="4d96e-116">Укажите код формата протокола передачи мультимедиа (MTP), который проигрыватель может использовать для определения того, поддерживает ли конкретное портативное устройство формат файла.</span><span class="sxs-lookup"><span data-stu-id="4d96e-116">Specify a Media Transport Protocol (MTP) format code that the Player can use to determine whether a particular portable device supports your file format.</span></span>

<span data-ttu-id="4d96e-117">Большинство предоставленных записей будут находиться в подразделе, связанном с расширением пользовательского имени файла.</span><span class="sxs-lookup"><span data-stu-id="4d96e-117">Most of the entries that you provide will be under a subkey that is associated with your custom file name extension.</span></span> <span data-ttu-id="4d96e-118">Этот подраздел можно создать в \_ поддереве "локальный \_ компьютер" hKey и в \_ поддереве hKey Current \_ User.</span><span class="sxs-lookup"><span data-stu-id="4d96e-118">You can create that subkey in the HKEY\_LOCAL\_MACHINE subtree and in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="4d96e-119">Проигрыватель Windows Media сначала ищет в \_ поддереве «локальный компьютер» hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="4d96e-119">Windows Media Player looks first in the HKEY\_LOCAL\_MACHINE subtree.</span></span> <span data-ttu-id="4d96e-120">Если он не находит нужные сведения, он ищет в \_ поддереве hKey текущий \_ пользователь.</span><span class="sxs-lookup"><span data-stu-id="4d96e-120">If it doesn't find what it needs there, it looks in the HKEY\_CURRENT\_USER subtree.</span></span> <span data-ttu-id="4d96e-121">Обратите внимание, что любой код, пытающийся выполнить запись в реестр на компьютере пользователя, может выполнять запись в \_ поддерево hKey на локальном компьютере \_ только в том случае, если у текущего пользователя есть права администратора.</span><span class="sxs-lookup"><span data-stu-id="4d96e-121">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="4d96e-122">Чтобы записать сведения о пользовательском формате файла в \_ поддерево hKey локального \_ компьютера, создайте следующий подраздел.</span><span class="sxs-lookup"><span data-stu-id="4d96e-122">To write information about your custom file format to the HKEY\_LOCAL\_MACHINE subtree, create the following subkey.</span></span>

<span data-ttu-id="4d96e-123">**HKey \_ Локальное \_ компьютерное \\ программное обеспечение \\ Microsoft \\ мультимедиа \\ вмплайер \\ Extensions \\** *кустомекстенсион*</span><span class="sxs-lookup"><span data-stu-id="4d96e-123">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="4d96e-124">где *кустомекстенсион* — это расширение имени файла, включая разделитель точек (.).</span><span class="sxs-lookup"><span data-stu-id="4d96e-124">where *customExtension* is the file name extension including the dot (.) separator.</span></span> <span data-ttu-id="4d96e-125">Например, если расширение для пользовательского формата файла —. XYZ, создайте следующий подраздел.</span><span class="sxs-lookup"><span data-stu-id="4d96e-125">For example, if the extension for your custom file format is .xyz, create the following subkey.</span></span>

<span data-ttu-id="4d96e-126">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ мультимедиа \\ вмплайер \\ Extensions \\ . XYZ**</span><span class="sxs-lookup"><span data-stu-id="4d96e-126">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Multimedia\\WMPlayer\\Extensions\\.xyz**</span></span>

<span data-ttu-id="4d96e-127">Чтобы записать сведения о пользовательском формате файла в \_ поддерево hKey Current \_ User, создайте следующий подраздел.</span><span class="sxs-lookup"><span data-stu-id="4d96e-127">To write information about your custom file format to the HKEY\_CURRENT\_USER subtree, create the following subkey.</span></span>

<span data-ttu-id="4d96e-128">**HKey \_ Текущее \_ пользовательское \\ программное обеспечение \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\** *кустомекстенсион*</span><span class="sxs-lookup"><span data-stu-id="4d96e-128">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Player\\Extensions\\** *customExtension*</span></span>

<span data-ttu-id="4d96e-129">В подразделе *кустомекстенсион* можно записать одну или несколько следующих записей.</span><span class="sxs-lookup"><span data-stu-id="4d96e-129">You can write one or more of the following entries in your *customExtension* subkey.</span></span>

-   <span data-ttu-id="4d96e-130">**Разрешения**</span><span class="sxs-lookup"><span data-stu-id="4d96e-130">**Permissions**</span></span>
-   <span data-ttu-id="4d96e-131">**Параметры выполнения**</span><span class="sxs-lookup"><span data-stu-id="4d96e-131">**Runtime**</span></span>
-   <span data-ttu-id="4d96e-132">**форматкоде**</span><span class="sxs-lookup"><span data-stu-id="4d96e-132">**FormatCode**</span></span>

<span data-ttu-id="4d96e-133">Чтобы указать подключаемые модули преобразования для пользовательского формата файлов мультимедиа, создайте подраздел **конвертплугинклсид** в подразделе *кустомекстенсион* .</span><span class="sxs-lookup"><span data-stu-id="4d96e-133">To specify conversion plug-ins for your custom media file format, create a **ConvertPluginCLSID** subkey in your *customExtension* subkey.</span></span>

<span data-ttu-id="4d96e-134">Чтобы указать, где проигрыватель Windows Media должен отображать файлы в представлении библиотеки, напишите запись, представляющую пользовательский формат файла, в следующем подразделе.</span><span class="sxs-lookup"><span data-stu-id="4d96e-134">To specify where Windows Media Player should display your files in its library view, write an entry that represents your custom file format in the following subkey.</span></span>

<span data-ttu-id="4d96e-135">**HKEY \_ , \_ \\ программное обеспечение локального компьютера, \\ \\ расширения Microsoft MediaPlayer \\ MLS \\**</span><span class="sxs-lookup"><span data-stu-id="4d96e-135">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="4d96e-136">В следующих разделах описываются подразделы и записи реестра, предоставляющие проигрывателю Windows Media сведения о пользовательских форматах файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4d96e-136">The following topics describe the registry subkeys and entries that provide Windows Media Player with information about custom media file formats.</span></span>

-   [<span data-ttu-id="4d96e-137">Запись реестра разрешений</span><span class="sxs-lookup"><span data-stu-id="4d96e-137">Permissions Registry Entry</span></span>](permissions-registry-entry.md)
-   [<span data-ttu-id="4d96e-138">Запись реестра времени выполнения</span><span class="sxs-lookup"><span data-stu-id="4d96e-138">Runtime Registry Entry</span></span>](runtime-registry-entry.md)
-   [<span data-ttu-id="4d96e-139">Запись реестра Форматкоде</span><span class="sxs-lookup"><span data-stu-id="4d96e-139">FormatCode Registry Entry</span></span>](formatcode-registry-entry.md)
-   [<span data-ttu-id="4d96e-140">Записи реестра классификации библиотеки</span><span class="sxs-lookup"><span data-stu-id="4d96e-140">Library Classification Registry Entries</span></span>](library-classification-registry-entries.md)
-   [<span data-ttu-id="4d96e-141">Подраздел Конвертплугинклсид</span><span class="sxs-lookup"><span data-stu-id="4d96e-141">ConvertPluginCLSID Subkey</span></span>](convertpluginclsid-subkey.md)

## <a name="related-topics"></a><span data-ttu-id="4d96e-142">См. также</span><span class="sxs-lookup"><span data-stu-id="4d96e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d96e-143">**Параметры реестра**</span><span class="sxs-lookup"><span data-stu-id="4d96e-143">**Registry Settings**</span></span>](registry-settings.md)
</dt> <dt>

[<span data-ttu-id="4d96e-144">**Подключаемые модули преобразования проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4d96e-144">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




