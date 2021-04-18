---
description: Объект PublicKey представляет открытый ключ в объекте сертификата.
title: Объект PublicKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649099"
---
# <a name="publickey-object"></a>Объект PublicKey

\[Объект **PublicKey** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**свойство X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Объект **PublicKey** представляет открытый ключ в объекте [**сертификата**](certificate.md) .

## <a name="when-to-use"></a>Назначение

Объект **PublicKey** используется для получения данных об открытом ключе.

## <a name="members"></a>Элементы

Объект **PublicKey** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **PublicKey** имеет следующие свойства.



| Свойство                                                            | Тип доступа          | Описание                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Алгоритм**](publickey-algorithm.md)<br/>                 | Только для чтения<br/> | Извлекает объект [**OID**](oid.md) , определяющий алгоритм, используемый открытым ключом. Это свойство по умолчанию.<br/> |
| [**енкодедкэй**](publickey-encodedkey.md)<br/>               | Только для чтения<br/> | Извлекает объект [**енкодеддата**](encodeddata.md) , который предоставляет доступ к значению открытого ключа.<br/>                 |
| [**енкодедпараметерс**](publickey-encodedparameters.md)<br/> | Только для чтения<br/> | Извлекает объект [**енкодеддата**](encodeddata.md) , предоставляющий доступ к параметрам алгоритма открытого ключа.<br/>  |
| [**Длина**](publickey-length.md)<br/>                       | Только для чтения<br/> | Возвращает длину открытого ключа в битах.<br/>                                                                             |



 

## <a name="remarks"></a>Комментарии

Не удается создать объект **PublicKey** .

Объект **PublicKey** используется методом [**Certificate. publickey**](certificate-publickey.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
