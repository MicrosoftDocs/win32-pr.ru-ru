---
title: Параметры реестра мониторинга папок
description: Параметры реестра мониторинга папок
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Проигрыватель Windows Media, параметры реестра мониторинга папок
- Проигрыватель Windows Media, параметры реестра для мониторинга папки с файлами
- Проигрыватель Windows Media, реестр
- реестр, параметры наблюдения за папками
- реестр, параметры наблюдения за папкой файлов
- реестр, параметры для проигрывателя Windows Media
- параметры реестра мониторинга папок
- параметры реестра для мониторинга папки файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104413960"
---
# <a name="folder-monitoring-registry-settings"></a><span data-ttu-id="82298-111">Параметры реестра мониторинга папок</span><span class="sxs-lookup"><span data-stu-id="82298-111">Folder Monitoring Registry Settings</span></span>

<span data-ttu-id="82298-112">Проигрыватель Windows Media 9 Series или более поздней версии может отслеживать файловые папки для новых файлов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="82298-112">Windows Media Player 9 Series or later can monitor file folders for new digital media files.</span></span> <span data-ttu-id="82298-113">Когда проигрыватель обнаруживает новый файл в наблюдаемой папке, он автоматически добавляет файл в библиотеку.</span><span class="sxs-lookup"><span data-stu-id="82298-113">When the Player detects a new file in a monitored folder, it automatically adds the file to the library.</span></span> <span data-ttu-id="82298-114">Для проигрывателя Windows Media 9 через проигрыватель Windows Media 11 Пользователи могут изменить список наблюдаемых папок, нажав кнопку **мониторинг папок** на вкладке Библиотека диалогового окна **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="82298-114">For Windows Media Player 9 through Windows Media Player 11, users can change the list of monitored folders by clicking **Monitor Folders** on the library tab of the **Options** dialog box.</span></span> <span data-ttu-id="82298-115">Для проигрывателя Windows Media 12 пользователь может изменить список наблюдаемых папок, следуя инструкциям в разделе [Добавление элементов в библиотеку проигрывателя Windows Media](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span><span class="sxs-lookup"><span data-stu-id="82298-115">For Windows Media Player 12, a user can change the list of monitored folders by following the instructions in the topic [Add items to the Windows Media Player Library](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library).</span></span> <span data-ttu-id="82298-116">Для проигрывателя Windows Media 9 и Windows Media Player 11 можно программно добавить отслеживаемую папку, добавив значение в реестр.</span><span class="sxs-lookup"><span data-stu-id="82298-116">For Windows Media Player 9 through Windows Media Player 11, you can programmatically add a folder to be monitored by adding a value to the registry.</span></span> <span data-ttu-id="82298-117">Для Windows Media Player 12 нельзя использовать реестр для программного добавления и удаления отслеживаемых папок.</span><span class="sxs-lookup"><span data-stu-id="82298-117">For Windows Media Player 12, you cannot use the registry to programmatically add or remove folders to be monitored.</span></span>

<span data-ttu-id="82298-118">Для добавления папки для мониторинга в проигрывателе Windows Media 9 — в проигрывателе Windows Media 11 необходимо сначала создать или изменить два значения в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="82298-118">For Windows Media Player 9 through Windows Media Player 11, to add a folder for monitoring you must first create or modify two values in the following registry key:</span></span>

<span data-ttu-id="82298-119">**\_ \_ \\ \\ Параметры по Microsoft \\ MediaPlayer \\ для текущего пользователя hKey\\**</span><span class="sxs-lookup"><span data-stu-id="82298-119">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Preferences\\**</span></span>

<span data-ttu-id="82298-120">Новые значения должны называться следующим образом.</span><span class="sxs-lookup"><span data-stu-id="82298-120">The new values must be named as follows.</span></span>



| <span data-ttu-id="82298-121">Имя</span><span class="sxs-lookup"><span data-stu-id="82298-121">Name</span></span>                           | <span data-ttu-id="82298-122">Тип</span><span class="sxs-lookup"><span data-stu-id="82298-122">Type</span></span>           | <span data-ttu-id="82298-123">Описание</span><span class="sxs-lookup"><span data-stu-id="82298-123">Description</span></span>                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82298-124">**траккфолдерсдиректориес**</span><span class="sxs-lookup"><span data-stu-id="82298-124">**TrackFoldersDirectories**</span></span>    | <span data-ttu-id="82298-125">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="82298-125">**REG\_DWORD**</span></span> | <span data-ttu-id="82298-126">Значение **типа DWORD** , представляющее число отслеживаемых папок.</span><span class="sxs-lookup"><span data-stu-id="82298-126">A **DWORD** value that represents the count of folders to monitor.</span></span> <span data-ttu-id="82298-127">Оно должно соответствовать числу значений \**траккфолдерсдиректориес \* \* \* X* .</span><span class="sxs-lookup"><span data-stu-id="82298-127">This must match the count of \**TrackFoldersDirectories\*\*\*X* values.</span></span>                                                                                                                                         |
| <span data-ttu-id="82298-128">\**Траккфолдерсдиректориес \* \* \* X*</span><span class="sxs-lookup"><span data-stu-id="82298-128">\**TrackFoldersDirectories\*\*\*X*</span></span> | <span data-ttu-id="82298-129">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="82298-129">**REG\_SZ**</span></span>    | <span data-ttu-id="82298-130">Строковое значение, представляющее путь к отслеживаемой папке.</span><span class="sxs-lookup"><span data-stu-id="82298-130">A string value that represents the path of the folder to monitor.</span></span> <span data-ttu-id="82298-131">Каждой отслеживаемой папке требуется отдельное значение.</span><span class="sxs-lookup"><span data-stu-id="82298-131">Each folder to monitor requires a separate value.</span></span> <span data-ttu-id="82298-132">Суффикс *X* — это целое число, которое всегда должно начинаться с 0 и затем увеличиваться на 1.</span><span class="sxs-lookup"><span data-stu-id="82298-132">The suffix *X* is an integer that should always begin at 0 and then increment by 1.</span></span> <span data-ttu-id="82298-133">Проигрыватель Windows Media также отслеживает вложенные папки указанной папки.</span><span class="sxs-lookup"><span data-stu-id="82298-133">Windows Media Player also monitors subfolders of the specified folder.</span></span> |



 

<span data-ttu-id="82298-134">Например, чтобы добавить первую отслеживаемую папку, добавьте следующее значение:</span><span class="sxs-lookup"><span data-stu-id="82298-134">For example, to add the first folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



<span data-ttu-id="82298-135">Затем создайте значение Count:</span><span class="sxs-lookup"><span data-stu-id="82298-135">Then, create the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



<span data-ttu-id="82298-136">Чтобы добавить вторую папку для отслеживания, добавьте следующее значение:</span><span class="sxs-lookup"><span data-stu-id="82298-136">To add a second folder to monitor, add the following value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



<span data-ttu-id="82298-137">Затем увеличьте значение счетчика:</span><span class="sxs-lookup"><span data-stu-id="82298-137">Then, increment the count value:</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a><span data-ttu-id="82298-138">См. также</span><span class="sxs-lookup"><span data-stu-id="82298-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82298-139">**Параметры реестра**</span><span class="sxs-lookup"><span data-stu-id="82298-139">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




