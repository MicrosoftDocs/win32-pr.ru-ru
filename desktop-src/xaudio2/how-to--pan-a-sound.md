---
description: В этом разделе показано, как можно задать выходную матрицу исходного голоса Mono, которая выводит на стерео-находящийся звуковой поток, чтобы выполнить панорамирование между левым и верным динамиками.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: Как сдвигать звук
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911100"
---
# <a name="how-to-pan-a-sound"></a><span data-ttu-id="a43ba-103">Как сдвигать звук</span><span class="sxs-lookup"><span data-stu-id="a43ba-103">How to: Pan a Sound</span></span>

<span data-ttu-id="a43ba-104">В этом разделе показано, как можно задать выходную матрицу исходного голоса Mono, которая выводит на стерео-находящийся звуковой поток, чтобы выполнить панорамирование между левым и верным динамиками.</span><span class="sxs-lookup"><span data-stu-id="a43ba-104">This topic shows you how you can set the output matrix of a mono source voice that outputs to a stereo mastering voice in order to achieve panning between the left and right speakers.</span></span>

## <a name="to-setup-panning"></a><span data-ttu-id="a43ba-105">Настройка панорамирования</span><span class="sxs-lookup"><span data-stu-id="a43ba-105">To setup panning</span></span>

1.  <span data-ttu-id="a43ba-106">Извлеките конфигурацию динамика с помощью [**IXAudio2MasteringVoice:: жетчаннелмаск**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="a43ba-106">Retrieve the speaker configuration using [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  <span data-ttu-id="a43ba-107">Создайте массив для хранения выходной матрицы.</span><span class="sxs-lookup"><span data-stu-id="a43ba-107">Create an array to hold the output matrix.</span></span> <span data-ttu-id="a43ba-108">Минимальный размер выходной матрицы — число каналов в исходном речевом формате, которое превышает количество каналов в выходном голосовом потоке.</span><span class="sxs-lookup"><span data-stu-id="a43ba-108">The minimum size of the output matrix is the number of channels in the source voice times the number of channels in the output voice.</span></span> <span data-ttu-id="a43ba-109">В этом случае восемь массивов элементов будут обработаны в любом выходном формате до 7,1ного звучания.</span><span class="sxs-lookup"><span data-stu-id="a43ba-109">In this case an eight element array will handle a mono voice outputting to any output format up to 7.1 surround sound.</span></span>

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  <span data-ttu-id="a43ba-110">Вычислите уровни отправки на основе требуемого панорамирования между левым и верным колонками.</span><span class="sxs-lookup"><span data-stu-id="a43ba-110">Calculate the send levels based on the desired panning between the left and right speakers.</span></span> <span data-ttu-id="a43ba-111">В этом примере значения панорамы будут находиться в диапазоне от-1 до 1 с параметром-1, что означает, что весь звук отображается на левом динамике, а 1 — на правом докладчике.</span><span class="sxs-lookup"><span data-stu-id="a43ba-111">In this example, pan values will range from -1 to 1 with -1 indicating all sound to the left speaker and 1 indicating all sound to the right speaker.</span></span>

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  <span data-ttu-id="a43ba-112">Задайте индексы выходной матрицы, соответствующие левым и правым колонкам, со значениями, вычисленными на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="a43ba-112">Set the output matrix indices corresponding to the left and right speakers with the values calculated in the previous step.</span></span> <span data-ttu-id="a43ba-113">Левый и правый динамики определяются по маске канала, возвращенной [**IXAudio2MasteringVoice:: жетчаннелмаск**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="a43ba-113">The left and right speakers are determined by looking at the channel mask returned by [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span> <span data-ttu-id="a43ba-114">Так как каналы всегда должны быть закодированы в порядке, указанном на странице ссылки [**вавеформатекстенсибле**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , можно определить индекс массива, соответствующий отдельному докладчику.</span><span class="sxs-lookup"><span data-stu-id="a43ba-114">Since the channels must always be encoded in the order specified on the [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) reference page, it is possible to determine the array index corresponding to an individual speaker.</span></span>

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  <span data-ttu-id="a43ba-115">Примените выходную матрицу к исходному голосовому счету с помощью [**IXAudio2Voice:: сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span><span class="sxs-lookup"><span data-stu-id="a43ba-115">Apply the output matrix to the originating voice by using [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span></span> <span data-ttu-id="a43ba-116">Исходным голосовым назначением является либо исходный или субмикс, либо отправка голоса на субмикс или на основной Voice.</span><span class="sxs-lookup"><span data-stu-id="a43ba-116">The originating voice will be either a source voice or a submix voice sending to either a submix voice or a mastering voice.</span></span> <span data-ttu-id="a43ba-117">Сведения об исходном и целевом голоса, например их количестве каналов, можно получить с помощью [**IXAudio2Voice:: жетвоицедетаилс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span><span class="sxs-lookup"><span data-stu-id="a43ba-117">You can get info about the originating and destination voices, like their number of channels, by using [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span></span>

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="a43ba-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a43ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a43ba-119">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="a43ba-119">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a43ba-120">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="a43ba-120">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="a43ba-121">Элемент управления громкостью и шагом XAudio2</span><span class="sxs-lookup"><span data-stu-id="a43ba-121">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
