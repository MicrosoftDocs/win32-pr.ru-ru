---
description: Возвращает начальную дату срока действия сертификата.
ms.assetid: d1caa7d3-ed5c-4637-bcb6-5a3fda8b978e
title: Свойство Certificate. Валидфромдате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidFromDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fae36cc51463d94021196139a09e9d410c68bf5af5aa5d29cc26ac263f82addc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771080"
---
# <a name="certificatevalidfromdate-property"></a>Свойство Certificate. Валидфромдате

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **валидфромдате** извлекает дату начала срока действия сертификата.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.ValidFromDate As Date
```



## <a name="property-value"></a>Значение свойства

Дата, указывающая начальную дату срока действия сертификата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сертификат**](certificate.md)
</dt> </dl>

 

 
