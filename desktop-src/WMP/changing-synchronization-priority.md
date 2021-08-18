---
title: Изменение приоритета синхронизации
description: Изменение приоритета синхронизации
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
keywords:
- проигрыватель Windows Media, списки воспроизведения синхронизации
- объектная модель проигрыватель Windows Media, списки воспроизведения синхронизации
- Объектная модель, списки воспроизведения синхронизации
- проигрыватель Windows Media Мобильные устройства, списки синхронизации
- проигрыватель Windows Media ActiveX элемент управления, списки воспроизведения синхронизации
- проигрыватель Windows Media управление мобильными ActiveXми, списки воспроизведения синхронизации
- элемент управления ActiveX, списки воспроизведения синхронизации
- списки воспроизведения, синхронизация
- списки воспроизведения метафайлов, синхронизация
- Windows Списки воспроизведения мультимедийных метафайлов, синхронизация
- переносные устройства, изменение приоритетов списков воспроизведения синхронизации
- списки воспроизведения синхронизации, приоритеты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1513679bcde31893cd7c4f456bc0e99404bb5dc66de37976f2053ae1559a4cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997664"
---
# <a name="changing-synchronization-priority"></a>Изменение приоритета синхронизации

В следующем примере кода указывается значение приоритета для каждого элемента в элементе управления ListView, определяемом IDC \_ плвиев. Элементам, отмеченным флажком, назначается значение приоритета в зависимости от их порядка в списке. Элементам, которые не проверялись, присваивается нулевое значение приоритета.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмпмедиа**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Интерфейс Ивмпплайлист**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Управление списками воспроизведения синхронизации**](managing-synchronization-playlists.md)
</dt> </dl>

 

 




