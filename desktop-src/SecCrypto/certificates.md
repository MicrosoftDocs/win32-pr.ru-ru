---
description: Certificates-объект — представляет коллекцию объектов сертификата.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Объект Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8efb9221f39b8544eabe8f6c00d21f6cfdf20c14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098392"
---
# <a name="certificates-object"></a>Объект Certificates

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Объект **Certificates** представляет коллекцию объектов [**Certificate**](certificate.md) . Каждый объект [**сертификата**](certificate.md) представляет один [*цифровой сертификат*](../secgloss/d-gly.md).

Объект **Certificates** предоставляет следующие интерфейсы:

-   **ICertificates2**: представлено в CAPICOM 2,0.
-   **Ицертификатес**: представлено в CAPICOM 1,0.

## <a name="when-to-use"></a>Назначение

Объект **Certificates** используется для выполнения следующих задач:

-   Добавление или удаление объекта [**сертификата**](certificate.md) в коллекции или из нее.
-   Создание подмножества коллекции путем поиска набора сертификатов или отображения диалогового окна для выбора сертификатов.
-   Очистить все объекты [**сертификата**](certificate.md) из коллекции.
-   Получение числа сертификатов в коллекции.
-   Получение конкретного объекта [**сертификата**](certificate.md) из коллекции.
-   Выполните итерацию по коллекции.

## <a name="members"></a>Элементы

Объект **Certificates** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **Certificates** содержит следующие методы.



| Метод                                | Описание                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Включить**](certificates-add.md)       | Добавляет объект [**сертификата**](certificate.md) в коллекцию.<br/> (Наследуется от **CertificatesICertificates2**)                                        |
| [**Очистить**](certificates-clear.md)   | Удаляет все объекты [**сертификата**](certificate.md) из коллекции.<br/> (Наследуется от **CertificatesICertificates2**)                                |
| [**Поиск**](certificates-find.md)     | Возвращает объект **Certificates** , который содержит все сертификаты, соответствующие указанным условиям поиска.<br/> (Наследуется от **CertificatesICertificates2**) |
| [**Удалить**](certificates-remove.md) | Удаляет из коллекции один объект [**сертификата**](certificate.md) .<br/> (Наследуется от **CertificatesICertificates2**)                            |
| [**Сохранить**](certificates-save.md)     | Сохраняет сертификаты в указанный файл.<br/> (Наследуется от **CertificatesICertificates2**)                                                                |
| [**Метьте**](certificates-select.md) | Отображает диалоговое окно для выбора сертификатов и возвращает коллекцию выбранных сертификатов.<br/> (Наследуется от **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Свойства

Объект **Certificates** имеет следующие свойства.



| Свойство                                             | Тип доступа          | Описание                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Только для чтения<br/> | Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).<br/> |
| [**Расчета**](certificates-count.md)<br/>       | Только для чтения<br/> | Возвращает количество объектов [**сертификата**](certificate.md) в коллекции.<br/>                                                                                                                                |
| [**Элемент**](certificates-item.md)<br/>         | Только для чтения<br/> | Извлекает объект [**сертификата**](certificate.md) , представляющий индексированный сертификат коллекции. Это свойство по умолчанию.<br/> (Наследуется от **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Remarks

Объект **Certificates** может быть создан и защищен для создания скриптов. ProgID для объекта **Certificates** — CAPICOM. Certificates. 2.

**CAPICOM 1. *x*:** ProgID для объекта **Certificates** — CAPICOM. Certificates. 1.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> </dl>

 

 
