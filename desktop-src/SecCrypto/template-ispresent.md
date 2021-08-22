---
description: Получает логическое значение, указывающее, имеется ли расширение шаблона.
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: Свойство Template. Present
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0492f6abccf2ade6e652dba2c4ea13d9bbfc28f1a3d3c34008eb3338ccb1e426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897399"
---
# <a name="templateispresent-property"></a>Свойство Template. Present

\[Свойство **Present** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]

Свойство **Present** получает логическое значение, указывающее, имеется ли расширение шаблона.

## <a name="syntax"></a>Синтаксис


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a>Значение свойства

Если **значение равно true**, имеется расширение шаблона.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Шаблон**](template.md)
</dt> </dl>

 

 
