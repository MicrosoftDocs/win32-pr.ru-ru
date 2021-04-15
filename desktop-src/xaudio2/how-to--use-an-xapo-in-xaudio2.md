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
# <a name="how-to-use-an-xapo-in-xaudio2"></a><span data-ttu-id="60574-103">Руководство: использование XAPO в XAudio2</span><span class="sxs-lookup"><span data-stu-id="60574-103">How to: Use an XAPO in XAudio2</span></span>

<span data-ttu-id="60574-104">В этом разделе показано, как использовать воздействие, созданное с помощью API КСАПО в цепочке эффектов XAudio2.</span><span class="sxs-lookup"><span data-stu-id="60574-104">This topic shows you how to use an effect created with the XAPO API in an XAudio2 effect chain.</span></span>

1.  <span data-ttu-id="60574-105">Создайте КСАПО, как описано в разделе [инструкции. Создание ксапо](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="60574-105">Create the XAPO as described in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

    <span data-ttu-id="60574-106">Можно также реализовать функциональные возможности параметров времени выполнения, как описано в разделе [как добавить поддержку параметров времени выполнения в ксапо](how-to--add-run-time-parameter-support-to-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="60574-106">You can also implement run-time parameter functionality as described in [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

2.  <span data-ttu-id="60574-107">Создайте экземпляр КСАПО.</span><span class="sxs-lookup"><span data-stu-id="60574-107">Create an instance of the XAPO.</span></span>

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  <span data-ttu-id="60574-108">Заполнить структуру [**\_ \_ дескриптора XAUDIO2 Effect**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) данными.</span><span class="sxs-lookup"><span data-stu-id="60574-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  <span data-ttu-id="60574-109">Заполнение структуры [**\_ \_ цепочки эффектов XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) данными.</span><span class="sxs-lookup"><span data-stu-id="60574-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  <span data-ttu-id="60574-110">Примените цепочку эффектов к XAudio2 Voice с помощью функции [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) .</span><span class="sxs-lookup"><span data-stu-id="60574-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="60574-111">Цепочку эффектов можно также применить к голоса при создании голоса, передав цепочку в качестве параметра в [**IXAudio2:: креатесаурцевоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: креатесубмиксвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)или [**IXAudio2:: креатемастерингвоице**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span><span class="sxs-lookup"><span data-stu-id="60574-111">An effect chain can also be applied to a voice when the voice is created by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

6.  <span data-ttu-id="60574-112">Отпустите этот результат с помощью IUnknown:: Release.</span><span class="sxs-lookup"><span data-stu-id="60574-112">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="60574-113">При создании КСАПО у него будет значение счетчика ссылок, равное 1.</span><span class="sxs-lookup"><span data-stu-id="60574-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="60574-114">Если КСАПО передается в XAudio2 с помощью [**сетеффектчаин**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 увеличивает значение счетчика ссылок в ксапо.</span><span class="sxs-lookup"><span data-stu-id="60574-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="60574-115">Освобождение ссылки клиента на КСАПО позволяет XAudio2 стать владельцем КСАПО.</span><span class="sxs-lookup"><span data-stu-id="60574-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="60574-116">Если XAudio2 содержит единственную ссылку на КСАПО, он будет удален, когда он больше не используется XAudio2.</span><span class="sxs-lookup"><span data-stu-id="60574-116">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="60574-117">Если код клиента должен поддерживать ссылку на КСАПО для последующего повторного использования, например, этот шаг следует пропустить.</span><span class="sxs-lookup"><span data-stu-id="60574-117">If the client code needs to maintain a reference to the XAPO for later reuse, for example, you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

7.  <span data-ttu-id="60574-118">Заполните структуру параметра (при наличии), связанную с этим действием.</span><span class="sxs-lookup"><span data-stu-id="60574-118">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="60574-119">В этом случае это процент полной силы, к которой должен применяться этот результат.</span><span class="sxs-lookup"><span data-stu-id="60574-119">In this case, the percentage of full strength at which the effect should be applied.</span></span>

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  <span data-ttu-id="60574-120">Передайте в действие структуру параметра Effect, вызвав функцию [**сетеффектпараметерс**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) для голоса, к которому присоединен этот результат.</span><span class="sxs-lookup"><span data-stu-id="60574-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="60574-121">См. также</span><span class="sxs-lookup"><span data-stu-id="60574-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60574-122">Звуковые эффекты</span><span class="sxs-lookup"><span data-stu-id="60574-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="60574-123">Обзор протокола XAPO</span><span class="sxs-lookup"><span data-stu-id="60574-123">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="60574-124">Руководство по программированию для XAudio2</span><span class="sxs-lookup"><span data-stu-id="60574-124">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
