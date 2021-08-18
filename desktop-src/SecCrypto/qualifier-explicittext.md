---
description: Извлекает содержимое уведомления пользователя.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Свойство квалификатора. ЕксплиЦиттекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 60753e0e7fa9996f9584070d6fac2d12d3a483b681fa61b72cf2e59cc2898995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901115"
---
# <a name="qualifierexplicittext-property"></a>Свойство квалификатора. ЕксплиЦиттекст

\[Свойство **експлиЦиттекст** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]

Свойство **експлиЦиттекст** извлекает содержимое уведомления пользователя. Это свойство может быть пустым.

## <a name="syntax"></a>Синтаксис


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a>Значение свойства

Содержимое уведомления пользователя.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Квалификатор**](qualifier.md)
</dt> </dl>

 

 
