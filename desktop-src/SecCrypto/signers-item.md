---
description: Извлекает объект подписавший, представляющий индексированный подписывающий.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Свойство Signs. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33630586282b745da94a442c13a0e85574c5f2e06fc04ab909e4ebf59fc2707b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898411"
---
# <a name="signersitem-property"></a>Свойство Signs. Item

\[Свойство **Item** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте коллекцию объектов Кмссигнер. Дополнительные сведения см. в описании [**класса кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Item** получает объект [**подписавший**](signer.md) , представляющий индексированный подписывающий. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Значение свойства

Объект [**SignIn**](signer.md) , представляющий индексированный подписывающий.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Подписавшими**](signers.md)
</dt> </dl>

 

 
