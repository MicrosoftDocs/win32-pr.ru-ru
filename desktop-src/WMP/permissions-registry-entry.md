---
title: Запись реестра разрешений
description: Запись реестра разрешений
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Проигрыватель Windows Media, расширения имен файлов
- Проигрыватель Windows Media, разрешения
- Проигрыватель Windows Media, реестр
- реестр, расширения имен файлов
- реестр, разрешения
- реестр, параметры для проигрывателя Windows Media
- параметры реестра для расширения имени файла
- разрешения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069544"
---
# <a name="permissions-registry-entry"></a><span data-ttu-id="5cb2a-111">Запись реестра разрешений</span><span class="sxs-lookup"><span data-stu-id="5cb2a-111">Permissions Registry Entry</span></span>

<span data-ttu-id="5cb2a-112">Когда проигрыватель Windows Media обнаруживает пользовательское расширение имени файла, он ищет подраздел реестра, соответствующий этому расширению.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="5cb2a-113">Подраздел описывается в [разделе Параметры реестра расширения имени файла](file-name-extension-registry-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5cb2a-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="5cb2a-114">Одна из записей реестра, которые могут отображаться в подразделе расширения, — это запись **разрешений** .</span><span class="sxs-lookup"><span data-stu-id="5cb2a-114">One of the registry entries that can appear under the extension's subkey is the **Permissions** entry.</span></span>

<span data-ttu-id="5cb2a-115">Запись **Permissions** указывает действия, которые проигрыватель Windows Media может выполнять для файлов с пользовательским расширением.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-115">The **Permissions** entry specifies the actions that Windows Media Player is allowed to perform on files that have the custom extension.</span></span> <span data-ttu-id="5cb2a-116">Запись **разрешений** имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-116">The **Permissions** entry has the following form.</span></span>



| <span data-ttu-id="5cb2a-117">Имя</span><span class="sxs-lookup"><span data-stu-id="5cb2a-117">Name</span></span>        | <span data-ttu-id="5cb2a-118">Тип</span><span class="sxs-lookup"><span data-stu-id="5cb2a-118">Type</span></span>           | <span data-ttu-id="5cb2a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5cb2a-119">Value</span></span>                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="5cb2a-120">Разрешения</span><span class="sxs-lookup"><span data-stu-id="5cb2a-120">Permissions</span></span> | <span data-ttu-id="5cb2a-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5cb2a-121">**REG\_DWORD**</span></span> | <span data-ttu-id="5cb2a-122">Набор флагов, каждый из которых предоставляет разрешение для конкретного действия.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-122">A set of flags, each of which grants permission for a specific action.</span></span> |



 

<span data-ttu-id="5cb2a-123">Значение записи **разрешений** является побитовым **или** одним или несколькими из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-123">The value of the **Permissions** entry is a bitwise **OR** of one or more of the following flags.</span></span>



| <span data-ttu-id="5cb2a-124">Флаг (десятичное значение)</span><span class="sxs-lookup"><span data-stu-id="5cb2a-124">Flag (decimal value)</span></span> | <span data-ttu-id="5cb2a-125">Описание</span><span class="sxs-lookup"><span data-stu-id="5cb2a-125">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb2a-126">1</span><span class="sxs-lookup"><span data-stu-id="5cb2a-126">1</span></span>                    | <span data-ttu-id="5cb2a-127">Разрешение на воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-127">Permission for playback.</span></span> <span data-ttu-id="5cb2a-128">Файлы с зарегистрированным расширением имени файла можно воспроизводить.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-128">Files having the registered file name extension can be played.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="5cb2a-129">2</span><span class="sxs-lookup"><span data-stu-id="5cb2a-129">2</span></span>                    | <span data-ttu-id="5cb2a-130">Разрешение на удаление папки.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-130">Permission for folder drop.</span></span> <span data-ttu-id="5cb2a-131">Файлы с зарегистрированным расширением имени файла будут включаться в список воспроизведения, когда пользователь перетаскивает папку с файлами и удаляет ее в пользовательском интерфейсе проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-131">Files having the registered file name extension will be included in the playlist created when the user drags a folder containing the files and drops it on the user interface of the Player.</span></span>                                                      |
| <span data-ttu-id="5cb2a-132">4</span><span class="sxs-lookup"><span data-stu-id="5cb2a-132">4</span></span>                    | <span data-ttu-id="5cb2a-133">Разрешение для компакт-диска мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-133">Permission for media CD.</span></span> <span data-ttu-id="5cb2a-134">Файлы, имеющие зарегистрированное расширение имени файла, будут включены в список воспроизведения, созданный при вставке компакт-диска с файлами в устройство чтения компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-134">Files having the registered file name extension will be included in the playlist created when a CD containing the files is inserted into the CD-ROM drive.</span></span>                                                                                           |
| <span data-ttu-id="5cb2a-135">8</span><span class="sxs-lookup"><span data-stu-id="5cb2a-135">8</span></span>                    | <span data-ttu-id="5cb2a-136">Разрешение для библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-136">Permission for the library.</span></span> <span data-ttu-id="5cb2a-137">Файлы с зарегистрированным расширением имени файла можно добавить в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-137">Files having the registered file name extension can be added to the library.</span></span> <span data-ttu-id="5cb2a-138">Требуется для подключаемых модулей преобразования.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-138">Required for conversion plug-ins.</span></span>                                                                                                                                    |
| <span data-ttu-id="5cb2a-139">16</span><span class="sxs-lookup"><span data-stu-id="5cb2a-139">16</span></span>                   | <span data-ttu-id="5cb2a-140">Разрешение для потоковой передачи HTML.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-140">Permission for HTML streaming.</span></span> <span data-ttu-id="5cb2a-141">Файлы с зарегистрированным расширением имени файла будут вставлены в кэш Internet Explorer при доставке из веб-потока.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-141">Files having the registered file name extension will be inserted into the Internet Explorer cache when delivered from a Web stream.</span></span>                                                                                                            |
| <span data-ttu-id="5cb2a-142">128</span><span class="sxs-lookup"><span data-stu-id="5cb2a-142">128</span></span>                  | <span data-ttu-id="5cb2a-143">Разрешение на перекодирование.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-143">Permission for transcoding.</span></span> <span data-ttu-id="5cb2a-144">Файлы с зарегистрированным расширением имени файла можно перекодировать в формат Windows Media при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-144">Files having the registered file name extension can be transcoded to Windows Media Format under certain conditions.</span></span> <span data-ttu-id="5cb2a-145">См. раздел [ивмптранскодеполици:: алловтранскоде](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span><span class="sxs-lookup"><span data-stu-id="5cb2a-145">See [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode).</span></span> <span data-ttu-id="5cb2a-146">Требуется проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-146">Requires Windows Media Player 10 or later.</span></span> |



 

<span data-ttu-id="5cb2a-147">Когда пользователь пытается воспроизвести файл мультимедиа с пользовательским расширением имени файла, проигрыватель Windows Media ищет подраздел реестра, соответствующий этому расширению.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-147">When the user attempts to play a media file that has a custom file name extension, Windows Media Player looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="5cb2a-148">Если совпадений не найдено, проигрыватель предоставляет пользователю диалоговое окно с предупреждением, предлагающее пользователю получить разрешение на попытку воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-148">If no match is found, the Player presents the user with a warning dialog box that prompts the user for permission to attempt to play the file.</span></span> <span data-ttu-id="5cb2a-149">Если вы создаете цифровые файлы мультимедиа с пользовательскими расширениями имени файла, вы можете предотвратить отображение этого предупреждения на компьютере пользователя путем регистрации расширения имени файла и предоставления записи **разрешений** .</span><span class="sxs-lookup"><span data-stu-id="5cb2a-149">If you create digital media files with custom file name extensions, you can prevent this warning from appearing on the user's computer by registering the file name extension and providing a **Permissions** entry.</span></span>

<span data-ttu-id="5cb2a-150">Запись **разрешений** (кроме значения флага 128) поддерживается в проигрывателе Windows Media 9 Series и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-150">The **Permissions** entry (except for the flag value 128) is supported by Windows Media Player 9 Series and later.</span></span> <span data-ttu-id="5cb2a-151">Значение флага 128 поддерживается проигрывателем Windows Media 10 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="5cb2a-151">The flag value 128 is supported by Windows Media Player 10 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cb2a-152">См. также</span><span class="sxs-lookup"><span data-stu-id="5cb2a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cb2a-153">**Параметры реестра для расширения имени файла**</span><span class="sxs-lookup"><span data-stu-id="5cb2a-153">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




