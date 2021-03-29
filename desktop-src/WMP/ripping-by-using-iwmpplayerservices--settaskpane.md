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
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a><span data-ttu-id="ec896-113">Копирование с помощью Ивмпплайерсервицес:: Сеттаскпане</span><span class="sxs-lookup"><span data-stu-id="ec896-113">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="ec896-114">В этом разделе документируется функция элементов управления ActiveX проигрывателя Windows Media 9 и Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="ec896-114">This section documents a feature of the Windows Media Player 9 Series and Windows Media Player 10 ActiveX controls.</span></span> <span data-ttu-id="ec896-115">Рекомендуется использовать интерфейс **ивмпкдромрип** с более поздними версиями.</span><span class="sxs-lookup"><span data-stu-id="ec896-115">It is recommended that you use the **IWMPCdromRip** interface with later versions.</span></span> <span data-ttu-id="ec896-116">См. раздел [интерфейс ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span><span class="sxs-lookup"><span data-stu-id="ec896-116">See [IWMPCdromRip Interface](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span></span>

 

<span data-ttu-id="ec896-117">Для копирования дорожек с компакт-диска на компьютер пользователя можно использовать проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ec896-117">You can use the Windows Media Player 9 Series or later control to copy CD tracks to the user's computer.</span></span> <span data-ttu-id="ec896-118">Этот процесс называется *копированием*.</span><span class="sxs-lookup"><span data-stu-id="ec896-118">This process is called *ripping*.</span></span> <span data-ttu-id="ec896-119">Для этого необходимо внедрить элемент управления проигрывателя Windows Media в удаленный режим.</span><span class="sxs-lookup"><span data-stu-id="ec896-119">To do this, you must embed the Windows Media Player control in remote mode.</span></span> <span data-ttu-id="ec896-120">Дополнительные сведения об удаленном режиме см. [в разделе Удаленное взаимодействие с элементом управления проигрывателя Windows Media](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="ec896-120">For more information about remote mode, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

<span data-ttu-id="ec896-121">Чтобы начать процесс копирования, вызовите [ивмпплайерсервицес:: сеттаскпане](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), передав копифромкд? Автокопирование: значение *идентификатора* для параметра *бстртаскпане* , где *ID* — это индекс компакт-диска, с которого производится копирование.</span><span class="sxs-lookup"><span data-stu-id="ec896-121">To start the ripping process, call [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passing the CopyFromCD?AutoCopy:*id* value for the *bstrTaskPane* parameter, where *id* is the index of the CD drive from which to copy.</span></span> <span data-ttu-id="ec896-122">Этот индекс соответствует индексу объекта **CDROM** в интерфейсе **ивмпкдромколлектион** или событии **кдроммедиачанже** .</span><span class="sxs-lookup"><span data-stu-id="ec896-122">This index corresponds to the index of a **Cdrom** object in the **IWMPCdromCollection** interface or the **CdromMediaChange** event.</span></span>

<span data-ttu-id="ec896-123">Следующий пример кода — это функция, которая запускает процесс копирования компакт-диска с компакт-диска, идентифицируемого нулевым индексом.</span><span class="sxs-lookup"><span data-stu-id="ec896-123">The following example code is a function that starts the process of ripping a CD from the CD drive identified by index zero.</span></span> <span data-ttu-id="ec896-124">Функция использует следующую переменную члена:</span><span class="sxs-lookup"><span data-stu-id="ec896-124">The function uses the following member variable:</span></span>


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



<span data-ttu-id="ec896-125">В следующем коде показан текст функции:</span><span class="sxs-lookup"><span data-stu-id="ec896-125">The following code shows the body of the function:</span></span>


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



<span data-ttu-id="ec896-126">Отображение состояния для пользователя</span><span class="sxs-lookup"><span data-stu-id="ec896-126">Displaying Status to the User</span></span>

<span data-ttu-id="ec896-127">При копировании с компакт-диска можно получить строку, содержащую сведения о состоянии операции копирования.</span><span class="sxs-lookup"><span data-stu-id="ec896-127">When copying from a CD, you can retrieve a string containing status information about the copy operation.</span></span> <span data-ttu-id="ec896-128">Для этого необходимо сначала получить список воспроизведения, содержащий элементы мультимедиа, представляющие дорожки компакт-диска, вызвав [ивмпкдром: \_ : Get](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist)Remedia.</span><span class="sxs-lookup"><span data-stu-id="ec896-128">To do this, you must first retrieve a playlist containing media items that represent the CD tracks by calling [IWMPCdrom::get\_playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span></span> <span data-ttu-id="ec896-129">Как и в предыдущем примере, приведенный ниже пример кода работает с нулевым индексом компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="ec896-129">Like the previous example, the following example code works with CD drive index zero.</span></span> <span data-ttu-id="ec896-130">Полученный список воспроизведения сохраняется в следующей переменной члена:</span><span class="sxs-lookup"><span data-stu-id="ec896-130">It stores the retrieved playlist in the following member variable:</span></span>


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



<span data-ttu-id="ec896-131">В следующем коде показан текст функции:</span><span class="sxs-lookup"><span data-stu-id="ec896-131">The following code shows the body of the function:</span></span>


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



<span data-ttu-id="ec896-132">Затем обработайте событие [ивмпевентс:: медиачанже](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) .</span><span class="sxs-lookup"><span data-stu-id="ec896-132">Next, handle the [IWMPEvents::MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) event.</span></span> <span data-ttu-id="ec896-133">Это событие возникает при копировании дорожки компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="ec896-133">This event occurs when a CD track is being ripped.</span></span> <span data-ttu-id="ec896-134">Указатель **IDispatch** , передаваемый обработчику событий, указывает на интерфейс **ивмпмедиа** для записи компакт-диска. Вызовите метод **QueryInterface** через **IDispatch** , чтобы получить указатель на **ивмпмедиа**.</span><span class="sxs-lookup"><span data-stu-id="ec896-134">The **IDispatch** pointer passed to the event handler points to the **IWMPMedia** interface for the CD track. Call **QueryInterface** through **IDispatch** to retrieve the pointer to **IWMPMedia**.</span></span>

<span data-ttu-id="ec896-135">Чтобы определить, какая дорожка компакт-диска скопирована, Сравните указатель **ивмпмедиа** из события с элементами мультимедиа в списке воспроизведения компакт-дисков, вызвав [ивмпмедиа:: Get \_ одинаковы](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span><span class="sxs-lookup"><span data-stu-id="ec896-135">To detect which CD track is being ripped, compare the **IWMPMedia** pointer from the event to the media items in the CD playlist by calling [IWMPMedia::get\_isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span></span>

<span data-ttu-id="ec896-136">Вызовите [ивмпмедиа:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), передав в качестве имени элемента строку "Status".</span><span class="sxs-lookup"><span data-stu-id="ec896-136">Call [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passing the string "Status" as the item name.</span></span> <span data-ttu-id="ec896-137">**Состояние** — это временный атрибут, заданный проигрывателем Windows Media в элементах мультимедиа, когда они копируются с компакт-диска. она недоступна из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="ec896-137">**Status** is a temporary attribute set by Windows Media Player on media items while they are being ripped from CD; it is not available from the library.</span></span>

<span data-ttu-id="ec896-138">В следующем примере кода показан обработчик событий **медиачанже** .</span><span class="sxs-lookup"><span data-stu-id="ec896-138">The following example code shows a **MediaChange** event handler.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ec896-139">См. также</span><span class="sxs-lookup"><span data-stu-id="ec896-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec896-140">**Интерфейс Ивмпкдром**</span><span class="sxs-lookup"><span data-stu-id="ec896-140">**IWMPCdrom Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[<span data-ttu-id="ec896-141">**Интерфейс Ивмпкдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="ec896-141">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[<span data-ttu-id="ec896-142">**Интерфейс Ивмпевентс**</span><span class="sxs-lookup"><span data-stu-id="ec896-142">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[<span data-ttu-id="ec896-143">**Интерфейс Ивмпмедиа**</span><span class="sxs-lookup"><span data-stu-id="ec896-143">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="ec896-144">**Интерфейс Ивмпплайерсервицес**</span><span class="sxs-lookup"><span data-stu-id="ec896-144">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[<span data-ttu-id="ec896-145">**Интерфейс Ивмпплайлист**</span><span class="sxs-lookup"><span data-stu-id="ec896-145">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="ec896-146">**Управление проигрывателем**</span><span class="sxs-lookup"><span data-stu-id="ec896-146">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> <dt>

[<span data-ttu-id="ec896-147">**Копирование с помощью интерфейса Ивмпкдромрип**</span><span class="sxs-lookup"><span data-stu-id="ec896-147">**Ripping by Using the IWMPCdromRip Interface**</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




