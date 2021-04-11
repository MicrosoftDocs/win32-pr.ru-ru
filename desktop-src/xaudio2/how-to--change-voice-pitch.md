---
description: В этом разделе показано, как можно увеличить или уменьшить тон звуковых данных, изменив скорость воспроизведения с помощью функции Сетфрекуенциратио на исходном голоса.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: Как изменить тон голоса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154618"
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

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Элемент управления громкостью и шагом XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
