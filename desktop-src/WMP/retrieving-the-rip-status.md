---
title: Получение состояния копирования
description: Получение состояния копирования
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование с компакт-диска, получение состояния RIP
- Копирование компакт-дисков, получение состояния RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069608"
---
# <a name="retrieving-the-rip-status"></a>Получение состояния копирования

Ход выполнения операции копирования можно отслеживать, периодически вызывая [ивмпкдромрип:: Get \_ риппрогресс](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Этот метод получает значение хода выполнения для всей операции копирования. Полученное значение является числом, представляющим процент завершения копирования с 0 до 100.

Значение Progress представляет завершенный процент всего процесса копирования. Чтобы определить ход выполнения определенной записи, используйте в качестве имени атрибута [ивмпмедиа:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) с именем "риппрогресс". Чтобы определить индекс дорожки, скопированной в данный момент, вызовите **ивмпплайлист:: getItemInfo** с "куррентриптраккиндекс" в качестве имени атрибута.

Состояние операции копирования можно отслеживать, периодически вызывая [ивмпкдромрип:: Get \_ рипстате](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Этот метод получает значение перечисления [вмприпстате](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) , указывающее, выполняется ли операция или она остановлена. Можно также отслеживать состояние операции копирования, обрабатывая событие [IWMPEvents3:: кдромрипстатечанже](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . (См. раздел [Обработка событий в C++](handling-events-in-c.md).) Будьте внимательны при сравнении указателя **ивмпкдромрип** (предоставленного событием) с указателем, который представляет операцию копирования, чтобы убедиться, что событие было вызвано операцией.

В следующем примере кода показано, как использовать эти функции для получения состояния операции копирования.

Для примера кода определены следующие элементы управления диалогового окна.



| Идентификатор элемента управления                   | Описание                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| \_Текущая \_ запись IDC          | Статический текст, представляющий индекс дорожки, которую в данный момент копируются.                                         |
| \_ \_ текст хода выполнения отслеживания IDC \_   | Статический текст, представляющий ход выполнения дорожки, скопированной в данный момент в процентах.                      |
| \_Трассировка хода выполнения IDC \_         | Индикатор выполнения с диапазоном от 0 до 100, который представляет ход выполнения дорожки, скопированной в данный момент в процентах. |
| \_Общий \_ текст хода выполнения \_ IDC | Статический текст, представляющий ход выполнения общего процесса копирования в процентах.                             |
| \_Общие сведения о ходе выполнения IDC \_       | Индикатор выполнения с диапазоном от 0 до 100, который представляет ход выполнения всего процесса копирования в процентах.        |
| \_состояние IDC RIP \_              | Статический текст, отображающий выполняемую в данный момент операцию ("копирование", "остановлено" или "неизвестно")             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Копирование компакт-диска**](ripping-a-cd.md)
</dt> <dt>

[**Получение интерфейса копирования данных с компакт-диска**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Запуск процесса копирования**](starting-the-rip-process.md)
</dt> <dt>

[**Выбор элементов для копирования**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




