---
title: Получение интерфейса копирования данных с компакт-диска
description: Получение интерфейса копирования данных с компакт-диска
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Интерфейс Ивмпкдромрип
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "103890311"
---
# <a name="retrieving-the-ripping-interface"></a><span data-ttu-id="882b9-113">Получение интерфейса копирования данных с компакт-диска</span><span class="sxs-lookup"><span data-stu-id="882b9-113">Retrieving the Ripping Interface</span></span>

<span data-ttu-id="882b9-114">Чтобы перечислить дисководы компакт-дисков на компьютере пользователя, используйте интерфейс **ивмпкдромколлектион** .</span><span class="sxs-lookup"><span data-stu-id="882b9-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="882b9-115">Получите указатель на этот интерфейс, вызвав [ивмпкоре:: Get \_ кдромколлектион](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="882b9-115">Retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="882b9-116">С помощью методов [Get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) и [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) можно выполнить итерацию коллекции, чтобы получить интерфейс [ивмпкдром](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) для каждого компакт-диска на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="882b9-116">By using the [get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) and [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface for each CD drive on the user's computer.</span></span>

<span data-ttu-id="882b9-117">Интерфейс **ивмпкдром** представляет отдельный компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="882b9-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="882b9-118">Прежде чем начать копирование компакт-диска, необходимо сначала вызвать **QueryInterface** через указатель **ивмпкдром** , чтобы получить интерфейс [ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .</span><span class="sxs-lookup"><span data-stu-id="882b9-118">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface.</span></span>

<span data-ttu-id="882b9-119">В следующем примере кода показано, как получить интерфейс для копирования компакт-диска с определенного диска:</span><span class="sxs-lookup"><span data-stu-id="882b9-119">The following code example demonstrates how to retrieve an interface for ripping a CD from a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="882b9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="882b9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="882b9-121">**Копирование компакт-диска**</span><span class="sxs-lookup"><span data-stu-id="882b9-121">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="882b9-122">**Запуск процесса копирования**</span><span class="sxs-lookup"><span data-stu-id="882b9-122">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="882b9-123">**Получение состояния копирования**</span><span class="sxs-lookup"><span data-stu-id="882b9-123">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="882b9-124">**Выбор элементов для копирования**</span><span class="sxs-lookup"><span data-stu-id="882b9-124">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> <dt>

[<span data-ttu-id="882b9-125">**Интерфейс Ивмпкдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="882b9-125">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




