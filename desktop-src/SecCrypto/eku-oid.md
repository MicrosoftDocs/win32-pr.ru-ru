---
description: Задает или получает строку, содержащую строковое значение EKU OID, определенное в Винкрипт. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'Свойство ИЕКУ:: OID'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 49a35cb223c338573ba0a52288a1e5528820dcbd4c7589548ce31f9df46dc1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875254"
---
# <a name="iekuoid-property"></a>Свойство ИЕКУ:: OID

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **OID** задает или получает строку, содержащую строковое значение EKU OID, определенное в винкрипт. h.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
EKU.OID As String
```



## <a name="property-value"></a>Значение свойства

Строка, содержащая строковое значение EKU OID, определенное в Винкрипт. h.

## <a name="remarks"></a>Remarks

Это свойство не использует объект [**OID**](oid.md) , представленный в элементе CAPICOM 2,0.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
