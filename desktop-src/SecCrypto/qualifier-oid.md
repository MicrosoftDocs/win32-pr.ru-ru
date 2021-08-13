---
description: Возвращает идентификатор объекта квалификатора.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Свойство квалификатора. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42c2f83d4fa8be31991a98b6fe4cfc6a741e2190cd12d54bfd5e968951472bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901054"
---
# <a name="qualifieroid-property"></a>Свойство квалификатора. OID

\[Свойство **OID** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]

Свойство **OID** получает идентификатор объекта квалификатора. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a>Значение свойства

Объект [**OID**](oid.md) , определяющий квалификатор.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Квалификатор**](qualifier.md)
</dt> </dl>

 

 
