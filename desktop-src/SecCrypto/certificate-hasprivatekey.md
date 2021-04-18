---
description: Определяет, связан ли сертификат с закрытым ключом. Метод определяет это путем проверки наличия \_ \_ \_ свойства ID Prov сведений для ключа \_ сертификата \_ .
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'Метод ICertificate2:: HasPrivateKey'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665188"
---
# <a name="icertificate2hasprivatekey-method"></a>Метод ICertificate2:: HasPrivateKey

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **HasPrivateKey** определяет, связан ли [*сертификат*](../secgloss/c-gly.md) с [*закрытым ключом*](../secgloss/p-gly.md) . Метод определяет это путем проверки наличия \_ \_ \_ свойства ID Prov сведений для ключа \_ сертификата \_ .

## <a name="syntax"></a>Синтаксис


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PrivateKey. Open**](privatekey-open.md)
</dt> <dt>

[Криптографические объекты](cryptography-objects.md)
</dt> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
