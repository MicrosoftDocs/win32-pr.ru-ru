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
# <a name="sorting-playlists-by-synchronization-priority"></a>Сортировка списков воспроизведения по приоритету синхронизации

В следующем коде выполняется простая Сортировка списков воспроизведения. Вы можете увидеть, как эта функция используется в примере кода в разделе [Перечисление списков воспроизведения синхронизации](enumerating-synchronization-playlists.md). Функция принимает следующие параметры:

-   *пплайлист*. Указатель на список воспроизведения проигрывателя Windows Media для сортировки. Элементы мультимедиа в списке воспроизведения должны указывать на другие списки воспроизведения, а не отдельные цифровые файлы мультимедиа.
-   *бстрсинкаттрибуте*. Значение типа BSTR, содержащее имя атрибута партнерства синхронизации для текущего устройства ("Sync01", "Sync02" и т. д.).
-   *плселектед*. Указатель на **длинную** переменную, которая получает число списков воспроизведения синхронизации.

Функция проверяет атрибут партнерства синхронизации для каждого элемента мультимедиа (представляющего список воспроизведения) в списке воспроизведения, указанном параметром *пплайлист*. Если атрибут имеет ненулевое значение, код перемещает элемент мультимедиа в начало списка воспроизведения и вставляет его в порядок приоритета.

По завершении функция возвращает количество элементов мультимедиа (списков воспроизведения синхронизации) с ненулевым значением для атрибута партнерства синхронизации.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Ивмпмедиа:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**Ивмпплайлист:: получение \_ элемента**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[**Ивмпплайлист:: Мовеитем**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[**Управление списками воспроизведения синхронизации**](managing-synchronization-playlists.md)
</dt> <dt>

[**Атрибуты синхронизации**](sync-attributes.md)
</dt> </dl>

 

 




