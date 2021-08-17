---
description: Задает или получает продолжительность времени до того, как URL-адрес будет определен как недоступный.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Цертификатестатус. Урлретриевалтимеаут, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b56e9bca2cc7c666f980df8905ac79fc885050d37359e524a83e287dcd5415e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770094"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>Цертификатестатус. Урлретриевалтимеаут, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **урлретриевалтимеаут** задает или получает продолжительность времени до того, как URL-адрес будет определен как недоступный.

## <a name="syntax"></a>Синтаксис


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>Значение свойства

Число секунд, по истечении которого URL-адрес будет недоступен.

## <a name="remarks"></a>Remarks

Если это свойство не задано, время ожидания по умолчанию — 15 секунд.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
