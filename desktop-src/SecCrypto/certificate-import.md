---
description: Импортирует ранее закодированный сертификат из строки в объект сертификата.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'Метод ICertificate2:: Import'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1f47ebe884c8fb3a10a8ebdef89353e7549c916a7793075d0086d2f0cd2ce717
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127014"
---
# <a name="icertificate2import-method"></a>Метод ICertificate2:: Import

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **Import** импортирует ранее закодированный сертификат из строки в объект [**сертификата**](certificate.md) . При вызове этого метода происходит сброс [*состояния*](../secgloss/s-gly.md) этого объекта.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Енкодедцертификате* \[ окне\]
</dt> <dd>

Строка, содержащая закодированные данные сертификата для импорта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Криптографические объекты](cryptography-objects.md)
</dt> <dt>

[**Сертификат**](certificate.md)
</dt> </dl>

 

 
