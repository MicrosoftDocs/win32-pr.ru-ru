---
description: Извлекает коллекцию сертификатов, связанную с объектом Сигнеддата. После извлечения можно перечислить отдельные объекты сертификата в коллекции.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Сигнеддата. Certificates, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2dc04092ad6deb46249dd1155f01bac500ef240ef328ef100dc622e9b62e5835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973975"
---
# <a name="signeddatacertificates-property"></a>Сигнеддата. Certificates, свойство

\[Свойство **Certificates** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Certificates** извлекает коллекцию [**сертификатов**](certificates.md) , связанную с объектом [**сигнеддата**](signeddata.md) . После извлечения можно перечислить отдельные объекты [**сертификата**](certificate.md) в коллекции.

## <a name="syntax"></a>Синтаксис


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>Значение свойства

Коллекция [**сертификатов**](certificates.md) , связанная с объектом [**сигнеддата**](signeddata.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сигнеддата**](signeddata.md)
</dt> </dl>

 

 
