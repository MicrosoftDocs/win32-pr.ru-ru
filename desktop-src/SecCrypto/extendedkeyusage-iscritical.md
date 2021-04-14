---
description: Возвращает логическое значение, указывающее, помечено ли расширение EKU как критическое.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: Свойство Екстендедкэйусаже. Critical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648127"
---
# <a name="extendedkeyusageiscritical-property"></a>Свойство Екстендедкэйусаже. Critical

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство « **Critical** » возвращает логическое значение, указывающее, помечено ли расширение EKU как критическое.

## <a name="syntax"></a>Синтаксис


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a>Значение свойства

Если **значение — true**, расширение EKU помечено как критическое.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**екстендедкэйусаже**](extendedkeyusage.md)
</dt> </dl>

 

 
