---
title: Сообщение TB_GETCOLORSCHEME (Коммктрл. h)
description: Извлекает сведения о цветовой схеме из элемента управления ToolBar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- элементы управления Windows сообщений TB_GETCOLORSCHEME
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fca3a7a88fd108454c3838d646db311c9be19bf04163b4c8987db67f6c09c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918874"
---
# <a name="tb_getcolorscheme-message"></a>\_Сообщение ЖЕТКОЛОРСЧЕМЕ ТБ

Извлекает сведения о цветовой схеме из элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**колорсчеме**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) , которая получит сведения о цветовой схеме. Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(колорсчеме).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТКОЛОРСЧЕМЕ ТБ**](tb-setcolorscheme.md)
</dt> </dl>

 

 





