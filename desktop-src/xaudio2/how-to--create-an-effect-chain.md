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
# <a name="how-to-create-an-effect-chain"></a><span data-ttu-id="f9f4a-104">Руководство: создание цепи эффектов</span><span class="sxs-lookup"><span data-stu-id="f9f4a-104">How to: Create an Effect Chain</span></span>

<span data-ttu-id="f9f4a-105">В этом разделе показано, как можно применить цепочку эффектов к голоса, чтобы разрешить пользовательскую обработку звуковых данных для этого голоса.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-105">This topic shows you how you can apply an effect chain to a voice to allow custom processing of the audio data for that voice.</span></span> <span data-ttu-id="f9f4a-106">В этом разделе описывается использование эффекта переглагола, который является одним из встроенных эффектов XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-106">This topic describes how to use the reverb effect, which is one of the built-in XAudio2 effects.</span></span>

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a><span data-ttu-id="f9f4a-107">Создание базовой цепочки эффектов, которая применяет воздействие к голоса</span><span class="sxs-lookup"><span data-stu-id="f9f4a-107">To create a basic effect chain that applies an effect to a voice</span></span>

1.  <span data-ttu-id="f9f4a-108">Создайте результат.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-108">Create the effect.</span></span>

    <span data-ttu-id="f9f4a-109">В этом примере функция [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) создает переглаголный результат.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-109">In this example, the [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) function creates a reverb effect.</span></span> <span data-ttu-id="f9f4a-110">Список возможных источников эффектов для использования с XAudio2 см. в статье [XAudio2 Audio Effects](xaudio2-audio-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="f9f4a-110">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for a list of possible sources of effects for use with XAudio2.</span></span>

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  <span data-ttu-id="f9f4a-111">Заполнить структуру [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) данными.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-111">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    <span data-ttu-id="f9f4a-112">Если в цепочке есть несколько эффектов, для каждого из них потребуется структура [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="f9f4a-112">If there are multiple effects in the chain, each effect will need a [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="f9f4a-113">Заполнение структуры [**\_ \_ цепочки эффектов XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) данными.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-113">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span> <span data-ttu-id="f9f4a-114">В этом случае цепочка имеет только один результат.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-114">In this case, the chain only has one effect.</span></span> <span data-ttu-id="f9f4a-115">Если цепочка имеет более одного эффекта, элемент Еффекткаунт будет содержать количество эффектов, а элемент Пеффектдескрипторс будет указывать на массив \_ \_ структур дескрипторов XAUDIO2.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-115">If the chain has more than one effect, the EffectCount member will contain the count of effects, and the pEffectDescriptors member will point to an array of XAUDIO2\_EFFECT\_DESCRIPTOR structures.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="f9f4a-116">Примените цепочку эффектов к голоса с помощью функции [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="f9f4a-116">Apply the effect chain to a voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    <span data-ttu-id="f9f4a-117">Вы можете применять цепочки эффектов к основным голосовым, исходным и голосовым субмикс.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-117">You can apply effect chains to master voices, source voices, and submix voices.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  <span data-ttu-id="f9f4a-118">Отпустите этот результат с помощью IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-118">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="f9f4a-119">При создании КСАПО у него будет значение счетчика ссылок, равное 1.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-119">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="f9f4a-120">Если КСАПО передается в XAudio2 с помощью [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 увеличивает значение счетчика ссылок в ксапо.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-120">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="f9f4a-121">Освобождение ссылки клиента на КСАПО позволяет XAudio2 стать владельцем КСАПО.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-121">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="f9f4a-122">Если XAudio2 содержит единственную ссылку на КСАПО, он будет удален, когда он больше не используется XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-122">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="f9f4a-123">Если код клиента должен поддерживать ссылку на КСАПО — например, для использования в дальнейшем, этот шаг следует пропустить.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-123">If the client code needs to maintain a reference to the XAPO—for example for later reuse—you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="f9f4a-124">Заполните структуру параметра (при наличии), связанную с этим действием.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-124">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="f9f4a-125">В результате переглагола используется [**Структура \_ \_ параметров переглагола XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) .</span><span class="sxs-lookup"><span data-stu-id="f9f4a-125">The reverb effect uses an [**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) structure.</span></span>

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

    

7.  <span data-ttu-id="f9f4a-126">Передайте в действие структуру параметра Effect, вызвав функцию [**сетеффектпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) для голоса, к которому присоединен этот результат.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-126">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  <span data-ttu-id="f9f4a-127">При необходимости отключите или включите нужный результат.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-127">Disable or enable the effect, whenever appropriate.</span></span>

    <span data-ttu-id="f9f4a-128">Вы можете использовать [**дисаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) в любое время, чтобы отключить воздействие.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-128">You can use [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) at any time to turn an effect off.</span></span>

    ```
    pVoice->DisableEffect(0);
    ```

    

    <span data-ttu-id="f9f4a-129">Вы можете снова включить этот результат с помощью [**енаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span><span class="sxs-lookup"><span data-stu-id="f9f4a-129">You can turn on an effect again with [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span></span>

    ```
    pVoice->EnableEffect(0);
    ```

    

    <span data-ttu-id="f9f4a-130">Параметры для [**дисаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) и [**енаблиффект**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) указывают, какие действия в цепочке следует включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="f9f4a-130">The parameters for [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) and [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specify which effect in the chain to enable or disable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9f4a-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f9f4a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9f4a-132">Звуковые эффекты</span><span class="sxs-lookup"><span data-stu-id="f9f4a-132">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="f9f4a-133">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="f9f4a-133">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="f9f4a-134">Руководство: создание базовой схемы обработки звука</span><span class="sxs-lookup"><span data-stu-id="f9f4a-134">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="f9f4a-135">Обзор протокола XAPO</span><span class="sxs-lookup"><span data-stu-id="f9f4a-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="f9f4a-136">Как использовать КСАОПФКС в XAudio2</span><span class="sxs-lookup"><span data-stu-id="f9f4a-136">How to: Use XAOPFX in XAudio2</span></span>](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="f9f4a-137">Как использовать КСАОП в XAudio2</span><span class="sxs-lookup"><span data-stu-id="f9f4a-137">How to: Use an XAOP in XAudio2</span></span>](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
