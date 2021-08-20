---
title: Сообщение TB_SETPADDING (Коммктрл. h)
description: Задает заполнение для элемента управления ToolBar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- элементы управления Windows сообщений TB_SETPADDING
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
ms.openlocfilehash: da488c7aab3a6856fd1bd8db6911336eb52881da396e287937678600158d9655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078168"
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

## <a name="remarks"></a>Remarks

Значения заполнения используются для создания пустой области между границей кнопки и изображением кнопки и (или) текстом. Где и как фактически применяется внутреннее заполнение, зависит от типа кнопки и наличия изображения. Отступ по горизонтали применяется как справа, так и слева от кнопки, а вертикальное заполнение применяется как к верхней, так и к нижней части кнопки. Заполнение применяется только к кнопкам, имеющим стиль [**\_ AUTOSIZE тбстиле**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_отбивка по ТБ**](tb-getpadding.md)
</dt> </dl>

 

