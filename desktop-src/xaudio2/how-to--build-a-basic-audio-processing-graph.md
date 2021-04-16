---
description: Минимальным требованием для включения XAudio2 для воспроизведения звуковых данных является график обработки звука, который формируется на основе одного голоса для главной системы и одного исходного голоса.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Руководство: создание базовой схемы обработки звука'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712285"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="4561d-103">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="4561d-103">How to: Build a Basic Audio Processing Graph</span></span>

<span data-ttu-id="4561d-104">Минимальным требованием для включения XAudio2 для воспроизведения звуковых данных является график обработки звука, который формируется на основе одного голоса для главной системы и одного исходного голоса.</span><span class="sxs-lookup"><span data-stu-id="4561d-104">The minimum requirement for enabling XAudio2 to play audio data is an audio processing graph, which is constructed from a single mastering voice and a single source voice.</span></span>

## <a name="to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="4561d-105">Создание базового графика обработки звука</span><span class="sxs-lookup"><span data-stu-id="4561d-105">To build a basic audio processing graph</span></span>

1.  <span data-ttu-id="4561d-106">Инициализируйте подсистему XAudio2, выполнив действия, описанные в разделе [инструкции. Инициализация XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="4561d-106">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="4561d-107">Заполните структуру [**\_ буфера**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **вавеформатекс** и XAUDIO2, выполнив действия, описанные в разделе [как загружать файлы аудиоданных в XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="4561d-107">Populate a **WAVEFORMATEX** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
3.  <span data-ttu-id="4561d-108">Создайте исходный голоса с помощью функции [**креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .</span><span class="sxs-lookup"><span data-stu-id="4561d-108">Create a source voice using the [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

    <span data-ttu-id="4561d-109">Если для аргумента Псендлист параметра [**креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)указано значение null, выходные данные исходного голоса будут переводиться на основной язык, созданный на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="4561d-109">When you specify NULL for the pSendList argument of [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), the source voice's output goes to the mastering voice created in step 1.</span></span>

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    <span data-ttu-id="4561d-110">После завершения этого шага появляется простой графический график, состоящий из исходного голоса, голоса для главной системы и звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="4561d-110">After you finish this step, there is a simple audio graph consisting of the source voice, the mastering voice, and the audio device.</span></span> <span data-ttu-id="4561d-111">Оставшиеся действия, описанные в этом разделе, показывают, как начать передачу звуковых данных через граф.</span><span class="sxs-lookup"><span data-stu-id="4561d-111">The remaining steps in this how-to topic show you how to start audio data flowing through the graph.</span></span>

    <span data-ttu-id="4561d-112">Простая звуковая диаграмма</span><span class="sxs-lookup"><span data-stu-id="4561d-112">A simple audio graph</span></span>

    ![простая звуковая диаграмма.](images/xaudio2-audio-graph.png)

4.  <span data-ttu-id="4561d-114">Используйте функцию [**субмитсаурцебуффер**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) для отправки [**\_ буфера XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) в исходный голоса.</span><span class="sxs-lookup"><span data-stu-id="4561d-114">Use the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) to submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice.</span></span>

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  <span data-ttu-id="4561d-115">Используйте функцию [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) для запуска исходного голоса.</span><span class="sxs-lookup"><span data-stu-id="4561d-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span>

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4561d-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4561d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4561d-117">Графики воспроизведения</span><span class="sxs-lookup"><span data-stu-id="4561d-117">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="4561d-118">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="4561d-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
