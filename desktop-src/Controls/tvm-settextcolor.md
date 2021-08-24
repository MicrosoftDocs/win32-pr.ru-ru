---
title: Сообщение TVM_SETTEXTCOLOR (Коммктрл. h)
description: Задает цвет текста элемента управления. Это сообщение можно отправить явно или с помощью \_ макроса Сеттекстколор TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- элементы управления Windows сообщений TVM_SETTEXTCOLOR
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
ms.openlocfilehash: 41559abd6724ee9c8ce9f86cfcff092ad13d949a80a55d45ff996f36b284932d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503614"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**TVM \_ жеттекстколор**](tvm-gettextcolor.md)
</dt> </dl>

 

