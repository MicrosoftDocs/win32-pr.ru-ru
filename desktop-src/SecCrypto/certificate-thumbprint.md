---
description: Извлекает шестнадцатеричную строку, содержащую хэш SHA-1 сертификата.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Свойство Certificate. Thumbprint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 64748f3eb8b9623ea7c07a7428f29b30276c34ab38631fdbf210b25b5be92a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878164"
---
# <a name="certificatethumbprint-property"></a>Свойство Certificate. Thumbprint

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Thumbprint** извлекает шестнадцатеричную строку, содержащую хэш [*SHA-1*](../secgloss/s-gly.md) сертификата.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a>Значение свойства

Шестнадцатеричная строка, содержащая хэш SHA-1 сертификата.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сертификат**](certificate.md)
</dt> </dl>

 

 
