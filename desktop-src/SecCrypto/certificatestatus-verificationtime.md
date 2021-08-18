---
description: Задает или получает время проверки сертификата.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Цертификатестатус. Верификатионтиме, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 02457355fdb9f01605470ea10e30d69caaa6149837480ebe7bd20340d7c6cae2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993154"
---
# <a name="certificatestatusverificationtime-property"></a>Цертификатестатус. Верификатионтиме, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **верификатионтиме** задает или получает время проверки сертификата.

## <a name="syntax"></a>Синтаксис


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Значение свойства

Время проверки сертификата.

## <a name="remarks"></a>Remarks

Если это свойство не задано, используется текущее время.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
