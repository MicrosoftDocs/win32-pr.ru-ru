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
# <a name="selecting-items-for-ripping"></a><span data-ttu-id="203a9-112">Выбор элементов для копирования</span><span class="sxs-lookup"><span data-stu-id="203a9-112">Selecting Items for Ripping</span></span>

<span data-ttu-id="203a9-113">Иногда пользователю не нужно копировать каждую дорожку на компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="203a9-113">Sometimes a user does not want to rip every track on a CD.</span></span> <span data-ttu-id="203a9-114">Проигрыватель Windows Media предоставляет интерфейс для указания дорожек, выбранных для копирования.</span><span class="sxs-lookup"><span data-stu-id="203a9-114">Windows Media Player provides an interface for specifying which tracks are selected for ripping.</span></span> <span data-ttu-id="203a9-115">Как правило, в приложении для копирования компакт-дисков существует пользовательский интерфейс, позволяющий пользователю выбирать флажки в списке дорожек на компакт-диске.</span><span class="sxs-lookup"><span data-stu-id="203a9-115">Typically in a CD ripping application there is a user interface that lets the user select check boxes in a list of tracks on the CD.</span></span>

<span data-ttu-id="203a9-116">Некоторые дорожки не могут быть выбраны для копирования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="203a9-116">Some tracks might not be selected for ripping by default.</span></span> <span data-ttu-id="203a9-117">Если дорожка уже находится в библиотеке проигрывателя Windows Media, она не будет автоматически выбрана для копирования.</span><span class="sxs-lookup"><span data-stu-id="203a9-117">If a track is already in the Windows Media Player library, it will not be automatically selected for ripping.</span></span> <span data-ttu-id="203a9-118">Во втором примере кода в этом разделе показано, как обойти значение по умолчанию и вручную выбрать дорожку для копирования, если она уже скопирована.</span><span class="sxs-lookup"><span data-stu-id="203a9-118">The second code example in this section demonstrates how to bypass the default value and manually select a track for ripping if it has already been ripped.</span></span>

<span data-ttu-id="203a9-119">В следующем примере кода показано, как определить, выбрана ли дорожка для копирования.</span><span class="sxs-lookup"><span data-stu-id="203a9-119">The following code example demonstrates how to determine whether a track is selected for ripping:</span></span>


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



<span data-ttu-id="203a9-120">В следующем примере кода показано, как указать, выбрана ли дорожка для копирования.</span><span class="sxs-lookup"><span data-stu-id="203a9-120">The following code example demonstrates how to specify whether a track is selected for ripping.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="203a9-121">См. также</span><span class="sxs-lookup"><span data-stu-id="203a9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="203a9-122">**Копирование компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="203a9-122">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="203a9-123">**Получение интерфейса копирования данных с компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="203a9-123">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="203a9-124">**Запуск процесса копирования**</span><span class="sxs-lookup"><span data-stu-id="203a9-124">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="203a9-125">**Получение состояния копирования**</span><span class="sxs-lookup"><span data-stu-id="203a9-125">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> </dl>

 

 




