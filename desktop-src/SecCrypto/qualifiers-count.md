---
description: Возвращает количество объектов квалификатора в коллекции.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Свойство квалификаторов. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fd4cfe0d600c99251db77b1764edb83353b01143fc5179c1efc29673e30e734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900950"
---
# <a name="qualifierscount-property"></a>Свойство квалификаторов. Count

\[Свойство **Count** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]

Свойство **Count** извлекает количество объектов [**квалификатора**](qualifier.md) в коллекции.

## <a name="syntax"></a>Синтаксис


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a>Значение свойства

Количество объектов [**квалификатора**](qualifier.md) в коллекции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Квалификаторы**](qualifiers.md)
</dt> </dl>

 

 
