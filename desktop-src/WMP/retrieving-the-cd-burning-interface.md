---
title: Получение интерфейса записи компакт-дисков
description: Получение интерфейса записи компакт-дисков
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Проигрыватель Windows Media, запись компакт-дисков
- Объектная модель проигрывателя Windows Media, запись компакт-дисков
- Объектная модель, запись компакт-диска
- Элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Элемент управления ActiveX, запись компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, запись компакт-дисков
- Проигрыватель Windows Media Mobile, запись компакт-дисков
- Запись компакт-дисков, получение интерфейса Ивмпкдромколлектион
- запись компакт-дисков, получение интерфейса Ивмпкдромколлектион
- Интерфейс Ивмпкдромколлектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069685"
---
# <a name="retrieving-the-cd-burning-interface"></a><span data-ttu-id="577df-113">Получение интерфейса записи компакт-дисков</span><span class="sxs-lookup"><span data-stu-id="577df-113">Retrieving the CD Burning Interface</span></span>

<span data-ttu-id="577df-114">Чтобы перечислить дисководы компакт-дисков на компьютере пользователя, используйте интерфейс **ивмпкдромколлектион** .</span><span class="sxs-lookup"><span data-stu-id="577df-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="577df-115">Чтобы получить указатель на этот интерфейс, вызовите [ивмпкоре:: Get \_ кдромколлектион](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="577df-115">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="577df-116">С помощью методов **Get \_ Count** и **Item** можно выполнить итерацию коллекции, чтобы получить указатель интерфейса [ивмпкдром](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) для каждого компакт-дисковода на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="577df-116">By using the **get\_count** and **item** methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface pointer for each CD drive on the user's computer.</span></span>

<span data-ttu-id="577df-117">Интерфейс **ивмпкдром** представляет отдельный компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="577df-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="577df-118">Перед началом записи компакт-диска необходимо сначала вызвать **QueryInterface** через указатель **ивмпкдром** , чтобы получить указатель на интерфейс [ивмпкдромбурн](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .</span><span class="sxs-lookup"><span data-stu-id="577df-118">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface.</span></span>

<span data-ttu-id="577df-119">В следующем примере кода показано, как получить интерфейс для записи компакт-диска на конкретный диск:</span><span class="sxs-lookup"><span data-stu-id="577df-119">The following code example demonstrates how to retrieve an interface for burning a CD to a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="577df-120">См. также</span><span class="sxs-lookup"><span data-stu-id="577df-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="577df-121">**Запись компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="577df-121">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="577df-122">**Запуск процесса записи**</span><span class="sxs-lookup"><span data-stu-id="577df-122">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="577df-123">**Стирание перезаписываемого компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="577df-123">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="577df-124">**Получение состояния диска и диска**</span><span class="sxs-lookup"><span data-stu-id="577df-124">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="577df-125">**Получение состояния записи**</span><span class="sxs-lookup"><span data-stu-id="577df-125">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> <dt>

[<span data-ttu-id="577df-126">**Интерфейс Ивмпкдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="577df-126">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




