---
description: Запись ТВ-звука
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Запись ТВ-звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662035"
---
# <a name="capturing-tv-audio"></a>Запись ТВ-звука

Чтобы записать звук из аналогового телевидения в файл, используйте [фильтр записи звука](audio-capture-filter.md). Используйте перечислитель системных устройств для создания фильтра записи звука. В системе пользователя может быть несколько устройств записи звука. пользователь должен выбрать устройство, представляющее звуковую карту.

Подключите выходную закрепление записи звука к фильтру мультиплексора:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



Входные контакты не обязательно должны быть подключены к чему угодно. Каждый входной ПИН-код представляет собой физический ввод на устройстве аудиозаписи. Используйте интерфейс [**иамаудиоинпутмиксер**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) , чтобы включить входные данные, получающие аудиопоток из тюнера. Входные контакты идентифицируются по имени, например "строка in" или "CD Audio". К сожалению, имена могут изменяться с одного устройства на другое. Кроме того, разные платы ТВ-тюнера используют различные входные данные для звуковой карты. Поэтому пользователь может указать, какие входные данные следует использовать.


```C++
IEnumPins *pEnum = NULL;
hr = pAudioCap->EnumPins(&pEnum);
if (SUCCEEDED(hr))
{
    IPin *pPin = NULL;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        IAMAudioInputMixer *pMix;
        hr = pPin->QueryInterface(IID_IAMAudioInputMixer, (void**)&pMix);
        if (SUCCEEDED(hr))
        {
            // Use IPin::QueryPinInfo to get the pin name.
            pPin->Release();
            if (...) // If the user selects this pin:
            {
                pMix->put_Enable(TRUE);
                pMix->put_MixLevel(1.0);
                pMix->Release();
                break;
            }
            pMix->Release();
        }
    }
}
pEnum->Release();
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Аналоговый телевизор](analog-television-audio.md)
</dt> <dt>

[Запись звука](audio-capture.md)
</dt> </dl>

 

 



