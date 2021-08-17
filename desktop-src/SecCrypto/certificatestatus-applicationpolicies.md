---
description: Возвращает коллекцию OID, которая представляет политики приложения, используемые для создания объекта цепочки.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Цертификатестатус. АппликатионполиЦиес, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a27bc08f658e317b41380b2dabd9aadc13e8b50bd4985c0fd13211fa81fd507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770445"
---
# <a name="certificatestatusapplicationpolicies-method"></a>Цертификатестатус. АппликатионполиЦиес, метод

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **аппликатионполиЦиес** Возвращает коллекцию [**OID**](oids.md) , которая представляет политики приложения, используемые для создания объекта [**цепочки**](chain.md) .

## <a name="syntax"></a>Синтаксис


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Коллекция [**OID**](oids.md) . Каждый объект [**OID**](oid.md) в коллекции представляет OID политики приложения.

## <a name="remarks"></a>Remarks

Добавьте идентификаторы объектов политики приложений в коллекцию, чтобы указать политики приложений, которые должны использоваться для создания цепочки доверия сертификатов. Если коллекция содержит по крайней мере один объект [**OID**](oid.md) , то объект [**EKU**](eku.md) , возвращенный методом [**цертификатестатус. EKU**](certificatestatus-eku.md) , игнорируется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
