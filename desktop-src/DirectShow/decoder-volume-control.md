---
description: Регулятор громкости декодера
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Регулятор громкости декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ce525f8b39e873d2c0002ac283014a9bcbe87c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423098"
---
# <a name="decoder-volume-control"></a><span data-ttu-id="1601c-103">Регулятор громкости декодера</span><span class="sxs-lookup"><span data-stu-id="1601c-103">Decoder Volume Control</span></span>

<span data-ttu-id="1601c-104">Приложения контролируют громкость звука через интерфейс [**ибасикаудио**](/windows/desktop/api/Control/nn-control-ibasicaudio) .</span><span class="sxs-lookup"><span data-stu-id="1601c-104">Applications control audio volume through the [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) interface.</span></span> <span data-ttu-id="1601c-105">Для Кспрокси предусмотрен обработчик интерфейса **ибасикаудио** .</span><span class="sxs-lookup"><span data-stu-id="1601c-105">An **IBasicAudio** interface handler is provided for KSProxy.</span></span> <span data-ttu-id="1601c-106">Чтобы декодер обрабатывал команды Volume из Кспрокси, он должен добавить несколько разделов реестра в сценарий установки и поддерживать набор свойств **\_ Wave кспропсетид** .</span><span class="sxs-lookup"><span data-stu-id="1601c-106">For a decoder to handle the volume commands from KSProxy, it must add several registry keys in its setup script and support the **KSPROPSETID\_Wave** property set.</span></span>

<span data-ttu-id="1601c-107">Создайте новые разделы реестра для драйвера:</span><span class="sxs-lookup"><span data-stu-id="1601c-107">Create some new registry keys for the driver:</span></span>


```C++
HKLM\SYSTEM\
  CurrentControlSet\Control
    DeviceClasses
      (decoder guid, eg 2721AE....)
        (Pnp id, eg ##?#VDGENDEV#...)
          #GLOBAL
            Device Parameters
              CLSID      REG_SZ   {17CCA...}
                FriendlyName   REG_SZ   WDM DVD Driver
                  Interfaces <--- create this key
                  {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
    MediaInterfaces
      {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
        (default)  REG_SZ   'KsProxy IBasicAudio handler' // Set this value.
        IID        REG_SZ   56 a8 68 b3 0a d4 11 ce b0 3a 00 20 af 0b a7 70 
                            // Create this key.
```



<span data-ttu-id="1601c-108">Для реализации регулятора громкости драйвер также должен поддерживать **кспропсетид \_ wave** и KsProperty.ID = кспроперти \_ Wave \_ .</span><span class="sxs-lookup"><span data-stu-id="1601c-108">To implement volume control, the driver also must support **KSPROPSETID\_Wave**, along with KsProperty.Id = KSPROPERTY\_WAVE\_VOLUME.</span></span> <span data-ttu-id="1601c-109">Это свойство передается в драйвер с помощью методов [**икспропертисет:: Get**](ikspropertyset-get.md) и [**Икспропертисет:: Set**](ikspropertyset-set.md) .</span><span class="sxs-lookup"><span data-stu-id="1601c-109">This property is passed to the driver through the [**IKsPropertySet::Get**](ikspropertyset-get.md) and [**IKsPropertySet::Set**](ikspropertyset-set.md) methods.</span></span> <span data-ttu-id="1601c-110">В полях Лефтаттенуатион и Ригхтаттентуатион в качестве линейных значений в диапазоне от Символ 0x0000 до 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="1601c-110">The LeftAttenuation and RightAttentuation fields specify the left/right speaker volumes as linear values from 0x0000 to 0xffff.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1601c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="1601c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1601c-112">Интерфейсы и спецификации декодера</span><span class="sxs-lookup"><span data-stu-id="1601c-112">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



