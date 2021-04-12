---
title: Сведения об объекте Player
description: Сведения об объекте Player
ms.assetid: db995e75-d4e3-4f50-a34a-cc1b2f2c5db5
keywords:
- Проигрыватель Windows Media Player, объект Player
- Объектная модель проигрывателя Windows Media, объект Player
- Объектная модель, объект Player
- Элемент управления ActiveX проигрывателя Windows Media, объект Player
- Элемент управления ActiveX, объект Player
- Элемент управления ActiveX проигрывателя Windows Media Mobile, объект Player
- Проигрыватель Windows Media Mobile, объект Player
- Объект Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c030d42cd6fd65811c41af7401ec3e60c8c7801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133026"
---
# <a name="about-the-player-object"></a>Сведения об объекте Player

Объект **Player** — это основной объект для элемента управления проигрывателя Windows Media. Все прочие связанные объекты подключаются к этому объекту через определенные свойства, которые возвращают объект. Например, доступ к объекту **параметров** осуществляется через свойство **Settings** . Объект **Player** предоставляет методы, свойства и события, относящиеся к основным функциям проигрывателя Windows Media.

Так как эта ссылка также используется для программирования обложек, идентификатор объекта **проигрывателя** будет "Player" для примеров синтаксиса.

Использование глобального атрибута **Player** в файле определения обложки предоставляет доступ к объекту **Player** для использования в сценариях. С помощью объекта **Player** все остальные объекты в элементе управления проигрывателя Windows Media также становятся доступными для сценариев. События объекта **Player** и свойства **URL-адреса** можно также указать во время разработки с помощью элемента Skin [проигрывателя](player-element.md) . Дополнительные сведения см. в разделе [обложки проигрывателя Windows Media](windows-media-player-skins.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Объектная модель проигрывателя для языков сценариев**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




