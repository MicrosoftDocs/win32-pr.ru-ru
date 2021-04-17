---
description: Свойство Algorithm извлекает объект OID, определяющий алгоритм, используемый открытым ключом. Это свойство по умолчанию.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: Свойство PublicKey. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668724"
---
# <a name="publickeyalgorithm-property"></a>Свойство PublicKey. Algorithm

\[Свойство **Algorithm** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**свойство X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Algorithm** извлекает объект [**OID**](oid.md) , определяющий алгоритм, используемый открытым ключом. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>Значение свойства

Объект [**OID**](oid.md) , определяющий алгоритм, используемый открытым ключом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
