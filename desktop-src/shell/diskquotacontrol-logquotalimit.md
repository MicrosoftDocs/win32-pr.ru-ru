---
description: Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем назначенной квоты.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Дисккуотаконтрол. Логкуоталимит, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f10710c5a16feb946caa78394d5e57e5d7d4884a50d45dc3e37291f40e7d283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455884"
---
# <a name="diskquotacontrollogquotalimit-property"></a>Дисккуотаконтрол. Логкуоталимит, свойство

Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем назначенной квоты.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Значение свойства

Это свойство имеет значение **true** , если запись в журнале системных событий выполняется при превышении пользователем предела квоты или **false** в противном случае.

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

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> <dt>

[**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




