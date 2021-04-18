---
description: Извлекает коллекцию квалификаторов политики.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: Свойство Полициинформатион. квалификаторы (iAds. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685140"
---
# <a name="policyinformationqualifiers-property"></a>Полициинформатион. квалификаторы, свойство

\[Свойство **Квалификаторы** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки сведений о политике в расширении политик сертификатов.\]

Свойство **Квалификаторы** получает коллекцию квалификаторов политики.

## <a name="syntax"></a>Синтаксис


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a>Значение свойства

В качестве [**квалификатора**](qualifiers.md) объекта можно увидеть указатель на политику сертификации (или квалификаторы уведомления пользователя).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| Header<br/>          | <dl> <dt>IAds. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**полициинформатион**](policyinformation.md)
</dt> </dl>

 

 
