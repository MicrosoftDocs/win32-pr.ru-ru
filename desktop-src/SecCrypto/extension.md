---
description: Представляет одно расширение сертификата.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Объект расширения (Ммкобж. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685328"
---
# <a name="extension-object"></a>Объект расширения

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Объект **расширения** представляет одно расширение сертификата.

## <a name="when-to-use"></a>Назначение

Объект **расширения** используется для выполнения следующих задач:

-   Получите идентификатор объекта для расширения сертификата.
-   Получите данные о расширении сертификата, представленные объектом [**енкодеддата**](encodeddata.md) .
-   Определите, помечено ли расширение сертификата как критическое.

## <a name="members"></a>Элементы

Объект **расширения** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **расширения** имеет следующие свойства.



| Свойство                                                | Тип доступа          | Описание                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**енкодеддата**](extension-encodeddata.md)<br/> | Только для чтения<br/> | Извлекает закодированные данные для расширения.<br/>                                      |
| [**Критическое**](extension-iscritical.md)<br/>   | Только для чтения<br/> | Получает логическое значение, указывающее, помечено ли расширение как критическое.<br/> |
| [**КОДА**](extension-oid.md)<br/>                 | Только для чтения<br/> | Возвращает идентификатор объекта для расширения. Это свойство по умолчанию.<br/>   |



 

## <a name="remarks"></a>Комментарии

Не удается создать объект **расширения** .

Объект **расширения** используется объектом коллекции [**Extensions**](extensions.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| Header<br/>                | <dl> <dt>Ммкобж. h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
