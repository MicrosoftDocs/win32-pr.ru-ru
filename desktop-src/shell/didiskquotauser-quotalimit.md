---
description: Задает или возвращает текущую квоту пользователя.
title: Дидисккуотаусер. QuotaLimit, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984272"
---
# <a name="didiskquotauserquotalimit-property"></a>Дидисккуотаусер. QuotaLimit, свойство

Задает или возвращает текущую [**квоту**](diskquotacontrol-object.md)пользователя.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a>Значение свойства

**Целочисленное** значение, которое указывает или получает текущее ограничение квоты пользователя в байтах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дефаулткуоталимит**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**дидисккуотаусер**](didiskquotauser-object.md)
</dt> <dt>

[**куоталимиттекст**](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




