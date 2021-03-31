---
title: Сообщение TB_GETCOLORSCHEME (Коммктрл. h)
description: Извлекает сведения о цветовой схеме из элемента управления ToolBar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- Элементы управления Windows для TB_GETCOLORSCHEME сообщений
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
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490998"
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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СЕТКОЛОРСЧЕМЕ ТБ**](tb-setcolorscheme.md)
</dt> </dl>

 

 





