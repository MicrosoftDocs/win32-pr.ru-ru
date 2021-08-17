---
description: Возвращает число объектов EKU в коллекции.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: Свойство EKU. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4ef512c62058d2f4726c21aa8631fef5230ec35ecfe39a3b8dc5470fc93b74e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767168"
---
# <a name="ekuscount-property"></a>Свойство EKU. Count

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Count** извлекает количество объектов [**EKU**](eku.md) в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
EKUs.Count As Long
```



## <a name="property-value"></a>Значение свойства

Число объектов [**EKU**](eku.md) в коллекции. Каждый объект **EKU** представляет одно свойство расширенного использования ключа (EKU) сертификата.

## <a name="remarks"></a>Remarks

Свойство **Count** можно использовать для указания последнего объекта [**EKU**](eku.md) в коллекции при извлечении определенного объекта **EKU** с помощью свойства [**EKU. Item**](ekus-item.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
