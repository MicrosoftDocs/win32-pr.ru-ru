---
description: Представляет коллекцию объектов Extension.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Объект Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e484de5b4266c5a2458d15365d44a3461a7d1d0589e22391b1afd66e437e02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006842"
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

### <a name="properties"></a>Элемент Property

Объект **Extensions** имеет следующие свойства.



| Свойство                                           | Тип доступа          | Описание                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Только для чтения<br/> | Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции. это свойство скрыто в Visual Basic scripting Edition (VBScript).<br/> |
| [**Count**](extensions-count.md)<br/>       | Только для чтения<br/> | Возвращает число объектов [**расширения**](extension.md) в коллекции.<br/>                                                                                                                                    |
| [**Компонент**](extensions-item.md)<br/>         | Только для чтения<br/> | Извлекает объект [**расширения**](extension.md) , представляющий индексированное расширение сертификата коллекции. Это свойство по умолчанию.<br/>                                                               |



 

## <a name="remarks"></a>Remarks

Объект **Extensions** возвращается методом [**Certificate. Extensions**](certificate-extensions.md) .

Не удается создать объект **Extensions** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
