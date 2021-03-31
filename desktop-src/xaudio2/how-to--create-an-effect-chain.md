---
description: В этом разделе показано, как можно применить цепочку эффектов к голоса, чтобы разрешить пользовательскую обработку звуковых данных для этого голоса. В этом разделе описывается использование эффекта переглагола, который является одним из встроенных эффектов XAudio2.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: 'Руководство: создание цепи эффектов'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154615"
---
# <a name="how-to-create-an-effect-chain"></a>Руководство: создание цепи эффектов

В этом разделе показано, как можно применить цепочку эффектов к голоса, чтобы разрешить пользовательскую обработку звуковых данных для этого голоса. В этом разделе описывается использование эффекта переглагола, который является одним из встроенных эффектов XAudio2.

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>Создание базовой цепочки эффектов, которая применяет воздействие к голоса

1.  Создайте результат.

    В этом примере функция [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) создает переглаголный результат. Список возможных источников эффектов для использования с XAudio2 см. в статье [XAudio2 Audio Effects](xaudio2-audio-effects.md) .

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  Заполнить структуру [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) данными.

    Если в цепочке есть несколько эффектов, для каждого из них потребуется структура [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Заполнение структуры [**\_ \_ цепочки эффектов XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) данными. В этом случае цепочка имеет только один результат. Если цепочка имеет более одного эффекта, элемент Еффекткаунт будет содержать количество эффектов, а элемент Пеффектдескрипторс будет указывать на массив \_ \_ структур дескрипторов XAUDIO2.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Примените цепочку эффектов к голоса с помощью функции [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .

    Вы можете применять цепочки эффектов к основным голосовым, исходным и голосовым субмикс.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  Отпустите этот результат с помощью IUnknown:: Release.

    При создании КСАПО у него будет значение счетчика ссылок, равное 1. Если КСАПО передается в XAudio2 с помощью [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 увеличивает значение счетчика ссылок в ксапо. Освобождение ссылки клиента на КСАПО позволяет XAudio2 стать владельцем КСАПО. Если XAudio2 содержит единственную ссылку на КСАПО, он будет удален, когда он больше не используется XAudio2. Если код клиента должен поддерживать ссылку на КСАПО — например, для использования в дальнейшем, этот шаг следует пропустить.

    ```
    pXAPO->Release();
    ```

    

6.  Заполните структуру параметра (при наличии), связанную с этим действием. В результате переглагола используется [**Структура \_ \_ параметров переглагола XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  Передайте в действие структуру параметра Effect, вызвав функцию [**сетеффектпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) для голоса, к которому присоединен этот результат.

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  При необходимости отключите или включите нужный результат.

    Вы можете использовать [**дисаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) в любое время, чтобы отключить воздействие.

    ```
    pVoice->DisableEffect(0);
    ```

    

    Вы можете снова включить этот результат с помощью [**енаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).

    ```
    pVoice->EnableEffect(0);
    ```

    

    Параметры для [**дисаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) и [**енаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) указывают, какие действия в цепочке следует включить или отключить.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Звуковые эффекты](audio-effects.md)
</dt> <dt>

[Руководство по программированию для XAudio2](programming-guide.md)
</dt> <dt>

[Руководство: создание базовой схемы обработки звука](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Обзор протокола XAPO](xapo-overview.md)
</dt> <dt>

[Как использовать КСАОПФКС в XAudio2](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[Как использовать КСАОП в XAudio2](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
