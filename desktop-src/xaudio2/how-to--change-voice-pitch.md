---
description: В этом разделе показано, как можно увеличить или уменьшить тон звуковых данных, изменив скорость воспроизведения с помощью функции Сетфрекуенциратио на исходном голоса.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: Как изменить тон голоса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc44fe757c563e3556f760ead594bb619da9f62fb2c3eafc774e15d7b9e5bc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926474"
---
# <a name="how-to-change-voice-pitch"></a>Как изменить тон голоса

В этом разделе показано, как можно увеличить или уменьшить тон звуковых данных, изменив скорость воспроизведения с помощью функции [**сетфрекуенциратио**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) на исходном голоса.

## <a name="to-change-the-pitch-of-a-source-voice"></a>Изменение тона исходного голоса

1.  Определите желаемый коэффициент частоты для [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).

    Дополнительные сведения о вычислении коэффициента частоты см. в разделе [XAudio2 Volume and кувшин Control](xaudio2-volume-and-pitch-control.md) .

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Используйте функцию [**сетфрекуенциратио**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , чтобы задать коэффициент частоты исходного голоса.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Элемент управления громкостью и шагом XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
