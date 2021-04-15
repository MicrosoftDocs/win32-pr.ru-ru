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
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648890"
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

 

 
