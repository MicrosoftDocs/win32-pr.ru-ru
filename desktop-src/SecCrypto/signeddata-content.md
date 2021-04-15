---
description: Задает или получает данные для подписи. Это свойство по умолчанию.
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: Сигнеддата. Content, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669315"
---
# <a name="signeddatacontent-property"></a>Сигнеддата. Content, свойство

\[Свойство **Content** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Content** задает или получает данные для подписи. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
SignedData.Content As String
```



## <a name="property-value"></a>Значение свойства

Данные, которые должны быть подписаны.

## <a name="remarks"></a>Комментарии

Это свойство должно быть инициализировано до вызова метода [**Sign**](signeddata-sign.md) . Когда значение этого свойства сбрасывается прямо или косвенно, все [*состояние*](../secgloss/s-gly.md) объекта сбрасывается, и все сигнатуры, связанные с объектом до изменения свойства, теряются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сигнеддата**](signeddata.md)
</dt> </dl>

 

 
