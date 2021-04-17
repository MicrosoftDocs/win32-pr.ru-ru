---
description: Задает или получает коллекцию сертификатов, которые можно использовать для построения цепочки сертификатов.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Цертификатестатус. Certificates, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665355"
---
# <a name="certificatestatuscertificates-property"></a>Цертификатестатус. Certificates, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Certificates** задает или получает коллекцию сертификатов, которые могут использоваться для построения цепочки сертификатов.

## <a name="syntax"></a>Синтаксис


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a>Значение свойства

Объект [**Certificates**](certificates.md) , представляющий коллекцию сертификатов, которые могут использоваться для создания цепочки сертификатов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
