---
description: Задает или получает содержимое открытого текста сообщения, которое будет запечатано. Это свойство по умолчанию.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Енвелопеддата. Content, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4115b55b7f9542c5a31c9abd3bcbbaec5256be4283675becac2f011ec76c8cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766075"
---
# <a name="envelopeddatacontent-property"></a>Енвелопеддата. Content, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **Content** задает или получает содержимое открытого текста сообщения, которое должно быть запечатано. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Значение свойства

Содержимое открытого текста сообщения, которое должно быть запечатано.

## <a name="remarks"></a>Remarks

Задание этого свойства должно выполняться до вызова метода [**Encrypt**](envelopeddata-encrypt.md) . Если значение этого свойства сбрасывается прямо или косвенно, все [*состояние*](../secgloss/s-gly.md) объекта сбрасывается, а все зашифрованное содержимое объекта теряется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**енвелопеддата**](envelopeddata.md)
</dt> </dl>

 

 
