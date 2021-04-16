---
description: Получает логическое значение, указывающее, имеется ли расширение Кэйусаже.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Кэйусаже. Present, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665029"
---
# <a name="keyusageispresent-property"></a>Кэйусаже. Present, свойство

\[Свойство **Present** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Present** получает логическое значение, указывающее, имеется ли расширение [**кэйусаже**](keyusage.md) .

Это свойство является свойством по умолчанию объекта [**кэйусаже**](keyusage.md) .

## <a name="syntax"></a>Синтаксис


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Значение свойства

Если задано **значение true**, используется расширение кэйусаже.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кэйусаже**](keyusage.md)
</dt> </dl>

 

 
