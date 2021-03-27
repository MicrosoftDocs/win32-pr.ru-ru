---
description: Возвращает пороговое значение квоты по умолчанию в виде текстовой строки.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Дисккуотаконтрол. Дефаулткуотасрешолдтекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143936"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>Дисккуотаконтрол. Дефаулткуотасрешолдтекст, свойство

Возвращает пороговое значение квоты по умолчанию в виде текстовой строки.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>Значение свойства

Строковое значение, содержащее порог квоты по умолчанию для тома.

## <a name="remarks"></a>Примечания

Пороговое значение квоты по умолчанию применяется автоматически к новым пользователям тома. Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий. Например, если пороговое значение по умолчанию — 10,0 МБ, значение свойства равно "10,0 МБ". Если для тома не задано пороговое значение по умолчанию, свойство имеет значение "без ограничений" или локализованный эквивалент.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




