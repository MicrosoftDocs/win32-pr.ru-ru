---
title: Сообщение TB_SETPADDING (Коммктрл. h)
description: Задает заполнение для элемента управления ToolBar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Элементы управления Windows для TB_SETPADDING сообщений
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137279"
---
# <a name="tb_setpadding-message"></a>\_Сообщение СЕТПАДДИНГ ТБ

Задает заполнение для элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает горизонтальное заполнение в пикселях. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает вертикальное заполнение в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа DWORD** , содержащее предыдущее горизонтальное заполнение в [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) и предыдущее вертикальное заполнение в [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(в пикселях).

## <a name="remarks"></a>Комментарии

Значения заполнения используются для создания пустой области между границей кнопки и изображением кнопки и (или) текстом. Где и как фактически применяется внутреннее заполнение, зависит от типа кнопки и наличия изображения. Отступ по горизонтали применяется как справа, так и слева от кнопки, а вертикальное заполнение применяется как к верхней, так и к нижней части кнопки. Заполнение применяется только к кнопкам, имеющим стиль [**\_ AUTOSIZE тбстиле**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_отбивка по ТБ**](tb-getpadding.md)
</dt> </dl>

 

