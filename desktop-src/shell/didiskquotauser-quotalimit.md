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
ms.openlocfilehash: b1971871bdeb18e3c7dd4c7978152bbec276fa8b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841635"
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

## <a name="requirements"></a>Requirements (Требования)



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

 

 




