---
title: Об ошибках и объектах Ерроритем
description: Об ошибках и объектах Ерроритем
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- проигрыватель Windows Media, объект Error
- объектная модель проигрыватель Windows Media, объект Error
- Объектная модель, объект Error
- проигрыватель Windows Media ActiveX элемент управления, объект Error
- элемент управления ActiveX, объект Error
- проигрыватель Windows Media мобильный ActiveX элемент управления, объект Error
- проигрыватель Windows Media Мобильный, объект Error
- Объект ошибки
- проигрыватель Windows Media, объект ерроритем
- объектная модель проигрыватель Windows Media, объект ерроритем
- Объектная модель, объект Ерроритем
- проигрыватель Windows Media элемент управления ActiveX, объект ерроритем
- элемент управления ActiveX, объект ерроритем
- проигрыватель Windows Media мобильный ActiveX элемент управления, объект ерроритем
- проигрыватель Windows Media Мобильные устройства, объект Ерроритем
- Объект Ерроритем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84dcd8e0961007c185640b32ac53d249d2e739ca5e1aa4247a6735e09b2a3242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004404"
---
# <a name="about-the-error-and-erroritem-objects"></a>Об ошибках и объектах Ерроритем

объекты **Error** и **ерроритем** управляют возможностями обработки ошибок проигрыватель Windows Media. Объект **Error** извлекается из объекта **Player** через свойство **Error** . Вы можете получить конкретный код из объекта **Error** , используя свойство **Item** объекта **Error** для создания объекта **ерроритем** . Например, чтобы получить код ошибки первого элемента ошибки, введите:


```C++
myerrorcode = player.error.item(0).errorCode;

```



Также можно вызвать веб-справку с объектом **Error** , используя следующий код:


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Объект Error**](error-object.md)
</dt> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> <dt>

[**Объектная модель проигрывателя для языков сценариев**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




