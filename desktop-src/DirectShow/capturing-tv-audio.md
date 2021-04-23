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
# <a name="capturing-tv-audio"></a><span data-ttu-id="ca2a1-103">Запись ТВ-звука</span><span class="sxs-lookup"><span data-stu-id="ca2a1-103">Capturing TV Audio</span></span>

<span data-ttu-id="ca2a1-104">Чтобы записать звук из аналогового телевидения в файл, используйте [фильтр записи звука](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ca2a1-104">To capture audio from analog television to a file, use the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="ca2a1-105">Используйте перечислитель системных устройств для создания фильтра записи звука.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-105">Use the System Device Enumerator to create the Audio Capture Filter.</span></span> <span data-ttu-id="ca2a1-106">В системе пользователя может быть несколько устройств записи звука. пользователь должен выбрать устройство, представляющее звуковую карту.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-106">There may be several audio capture devices on the user's system; the user must select the device that represents the sound card.</span></span>

<span data-ttu-id="ca2a1-107">Подключите выходную закрепление записи звука к фильтру мультиплексора:</span><span class="sxs-lookup"><span data-stu-id="ca2a1-107">Connect the audio capture output pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



<span data-ttu-id="ca2a1-108">Входные контакты не обязательно должны быть подключены к чему угодно.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-108">The input pins do not have to be connected to anything.</span></span> <span data-ttu-id="ca2a1-109">Каждый входной ПИН-код представляет собой физический ввод на устройстве аудиозаписи.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-109">Each input pin represents a physical input on the audio capture device.</span></span> <span data-ttu-id="ca2a1-110">Используйте интерфейс [**иамаудиоинпутмиксер**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) , чтобы включить входные данные, получающие аудиопоток из тюнера.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-110">Use the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface to enable the input that receives the audio stream from the tuner.</span></span> <span data-ttu-id="ca2a1-111">Входные контакты идентифицируются по имени, например "строка in" или "CD Audio".</span><span class="sxs-lookup"><span data-stu-id="ca2a1-111">The input pins are identified by name, such as "Line In" or "CD Audio."</span></span> <span data-ttu-id="ca2a1-112">К сожалению, имена могут изменяться с одного устройства на другое.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-112">Unfortunately, the names can change from one device to the next.</span></span> <span data-ttu-id="ca2a1-113">Кроме того, разные платы ТВ-тюнера используют различные входные данные для звуковой карты.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-113">Also, different TV tuner cards use different inputs to the sound card.</span></span> <span data-ttu-id="ca2a1-114">Поэтому пользователь может указать, какие входные данные следует использовать.</span><span class="sxs-lookup"><span data-stu-id="ca2a1-114">Therefore, it is up to the user to identify which input to use.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ca2a1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ca2a1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca2a1-116">Аналоговый телевизор</span><span class="sxs-lookup"><span data-stu-id="ca2a1-116">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="ca2a1-117">Запись звука</span><span class="sxs-lookup"><span data-stu-id="ca2a1-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



