---
description: Задает или получает объект сертификата, представляющий сертификат для подписи данных.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Свойство SignIn. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685090"
---
# <a name="signercertificate-property"></a>Свойство SignIn. Certificate

\[Свойство **Certificate** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Certificate** задает или получает объект [**сертификата**](certificate.md) , представляющий сертификат для подписи данных. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a>Значение свойства

Объект [**сертификата**](certificate.md) , представляющий сертификат подписи данных.

## <a name="remarks"></a>Комментарии

Когда значение этого свойства сбрасывается прямо или косвенно, полное [*состояние*](../secgloss/s-gly.md) объекта сбрасывается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Автор подписи**](signer.md)
</dt> </dl>

 

 
