---
title: Копирование данных с компакт-диска с помощью setTaskPane в IWMPPlayerServices
description: Копирование данных с компакт-диска с помощью setTaskPane в IWMPPlayerServices
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование компакт-дисков, интерфейс Ивмпплайерсервицес Сеттаскпане
- Копирование компакт-дисков, интерфейс Ивмпплайерсервицес Сеттаскпане
- Интерфейс Ивмпплайерсервицес Сеттаскпане
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104487353"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Копирование с помощью Ивмпплайерсервицес:: Сеттаскпане

> [!Note]  
> В этом разделе документируется функция элементов управления ActiveX проигрывателя Windows Media 9 и Windows Media Player 10. Рекомендуется использовать интерфейс **ивмпкдромрип** с более поздними версиями. См. раздел [интерфейс ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).

 

Для копирования дорожек с компакт-диска на компьютер пользователя можно использовать проигрыватель Windows Media 9 Series или более поздней версии. Этот процесс называется *копированием*. Для этого необходимо внедрить элемент управления проигрывателя Windows Media в удаленный режим. Дополнительные сведения об удаленном режиме см. [в разделе Удаленное взаимодействие с элементом управления проигрывателя Windows Media](remoting-the-windows-media-player-control.md).

Чтобы начать процесс копирования, вызовите [ивмпплайерсервицес:: сеттаскпане](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), передав копифромкд? Автокопирование: значение *идентификатора* для параметра *бстртаскпане* , где *ID* — это индекс компакт-диска, с которого производится копирование. Этот индекс соответствует индексу объекта **CDROM** в интерфейсе **ивмпкдромколлектион** или событии **кдроммедиачанже** .

Следующий пример кода — это функция, которая запускает процесс копирования компакт-диска с компакт-диска, идентифицируемого нулевым индексом. Функция использует следующую переменную члена:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



В следующем коде показан текст функции:


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



Отображение состояния для пользователя

При копировании с компакт-диска можно получить строку, содержащую сведения о состоянии операции копирования. Для этого необходимо сначала получить список воспроизведения, содержащий элементы мультимедиа, представляющие дорожки компакт-диска, вызвав [ивмпкдром: \_ : Get](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist)Remedia. Как и в предыдущем примере, приведенный ниже пример кода работает с нулевым индексом компакт-диска. Полученный список воспроизведения сохраняется в следующей переменной члена:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



В следующем коде показан текст функции:


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



Затем обработайте событие [ивмпевентс:: медиачанже](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) . Это событие возникает при копировании дорожки компакт-диска. Указатель **IDispatch** , передаваемый обработчику событий, указывает на интерфейс **ивмпмедиа** для записи компакт-диска. Вызовите метод **QueryInterface** через **IDispatch** , чтобы получить указатель на **ивмпмедиа**.

Чтобы определить, какая дорожка компакт-диска скопирована, Сравните указатель **ивмпмедиа** из события с элементами мультимедиа в списке воспроизведения компакт-дисков, вызвав [ивмпмедиа:: Get \_ одинаковы](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).

Вызовите [ивмпмедиа:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), передав в качестве имени элемента строку "Status". **Состояние** — это временный атрибут, заданный проигрывателем Windows Media в элементах мультимедиа, когда они копируются с компакт-диска. она недоступна из библиотеки.

В следующем примере кода показан обработчик событий **медиачанже** .


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпкдром**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Интерфейс Ивмпкдромколлектион**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Интерфейс Ивмпевентс**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**Интерфейс Ивмпмедиа**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Интерфейс Ивмпплайерсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**Интерфейс Ивмпплайлист**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Управление проигрывателем**](player-control-guide.md)
</dt> <dt>

[**Копирование с помощью интерфейса Ивмпкдромрип**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




