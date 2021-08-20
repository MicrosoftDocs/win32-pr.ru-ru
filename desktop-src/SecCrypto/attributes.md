---
description: Представляет коллекцию объектов Attribute.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Объект Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61936fff0421c43a07483fb8489cca755154a8cfbdd524da5837b12f90add969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773185"
---
# <a name="attributes-object"></a>Объект Attributes

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Объект **Attributes** представляет коллекцию объектов [**Attribute**](attribute.md) . Каждый объект [**атрибута**](attribute.md) представляет один атрибут сообщения.

## <a name="when-to-use"></a>Назначение

Объект **Attributes** используется для выполнения следующих задач:

-   Добавление или удаление определенного объекта [**атрибута**](attribute.md) из коллекции.
-   Очистите коллекцию.
-   Получение числа атрибутов в коллекции.
-   Извлечение определенного объекта [**атрибута**](attribute.md) из коллекции.
-   Выполните итерацию по коллекции.

## <a name="members"></a>Элементы

Объект **Attributes** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **Attributes** содержит эти методы.



| Метод                              | Описание                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Включить**](attributes-add.md)       | Добавляет объект [**атрибута**](attribute.md) в коллекцию.<br/>       |
| [**Clear**](attributes-clear.md)   | Удаляет все объекты [**атрибутов**](attribute.md) из коллекции.<br/> |
| [**Отменит**](attributes-remove.md) | Удаляет объект [**атрибута**](attribute.md) из коллекции.<br/>  |



 

### <a name="properties"></a>Свойства

Объект **Attributes** имеет следующие свойства.



| Свойство                                           | Тип доступа          | Описание                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Только для чтения<br/> | Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции. это свойство скрыто в Visual Basic scripting Edition (VBScript).<br/> |
| [**Расчета**](attributes-count.md)<br/>       | Только для чтения<br/> | Возвращает количество объектов [**атрибутов**](attribute.md) в коллекции.<br/>                                                                                                                                    |
| [**Элемент**](attributes-item.md)<br/>         | Только для чтения<br/> | Извлекает объект [**атрибута**](attribute.md) , представляющий индексированный атрибут. Это свойство по умолчанию.<br/>                                                                                             |



 

## <a name="remarks"></a>Remarks

Не удается создать объект **атрибутов** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Криптографические объекты](cryptography-objects.md)
</dt> </dl>

 

 
