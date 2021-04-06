---
title: Сообщение TVM_SETTEXTCOLOR (Коммктрл. h)
description: Задает цвет текста элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Сеттекстколор TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Элементы управления Windows для TVM_SETTEXTCOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802650"
---
# <a name="tvm_settextcolor-message"></a>\_Сообщение TVM сеттекстколор

Задает цвет текста элемента управления. Это сообщение можно отправить явно или с помощью макроса [**\_ сеттекстколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение [**COLORREF**](/windows/desktop/gdi/colorref) , содержащее новый цвет текста. Если этот аргумент равен-1, элемент управления вернется к использованию системного цвета для цвета текста.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **COLORREF** , представляющее предыдущий цвет текста. Если это значение равно-1, элемент управления использует системный цвет для цвета текста.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TVM \_ жеттекстколор**](tvm-gettextcolor.md)
</dt> </dl>

 

