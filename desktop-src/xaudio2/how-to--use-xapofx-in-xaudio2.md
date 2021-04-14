---
description: В этом разделе показано, как использовать один из эффектов, входящих в КСАПОФКС, в цепочку эффектов XAudio2.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 'Руководство: использование XAPOFX в XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692496"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>Руководство: использование XAPOFX в XAudio2

В этом разделе показано, как использовать один из эффектов, входящих в КСАПОФКС, в цепочку эффектов XAudio2.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>Использование действия из КСАПОФКС в цепочке эффектов XAudio2

1.  Создайте результат, передав CLSID КСАПОФКСного действия в функцию [**креатефкс**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .

    В этом случае создается упрощенный Фксревербй эффекты.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Заполнить структуру [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) данными.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Заполнение структуры [**\_ \_ цепочки эффектов XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) данными.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Примените цепочку эффектов к XAudio2 Voice с помощью функции [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Вы также можете применить цепочку эффектов к голоса при создании голоса, передав цепочку в качестве параметра в [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: креатесубмиксвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)или [**IXAudio2:: креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

5.  Отпустите этот результат с помощью IUnknown:: Release. При создании КСАПО у него будет значение счетчика ссылок, равное 1. Если КСАПО передается в XAudio2 с помощью [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 увеличивает значение счетчика ссылок в ксапо. Освобождение ссылки клиента на КСАПО позволяет XAudio2 стать владельцем КСАПО. Если XAudio2 содержит единственную ссылку на КСАПО, эта ссылка удаляется, когда она больше не используется XAudio2. Если код клиента должен поддерживать ссылку на КСАПО (например, для дальнейшего использования), этот шаг можно пропустить.

    ```
    pXAPO->Release();
    ```

    

6.  Заполните структуру параметра (при наличии), связанную с этим действием.

    В этом случае структура [**\_ параметров фксреверб**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) используется для установки рассеяния и размера комнаты, которые должен использовать измененный результат.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Передайте в действие структуру параметра Effect, вызвав функцию [**сетеффектпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) для голоса, к которому присоединен этот результат.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Звуковые эффекты](audio-effects.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> </dl>

 

 
