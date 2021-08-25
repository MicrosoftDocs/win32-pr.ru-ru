---
title: Сообщение EM_GETSCROLLPOS (RichEdit. h)
description: Получает текущую точку прокрутки элемента управления "поле ввода".
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- элементы управления Windows сообщений EM_GETSCROLLPOS
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42bde137096ae3c13582017f91b82c1eb9100097bb76f0d1babb91fa47b52196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800034"
---
# <a name="em_getscrollpos-message"></a>\_Сообщение ЖЕТСКРОЛЛПОС EM

Получает текущую точку прокрутки элемента управления "поле ввода".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется; оно должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) . После вызова **EM \_ жетскроллпос** эти параметры содержат точку в виртуальном текстовом пространстве документа, выраженную в пикселях. Это будет точка, которая в данный момент находится в левом верхнем углу окна редактирования элемента управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение всегда возвращает значение 1.

## <a name="remarks"></a>Remarks

Значения, возвращаемые в структуре [**Point**](/previous-versions//dd162805(v=vs.85)) , представляют собой 16-разрядные значения (даже в 32-разрядных полях).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Распространяемые компоненты<br/>          | Расширенное редактирование 3,0<br/>                                                              |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ сетскроллпос**](em-setscrollpos.md)
</dt> </dl>

 

