---
description: В этом разделе показано, как использовать воздействие, созданное с помощью API КСАПО в цепочке эффектов XAudio2.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 'Руководство: использование XAPO в XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682874"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a>Руководство: использование XAPO в XAudio2

В этом разделе показано, как использовать воздействие, созданное с помощью API КСАПО в цепочке эффектов XAudio2.

1.  Создайте КСАПО, как описано в разделе [инструкции. Создание ксапо](how-to--create-an-xapo.md).

    Можно также реализовать функциональные возможности параметров времени выполнения, как описано в разделе [как добавить поддержку параметров времени выполнения в ксапо](how-to--add-run-time-parameter-support-to-an-xapo.md).

2.  Создайте экземпляр КСАПО.

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  Заполнить структуру [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) данными.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  Заполнение структуры [**\_ \_ цепочки эффектов XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) данными.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  Примените цепочку эффектов к XAudio2 Voice с помощью функции [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Цепочку эффектов можно также применить к голоса при создании голоса, передав цепочку в качестве параметра в [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: креатесубмиксвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)или [**IXAudio2:: креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

     

6.  Отпустите этот результат с помощью IUnknown:: Release.

    При создании КСАПО у него будет значение счетчика ссылок, равное 1. Если КСАПО передается в XAudio2 с помощью [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 увеличивает значение счетчика ссылок в ксапо. Освобождение ссылки клиента на КСАПО позволяет XAudio2 стать владельцем КСАПО. Если XAudio2 содержит единственную ссылку на КСАПО, он будет удален, когда он больше не используется XAudio2. Если код клиента должен поддерживать ссылку на КСАПО для последующего повторного использования, например, этот шаг следует пропустить.

    ```
    pXAPO->Release();
    ```

    

7.  Заполните структуру параметра (при наличии), связанную с этим действием. В этом случае это процент полной силы, к которой должен применяться этот результат.

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  Передайте в действие структуру параметра Effect, вызвав функцию [**сетеффектпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) для голоса, к которому присоединен этот результат.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>См. также

<dl> <dt>

[Звуковые эффекты](audio-effects.md)
</dt> <dt>

[Обзор протокола XAPO](xapo-overview.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> </dl>

 

 
