---
title: Сообщение TVM_SETBKCOLOR (Коммктрл. h)
description: Задает цвет фона элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Сетбкколор TreeView.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- элементы управления Windows сообщений TVM_SETBKCOLOR
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0609a15be2b8e05b1f8ca8f4f999cd4888ee946969c25f5bc1d86420b7529f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060124"
---
# <a name="tvm_setbkcolor-message"></a>\_Сообщение TVM сетбкколор

Задает цвет фона элемента управления. Это сообщение можно отправить явно или с помощью макроса [**\_ сетбкколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее новый цвет фона. Если это значение равно-1, то элемент управления вернется к использованию системного цвета для цвета фона.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее предыдущий цвет фона. Если это значение равно-1, то элемент управления использовал системный цвет для цвета фона.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**TVM \_ жетбкколор**](tvm-getbkcolor.md)
</dt> </dl>

 

