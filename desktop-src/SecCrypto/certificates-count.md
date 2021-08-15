---
description: Возвращает количество объектов сертификата в коллекции.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Свойство Certificates. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 703b929ee4b9cbe69a0f2ff37ad7e1d0c2c0005c0aa461fc38a14baa8a8ab443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770553"
---
# <a name="certificatescount-property"></a>Свойство Certificates. Count

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Count** извлекает количество объектов [**сертификата**](certificate.md) в коллекции.

## <a name="syntax"></a>Синтаксис


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Значение свойства

Число объектов [**сертификата**](certificate.md) в коллекции. Каждый объект **сертификата** представляет один сертификат в коллекции.

## <a name="remarks"></a>Remarks

CAPICOM поддерживает только один сертификат для хранилища [*смарт-карт*](../secgloss/s-gly.md) . Даже если хранилище смарт-карт содержит более одного сертификата, это свойство будет содержать значение 1. Дополнительные сведения о хранилище смарт-карт см. в разделе **элемент \_ \_ \_ пользовательского \_ хранилища CAPICOM смарт-карты** перечисление [**\_ \_ расположения CAPICOM Store**](capicom-store-location.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сертификаты**](certificates.md)
</dt> </dl>

 

 
