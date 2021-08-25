---
description: Задает или возвращает пороговое значение квоты по умолчанию.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Дисккуотаконтрол. Дефаулткуотасрешолд, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 46d44f2e2df24c5ee1cbf646643810e09d007eb15ba6c9a352eb492dfb104752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943114"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>Дисккуотаконтрол. Дефаулткуотасрешолд, свойство

Задает или возвращает пороговое значение квоты по умолчанию.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Значение свойства

**Целочисленное** значение, заданное по умолчанию для порога предупреждения для новых пользователей в байтах.

## <a name="remarks"></a>Remarks

Пороговое значение квоты по умолчанию применяется автоматически к новым пользователям тома. Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий. Например, если пороговое значение по умолчанию — 10,0 МБ, значение свойства равно "10,0 МБ". Если для тома не задано пороговое значение по умолчанию, свойство имеет значение "без ограничений" или локализованный эквивалент.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




