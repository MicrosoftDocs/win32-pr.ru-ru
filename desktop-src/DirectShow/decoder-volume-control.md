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
# <a name="decoder-volume-control"></a>Регулятор громкости декодера

Приложения контролируют громкость звука через интерфейс [**ибасикаудио**](/windows/desktop/api/Control/nn-control-ibasicaudio) . Для Кспрокси предусмотрен обработчик интерфейса **ибасикаудио** . Чтобы декодер обрабатывал команды Volume из Кспрокси, он должен добавить несколько разделов реестра в сценарий установки и поддерживать набор свойств **\_ Wave кспропсетид** .

Создайте новые разделы реестра для драйвера:


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



Для реализации регулятора громкости драйвер также должен поддерживать **кспропсетид \_ wave** и KsProperty.ID = кспроперти \_ Wave \_ . Это свойство передается в драйвер с помощью методов [**икспропертисет:: Get**](ikspropertyset-get.md) и [**Икспропертисет:: Set**](ikspropertyset-set.md) . В полях Лефтаттенуатион и Ригхтаттентуатион в качестве линейных значений в диапазоне от Символ 0x0000 до 0xFFFF.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы и спецификации декодера](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



