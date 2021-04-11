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
# <a name="how-to-use-submix-voices"></a>Руководство: использование субмикшированной речи

В этом разделе показано, как можно задать группы голосов для отправки выходных данных в один и тот же субмикс голос. Это позволяет одному изменению субмикс голоса, чтобы повлиять на всю группу голосов.

1.  Создайте [**субмиксный голос**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) , на который будут отсылаться все голоса звуковых эффектов игры.
    ```
    IXAudio2SubmixVoice * pSFXSubmixVoice;
    pXAudio2->CreateSubmixVoice(&pSFXSubmixVoice,1,44100,0,0,0,0);
    ```

    

2.  Создание [**голоса XAUDIO2 \_ \_ отправляет**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) структуру, содержащую ссылку на субмикс Voice.
    ```
    XAUDIO2_SEND_DESCRIPTOR SFXSend = {0, pSFXSubmixVoice};
    XAUDIO2_VOICE_SENDS SFXSendList = {1, &SFXSend};
    ```

    

3.  Передайте структуру [**XAUDIO2 Voice в новые \_ \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends) исходные голоса по мере их создания.
    ```
    IXAudio2SourceVoice* pSFXSourceVoice;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSFXSourceVoice, (WAVEFORMATEX*)&wfx,
        0, XAUDIO2_DEFAULT_FREQ_RATIO, pCallback, pSFXSendList, NULL ) ) )
        return hr;
    ```

    

4.  Примените изменения для всех голосов звуковых эффектов, настроив голос субмикс.

    В этом примере изменение объема голоса субмикс с помощью функции [**сетволуме**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) эффективно изменяет объем всех голосов, которые выводят на печать.

    ```
    pSFXSubmixVoice->SetVolume(0.1);
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Голоса](voices.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> </dl>

 

 
