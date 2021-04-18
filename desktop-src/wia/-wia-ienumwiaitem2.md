---
description: Используется приложениями для перечисления объектов IWiaItem2 в текущей папке дерева элементов.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Интерфейс IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650590"
---
# <a name="ienumwiaitem2-interface"></a>Интерфейс IEnumWiaItem2

Используется приложениями для перечисления объектов [**IWiaItem2**](-wia-iwiaitem2.md) в текущей папке дерева элементов.

## <a name="members"></a>Элементы

Интерфейс **IEnumWiaItem2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumWiaItem2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IEnumWiaItem2** содержит следующие методы.



| Метод                                          | Описание                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Клонировать**](-wia-ienumwiaitem2-clone.md)       | Создает дополнительный экземпляр интерфейса **IEnumWiaItem2** и отправляет обратный указатель на него. <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | Возвращает количество элементов, хранящихся в этом перечислителе. <br/>                                                          |
| [**Далее**](-wia-ienumwiaitem2-next.md)         | Заполняет массив указателей на интерфейсы [**IWiaItem2**](-wia-iwiaitem2.md) .<br/>                                       |
| [**Перезапуск**](-wia-ienumwiaitem2-reset.md)       | Сбрасывает ссылку перечисления на первый объект [**IWiaItem2**](-wia-iwiaitem2.md) . <br/>                          |
| [**Пропустить**](-wia-ienumwiaitem2-skip.md)         | Пропускает указанное число элементов во время перечисления доступных объектов [**IWiaItem2**](-wia-iwiaitem2.md) .<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
