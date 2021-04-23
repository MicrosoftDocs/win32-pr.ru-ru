---
title: Сортировка списков воспроизведения по приоритету синхронизации
description: Сортировка списков воспроизведения по приоритету синхронизации
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
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
- переносные устройства, сортировка списков воспроизведения синхронизации
- синхронизации списков воспроизведения, сортировка
- списки воспроизведения синхронизации, приоритеты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890252"
---
# <a name="sorting-playlists-by-synchronization-priority"></a><span data-ttu-id="6056c-116">Сортировка списков воспроизведения по приоритету синхронизации</span><span class="sxs-lookup"><span data-stu-id="6056c-116">Sorting Playlists by Synchronization Priority</span></span>

<span data-ttu-id="6056c-117">В следующем коде выполняется простая Сортировка списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6056c-117">The following code performs a simple sort of playlists.</span></span> <span data-ttu-id="6056c-118">Вы можете увидеть, как эта функция используется в примере кода в разделе [Перечисление списков воспроизведения синхронизации](enumerating-synchronization-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="6056c-118">You can see how this function is used in the example code in [Enumerating Synchronization Playlists](enumerating-synchronization-playlists.md).</span></span> <span data-ttu-id="6056c-119">Функция принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6056c-119">The function takes the following parameters:</span></span>

-   <span data-ttu-id="6056c-120">*пплайлист*.</span><span class="sxs-lookup"><span data-stu-id="6056c-120">*pPlaylist*.</span></span> <span data-ttu-id="6056c-121">Указатель на список воспроизведения проигрывателя Windows Media для сортировки.</span><span class="sxs-lookup"><span data-stu-id="6056c-121">The pointer to the Windows Media Player playlist to sort.</span></span> <span data-ttu-id="6056c-122">Элементы мультимедиа в списке воспроизведения должны указывать на другие списки воспроизведения, а не отдельные цифровые файлы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6056c-122">The media items in the playlist must point to other playlists, not individual digital media files.</span></span>
-   <span data-ttu-id="6056c-123">*бстрсинкаттрибуте*.</span><span class="sxs-lookup"><span data-stu-id="6056c-123">*bstrSyncAttribute*.</span></span> <span data-ttu-id="6056c-124">Значение типа BSTR, содержащее имя атрибута партнерства синхронизации для текущего устройства ("Sync01", "Sync02" и т. д.).</span><span class="sxs-lookup"><span data-stu-id="6056c-124">A BSTR containing the name of the synchronization partnership attribute for the current device ("Sync01", "Sync02", and so on).</span></span>
-   <span data-ttu-id="6056c-125">*плселектед*.</span><span class="sxs-lookup"><span data-stu-id="6056c-125">*plSelected*.</span></span> <span data-ttu-id="6056c-126">Указатель на **длинную** переменную, которая получает число списков воспроизведения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6056c-126">Pointer to a **long** variable that receives the count of synchronization playlists.</span></span>

<span data-ttu-id="6056c-127">Функция проверяет атрибут партнерства синхронизации для каждого элемента мультимедиа (представляющего список воспроизведения) в списке воспроизведения, указанном параметром *пплайлист*.</span><span class="sxs-lookup"><span data-stu-id="6056c-127">The function inspects the synchronization partnership attribute for each media item (representing a playlist) in the playlist specified by *pPlaylist*.</span></span> <span data-ttu-id="6056c-128">Если атрибут имеет ненулевое значение, код перемещает элемент мультимедиа в начало списка воспроизведения и вставляет его в порядок приоритета.</span><span class="sxs-lookup"><span data-stu-id="6056c-128">If the attribute has a nonzero value, the code moves the media item to the beginning of the playlist and inserts it in priority order.</span></span>

<span data-ttu-id="6056c-129">По завершении функция возвращает количество элементов мультимедиа (списков воспроизведения синхронизации) с ненулевым значением для атрибута партнерства синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6056c-129">When finished, the function returns the count of media items (synchronization playlists) that had a nonzero value for the synchronization partnership attribute.</span></span>


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6056c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6056c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6056c-131">**Ивмпмедиа:: getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="6056c-131">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="6056c-132">**Ивмпплайлист:: получение \_ элемента**</span><span class="sxs-lookup"><span data-stu-id="6056c-132">**IWMPPlaylist::get\_item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[<span data-ttu-id="6056c-133">**Ивмпплайлист:: Мовеитем**</span><span class="sxs-lookup"><span data-stu-id="6056c-133">**IWMPPlaylist::moveItem**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[<span data-ttu-id="6056c-134">**Управление списками воспроизведения синхронизации**</span><span class="sxs-lookup"><span data-stu-id="6056c-134">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="6056c-135">**Атрибуты синхронизации**</span><span class="sxs-lookup"><span data-stu-id="6056c-135">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




