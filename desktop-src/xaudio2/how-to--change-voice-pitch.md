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
# <a name="how-to-change-voice-pitch"></a><span data-ttu-id="046c2-103">Как изменить тон голоса</span><span class="sxs-lookup"><span data-stu-id="046c2-103">How to: Change Voice Pitch</span></span>

<span data-ttu-id="046c2-104">В этом разделе показано, как можно увеличить или уменьшить тон звуковых данных, изменив скорость воспроизведения с помощью функции [**сетфрекуенциратио**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) на исходном голоса.</span><span class="sxs-lookup"><span data-stu-id="046c2-104">This topic shows you how you can raise or lower the pitch of audio data by changing its rate of playback using the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function on a source voice.</span></span>

## <a name="to-change-the-pitch-of-a-source-voice"></a><span data-ttu-id="046c2-105">Изменение тона исходного голоса</span><span class="sxs-lookup"><span data-stu-id="046c2-105">To change the pitch of a source voice</span></span>

1.  <span data-ttu-id="046c2-106">Определите желаемый коэффициент частоты для [**исходного голоса**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span><span class="sxs-lookup"><span data-stu-id="046c2-106">Determine the desired frequency ratio for the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span></span>

    <span data-ttu-id="046c2-107">Дополнительные сведения о вычислении коэффициента частоты см. в разделе [XAudio2 Volume and кувшин Control](xaudio2-volume-and-pitch-control.md) .</span><span class="sxs-lookup"><span data-stu-id="046c2-107">See [XAudio2 Volume and Pitch Control](xaudio2-volume-and-pitch-control.md) for more information about calculating the frequency ratio.</span></span>

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  <span data-ttu-id="046c2-108">Используйте функцию [**сетфрекуенциратио**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , чтобы задать коэффициент частоты исходного голоса.</span><span class="sxs-lookup"><span data-stu-id="046c2-108">Use the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function to set the frequency ratio of the source voice.</span></span>

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="046c2-109">См. также</span><span class="sxs-lookup"><span data-stu-id="046c2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="046c2-110">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="046c2-110">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="046c2-111">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="046c2-111">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="046c2-112">Элемент управления громкостью и шагом XAudio2</span><span class="sxs-lookup"><span data-stu-id="046c2-112">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
