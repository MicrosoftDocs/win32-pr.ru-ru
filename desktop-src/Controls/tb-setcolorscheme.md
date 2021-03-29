---
title: Сообщение TB_SETCOLORSCHEME (Коммктрл. h)
description: Задает сведения о цветовой схеме для элемента управления ToolBar.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- Элементы управления Windows для TB_SETCOLORSCHEME сообщений
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892617"
---
# <a name="tb_setcolorscheme-message"></a>\_Сообщение СЕТКОЛОРСЧЕМЕ ТБ

Задает сведения о цветовой схеме для элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**колорсчеме**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) , содержащую сведения о цветовой схеме.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение для этого сообщения не используется.

## <a name="remarks"></a>Комментарии

Элемент управления ToolBar использует сведения о цветовой схеме при рисовании трехмерных элементов в элементе управления.

Если стили оформления включены, это сообщение не действует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЖЕТКОЛОРСЧЕМЕ ТБ**](tb-getcolorscheme.md)
</dt> </dl>

 

 





