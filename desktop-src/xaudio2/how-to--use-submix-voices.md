---
description: В этом разделе показано, как можно задать группы голосов для отправки выходных данных в один и тот же субмикс голос. Это позволяет одному изменению субмикс голоса, чтобы повлиять на всю группу голосов.
ms.assetid: 76c1c138-4846-9c4f-7875-446867436ee9
title: 'Руководство: использование субмикшированной речи'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7152c3224d6528ac52651f2ca2f433631b347c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265269"
---
# <a name="how-to-use-submix-voices"></a><span data-ttu-id="f3024-104">Руководство: использование субмикшированной речи</span><span class="sxs-lookup"><span data-stu-id="f3024-104">How to: Use Submix Voices</span></span>

<span data-ttu-id="f3024-105">В этом разделе показано, как можно задать группы голосов для отправки выходных данных в один и тот же субмикс голос.</span><span class="sxs-lookup"><span data-stu-id="f3024-105">This topic shows you how you can set groups of voices to send their output to the same submix voice.</span></span> <span data-ttu-id="f3024-106">Это позволяет одному изменению субмикс голоса, чтобы повлиять на всю группу голосов.</span><span class="sxs-lookup"><span data-stu-id="f3024-106">This enables a single change to a submix voice to affect a whole group of voices.</span></span>

1.  <span data-ttu-id="f3024-107">Создайте [**субмиксный голос**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) , на который будут отсылаться все голоса звуковых эффектов игры.</span><span class="sxs-lookup"><span data-stu-id="f3024-107">Create a [**submix voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) to which all of the game's sound effect voices will send.</span></span>
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  <span data-ttu-id="f3024-108">Создание [**голоса XAUDIO2 \_ \_ отправляет**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) структуру, содержащую ссылку на субмикс Voice.</span><span class="sxs-lookup"><span data-stu-id="f3024-108">Create an [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure that contains a reference to the submix voice.</span></span>
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  <span data-ttu-id="f3024-109">Передайте структуру [**XAUDIO2 Voice в новые \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) исходные голоса по мере их создания.</span><span class="sxs-lookup"><span data-stu-id="f3024-109">Pass the [**XAUDIO2\_VOICE\_SENDS**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) structure to new source voices as they are created.</span></span>
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  <span data-ttu-id="f3024-110">Примените изменения для всех голосов звуковых эффектов, настроив голос субмикс.</span><span class="sxs-lookup"><span data-stu-id="f3024-110">Apply changes to all sound effect voices by adjusting the submix voice.</span></span>

    <span data-ttu-id="f3024-111">В этом примере изменение объема голоса субмикс с помощью функции [**сетволуме**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) эффективно изменяет объем всех голосов, которые выводят на печать.</span><span class="sxs-lookup"><span data-stu-id="f3024-111">In this example, changing the volume of the submix voice with the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function effectively changes the volume of all voices that output to it.</span></span>

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f3024-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f3024-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3024-113">Голоса</span><span class="sxs-lookup"><span data-stu-id="f3024-113">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="f3024-114">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="f3024-114">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="f3024-115">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="f3024-115">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
