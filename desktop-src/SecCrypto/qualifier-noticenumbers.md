---
description: Извлекает коллекцию номеров пользовательских уведомлений.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Свойство квалификатора. Нотиценумберс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f45954107dd452243985d246524fb3e1826e6361fd3d72583a27ec7a33c5960f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975811"
---
# <a name="qualifiernoticenumbers-property"></a>Свойство квалификатора. Нотиценумберс

\[Свойство **нотиценумберс** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]

Свойство **нотиценумберс** извлекает коллекцию номеров пользовательских уведомлений. Это свойство может быть пустым.

## <a name="syntax"></a>Синтаксис


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a>Значение свойства

Коллекция номеров пользовательских уведомлений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Квалификатор**](qualifier.md)
</dt> </dl>

 

 
