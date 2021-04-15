---
description: Коллекция объектов Полициинформатион.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Объект ЦертификатеполиЦиес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688814"
---
# <a name="certificatepolicies-object"></a>Объект ЦертификатеполиЦиес

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для получения политик сертификатов.\]

Объект **цертификатеполиЦиес** представляет коллекцию объектов [**полициинформатион**](policyinformation.md) . Каждый объект [**полициинформатион**](policyinformation.md) представляет одну политику сертификата.

## <a name="when-to-use"></a>Назначение

Объект **цертификатеполиЦиес** используется для выполнения следующих задач:

-   Получите количество политик сертификатов в коллекции.
-   Извлечение конкретного объекта [**полициинформатион**](policyinformation.md) из коллекции.
-   Выполните итерацию по коллекции.

## <a name="members"></a>Элементы

Объект **цертификатеполиЦиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **цертификатеполиЦиес** имеет следующие свойства.



| Свойство                                                    | Тип доступа          | Описание                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Только для чтения<br/> | Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).<br/> |
| [**Расчета**](certificatepolicies-count.md)<br/>       | Только для чтения<br/> | Возвращает число объектов [**полициинформатион**](policyinformation.md) в коллекции.<br/>                                                                                                                    |
| [**Элемент**](certificatepolicies-item.md)<br/>         | Только для чтения<br/> | Извлекает объект [**полициинформатион**](policyinformation.md) , представляющий политику индексированных сертификатов коллекции. Это свойство по умолчанию.<br/>                                                    |



 

## <a name="remarks"></a>Комментарии

Не удается создать объект **цертификатеполиЦиес** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
