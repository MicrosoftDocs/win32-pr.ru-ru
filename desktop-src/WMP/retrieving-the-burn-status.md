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
# <a name="retrieving-the-burn-status"></a><span data-ttu-id="990a7-112">Получение состояния записи</span><span class="sxs-lookup"><span data-stu-id="990a7-112">Retrieving the Burn Status</span></span>

<span data-ttu-id="990a7-113">В приведенном ниже примере кода определены следующие элементы управления диалогового окна:</span><span class="sxs-lookup"><span data-stu-id="990a7-113">In the code example that follows, the following dialog controls are defined:</span></span>



| <span data-ttu-id="990a7-114">Идентификатор элемента управления</span><span class="sxs-lookup"><span data-stu-id="990a7-114">Control ID</span></span>           | <span data-ttu-id="990a7-115">Описание</span><span class="sxs-lookup"><span data-stu-id="990a7-115">Description</span></span>                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="990a7-116">\_состояние записи \_ IDC</span><span class="sxs-lookup"><span data-stu-id="990a7-116">IDC\_BURN\_STATE</span></span>     | <span data-ttu-id="990a7-117">Статический текст, представляющий состояние операции записи компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="990a7-117">Static text that represents the state of the CD burning operation.</span></span>             |
| <span data-ttu-id="990a7-118">\_ход выполнения IDC</span><span class="sxs-lookup"><span data-stu-id="990a7-118">IDC\_PROGRESS</span></span>        | <span data-ttu-id="990a7-119">Индикатор выполнения с диапазоном от 0 до 100, который представляет общий ход выполнения записи.</span><span class="sxs-lookup"><span data-stu-id="990a7-119">Progress bar with a range of 0 to 100 that represents the total burn progress.</span></span> |
| <span data-ttu-id="990a7-120">\_текст хода выполнения IDC \_</span><span class="sxs-lookup"><span data-stu-id="990a7-120">IDC\_PROGRESS\_TEXT</span></span>  | <span data-ttu-id="990a7-121">Статический текст, представляющий общий ход выполнения записи в виде числа от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="990a7-121">Static text that represents the total burn progress as a number from 0 to 100.</span></span> |
| <span data-ttu-id="990a7-122">\_доступное \_ время IDC</span><span class="sxs-lookup"><span data-stu-id="990a7-122">IDC\_AVAILABLE\_TIME</span></span> | <span data-ttu-id="990a7-123">Статический текст для вывода времени, доступного на компакт-диске, в секундах.</span><span class="sxs-lookup"><span data-stu-id="990a7-123">Static text to display the time available on the CD, in seconds.</span></span>               |
| <span data-ttu-id="990a7-124">\_свободное \_ место в IDC</span><span class="sxs-lookup"><span data-stu-id="990a7-124">IDC\_FREE\_SPACE</span></span>     | <span data-ttu-id="990a7-125">Статический текст для вывода свободного места на компакт-диске в байтах.</span><span class="sxs-lookup"><span data-stu-id="990a7-125">Static text to display the free space on the CD, in bytes.</span></span>                     |
| <span data-ttu-id="990a7-126">\_Общее \_ пространство IDC</span><span class="sxs-lookup"><span data-stu-id="990a7-126">IDC\_TOTAL\_SPACE</span></span>    | <span data-ttu-id="990a7-127">Статический текст для вывода общей емкости компакт-диска в байтах.</span><span class="sxs-lookup"><span data-stu-id="990a7-127">Static text to display the total capacity of the CD, in bytes.</span></span>                 |



 

<span data-ttu-id="990a7-128">Ход выполнения операции записи можно отслеживать, периодически вызывая [ивмпкдромбурн:: Get \_ бурнпрогресс](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) , пока выполняется запись компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="990a7-128">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) while the CD is being burned.</span></span> <span data-ttu-id="990a7-129">Этот метод получает значение хода выполнения для всей операции записи.</span><span class="sxs-lookup"><span data-stu-id="990a7-129">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="990a7-130">Полученное значение является числом, представляющим процент выполненной записи от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="990a7-130">The value retrieved is a number that represents the percentage of burning completed, from 0 to 100.</span></span>


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



<span data-ttu-id="990a7-131">Текущее состояние операции записи можно получить, вызвав [ивмпкдромбурн:: Get \_ бурнстате](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span><span class="sxs-lookup"><span data-stu-id="990a7-131">You can get the current state of the burning operation by calling [IWMPCdromBurn::get\_burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span></span> <span data-ttu-id="990a7-132">Этот метод получает перечисление, указывающее текущую выполняемую операцию.</span><span class="sxs-lookup"><span data-stu-id="990a7-132">This method retrieves an enumeration specifying the current operation being performed.</span></span>


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



<span data-ttu-id="990a7-133">Чтобы получить количество секунд, которое может храниться на компакт-диске, вызовите [ивмпкдромбурн:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) с "аваилаблетиме" в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="990a7-133">To retrieve the number of seconds of audio the CD can hold, call [IWMPCdromBurn::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) with "AvailableTime" as the first parameter.</span></span> <span data-ttu-id="990a7-134">Значение, полученное этой функцией, представлено строкой.</span><span class="sxs-lookup"><span data-stu-id="990a7-134">The value retrieved by this function is represented by a string.</span></span>


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



<span data-ttu-id="990a7-135">Чтобы получить объем свободного места на диске, вызовите **ивмпкдромбурн:: getItemInfo** с "Freespace" в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="990a7-135">To retrieve the amount of free space on a disc, call **IWMPCdromBurn::getItemInfo** with "FreeSpace" as the first parameter.</span></span> <span data-ttu-id="990a7-136">Значение, полученное этой функцией, является строкой, представляющей количество свободных байтов, доступных на диске.</span><span class="sxs-lookup"><span data-stu-id="990a7-136">The value retrieved by this function is a string that represents the number of free bytes available on the disc.</span></span>


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



<span data-ttu-id="990a7-137">Чтобы получить общую емкость диска, вызовите **ивмпкдромбурн:: getItemInfo** с "тоталспаце" в качестве первого параметра.</span><span class="sxs-lookup"><span data-stu-id="990a7-137">To retrieve the total capacity of a disc, call **IWMPCdromBurn::getItemInfo** with "TotalSpace" as the first parameter.</span></span> <span data-ttu-id="990a7-138">Значение, полученное этой функцией, представляет собой строку, соответствующую общему количеству байтов на диске.</span><span class="sxs-lookup"><span data-stu-id="990a7-138">The value retrieved by this function is a string that corresponds to the total number of bytes on the disc.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="990a7-139">См. также</span><span class="sxs-lookup"><span data-stu-id="990a7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="990a7-140">**Запись компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="990a7-140">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="990a7-141">**Получение интерфейса записи компакт-дисков**</span><span class="sxs-lookup"><span data-stu-id="990a7-141">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="990a7-142">**Запуск процесса записи**</span><span class="sxs-lookup"><span data-stu-id="990a7-142">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="990a7-143">**Стирание перезаписываемого компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="990a7-143">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="990a7-144">**Получение состояния диска и диска**</span><span class="sxs-lookup"><span data-stu-id="990a7-144">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




