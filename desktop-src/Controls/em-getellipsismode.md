---
title: Сообщение EM_GETELLIPSISMODE (RichEdit. h)
description: Извлекает текущий режим с многоточием.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- Элементы управления Windows для EM_GETELLIPSISMODE сообщений
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
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135970"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сетеллипсисмоде**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ жетеллипсисстате**](em-getellipsisstate.md)
</dt> </dl>

 

 





