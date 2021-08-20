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
ms.openlocfilehash: d9797a5b2349dd52c21204016d501fc2a34e4f6d2f71d7d4ee696aa208db01b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670207"
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
| [**Сразу**](-wia-ienumwiaitem2-skip.md)         | Пропускает указанное число элементов во время перечисления доступных объектов [**IWiaItem2**](-wia-iwiaitem2.md) .<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
