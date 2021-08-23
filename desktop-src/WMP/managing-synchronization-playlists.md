---
title: Управление списками воспроизведения синхронизации
description: Управление списками воспроизведения синхронизации
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- проигрыватель Windows Media, портативные устройства
- объектная модель проигрыватель Windows Media, переносные устройства
- Объектная модель, портативные устройства
- проигрыватель Windows Media ActiveX элемент управления, портативные устройства
- ActiveX элемент управления, переносные устройства
- проигрыватель Windows Media мобильный ActiveX элемент управления, переносные устройства
- проигрыватель Windows Media Мобильные, портативные устройства
- переносные устройства, управление списками воспроизведения синхронизации
- синхронизация устройств, списки воспроизведения
- синхронизация устройств, списков воспроизведения
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
- списки воспроизведения синхронизации, управление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10253d7f08c618d62079ccc1767fdaf85560861eae68d39cd897e7959eaffcad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996374"
---
# <a name="managing-synchronization-playlists"></a>Управление списками воспроизведения синхронизации

проигрыватель Windows Media 10 или более поздней версии использует списки воспроизведения для синхронизации цифровых файлов мультимедиа с портативными устройствами. В этом разделе объясняется, как работать с списками воспроизведения синхронизации.

В примере кода в этом разделе для вывода информации используются два элемента управления ListView. первый элемент управления ListView (IDC \_ плвиев) отображает все списки воспроизведения в библиотеке проигрыватель Windows Media, при этом первыми появляются списки воспроизведения синхронизации. Списки воспроизведения синхронизации для текущего выбранного устройства отмечены галочкой и сортируются в порядке приоритета синхронизации. Все остальные списки воспроизведения не отмечены флажками. Элемент управления ListView настроен для выбора только одного элемента. Порядок списков воспроизведения в элементе управления ListView определяет приоритет синхронизации. Состояние проверки отдельного списка воспроизведения определяет, является ли он списком синхронизации для текущего выбранного устройства.

Второй элемент управления ListView (IDC \_ медиавиев) отображает элементы мультимедиа в выбранном списке воспроизведения. В двух дополнительных столбцах отображается текст, указывающий, был ли скопирован файл мультимедиа на устройство, и, в случае сбоя, неудачную попытку копирования из-за того, что файл цифрового мультимедиа не поместится.

В следующем примере кода показано, как инициализируются элементы управления ListView:


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



Следующий массив строк содержит имена атрибутов синхронизации, используемых в примерах:


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



следующая переменная-член содержит список воспроизведения, содержащий все списки воспроизведения в библиотеке проигрыватель Windows Media. Каждый список воспроизведения представлен в виде элемента мультимедиа.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



В следующих разделах приводится пример кода:

-   [Перечисление списков воспроизведения синхронизации](enumerating-synchronization-playlists.md)
-   [Сортировка списков воспроизведения по приоритету синхронизации](sorting-playlists-by-synchronization-priority.md)
-   [Перечисление элементов мультимедиа](enumerating-the-media-items.md)
-   [Определение состояния синхронизации списка воспроизведения](determining-playlist-synchronization-state.md)
-   [Изменение приоритета синхронизации](changing-synchronization-priority.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Работа с портативными устройствами**](working-with-portable-devices.md)
</dt> </dl>

 

 




