---
title: Сообщение EM_GETELLIPSISMODE (RichEdit. h)
description: Извлекает текущий режим с многоточием.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- элементы управления Windows сообщений EM_GETELLIPSISMODE
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6706c2b6ee75852fd0b3ee7a1a9d18b25d20d242d72068ba073d1bb025ff8ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019702"
---
# <a name="em_getellipsismode-message"></a>\_Сообщение ЖЕТЕЛЛИПСИСМОДЕ EM

Извлекает текущий режим с многоточием. Если этот параметр включен, для текста, который не умещается в окне отображения, отображается многоточие (). Многоточие используется только в том случае, если элемент управления неактивен. При активном режиме полосы прокрутки используются для отображения текста, который не умещается в окне отображения.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на DWORD, который получает одно из следующих значений.



| Значение                                                                                                                                                         | Значение                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**МНОГОТОЧИе \_ нет**</dt> </dl> | Многоточие не используется.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**конец МНОГОТОЧИя \_**</dt> </dl>    | Многоточие в конце (принудительное прерывание).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**слово МНОГОТОЧИя \_**</dt> </dl> | Многоточие в конце (разрыв слова).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если параметр wParam равен 0, а параметр lParam не равен NULL, то возвращаемое значение равно TRUE; в противном случае возвращаемое значение равно FALSE.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетеллипсисмоде**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ жетеллипсисстате**](em-getellipsisstate.md)
</dt> </dl>

 

 





