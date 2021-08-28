---
description: Возвращает коллекцию OID, представляющую политики сертификатов, используемые для создания объекта цепочки.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Цертификатестатус. ЦертификатеполиЦиес, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e4d6507446bf15d00d8e388699ee0c0892c8755b94913d18657634311db57ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126714"
---
# <a name="certificatestatuscertificatepolicies-method"></a>Цертификатестатус. ЦертификатеполиЦиес, метод

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **цертификатеполиЦиес** Возвращает коллекцию [**OID**](oids.md) , представляющую политики сертификатов, используемые для создания объекта [**цепочки**](chain.md) .

## <a name="syntax"></a>Синтаксис


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Коллекция [**OID**](oids.md) . Каждый объект [**OID**](oid.md) в коллекции представляет OID политики сертификата.

## <a name="remarks"></a>Remarks

Добавьте в коллекцию идентификаторы объектов политики сертификатов, чтобы указать политики сертификатов, которые должны использоваться для создания цепочки доверия сертификатов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
