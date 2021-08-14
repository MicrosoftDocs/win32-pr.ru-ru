---
title: Объект Error (пакет SDK для WMP)
description: Объект Error предоставляет доступ к коллекции объектов Ерроритем.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- объект Error проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c8e5b7627db2c55eb41a267f6c8d3a7a779e2f20190ca3061a49a41eb8577adb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748473"
---
# <a name="error-object"></a>Объект Error

Объект **Error** предоставляет доступ к коллекции объектов [ерроритем](erroritem-object.md) .

Объект **Error** поддерживает следующее свойство.



| Свойство.                           | Описание                                        |
|------------------------------------|----------------------------------------------------|
| [ерроркаунт](error-errorcount.md) | Возвращает количество ошибок в очереди ошибок. |



 

Объект **Error** поддерживает следующие методы.



| Метод                                       | Описание                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [клеарерроркуеуе](error-clearerrorqueue.md) | Удаляет ошибки из очереди ошибок.                                                         |
| [Item](error-item.md)                       | Извлекает объект [ерроритем](erroritem-object.md) из очереди ошибок.                     |
| [Справка](error-webhelp.md)                 | запускает проигрыватель Windows Media страницу веб-справки для вывода дополнительных сведений об ошибке. |



 

Доступ к объекту **Error** осуществляется через следующее свойство.



| Объект                      | Свойство                  |
|-----------------------------|---------------------------|
| [Игрок](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Справочник по объектной модели для создания сценариев**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




