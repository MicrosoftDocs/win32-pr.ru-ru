---
title: Объект Error (пакет SDK для WMP)
description: Объект Error предоставляет доступ к коллекции объектов Ерроритем.
ms.assetid: 1f026ad4-0240-48fe-90ad-739a24e8a7ca
keywords:
- Проигрыватель Windows Media Object Error
topic_type:
- apiref
api_name:
- Error Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0aae4c86dc3f5282be7a16207923e1238e217a9e
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2019
ms.locfileid: "105691426"
---
# <a name="error-object"></a>Объект Error

Объект **Error** предоставляет доступ к коллекции объектов [ерроритем](erroritem-object.md) .

Объект **Error** поддерживает следующее свойство.



| Свойство                           | Описание                                        |
|------------------------------------|----------------------------------------------------|
| [ерроркаунт](error-errorcount.md) | Возвращает количество ошибок в очереди ошибок. |



 

Объект **Error** поддерживает следующие методы.



| Метод                                       | Описание                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| [клеарерроркуеуе](error-clearerrorqueue.md) | Удаляет ошибки из очереди ошибок.                                                         |
| [Item](error-item.md)                       | Извлекает объект [ерроритем](erroritem-object.md) из очереди ошибок.                     |
| [Справка](error-webhelp.md)                 | Открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений об ошибке. |



 

Доступ к объекту **Error** осуществляется через следующее свойство.



| Объект                      | Свойство                  |
|-----------------------------|---------------------------|
| [Игрок](player-object.md) | [error](player-error.md) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Справочник по объектной модели для создания сценариев**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




