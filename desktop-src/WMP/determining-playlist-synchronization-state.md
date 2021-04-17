---
title: Определение состояния синхронизации списка воспроизведения
description: Определение состояния синхронизации списка воспроизведения
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Проигрыватель Windows Media, списки воспроизведения синхронизации
- Объектная модель проигрывателя Windows Media, списки воспроизведения синхронизации
- Объектная модель, списки воспроизведения синхронизации
- Проигрыватель Windows Media Mobile, списки воспроизведения синхронизации
- Элемент управления ActiveX проигрывателя Windows Media, списки воспроизведения синхронизации
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, списки синхронизации
- Элемент управления ActiveX, списки воспроизведения синхронизации
- списки воспроизведения, синхронизация
- списки воспроизведения метафайлов, синхронизация
- Списки воспроизведения метафайлов Windows Media, синхронизация
- переносные устройства, определение состояния списка воспроизведения синхронизации
- списки воспроизведения синхронизации, состояние синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691434"
---
# <a name="determining-playlist-synchronization-state"></a>Определение состояния синхронизации списка воспроизведения

Проигрыватель Windows Media 10 или более поздней версии использует атрибут **синкстате** , чтобы содержать сведения о том, скопирован ли конкретный файл мультимедиа на портативное устройство, а в случае сбоя копирование не удалось, так как на устройстве недостаточно памяти.

В следующем примере кода создается функция, которая получает эти сведения из цифрового файла мультимедиа. Функция принимает следующие параметры:

-   *пмедиа*. Указатель на интерфейс **ивмпмедиа** , представляющий файл цифрового мультимедиа для проверки.
-   *лпсиндекс*. Индекс партнерства текущего устройства.
-   *пулондевице*. Указатель на **длинную** переменную, которая получает значение, указывающее, скопирован ли цифровой файл мультимедиа на устройство.
-   *пулдиднотфит*. Указатель на **длинную** переменную, которая получает значение, указывающее, завершилась ли операция копирования неудачно из-за нехватки памяти на устройстве.

Сведения, содержащиеся в атрибуте **синкстате** , кодируются побитовым способом. Вы можете увидеть, как эта функция используется в примере кода в разделе [перечисление элементов мультимедиа](enumerating-the-media-items.md).


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпмедиа**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3:: Жетитеминфобитипе**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Управление списками воспроизведения синхронизации**](managing-synchronization-playlists.md)
</dt> <dt>

[**Атрибут Синкстате**](syncstate-attribute.md)
</dt> </dl>

 

 




