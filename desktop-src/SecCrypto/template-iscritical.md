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
ms.openlocfilehash: c86d03d0ebefe8c5e5c553b95843fd81343578d152e8abb5a3bf16dc07138b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972105"
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



## <a name="see-also"></a>См. также

<dl> <dt>

[**Шаблон**](template.md)
</dt> </dl>

 

 
