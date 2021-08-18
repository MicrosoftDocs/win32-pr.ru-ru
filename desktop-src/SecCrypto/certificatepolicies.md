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
ms.openlocfilehash: 8da0ad9681f3dd87227a7fe0b5a5419ceac4c7ee354fb1548427c100561e816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770843"
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

### <a name="properties"></a>Элемент Property

Объект **цертификатеполиЦиес** имеет следующие свойства.



| Свойство                                                    | Тип доступа          | Описание                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificatepolicies-newenum.md)<br/> | Только для чтения<br/> | Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции. это свойство скрыто в Visual Basic scripting Edition (VBScript).<br/> |
| [**Count**](certificatepolicies-count.md)<br/>       | Только для чтения<br/> | Возвращает число объектов [**полициинформатион**](policyinformation.md) в коллекции.<br/>                                                                                                                    |
| [**Компонент**](certificatepolicies-item.md)<br/>         | Только для чтения<br/> | Извлекает объект [**полициинформатион**](policyinformation.md) , представляющий политику индексированных сертификатов коллекции. Это свойство по умолчанию.<br/>                                                    |



 

## <a name="remarks"></a>Remarks

Не удается создать объект **цертификатеполиЦиес** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
