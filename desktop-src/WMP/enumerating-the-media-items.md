---
title: Перечисление элементов мультимедиа
description: Перечисление элементов мультимедиа
ms.assetid: 1819b4c3-57ae-48fc-8a01-b699b5802b64
keywords:
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
- списки воспроизведения синхронизации, перечисление
- переносные устройства, перечисление
- перечисления, списки воспроизведения синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e07148ed6978355056febfb2ad920e4b1380a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691451"
---
# <a name="enumerating-the-media-items"></a><span data-ttu-id="c6f16-116">Перечисление элементов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c6f16-116">Enumerating the Media Items</span></span>

<span data-ttu-id="c6f16-117">Следующий код отображает элементы мультимедиа, содержащиеся в отдельном списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c6f16-117">The following code displays the media items contained in an individual playlist.</span></span> <span data-ttu-id="c6f16-118">Этот код выполняется, когда пользователь щелкает список воспроизведения в элементе управления ListView, определяемом IDC \_ плвиев.</span><span class="sxs-lookup"><span data-stu-id="c6f16-118">This code runs when the user clicks a playlist in the ListView control identified by IDC\_PLVIEW.</span></span>


```C++
STDMETHODIMP CSyncSettings::ShowMedia(long lIndex)
{
    ATLASSERT(m_pMainDlg != NULL);
    ATLASSERT(m_spPlaylist.p);

    HRESULT hr = S_OK;
    long lCount = 0; // Count of items in the playlist.

    LVITEM lvI;
    ZeroMemory(&lvI, sizeof(LVITEM));
    lvI.mask = LVIF_TEXT;

    CComPtr<IWMPMedia> spPlaylist; // Playlist the user selected.
    CComBSTR bstrSourceURL; // The URL of a digital media file.
    CComPtr<IWMPPlaylist> spNewPlaylist; // Temporary playlist that contains media items.
    ULONG ulOnDevice = 0;
    ULONG ulDidNotFit = 0;

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    ListView_DeleteAllItems(m_hMediaView);

    // Retrieve the playlist the user selected.
    hr = m_spPlaylist->get_item(lIndex, &spPlaylist);
  
    if(SUCCEEDED(hr) && spPlaylist)
    {
         // Retrieve the source URL (the path).
         hr = spPlaylist->get_sourceURL(&bstrSourceURL);
    }

    if(SUCCEEDED(hr) && bstrSourceURL.Length())
    {
        CComPtr<IWMPCore3> spCore3;
        m_spPlayer.QueryInterface(&spCore3);

        // Create a temporary IWMPPlaylist object from the IWMPMedia 
        // playlist object.
        hr = spCore3->newPlaylist(CComBSTR("Temp"), bstrSourceURL, &spNewPlaylist);
    }

    if(SUCCEEDED(hr) && spNewPlaylist)
    {        
        hr = spNewPlaylist->get_count(&lCount);
    }

    // Walk the playlist.
    if(SUCCEEDED(hr) && lCount > 0)
    {
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            CComBSTR bstrMediaName; 
            CComBSTR bstrOnDevice = "???";
            CComBSTR bstrFit = "???";  

            hr = spNewPlaylist->get_item(i, &spMedia);
   
            if(SUCCEEDED(hr) && spMedia)
            {
                // Get the name.
                hr = spMedia->get_name(&bstrMediaName);                
            }

            if(SUCCEEDED(hr) && bstrMediaName.Length())
            {   
                // Show the media name.
                lvI.iItem = ListView_GetItemCount(m_hMediaView);
                lvI.iSubItem = 0;
                lvI.pszText = COLE2T(bstrMediaName);
                ListView_InsertItem(m_hMediaView, &lvI);
                
                // Retrieve the synchronization state information for 
                // the digital media file.
                hr = GetPartnershipSyncState(spMedia, m_lCurrentPSIndex, &ulOnDevice, &ulDidNotFit);
            }

            if(SUCCEEDED(hr))
            {                
                // Test whether the media is on the device.
                if(ulOnDevice == 1)
                {
                    bstrOnDevice = "Yes";
                    bstrFit = "Yes";
                }
                else
                {
                    bstrOnDevice = "No";
                    // 1 means media did not fit, 
                    // 0 means other reason for failure.
                    bstrFit = ulDidNotFit ? "No" : "Yes"; 
                }                 
            }
   
            ListView_SetItemText(m_hMediaView, lvI.iItem, 1, COLE2T(bstrOnDevice)); 
            ListView_SetItemText(m_hMediaView, lvI.iItem, 2, COLE2T(bstrFit));
        }
    } 

    if(SUCCEEDED(hr) && lCount == 0)
    {
        // Empty playlist.
        lvI.iItem = ListView_GetItemCount(m_hMediaView);
        lvI.iSubItem = 0;
        lvI.pszText = COLE2T(CComBSTR("No items to display."));
        ListView_InsertItem(m_hMediaView, &lvI);
    }
    
    SetCursor(hCursorOld);
    return hr;
}
```



<span data-ttu-id="c6f16-119">Сведения о реализации функции Жетпартнершипсинкстате см. в разделе [Определение состояния синхронизации списка воспроизведения](determining-playlist-synchronization-state.md).</span><span class="sxs-lookup"><span data-stu-id="c6f16-119">For the implementation of the GetPartnershipSyncState function, see [Determining Playlist Synchronization State](determining-playlist-synchronization-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6f16-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c6f16-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6f16-121">**Интерфейс Ивмпмедиа**</span><span class="sxs-lookup"><span data-stu-id="c6f16-121">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="c6f16-122">**Интерфейс Ивмпплайлист**</span><span class="sxs-lookup"><span data-stu-id="c6f16-122">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="c6f16-123">**Управление списками воспроизведения синхронизации**</span><span class="sxs-lookup"><span data-stu-id="c6f16-123">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> </dl>

 

 




