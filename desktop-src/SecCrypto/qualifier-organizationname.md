---
description: Возвращает имя Организации, связанной с квалификатором.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Свойство квалификатора. название_организации
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f082a821779cc6e2182e88cf9742c87de0417e7ac297fda2f799ca5878d4ce67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975774"
---
# <a name="qualifierorganizationname-property"></a>Свойство квалификатора. название_организации

\[Свойство **название_организации** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]

Свойство **название_организации** извлекает имя Организации, связанной с квалификатором. Это свойство может быть пустым.

## <a name="syntax"></a>Синтаксис


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a>Значение свойства

Имя Организации, связанной с квалификатором.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Квалификатор**](qualifier.md)
</dt> </dl>

 

 
