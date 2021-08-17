---
description: Определяет некоторые или все атрибуты символов, глифы, ширину аванса, позиции x и y, сопоставления символов с глифами и т. д. для строки.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9481c641f182015d7a318c21c490f45fcc934e0df1baa52483707628eb4daa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390303"
---
# <a name="script_string_analysis"></a>\_анализ строки скрипта \_

Определяет некоторые или все атрибуты символов, глифы, ширину аванса, позиции x и y, сопоставления символов с глифами и т. д. для строки.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Remarks

Это непрозрачная структура, которая выделяется динамически и извлекается с помощью [**скриптстринганалисе**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). Он необходим и для всех остальных **функций \* скриптстринг** .

Так как анализ может быть большим, важно, чтобы приложение вызывало [**скриптстрингфри**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) , как только оно завершится строкой.

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

 

 




