---
title: Об ошибках и объектах Ерроритем
description: Об ошибках и объектах Ерроритем
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Проигрыватель Windows Media, объект Error
- Объектная модель проигрывателя Windows Media, объект Error
- Объектная модель, объект Error
- Элемент управления ActiveX проигрывателя Windows Media, объект Error
- Элемент управления ActiveX, объект Error
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, объект Error
- Проигрыватель Windows Media Mobile, объект Error
- Объект ошибки
- Проигрыватель Windows Media, объект Ерроритем
- Объектная модель проигрывателя Windows Media, объект Ерроритем
- Объектная модель, объект Ерроритем
- Элемент управления ActiveX проигрывателя Windows Media, объект Ерроритем
- Элемент управления ActiveX, объект Ерроритем
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объект Ерроритем
- Проигрыватель Windows Media Mobile, объект Ерроритем
- Объект Ерроритем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330440"
---
# <a name="about-the-error-and-erroritem-objects"></a>Об ошибках и объектах Ерроритем

Объекты **Error** и **ерроритем** управляют функциями обработки ошибок проигрывателя Windows Media. Объект **Error** извлекается из объекта **Player** через свойство **Error** . Вы можете получить конкретный код из объекта **Error** , используя свойство **Item** объекта **Error** для создания объекта **ерроритем** . Например, чтобы получить код ошибки первого элемента ошибки, введите:


```C++
myerrorcode = player.error.item(0).errorCode;

```



Также можно вызвать веб-справку с объектом **Error** , используя следующий код:


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объект Error**](error-object.md)
</dt> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> <dt>

[**Объектная модель проигрывателя для языков сценариев**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




