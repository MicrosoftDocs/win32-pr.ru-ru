---
description: Представляет коллекцию объектов Extension.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Объект Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668691"
---
# <a name="extensions-object"></a>Объект Extensions

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Объект **Extensions** представляет коллекцию объектов [**Extension**](extension.md) . Каждый объект [**расширения**](extension.md) представляет одно расширение сертификата.

## <a name="when-to-use"></a>Назначение

Объект **Extensions** используется для выполнения следующих задач:

-   Получение числа расширений сертификата в коллекции.
-   Извлечение указанного объекта [**расширения**](extension.md) из коллекции.
-   Выполните итерацию по коллекции.

## <a name="members"></a>Элементы

Объект **Extensions** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **Extensions** имеет следующие свойства.



| Свойство                                           | Тип доступа          | Описание                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Только для чтения<br/> | Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).<br/> |
| [**Расчета**](extensions-count.md)<br/>       | Только для чтения<br/> | Возвращает число объектов [**расширения**](extension.md) в коллекции.<br/>                                                                                                                                    |
| [**Элемент**](extensions-item.md)<br/>         | Только для чтения<br/> | Извлекает объект [**расширения**](extension.md) , представляющий индексированное расширение сертификата коллекции. Это свойство по умолчанию.<br/>                                                               |



 

## <a name="remarks"></a>Комментарии

Объект **Extensions** возвращается методом [**Certificate. Extensions**](certificate-extensions.md) .

Не удается создать объект **Extensions** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
