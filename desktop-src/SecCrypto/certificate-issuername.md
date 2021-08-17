---
description: Извлекает строку, содержащую имя издателя сертификата.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Свойство Certificate. IssuerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f4404a105748a79ef942f37c088a5436fc3eeea0784bb6ff814dd0782262dcf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771587"
---
# <a name="certificateissuername-property"></a>Свойство Certificate. IssuerName

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **IssuerName** извлекает строку, содержащую имя издателя сертификата.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a>Значение свойства

Строка, содержащая имя издателя сертификата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
