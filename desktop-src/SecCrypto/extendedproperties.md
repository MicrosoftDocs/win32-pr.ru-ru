---
description: Представляет коллекцию объектов ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Объект расширенных свойств
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648821"
---
# <a name="extendedproperties-object"></a>Объект расширенных свойств

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Объект **расширенных свойств** представляет коллекцию объектов [**ExtendedProperty**](extendedproperty.md) . Каждый объект представляет одно расширенное свойство.

## <a name="when-to-use"></a>Назначение

Объект **расширенных свойств** используется для выполнения следующих задач:

-   Добавьте или удалите объект [**ExtendedProperty**](extendedproperty.md) из коллекции.
-   Получение числа расширенных свойств в коллекции.
-   Извлечение конкретного объекта [**ExtendedProperty**](extendedproperty.md) из коллекции.
-   Выполните итерацию по коллекции.

## <a name="members"></a>Элементы

Объект **расширенных свойств** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#extendedproperties-object)

### <a name="methods"></a>Методы

Объект **расширенных свойств** содержит эти методы.



| Метод                                      | Описание                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Включить**](extendedproperties-add.md)       | Добавляет объект [**ExtendedProperty**](extendedproperty.md) в коллекцию.<br/>      |
| [**Отменит**](extendedproperties-remove.md) | Удаляет объект [**ExtendedProperty**](extendedproperty.md) из коллекции.<br/> |



 

### <a name="properties"></a>Свойства

Объект **расширенных свойств** имеет следующие свойства.



| Свойство                                                   | Тип доступа          | Описание                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Только для чтения<br/> | Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).<br/> |
| [**Расчета**](extendedproperties-count.md)<br/>       | Только для чтения<br/> | Возвращает число объектов [**ExtendedProperty**](extendedproperty.md) в коллекции.<br/>                                                                                                                      |
| [**Элемент**](extendedproperties-item.md)<br/>         | Только для чтения<br/> | Извлекает объект [**ExtendedProperty**](extendedproperty.md) , представляющий индексированное расширенное свойство коллекции. Это свойство по умолчанию.<br/>                                                      |



 

## <a name="remarks"></a>Комментарии

Не удается создать объект **расширенных свойств** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
