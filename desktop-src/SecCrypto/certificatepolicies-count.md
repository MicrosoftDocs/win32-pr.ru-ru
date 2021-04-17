---
description: Возвращает число объектов Полициинформатион в коллекции.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: ЦертификатеполиЦиес. Count, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689426"
---
# <a name="certificatepoliciescount-property"></a>ЦертификатеполиЦиес. Count, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для получения политик сертификатов.\]

Свойство **Count** извлекает количество объектов [**полициинформатион**](policyinformation.md) в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Значение свойства

Число объектов [**полициинформатион**](policyinformation.md) в коллекции. Каждый объект **полициинформатион** представляет одну политику сертификата в коллекции.

## <a name="remarks"></a>Комментарии

Свойство **Count** можно использовать для указания последнего объекта [**полициинформатион**](policyinformation.md) в коллекции при извлечении определенного объекта **полициинформатион** с помощью свойства [**цертификатеполиЦиес. Item**](certificatepolicies-item.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
