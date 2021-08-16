---
description: Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем порога назначенной квоты.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Дисккуотаконтрол. Логкуотасрешолд, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bb2a2073a791fcbb8e5bb6db83480f0fcea52b35e0380c20be730265d5bb34ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090644"
---
# <a name="diskquotacontrollogquotathreshold-property"></a>Дисккуотаконтрол. Логкуотасрешолд, свойство

Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем порога назначенной квоты.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a>Значение свойства

Это свойство имеет значение **true** , если запись журнала системных событий выполняется при превышении пользователем порога предупреждения квоты или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дефаулткуотасрешолд**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> <dt>

[**логкуоталимит**](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




