---
description: Возвращает идентификатор объекта политики. Это свойство по умолчанию.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Полициинформатион. OID, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbe0bba2775f236aa8aa9bce668f7c63f07220616bc03bc05fddfbf18e72ed5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978720"
---
# <a name="policyinformationoid-property"></a>Полициинформатион. OID, свойство

\[Свойство **OID** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки сведений о политике в расширении политик сертификатов.\]

Свойство **OID** получает идентификатор объекта политики. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a>Значение свойства

Идентификатор объекта политики в виде объекта [**OID**](oid.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**полициинформатион**](policyinformation.md)
</dt> </dl>

 

 
