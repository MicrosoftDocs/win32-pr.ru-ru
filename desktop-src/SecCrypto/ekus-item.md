---
description: Извлекает объект EKU, представляющий свойство расширенного использования ключа (EKU).
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'Свойство Иекус:: Item'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b81e00de0ca8346d56ceafeb8b0d11353219c5fc6ab3eb0b29a9f7c868f79505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875154"
---
# <a name="iekusitem-property"></a>Свойство Иекус:: Item

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **Item** извлекает объект [**EKU**](eku.md) , представляющий свойство расширенного использования ключа (EKU).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Значение свойства

Объект [**EKU**](eku.md) , представляющий свойство с индексированным расширенным использованием ключа (EKU).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EKU**](ekus.md)
</dt> </dl>

 

 
