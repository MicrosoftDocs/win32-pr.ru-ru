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
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648716"
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

## <a name="remarks"></a>Комментарии

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

 

 
