---
title: Сообщение TVM_GETTEXTCOLOR (Коммктрл. h)
description: Извлекает текущий цвет текста элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Жеттекстколор TreeView.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- Элементы управления Windows для TVM_GETTEXTCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071367"
---
# <a name="tvm_gettextcolor-message"></a>\_Сообщение TVM жеттекстколор

Извлекает текущий цвет текста элемента управления. Это сообщение можно отправить явно или с помощью макроса [**\_ жеттекстколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**COLORREF**](/windows/desktop/gdi/colorref) , представляющее текущий цвет текста. Если это значение равно-1, то элемент управления использует системный цвет для цвета текста.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ сеттекстколор**](tvm-settextcolor.md)
</dt> </dl>

 

