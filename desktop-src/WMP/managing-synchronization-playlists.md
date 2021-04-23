---
title: Управление списками воспроизведения синхронизации
description: Управление списками воспроизведения синхронизации
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Проигрыватель Windows Media, переносные устройства
- Объектная модель проигрывателя Windows Media, переносные устройства
- Объектная модель, портативные устройства
- Элемент управления ActiveX проигрывателя Windows Media, переносные устройства
- Элемент управления ActiveX, переносные устройства
- Мобильный элемент управления ActiveX проигрывателя Windows Media, портативные устройства
- Проигрыватель Windows Media Mobile, переносные устройства
- переносные устройства, управление списками воспроизведения синхронизации
- синхронизация устройств, списки воспроизведения
- синхронизация устройств, списков воспроизведения
- Проигрыватель Windows Media, списки воспроизведения синхронизации
- Объектная модель проигрывателя Windows Media, списки воспроизведения синхронизации
- Объектная модель, списки воспроизведения синхронизации
- Проигрыватель Windows Media Mobile, списки воспроизведения синхронизации
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения синхронизации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, списки синхронизации
- Элемент управления ActiveX, списки воспроизведения синхронизации
- списки воспроизведения, синхронизация
- списки воспроизведения метафайлов, синхронизация
- Списки воспроизведения метафайлов Windows Media, синхронизация
- списки воспроизведения синхронизации, управление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0fe084918c0b69b827dbb941388246cbd177ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700718"
---
# <a name="managing-synchronization-playlists"></a><span data-ttu-id="07472-124">Управление списками воспроизведения синхронизации</span><span class="sxs-lookup"><span data-stu-id="07472-124">Managing Synchronization Playlists</span></span>

<span data-ttu-id="07472-125">Проигрыватель Windows Media 10 или более поздней версии использует списки воспроизведения для синхронизации цифровых файлов мультимедиа с портативными устройствами.</span><span class="sxs-lookup"><span data-stu-id="07472-125">Windows Media Player 10 or later uses playlists to synchronize digital media files with portable devices.</span></span> <span data-ttu-id="07472-126">В этом разделе объясняется, как работать с списками воспроизведения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="07472-126">This section explains how to work with synchronization playlists.</span></span>

<span data-ttu-id="07472-127">В примере кода в этом разделе для вывода информации используются два элемента управления ListView.</span><span class="sxs-lookup"><span data-stu-id="07472-127">The example code in this section uses two ListView controls to display information.</span></span> <span data-ttu-id="07472-128">Первый элемент управления ListView (IDC \_ плвиев) отображает все списки воспроизведения в библиотеке проигрывателя Windows Media с первыми появлением списков воспроизведения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="07472-128">The first ListView control (IDC\_PLVIEW) displays all of the playlists in the Windows Media Player library, with synchronization playlists appearing first.</span></span> <span data-ttu-id="07472-129">Списки воспроизведения синхронизации для текущего выбранного устройства отмечены галочкой и сортируются в порядке приоритета синхронизации.</span><span class="sxs-lookup"><span data-stu-id="07472-129">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="07472-130">Все остальные списки воспроизведения не отмечены флажками.</span><span class="sxs-lookup"><span data-stu-id="07472-130">All other playlists are unchecked.</span></span> <span data-ttu-id="07472-131">Элемент управления ListView настроен для выбора только одного элемента.</span><span class="sxs-lookup"><span data-stu-id="07472-131">The ListView control was configured for single selection.</span></span> <span data-ttu-id="07472-132">Порядок списков воспроизведения в элементе управления ListView определяет приоритет синхронизации.</span><span class="sxs-lookup"><span data-stu-id="07472-132">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="07472-133">Состояние проверки отдельного списка воспроизведения определяет, является ли он списком синхронизации для текущего выбранного устройства.</span><span class="sxs-lookup"><span data-stu-id="07472-133">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="07472-134">Второй элемент управления ListView (IDC \_ медиавиев) отображает элементы мультимедиа в выбранном списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="07472-134">The second ListView control (IDC\_MEDIAVIEW) displays the media items in the selected playlist.</span></span> <span data-ttu-id="07472-135">В двух дополнительных столбцах отображается текст, указывающий, был ли скопирован файл мультимедиа на устройство, и, в случае сбоя, неудачную попытку копирования из-за того, что файл цифрового мультимедиа не поместится.</span><span class="sxs-lookup"><span data-stu-id="07472-135">Two additional columns display text indicating whether the digital media file was copied to the device and, in the case of a failure, whether the copy failed because the digital media file did not fit.</span></span>

<span data-ttu-id="07472-136">В следующем примере кода показано, как инициализируются элементы управления ListView:</span><span class="sxs-lookup"><span data-stu-id="07472-136">The following example code shows how the ListView controls are initialized:</span></span>


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



<span data-ttu-id="07472-137">Следующий массив строк содержит имена атрибутов синхронизации, используемых в примерах:</span><span class="sxs-lookup"><span data-stu-id="07472-137">The following array of strings contains the names of the synchronization attributes used in the examples:</span></span>


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



<span data-ttu-id="07472-138">Следующая переменная-член содержит список воспроизведения, содержащий все списки воспроизведения в библиотеке проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="07472-138">The following member variable contains a playlist containing all playlists in the Windows Media Player library.</span></span> <span data-ttu-id="07472-139">Каждый список воспроизведения представлен в виде элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="07472-139">Each playlist is represented as a media item.</span></span>


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



<span data-ttu-id="07472-140">В следующих разделах приводится пример кода:</span><span class="sxs-lookup"><span data-stu-id="07472-140">The following sections provide example code:</span></span>

-   [<span data-ttu-id="07472-141">Перечисление списков воспроизведения синхронизации</span><span class="sxs-lookup"><span data-stu-id="07472-141">Enumerating Synchronization Playlists</span></span>](enumerating-synchronization-playlists.md)
-   [<span data-ttu-id="07472-142">Сортировка списков воспроизведения по приоритету синхронизации</span><span class="sxs-lookup"><span data-stu-id="07472-142">Sorting Playlists by Synchronization Priority</span></span>](sorting-playlists-by-synchronization-priority.md)
-   [<span data-ttu-id="07472-143">Перечисление элементов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="07472-143">Enumerating the Media Items</span></span>](enumerating-the-media-items.md)
-   [<span data-ttu-id="07472-144">Определение состояния синхронизации списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="07472-144">Determining Playlist Synchronization State</span></span>](determining-playlist-synchronization-state.md)
-   [<span data-ttu-id="07472-145">Изменение приоритета синхронизации</span><span class="sxs-lookup"><span data-stu-id="07472-145">Changing Synchronization Priority</span></span>](changing-synchronization-priority.md)

## <a name="related-topics"></a><span data-ttu-id="07472-146">См. также</span><span class="sxs-lookup"><span data-stu-id="07472-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07472-147">**Работа с портативными устройствами**</span><span class="sxs-lookup"><span data-stu-id="07472-147">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




