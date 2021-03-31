---
title: Сообщение TB_SETEXTENDEDSTYLE (Коммктрл. h)
description: Задает расширенные стили для элемента управления ToolBar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Элементы управления Windows для TB_SETEXTENDEDSTYLE сообщений
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
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136806"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТЕКСТЕНДЕДСТИЛЕ ТБ**](tb-getextendedstyle.md)
</dt> </dl>

 

 





