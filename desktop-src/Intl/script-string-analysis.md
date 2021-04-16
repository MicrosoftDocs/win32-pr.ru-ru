---
description: Определяет некоторые или все атрибуты символов, глифы, ширину аванса, позиции x и y, сопоставления символов с глифами и т. д. для строки.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651113"
---
# <a name="script_string_analysis"></a>\_анализ строки скрипта \_

Определяет некоторые или все атрибуты символов, глифы, ширину аванса, позиции x и y, сопоставления символов с глифами и т. д. для строки.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Комментарии

Это непрозрачная структура, которая выделяется динамически и извлекается с помощью [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). Он необходим и для всех остальных функций ** \* скриптстринг* _.

Так как анализ может быть большим, важно, чтобы приложение вызывало [_ *скриптстрингфри* *](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) сразу после завершения строки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Распространяемые компоненты<br/>          | Internet Explorer 5 или более поздняя версия — Windows Me/98/95<br/>                         |
| Header<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Структуры Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**скриптстрингфри**](script-string-analysis.md)
</dt> </dl>

 

 




