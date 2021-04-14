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
# <a name="how-to-use-xapofx-in-xaudio2"></a><span data-ttu-id="20c68-103">Руководство: использование XAPOFX в XAudio2</span><span class="sxs-lookup"><span data-stu-id="20c68-103">How to: Use XAPOFX in XAudio2</span></span>

<span data-ttu-id="20c68-104">В этом разделе показано, как использовать один из эффектов, входящих в КСАПОФКС, в цепочку эффектов XAudio2.</span><span class="sxs-lookup"><span data-stu-id="20c68-104">This topic shows you how to use one of the effects included in XAPOFX in an XAudio2 effect chain.</span></span>

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a><span data-ttu-id="20c68-105">Использование действия из КСАПОФКС в цепочке эффектов XAudio2</span><span class="sxs-lookup"><span data-stu-id="20c68-105">To use an effect from XAPOFX in an XAudio2 effect chain</span></span>

1.  <span data-ttu-id="20c68-106">Создайте результат, передав CLSID КСАПОФКСного действия в функцию [**креатефкс**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) .</span><span class="sxs-lookup"><span data-stu-id="20c68-106">Create the effect by passing the CLSID of an XAPOFX effect to the [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) function.</span></span>

    <span data-ttu-id="20c68-107">В этом случае создается упрощенный Фксревербй эффекты.</span><span class="sxs-lookup"><span data-stu-id="20c68-107">In this case, the simplified reverb effect FXReverb is being created.</span></span>

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  <span data-ttu-id="20c68-108">Заполнить структуру [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) данными.</span><span class="sxs-lookup"><span data-stu-id="20c68-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="20c68-109">Заполнение структуры [**\_ \_ цепочки эффектов XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) данными.</span><span class="sxs-lookup"><span data-stu-id="20c68-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="20c68-110">Примените цепочку эффектов к XAudio2 Voice с помощью функции [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="20c68-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="20c68-111">Вы также можете применить цепочку эффектов к голоса при создании голоса, передав цепочку в качестве параметра в [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: креатесубмиксвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)или [**IXAudio2:: креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="20c68-111">You can also apply an effect chain to a voice when you create the voice by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

5.  <span data-ttu-id="20c68-112">Отпустите этот результат с помощью IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="20c68-112">Release the effect with IUnknown::Release.</span></span> <span data-ttu-id="20c68-113">При создании КСАПО у него будет значение счетчика ссылок, равное 1.</span><span class="sxs-lookup"><span data-stu-id="20c68-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="20c68-114">Если КСАПО передается в XAudio2 с помощью [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 увеличивает значение счетчика ссылок в ксапо.</span><span class="sxs-lookup"><span data-stu-id="20c68-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="20c68-115">Освобождение ссылки клиента на КСАПО позволяет XAudio2 стать владельцем КСАПО.</span><span class="sxs-lookup"><span data-stu-id="20c68-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="20c68-116">Если XAudio2 содержит единственную ссылку на КСАПО, эта ссылка удаляется, когда она больше не используется XAudio2.</span><span class="sxs-lookup"><span data-stu-id="20c68-116">If XAudio2 has the only reference to the XAPO, this reference is disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="20c68-117">Если код клиента должен поддерживать ссылку на КСАПО (например, для дальнейшего использования), этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="20c68-117">If the client code needs to maintain a reference to the XAPO—for example, for reuse later—you can skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="20c68-118">Заполните структуру параметра (при наличии), связанную с этим действием.</span><span class="sxs-lookup"><span data-stu-id="20c68-118">Populate the parameter structure, if any, associated with the effect.</span></span>

    <span data-ttu-id="20c68-119">В этом случае структура [**\_ параметров фксреверб**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) используется для установки рассеяния и размера комнаты, которые должен использовать измененный результат.</span><span class="sxs-lookup"><span data-stu-id="20c68-119">In this case, the [**FXREVERB\_PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) structure is used to set the diffusion and room size that the reverb effect should use.</span></span>

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  <span data-ttu-id="20c68-120">Передайте в действие структуру параметра Effect, вызвав функцию [**сетеффектпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) для голоса, к которому присоединен этот результат.</span><span class="sxs-lookup"><span data-stu-id="20c68-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="20c68-121">См. также</span><span class="sxs-lookup"><span data-stu-id="20c68-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c68-122">Звуковые эффекты</span><span class="sxs-lookup"><span data-stu-id="20c68-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="20c68-123">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="20c68-123">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
