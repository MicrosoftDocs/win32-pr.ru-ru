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
ms.openlocfilehash: d2eb962445717743512de396065304f70c31f02cfa4f3448a08a2731ed1fd377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992864"
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

 

 
