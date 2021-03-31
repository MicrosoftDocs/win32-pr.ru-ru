---
title: Сообщение EM_GETELLIPSISSTATE (RichEdit. h)
description: Извлекает текущее состояние многоточия.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Элементы управления Windows для EM_GETELLIPSISSTATE сообщений
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490725"
---
# <a name="em_getellipsisstate-message"></a>\_Сообщение ЖЕТЕЛЛИПСИССТАТЕ EM

Извлекает текущее состояние многоточия.


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение равно TRUE, если отображается многоточие, и FALSE в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ жетеллипсисмоде**](em-getellipsismode.md)
</dt> <dt>

[**EM \_ сетеллипсисмоде**](em-setellipsismode.md)
</dt> </dl>

 

 





