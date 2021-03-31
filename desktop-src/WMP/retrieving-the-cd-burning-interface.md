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
# <a name="retrieving-the-cd-burning-interface"></a>Получение интерфейса записи компакт-дисков

Чтобы перечислить дисководы компакт-дисков на компьютере пользователя, используйте интерфейс **ивмпкдромколлектион** . Чтобы получить указатель на этот интерфейс, вызовите [ивмпкоре:: Get \_ кдромколлектион](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

С помощью методов **Get \_ Count** и **Item** можно выполнить итерацию коллекции, чтобы получить указатель интерфейса [ивмпкдром](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) для каждого компакт-дисковода на компьютере пользователя.

Интерфейс **ивмпкдром** представляет отдельный компакт-диск. Перед началом записи компакт-диска необходимо сначала вызвать **QueryInterface** через указатель **ивмпкдром** , чтобы получить указатель на интерфейс [ивмпкдромбурн](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .

В следующем примере кода показано, как получить интерфейс для записи компакт-диска на конкретный диск:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Запись компакт-диска**](burning-a-cd.md)
</dt> <dt>

[**Запуск процесса записи**](starting-the-burn-process.md)
</dt> <dt>

[**Стирание перезаписываемого компакт-диска**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Получение состояния диска и диска**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Получение состояния записи**](retrieving-the-burn-status.md)
</dt> <dt>

[**Интерфейс Ивмпкдромколлектион**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




