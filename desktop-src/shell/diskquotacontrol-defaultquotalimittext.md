---
description: Возвращает предельную квоту по умолчанию в виде текстовой строки.
title: Дисккуотаконтрол. Дефаулткуоталимиттекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 442e9094c62f22c3d990cf1112d145a1b2838e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143939"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>Дисккуотаконтрол. Дефаулткуоталимиттекст, свойство

Возвращает предельную квоту по умолчанию в виде текстовой строки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Значение свойства

Строковое значение, содержащее ограничение квоты по умолчанию для новых пользователей тома. Например, если квота по умолчанию — 10,5 МБ, значение свойства равно "10,5 МБ". Если у тома нет квоты по умолчанию, свойство имеет значение "без ограничений" или локализованный эквивалент.

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

[**дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




