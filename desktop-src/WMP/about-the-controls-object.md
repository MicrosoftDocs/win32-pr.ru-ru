---
title: Об объекте Controls
description: Об объекте Controls
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Проигрыватель Windows Media, объект Controls
- Объектная модель проигрывателя Windows Media, объект Controls
- Объектная модель, объект Controls
- Элемент управления ActiveX проигрывателя Windows Media, объект Controls
- Элемент управления ActiveX, объект Controls
- Элемент управления ActiveX проигрывателя Windows Media Mobile, объект Controls
- Проигрыватель Windows Media Mobile, объект Controls
- Объект Controls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410630"
---
# <a name="about-the-controls-object"></a>Об объекте Controls

Объект **Controls** управляет передачей цифрового мультимедийного содержимого через элемент управления с помощью таких методов, как **Play** и **останавливаться**. Доступ к нему осуществляется только через свойство **Controls** объекта **Player** . Свойство **Controls** возвращает объект **Controls** . Доступ к свойствам объекта **элементов управления** можно получить только после его создания. Например, чтобы использовать метод **Play** , необходимо использовать следующий код:


```C++
player.controls.play();

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Объектная модель проигрывателя для языков сценариев**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




