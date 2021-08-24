---
description: Предварительный просмотр ТВ-звука
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Предварительный просмотр ТВ-звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6b67e33ffd6f051363e8851afbc31b9f38bed17790687db615b679f6a80a63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748322"
---
# <a name="previewing-tv-audio"></a>Предварительный просмотр ТВ-звука

Для предварительного просмотра телевизионных передач направьте ПИН-код звукового декодера в фильтре микшера к ПИН-коду звукового тюнера. Чтобы отключить звук, направьте ПИН-код звукового декодера в-1, как показано на следующей схеме. (Фильтры микшера описаны в разделе [Работа с микшерами](working-with-crossbars.md).)

![Маршрутизация ПИН-кода звукового декодера](images/vidcap07.png)

Базовый подход выглядит следующим образом:

1.  Чтобы узнать Фильтр микшера, используйте метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) .
2.  Используйте метод [**иамкроссбар:: Get \_ кроссбарпининфо**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) для перечисления входных и выходных закрепления фильтра микшера. Поиск выходного ПИН-кода декодера и входного контакта звукового тюнера.
3.  Если вы нашли правильные ПИН-коды, вызовите [**иамкроссбар:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) , чтобы маршрутизировать контакты. Если нет, воссмотрите поток для другого микшера и повторите этот процесс.
4.  Чтобы отключить звук, направьте ПИН-код звукового декодера в значение – 1.

Большинство ТВ-тюнеров используют один фильтр микшера, но некоторые используют два фильтра микшера. Поэтому, если первый из них завершается ошибкой, может потребоваться выполнить поиск второго микшера.

> [!Note]  
> В отличие от того, что вы можете ожидать, для предварительного просмотра звука не требуется фильтр записи звука или модуль подготовки звука, так как между платой тюнера и звуковой картой есть физическое подключение.

 

В следующем коде эти действия показаны более подробно. Во-первых, это вспомогательная функция, которая выполняет поиск фильтра микшера для указанного типа ПИН-кода:


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



Следующая функция пытается активировать или отключить звук, в зависимости от значения параметра *бактивате* . Он выполняет поиск требуемых ПИН-кодов в указанном фильтре микшера. Если они не найдены, возвращается код ошибки.


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



Следующая функция выполняет поиск фильтра микшера на графе фильтра. Если он найден, он пытается активировать или отключить звук (с помощью функции Previous). Если эта операция завершается неудачно, метод выполняет поиск второго микшера и пытается повторить попытку. Более обобщенный подход к управлению несколькими фильтрами микшера в графе см. в описании класса Ккроссбар в примере приложения Амкап.


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



В следующем коде показано, как вызывать эти функции:


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



Обратите внимание, что эти примеры функций повторяют многие из одних и тех же вызовов функций. Например, они перечисляют контакты микшера каждый раз. В реальном приложении можно кэшировать некоторые из этих сведений.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Аналоговый телевизор](analog-television-audio.md)
</dt> <dt>

[Работа с микшерами](working-with-crossbars.md)
</dt> </dl>

 

 



