---
title: Изменение приоритета синхронизации
description: Изменение приоритета синхронизации
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
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
- переносные устройства, изменение приоритетов списков воспроизведения синхронизации
- списки воспроизведения синхронизации, приоритеты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327f211282e2e3b35c21dce721a17f99dcb6583d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788845"
---
# <a name="changing-synchronization-priority"></a><span data-ttu-id="0bdd0-115">Изменение приоритета синхронизации</span><span class="sxs-lookup"><span data-stu-id="0bdd0-115">Changing Synchronization Priority</span></span>

<span data-ttu-id="0bdd0-116">В следующем примере кода указывается значение приоритета для каждого элемента в элементе управления ListView, определяемом IDC \_ плвиев.</span><span class="sxs-lookup"><span data-stu-id="0bdd0-116">The following example code specifies a priority value for each item in the ListView control identified by IDC\_PLVIEW.</span></span> <span data-ttu-id="0bdd0-117">Элементам, отмеченным флажком, назначается значение приоритета в зависимости от их порядка в списке.</span><span class="sxs-lookup"><span data-stu-id="0bdd0-117">Items that are marked with a check mark are assigned a priority value based on their order in the list.</span></span> <span data-ttu-id="0bdd0-118">Элементам, которые не проверялись, присваивается нулевое значение приоритета.</span><span class="sxs-lookup"><span data-stu-id="0bdd0-118">Items that are not checked are assigned a priority value of zero.</span></span>


```C++
void CSyncSettings::SetPriorities()
{
    ATLASSERT(m_spPlaylist.p);
    
    long lCount = 0;
    CComBSTR bstrAttribute(g_szSyncAttributeNames[m_lCurrentPSIndex]); 
    long lPriorityCount = 0; // Tracks the next priority value to be assigned.
    long lNewPriority = 0; // Contains the new priority value for the playlist.

    HRESULT hr = m_spPlaylist->get_count(&lCount);

    if(SUCCEEDED(hr) && lCount > 0)
    {
        HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
        HCURSOR hCursorOld = SetCursor(hCursor);

        // Walk the list.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            BOOL bChecked = ListView_GetCheckState(m_hPlView, i);

            if(TRUE == bChecked)
            {
                // Assign a priority value.
                lNewPriority = ++lPriorityCount;
            }
            else
            {
                // Not a sync playlist.
                lNewPriority = 0;
            }

            // Set the attribute on the playlist.
            hr = m_spPlaylist->get_item(i, &spMedia);

            if(SUCCEEDED(hr))
            {     
                WCHAR buffer[30];
                _ltow(lNewPriority, buffer, 10);
                CComBSTR bstrPriority(buffer);
                hr = spMedia->setItemInfo(bstrAttribute, bstrPriority);
            }
        }
        SetCursor(hCursorOld);
    }       
}
```



## <a name="related-topics"></a><span data-ttu-id="0bdd0-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0bdd0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bdd0-120">**Интерфейс Ивмпмедиа**</span><span class="sxs-lookup"><span data-stu-id="0bdd0-120">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="0bdd0-121">**Интерфейс Ивмпплайлист**</span><span class="sxs-lookup"><span data-stu-id="0bdd0-121">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="0bdd0-122">**Управление списками воспроизведения синхронизации**</span><span class="sxs-lookup"><span data-stu-id="0bdd0-122">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> </dl>

 

 




