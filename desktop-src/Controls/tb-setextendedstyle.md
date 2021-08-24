---
title: Сообщение TB_SETEXTENDEDSTYLE (Коммктрл. h)
description: Задает расширенные стили для элемента управления ToolBar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- элементы управления Windows сообщений TB_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 600e5904637215eeb052c85ec0203c9b86c75ed6b179be643dc9a213156b3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318884"
---
# <a name="tb_setextendedstyle-message"></a>\_Сообщение СЕТЕКСТЕНДЕДСТИЛЕ ТБ

Задает расширенные стили для элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение, указывающее новые расширенные стили. Этот параметр может быть сочетанием [расширенных стилей](toolbar-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , представляющее предыдущие расширенные стили. Это значение может быть сочетанием [расширенных стилей](toolbar-extended-styles.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТЕКСТЕНДЕДСТИЛЕ ТБ**](tb-getextendedstyle.md)
</dt> </dl>

 

 





