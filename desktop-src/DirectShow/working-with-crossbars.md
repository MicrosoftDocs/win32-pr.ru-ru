---
description: Работа с микшерами
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Работа с микшерами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684508"
---
# <a name="working-with-crossbars"></a>Работа с микшерами

Если карта видеозаписи имеет несколько физических входных данных или поддерживает более одного аппаратного пути для данных, то граф фильтра может содержать [аналоговый фильтр микшера видео](analog-video-crossbar-filter.md). Построитель диаграмм для записи автоматически добавляет этот фильтр при необходимости. Он будет вышестоящей из фильтра записи. В зависимости от оборудования граф фильтра может содержать более одного экземпляра фильтра микшера.

Фильтр микшера предоставляет интерфейс [**иамкроссбар**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , который можно использовать для направления определенных входных данных в определенный выход. Например, видеоадаптер может иметь соединитель коаксиального подключения и вход S-Video. Они будут представлены в качестве входных контактов фильтра микшера. Чтобы выбрать входные данные, направьте соответствующий входной закрепление к выходному закрепления микшера с помощью метода [**иамкроссбар:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

Чтобы найти фильтры микширования на диаграмме, можно использовать метод [**ICaptureGraphBuilder2:: финдинтерфаце**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) для поиска фильтров, поддерживающих **иамкроссбар**. Например, следующий код выполняет поиск двух микшеров:


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



Более обобщенный подход см. в описании класса Ккроссбар в [примере амкап](amcap-sample.md).

Получив указатель на интерфейс **иамкроссбар** , можно получить сведения о фильтре микшера, включая физический тип каждого ПИН-кода, а также матрицу, на которой входные контакты могут маршрутизироваться с контактами выходных данных.

-   Чтобы определить тип физического соединителя, которому соответствует ПИН-код, вызовите метод [**иамкроссбар:: Get \_ кроссбарпининфо**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) . Метод возвращает член перечисления [**фисикалконнектортипе**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) . Например, в S-Video ПИН-код возвращает значение Фисконн \_ Video \_ свидео.

    Метод **Get \_ кроссбаринфо** также указывает, связаны ли два контакта друг с другом. Например, ПИН-код видеотюнера может быть связан с ПИН-кодом звукового тюнера. Связанные контакты имеют одинаковое направление ПИН-кода и обычно являются частью одной и той же физической розетки или соединителя на карте.

-   Чтобы определить, можно ли направить входной ПИН-код на определенный ПИН-код вывода, вызовите метод [**иамкроссбар:: канрауте**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .
-   Чтобы определить текущую маршрутизацию между закреплениями, вызовите метод [**иамкроссбар:: Get \_ исраутедто**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .

В предыдущих методах все задаются ПИН-коды по номеру индекса, а выходные контакты и входные контакты индексируются из нуля. Вызовите метод **иамкроссбар:: Get \_ пинкаунтс** , чтобы найти количество ПИН-кодов в фильтре.

Например, следующий код отображает сведения о фильтре микшера в окне консоли:


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



Для гипотетических карт эта функция может выдавать следующие выходные данные:


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



На стороне вывода S-Video и Video тюнер связаны с аудио-декодером. На стороне входа видеотюнер связан с звуковым тюнером, а S-Video — со звуковой линией в. Входные данные S-Video направляются на выход S-Video; и входные видеотюнеры направляются в выходные данные видеотюнера. В настоящее время не направляется в звуковой декодер, но в него можно направлять звуковую строку или звуковой тюнер.

Можно изменить существующую маршрутизацию, вызвав метод [**иамкроссбар:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

 

 



