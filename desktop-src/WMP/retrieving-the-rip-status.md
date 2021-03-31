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
# <a name="retrieving-the-rip-status"></a><span data-ttu-id="36a3d-112">Получение состояния копирования</span><span class="sxs-lookup"><span data-stu-id="36a3d-112">Retrieving the Rip Status</span></span>

<span data-ttu-id="36a3d-113">Ход выполнения операции копирования можно отслеживать, периодически вызывая [ивмпкдромрип:: Get \_ риппрогресс](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span><span class="sxs-lookup"><span data-stu-id="36a3d-113">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="36a3d-114">Этот метод получает значение хода выполнения для всей операции копирования.</span><span class="sxs-lookup"><span data-stu-id="36a3d-114">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="36a3d-115">Полученное значение является числом, представляющим процент завершения копирования с 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="36a3d-115">The value retrieved is a number that represents the percentage of ripping completed, from 0 to 100.</span></span>

<span data-ttu-id="36a3d-116">Значение Progress представляет завершенный процент всего процесса копирования.</span><span class="sxs-lookup"><span data-stu-id="36a3d-116">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="36a3d-117">Чтобы определить ход выполнения определенной записи, используйте в качестве имени атрибута [ивмпмедиа:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) с именем "риппрогресс".</span><span class="sxs-lookup"><span data-stu-id="36a3d-117">To determine the progress of a specific track, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) with "RipProgress" as the attribute name.</span></span> <span data-ttu-id="36a3d-118">Чтобы определить индекс дорожки, скопированной в данный момент, вызовите **ивмпплайлист:: getItemInfo** с "куррентриптраккиндекс" в качестве имени атрибута.</span><span class="sxs-lookup"><span data-stu-id="36a3d-118">To determine the index of the track currently being ripped, call **IWMPPlaylist::getItemInfo** with "CurrentRipTrackIndex" as the attribute name.</span></span>

<span data-ttu-id="36a3d-119">Состояние операции копирования можно отслеживать, периодически вызывая [ивмпкдромрип:: Get \_ рипстате](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span><span class="sxs-lookup"><span data-stu-id="36a3d-119">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="36a3d-120">Этот метод получает значение перечисления [вмприпстате](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) , указывающее, выполняется ли операция или она остановлена.</span><span class="sxs-lookup"><span data-stu-id="36a3d-120">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="36a3d-121">Можно также отслеживать состояние операции копирования, обрабатывая событие [IWMPEvents3:: кдромрипстатечанже](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) .</span><span class="sxs-lookup"><span data-stu-id="36a3d-121">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="36a3d-122">(См. раздел [Обработка событий в C++](handling-events-in-c.md).) Будьте внимательны при сравнении указателя **ивмпкдромрип** (предоставленного событием) с указателем, который представляет операцию копирования, чтобы убедиться, что событие было вызвано операцией.</span><span class="sxs-lookup"><span data-stu-id="36a3d-122">(See [Handling Events in C++](handling-events-in-c.md).) Be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation, to ensure that the event was raised by your operation.</span></span>

<span data-ttu-id="36a3d-123">В следующем примере кода показано, как использовать эти функции для получения состояния операции копирования.</span><span class="sxs-lookup"><span data-stu-id="36a3d-123">The following example code shows how to use these functions to retrieve the status of a ripping operation.</span></span>

<span data-ttu-id="36a3d-124">Для примера кода определены следующие элементы управления диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="36a3d-124">The following dialog controls are defined for the code example.</span></span>



| <span data-ttu-id="36a3d-125">Идентификатор элемента управления</span><span class="sxs-lookup"><span data-stu-id="36a3d-125">Control ID</span></span>                   | <span data-ttu-id="36a3d-126">Описание</span><span class="sxs-lookup"><span data-stu-id="36a3d-126">Description</span></span>                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a3d-127">\_Текущая \_ запись IDC</span><span class="sxs-lookup"><span data-stu-id="36a3d-127">IDC\_CURRENT\_TRACK</span></span>          | <span data-ttu-id="36a3d-128">Статический текст, представляющий индекс дорожки, которую в данный момент копируются.</span><span class="sxs-lookup"><span data-stu-id="36a3d-128">Static text that represents the index of the track currently being ripped.</span></span>                                         |
| <span data-ttu-id="36a3d-129">\_ \_ текст хода выполнения отслеживания IDC \_</span><span class="sxs-lookup"><span data-stu-id="36a3d-129">IDC\_TRACK\_PROGRESS\_TEXT</span></span>   | <span data-ttu-id="36a3d-130">Статический текст, представляющий ход выполнения дорожки, скопированной в данный момент в процентах.</span><span class="sxs-lookup"><span data-stu-id="36a3d-130">Static text that represents the progress of the track currently being ripped as a percentage.</span></span>                      |
| <span data-ttu-id="36a3d-131">\_Трассировка хода выполнения IDC \_</span><span class="sxs-lookup"><span data-stu-id="36a3d-131">IDC\_PROGRESS\_TRACK</span></span>         | <span data-ttu-id="36a3d-132">Индикатор выполнения с диапазоном от 0 до 100, который представляет ход выполнения дорожки, скопированной в данный момент в процентах.</span><span class="sxs-lookup"><span data-stu-id="36a3d-132">Progress bar with range 0 to 100 that represents the progress of the track currently being ripped as a percentage.</span></span> |
| <span data-ttu-id="36a3d-133">\_Общий \_ текст хода выполнения \_ IDC</span><span class="sxs-lookup"><span data-stu-id="36a3d-133">IDC\_OVERALL\_PROGRESS\_TEXT</span></span> | <span data-ttu-id="36a3d-134">Статический текст, представляющий ход выполнения общего процесса копирования в процентах.</span><span class="sxs-lookup"><span data-stu-id="36a3d-134">Static text that represents the progress of the total ripping process as a percentage.</span></span>                             |
| <span data-ttu-id="36a3d-135">\_Общие сведения о ходе выполнения IDC \_</span><span class="sxs-lookup"><span data-stu-id="36a3d-135">IDC\_PROGRESS\_OVERALL</span></span>       | <span data-ttu-id="36a3d-136">Индикатор выполнения с диапазоном от 0 до 100, который представляет ход выполнения всего процесса копирования в процентах.</span><span class="sxs-lookup"><span data-stu-id="36a3d-136">Progress bar with range 0 to 100 that represents the progress of the total ripping process as a percentage.</span></span>        |
| <span data-ttu-id="36a3d-137">\_состояние IDC RIP \_</span><span class="sxs-lookup"><span data-stu-id="36a3d-137">IDC\_RIP\_STATE</span></span>              | <span data-ttu-id="36a3d-138">Статический текст, отображающий выполняемую в данный момент операцию ("копирование", "остановлено" или "неизвестно")</span><span class="sxs-lookup"><span data-stu-id="36a3d-138">Static text that displays the operation currently being performed ("Ripping", "Stopped", or "Unknown")</span></span>             |



 


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



## <a name="related-topics"></a><span data-ttu-id="36a3d-139">См. также</span><span class="sxs-lookup"><span data-stu-id="36a3d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a3d-140">**Копирование компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="36a3d-140">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="36a3d-141">**Получение интерфейса копирования данных с компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="36a3d-141">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="36a3d-142">**Запуск процесса копирования**</span><span class="sxs-lookup"><span data-stu-id="36a3d-142">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="36a3d-143">**Выбор элементов для копирования**</span><span class="sxs-lookup"><span data-stu-id="36a3d-143">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




