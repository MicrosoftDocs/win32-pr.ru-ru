---
title: Записи реестра классификации библиотеки
description: Записи реестра классификации библиотеки
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Проигрыватель Windows Media, Библиотека
- Проигрыватель Windows Media, записи реестра классификации
- Проигрыватель Windows Media, расширения имен файлов
- Проигрыватель Windows Media, реестр
- реестр, расширения имен файлов
- реестр, записи классификации библиотеки
- реестр, параметры для проигрывателя Windows Media
- параметры реестра для расширения имени файла
- Библиотека, записи реестра классификации
- Библиотека, реестр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691296"
---
# <a name="library-classification-registry-entries"></a><span data-ttu-id="8a792-113">Записи реестра классификации библиотеки</span><span class="sxs-lookup"><span data-stu-id="8a792-113">Library Classification Registry Entries</span></span>

<span data-ttu-id="8a792-114">Когда проигрыватель Windows Media обнаруживает файл мультимедиа с пользовательским расширением имени файла, он не знает, следует ли классифицировать файл как аудио, видео или какой-либо другой тип.</span><span class="sxs-lookup"><span data-stu-id="8a792-114">When Windows Media Player encounters a media file that has a custom file name extension, it does not know whether the file should be classified as audio, video, or some other type.</span></span> <span data-ttu-id="8a792-115">По умолчанию проигрыватель Windows Media помещает такие файлы в другую часть носителя библиотеки.</span><span class="sxs-lookup"><span data-stu-id="8a792-115">By default, Windows Media Player places such files in the Other Media portion of the library.</span></span>

<span data-ttu-id="8a792-116">Если файлы цифрового мультимедиа имеют пользовательский формат, можно предоставить проигрывателю Windows Media сведения о том, где файлы должны отображаться в библиотеке проигрывателя, разместив две записи в реестре на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="8a792-116">If your digital media files have a custom format, you can provide Windows Media Player with information about where your files should appear in the Player's library by placing two entries in the registry on the user's computer.</span></span>

<span data-ttu-id="8a792-117">Одна запись помещается в следующий подраздел.</span><span class="sxs-lookup"><span data-stu-id="8a792-117">One entry goes in the following subkey.</span></span>

<span data-ttu-id="8a792-118">**HKEY \_ , \_ \\ программное обеспечение локального компьютера, \\ \\ расширения Microsoft MediaPlayer \\ MLS \\**</span><span class="sxs-lookup"><span data-stu-id="8a792-118">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MediaPlayer\\MLS\\Extensions**</span></span>

<span data-ttu-id="8a792-119">Запись реестра имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="8a792-119">The registry entry has the following format.</span></span>



| <span data-ttu-id="8a792-120">Имя</span><span class="sxs-lookup"><span data-stu-id="8a792-120">Name</span></span>                                                  | <span data-ttu-id="8a792-121">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8a792-121">Data type</span></span>   | <span data-ttu-id="8a792-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8a792-122">Value</span></span>                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| <span data-ttu-id="8a792-123">Расширение имени файла без разделителя с точкой (.)</span><span class="sxs-lookup"><span data-stu-id="8a792-123">The file name extension without the dot (.) separator</span></span> | <span data-ttu-id="8a792-124">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="8a792-124">**REG\_SZ**</span></span> | <span data-ttu-id="8a792-125">Строка, указывающая расположение библиотеки</span><span class="sxs-lookup"><span data-stu-id="8a792-125">A string that specifies a library location</span></span> |



 

<span data-ttu-id="8a792-126">Другая запись реестра находится в следующем созданном вами подразделе.</span><span class="sxs-lookup"><span data-stu-id="8a792-126">The other registry entry goes in the following subkey that you create.</span></span>

<span data-ttu-id="8a792-127">**HKey \_ \_Корневые \\** *кустомекстенсион* классов</span><span class="sxs-lookup"><span data-stu-id="8a792-127">**HKEY\_CLASSES\_ROOT\\** *customExtension*</span></span>

<span data-ttu-id="8a792-128">где *кустомекстенсион* — это расширение имени файла, включая разделитель точек (.).</span><span class="sxs-lookup"><span data-stu-id="8a792-128">where *customExtension* is the file name extension including the dot (.) separator.</span></span>

<span data-ttu-id="8a792-129">Запись реестра имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="8a792-129">The registry entry has the following format.</span></span>



| <span data-ttu-id="8a792-130">Имя</span><span class="sxs-lookup"><span data-stu-id="8a792-130">Name</span></span>          | <span data-ttu-id="8a792-131">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8a792-131">Data type</span></span>   | <span data-ttu-id="8a792-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8a792-132">Value</span></span>                                      |
|---------------|-------------|--------------------------------------------|
| <span data-ttu-id="8a792-133">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="8a792-133">PerceivedType</span></span> | <span data-ttu-id="8a792-134">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="8a792-134">**REG\_SZ**</span></span> | <span data-ttu-id="8a792-135">Строка, указывающая расположение библиотеки</span><span class="sxs-lookup"><span data-stu-id="8a792-135">A string that specifies a library location</span></span> |



 

<span data-ttu-id="8a792-136">Оба элемента реестра должны иметь одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="8a792-136">Both registry entries must have the same value.</span></span> <span data-ttu-id="8a792-137">Возможные значения приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8a792-137">Possible values are given in the following table.</span></span>



| <span data-ttu-id="8a792-138">Значение</span><span class="sxs-lookup"><span data-stu-id="8a792-138">Value</span></span> | <span data-ttu-id="8a792-139">Описание</span><span class="sxs-lookup"><span data-stu-id="8a792-139">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8a792-140">звук</span><span class="sxs-lookup"><span data-stu-id="8a792-140">audio</span></span> | <span data-ttu-id="8a792-141">Файлы с пользовательским расширением отображаются в музыкальной части библиотеки.</span><span class="sxs-lookup"><span data-stu-id="8a792-141">Files that have the custom extension appear in the music portion of the library.</span></span> |
| <span data-ttu-id="8a792-142">видео</span><span class="sxs-lookup"><span data-stu-id="8a792-142">video</span></span> | <span data-ttu-id="8a792-143">Файлы с пользовательским расширением отображаются в видеообласти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="8a792-143">Files that have the custom extension appear in the video portion of the library.</span></span> |



 

<span data-ttu-id="8a792-144">Например, следующие записи реестра указывают, что файлы с расширением. XYZ будут отображаться в музыкальной части библиотеки:</span><span class="sxs-lookup"><span data-stu-id="8a792-144">For example, the following registry entries specify that files having the file name extension .xyz will appear in the music portion of the library:</span></span>


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



<span data-ttu-id="8a792-145">Обратите внимание, что любой код, пытающийся выполнить запись в реестр на компьютере пользователя, может выполнять запись в \_ поддерево hKey на локальном компьютере \_ только в том случае, если у текущего пользователя есть права администратора.</span><span class="sxs-lookup"><span data-stu-id="8a792-145">Note that any code that attempts to write to the registry on the user's computer can write to the HKEY\_LOCAL\_MACHINE subtree only if the current user has administrative privileges.</span></span>

<span data-ttu-id="8a792-146">Записи реестра классификации библиотеки поддерживаются следующими версиями проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a792-146">Library classification registry entries are supported by the following versions of Windows Media Player.</span></span>

-   <span data-ttu-id="8a792-147">Проигрыватель Windows Media 9 Series с исправлением 823275</span><span class="sxs-lookup"><span data-stu-id="8a792-147">Windows Media Player 9 Series with hotfix 823275</span></span>
-   <span data-ttu-id="8a792-148">Проигрыватель Windows Media 10 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="8a792-148">Windows Media Player 10 and later</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a792-149">См. также</span><span class="sxs-lookup"><span data-stu-id="8a792-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a792-150">**Параметры реестра для расширения имени файла**</span><span class="sxs-lookup"><span data-stu-id="8a792-150">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




