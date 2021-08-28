---
title: Получение интерфейса копирования данных с компакт-диска
description: Получение интерфейса копирования данных с компакт-диска
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- проигрыватель Windows Media, копирование компакт-дисков
- проигрыватель Windows Mediaная модель объектов, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- проигрыватель Windows Media ActiveX управления, копирование компакт-дисков
- ActiveX управления, копирование компакт-дисков
- проигрыватель Windows Media мобильный ActiveX управление, копирование компакт-дисков
- проигрыватель Windows Media Мобильные устройства, копирование компакт-дисков
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Интерфейс Ивмпкдромрип
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2179e4f38eee121d7b8fefc028adf232eb724264362396c8cacedfcc55b162d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002554"
---
# <a name="retrieving-the-ripping-interface"></a>Получение интерфейса копирования данных с компакт-диска

Чтобы перечислить дисководы компакт-дисков на компьютере пользователя, используйте интерфейс **ивмпкдромколлектион** . Получите указатель на этот интерфейс, вызвав [ивмпкоре:: Get \_ кдромколлектион](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

С помощью методов [Get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) и [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) можно выполнить итерацию коллекции, чтобы получить интерфейс [ивмпкдром](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) для каждого компакт-диска на компьютере пользователя.

Интерфейс **ивмпкдром** представляет отдельный компакт-диск. Прежде чем начать копирование компакт-диска, необходимо сначала вызвать **QueryInterface** через указатель **ивмпкдром** , чтобы получить интерфейс [ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .

В следующем примере кода показано, как получить интерфейс для копирования компакт-диска с определенного диска:


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Копирование компакт-диска**](ripping-a-cd.md)
</dt> <dt>

[**Запуск процесса копирования**](starting-the-rip-process.md)
</dt> <dt>

[**Получение состояния копирования**](retrieving-the-rip-status.md)
</dt> <dt>

[**Выбор элементов для копирования**](selecting-items-for-ripping.md)
</dt> <dt>

[**Интерфейс Ивмпкдромколлектион**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




