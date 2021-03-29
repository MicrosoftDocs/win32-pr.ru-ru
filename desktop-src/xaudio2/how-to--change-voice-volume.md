---
description: В этом разделе показано, как можно изменить громкость голоса на общем уровне, на каждом выходном канале или между каждым каналом голоса и другим голосовым сендлист.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: Как изменить громкость голоса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815281"
---
# <a name="how-to-change-voice-volume"></a><span data-ttu-id="0f481-103">Как изменить громкость голоса</span><span class="sxs-lookup"><span data-stu-id="0f481-103">How to: Change Voice Volume</span></span>

<span data-ttu-id="0f481-104">В этом разделе показано, как можно изменить громкость голоса на общем уровне, на каждом выходном канале или между каждым каналом голоса и другим голосовым [**сендлист**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="0f481-104">This topic shows you how you can change the volume of a voice at an overall level, at each output channel, or between each channel of a voice and another voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a><span data-ttu-id="0f481-105">Установка общего уровня громкости для входных данных голоса</span><span class="sxs-lookup"><span data-stu-id="0f481-105">To set an overall volume level for the voice's input</span></span>

-   <span data-ttu-id="0f481-106">Используйте функцию [**сетволуме**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .</span><span class="sxs-lookup"><span data-stu-id="0f481-106">Use the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function.</span></span>

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a><span data-ttu-id="0f481-107">Задание объема выходных каналов голоса</span><span class="sxs-lookup"><span data-stu-id="0f481-107">To set the volume of the voice's output channels</span></span>

1.  <span data-ttu-id="0f481-108">Создайте массив чисел с плавающей запятой, содержащих нужные тома всех выходных каналов в голоса.</span><span class="sxs-lookup"><span data-stu-id="0f481-108">Create an array of floating point numbers that contain the desired volumes of all the output channels in the voice.</span></span>

    <span data-ttu-id="0f481-109">Массив будет иметь одну запись для каждого канала в голоса.</span><span class="sxs-lookup"><span data-stu-id="0f481-109">The array will have one entry for each channel in the voice.</span></span>

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  <span data-ttu-id="0f481-110">Используйте функцию [**сетчаннелволумес**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) , чтобы задать объем выходных каналов.</span><span class="sxs-lookup"><span data-stu-id="0f481-110">Use the [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) function to set the volume of the output channels.</span></span>

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a><span data-ttu-id="0f481-111">Задание объема подключений</span><span class="sxs-lookup"><span data-stu-id="0f481-111">To set the volume of connections</span></span>

<span data-ttu-id="0f481-112">Установите в [**сендлист**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)том соединения между голосовым и голосовым.</span><span class="sxs-lookup"><span data-stu-id="0f481-112">Set the connection volume between the voice and a voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

1.  <span data-ttu-id="0f481-113">Создайте массив чисел с плавающей запятой, определяющий выходную матрицу, если голоса отправляется другому голосовому.</span><span class="sxs-lookup"><span data-stu-id="0f481-113">Create an array of floating point numbers that defines an output matrix if the voice sends to another voice.</span></span>

    > [!Note]  
    > <span data-ttu-id="0f481-114">Массив должен иметь несколько записей, равных исходным голосовым каналам х назначения.</span><span class="sxs-lookup"><span data-stu-id="0f481-114">The array must have a number of entries equal to source voice channels × destination voice channels.</span></span> <span data-ttu-id="0f481-115">В этом примере Сопоставление осуществляется из голоса с одним каналом на голоса с двумя каналами.</span><span class="sxs-lookup"><span data-stu-id="0f481-115">In this example, the mapping is from a voice with one channel to a voice with two channels.</span></span>

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  <span data-ttu-id="0f481-116">Чтобы задать выходную матрицу, используйте функцию [**сетаутпутматрикс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) .</span><span class="sxs-lookup"><span data-stu-id="0f481-116">Use the [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) function to set the output matrix.</span></span>

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="0f481-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0f481-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f481-118">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="0f481-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="0f481-119">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="0f481-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="0f481-120">Элемент управления громкостью и шагом XAudio2</span><span class="sxs-lookup"><span data-stu-id="0f481-120">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
