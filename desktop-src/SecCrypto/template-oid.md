---
description: Извлекает объект OID, определяющий объект шаблона.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Свойство Template. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ecfc56210d5fa81f6e7623b2c471cf0df1b5f091f7dab6c797b56f6af8d2496e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897389"
---
# <a name="templateoid-property"></a>Свойство Template. OID

\[Свойство **OID** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]

Свойство **OID** извлекает объект [**OID**](oid.md) , определяющий объект [**шаблона**](template.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
Template.OID As OID
```



## <a name="property-value"></a>Значение свойства

Объект [**OID**](oid.md) , определяющий объект [**шаблона**](template.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Шаблон**](template.md)
</dt> </dl>

 

 
