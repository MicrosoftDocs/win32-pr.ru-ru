---
description: Получает значение открытого ключа.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: Свойство PublicKey. Енкодедкэй
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689356"
---
# <a name="publickeyencodedkey-property"></a>Свойство PublicKey. Енкодедкэй

\[Свойство **енкодедкэй** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**свойство X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **енкодедкэй** извлекает значение открытого ключа.

## <a name="syntax"></a>Синтаксис


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a>Значение свойства

Объект [**енкодеддата**](encodeddata.md) , предоставляющий доступ к значению открытого ключа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
