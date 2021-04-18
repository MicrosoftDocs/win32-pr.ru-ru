---
description: Получает логическое значение, указывающее, помечено ли расширение шаблона как критическое.
ms.assetid: 37e2000a-d3c8-46b5-84e5-a3904fdbaeea
title: Свойство Template. «Critical»
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66f9dc90828cd474497478872f154adbd3fcd12a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648767"
---
# <a name="templateiscritical-property"></a>Свойство Template. «Critical»

\[Свойство « **критическое** » доступно для использования в операционных системах, указанных в разделе «требования». Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для шаблона сертификата для получения шаблона расширения сертификата.\]

Свойство « **Critical** » получает логическое значение, указывающее, помечено ли расширение шаблона как критическое.

## <a name="syntax"></a>Синтаксис


```VB
Template.IsCritical As Boolean
```



## <a name="property-value"></a>Значение свойства

Если **значение равно true**, расширение шаблона помечено как критическое.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Шаблон**](template.md)
</dt> </dl>

 

 
