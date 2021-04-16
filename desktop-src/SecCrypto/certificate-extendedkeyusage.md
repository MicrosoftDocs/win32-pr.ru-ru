---
description: Возвращает объект Екстендедкэйусаже, указывающий допустимые варианты использования сертификата.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'Метод ICertificate2:: Екстендедкэйусаже'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668497"
---
# <a name="icertificate2extendedkeyusage-method"></a>Метод ICertificate2:: Екстендедкэйусаже

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **екстендедкэйусаже** возвращает объект [**екстендедкэйусаже**](extendedkeyusage.md) , указывающий допустимые варианты использования сертификата.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Объект [**екстендедкэйусаже**](extendedkeyusage.md) , связанный с сертификатом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Криптографические объекты](cryptography-objects.md)
</dt> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
