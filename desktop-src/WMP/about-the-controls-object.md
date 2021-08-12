---
title: Об объекте Controls
description: Об объекте Controls
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- проигрыватель Windows Media, объект controls
- объектная модель проигрыватель Windows Media, объект controls
- Объектная модель, объект Controls
- проигрыватель Windows Media ActiveX элемент управления, объект controls
- элемент управления ActiveX, объект controls
- проигрыватель Windows Media мобильный ActiveX элемент управления, объект controls
- проигрыватель Windows Media Мобильные устройства, объект Controls
- Объект Controls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea914234ce4458d296a27efe7cf3a392b45b09f05e81f35bef5a355a4e12eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583901"
---
# <a name="about-the-controls-object"></a>Об объекте Controls

Объект **Controls** управляет передачей цифрового мультимедийного содержимого через элемент управления с помощью таких методов, как **Play** и **останавливаться**. Доступ к нему осуществляется только через свойство **Controls** объекта **Player** . Свойство **Controls** возвращает объект **Controls** . Доступ к свойствам объекта **элементов управления** можно получить только после его создания. Например, чтобы использовать метод **Play** , необходимо использовать следующий код:


```C++
player.controls.play();

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Объектная модель проигрывателя для языков сценариев**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




