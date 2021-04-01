---
title: Выбор элементов для копирования
description: Выбор элементов для копирования
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование компакт-дисков, выбор элементов
- Копирование компакт-дисков, выбор элементов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986609"
---
# <a name="selecting-items-for-ripping"></a>Выбор элементов для копирования

Иногда пользователю не нужно копировать каждую дорожку на компакт-диске. Проигрыватель Windows Media предоставляет интерфейс для указания дорожек, выбранных для копирования. Как правило, в приложении для копирования компакт-дисков существует пользовательский интерфейс, позволяющий пользователю выбирать флажки в списке дорожек на компакт-диске.

Некоторые дорожки не могут быть выбраны для копирования по умолчанию. Если дорожка уже находится в библиотеке проигрывателя Windows Media, она не будет автоматически выбрана для копирования. Во втором примере кода в этом разделе показано, как обойти значение по умолчанию и вручную выбрать дорожку для копирования, если она уже скопирована.

В следующем примере кода показано, как определить, выбрана ли дорожка для копирования.


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



В следующем примере кода показано, как указать, выбрана ли дорожка для копирования.


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
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

[**Получение состояния копирования**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




