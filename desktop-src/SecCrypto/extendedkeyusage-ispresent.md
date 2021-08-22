---
description: Возвращает логическое значение, указывающее, имеется ли расширение EKU. Это свойство по умолчанию.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: Екстендедкэйусаже. Present, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43c561e6c848380326151af12aebf584fb53eb7332c8e6c0d61074da03f7d3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007342"
---
# <a name="extendedkeyusageispresent-property"></a>Екстендедкэйусаже. Present, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Present** возвращает логическое значение, указывающее, имеется ли расширение EKU. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Значение свойства

Если задано **значение true**, расширение EKU имеется.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**екстендедкэйусаже**](extendedkeyusage.md)
</dt> </dl>

 

 
