---
description: Возвращает дату окончания срока действия сертификата.
ms.assetid: 25e76b25-9a18-439c-acb8-e0af97b6fcd5
title: Свойство Certificate. Валидтодате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidToDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08f6c0748c38ec31085c937eda37a413a3644f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688817"
---
# <a name="certificatevalidtodate-property"></a>Свойство Certificate. Валидтодате

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **валидтодате** извлекает дату окончания срока действия сертификата.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.ValidToDate As Date
```



## <a name="property-value"></a>Значение свойства

Дата, указывающая дату окончания срока действия сертификата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Certificate**](certificate.md)
</dt> </dl>

 

 
