---
title: Получение состояния записи
description: Получение состояния записи
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-диска, получение состояния записи
- запись компакт-дисков, получение состояния записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987211"
---
# <a name="retrieving-the-burn-status"></a>Получение состояния записи

В приведенном ниже примере кода определены следующие элементы управления диалогового окна:



| Идентификатор элемента управления           | Описание                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| \_состояние записи \_ IDC     | Статический текст, представляющий состояние операции записи компакт-дисков.             |
| \_ход выполнения IDC        | Индикатор выполнения с диапазоном от 0 до 100, который представляет общий ход выполнения записи. |
| \_текст хода выполнения IDC \_  | Статический текст, представляющий общий ход выполнения записи в виде числа от 0 до 100. |
| \_доступное \_ время IDC | Статический текст для вывода времени, доступного на компакт-диске, в секундах.               |
| \_свободное \_ место в IDC     | Статический текст для вывода свободного места на компакт-диске в байтах.                     |
| \_Общее \_ пространство IDC    | Статический текст для вывода общей емкости компакт-диска в байтах.                 |



 

Ход выполнения операции записи можно отслеживать, периодически вызывая [ивмпкдромбурн:: Get \_ бурнпрогресс](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) , пока выполняется запись компакт-диска. Этот метод получает значение хода выполнения для всей операции записи. Полученное значение является числом, представляющим процент выполненной записи от 0 до 100.


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



Текущее состояние операции записи можно получить, вызвав [ивмпкдромбурн:: Get \_ бурнстате](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate). Этот метод получает перечисление, указывающее текущую выполняемую операцию.


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



Чтобы получить количество секунд, которое может храниться на компакт-диске, вызовите [ивмпкдромбурн:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) с "аваилаблетиме" в качестве первого параметра. Значение, полученное этой функцией, представлено строкой.


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



Чтобы получить объем свободного места на диске, вызовите **ивмпкдромбурн:: getItemInfo** с "Freespace" в качестве первого параметра. Значение, полученное этой функцией, является строкой, представляющей количество свободных байтов, доступных на диске.


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



Чтобы получить общую емкость диска, вызовите **ивмпкдромбурн:: getItemInfo** с "тоталспаце" в качестве первого параметра. Значение, полученное этой функцией, представляет собой строку, соответствующую общему количеству байтов на диске.


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Запись компакт-диска**](burning-a-cd.md)
</dt> <dt>

[**Получение интерфейса записи компакт-дисков**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Запуск процесса записи**](starting-the-burn-process.md)
</dt> <dt>

[**Стирание перезаписываемого компакт-диска**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Получение состояния диска и диска**](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




