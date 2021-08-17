---
description: Возвращает объект EKU, используемый для построения объекта цепочки.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Цертификатестатус. EKU, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 63ddc2cd793c786cff1f7c5bb983cdba525fb52f940723f826ab4b44b89bf1ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770297"
---
# <a name="certificatestatuseku-method"></a>Цертификатестатус. EKU, метод

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **EKU** возвращает объект [**EKU**](eku.md) , используемый для построения объекта [**цепочки**](chain.md) .

## <a name="syntax"></a>Синтаксис


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект [**EKU**](eku.md) , который указывает на параметр расширенного использования ключа [*сертификата*](../secgloss/c-gly.md). Параметр EKU устанавливает допустимое использование сертификата. Для каждого сертификата можно задать только один объект **EKU** .

## <a name="remarks"></a>Remarks

Метод [**цертификатестатус. аппликатионполиЦиес**](certificatestatus-applicationpolicies.md) предоставляет те же функциональные возможности, что и этот метод, но позволяет задавать множество параметров вместо одного. Если коллекция [**OID**](oids.md) , возвращенная методом **аппликатионполиЦиес** , содержит один или несколько объектов [**OID**](oid.md) , то объект [**EKU**](eku.md) , возвращаемый этим методом, игнорируется. Вместо этого метода используйте метод **аппликатионполиЦиес** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**цертификатестатус**](certificatestatus.md)
</dt> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
