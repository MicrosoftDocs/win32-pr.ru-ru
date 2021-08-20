---
title: Сообщение TB_SETBUTTONSIZE (Коммктрл. h)
description: Задает размер кнопок на панели инструментов.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- элементы управления Windows сообщений TB_SETBUTTONSIZE
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b0b957ad6328515da7aee2f978870662801aa6aba81133e9e4bc22ee7d9c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167737"
---
# <a name="tb_setbuttonsize-message"></a>\_Сообщение СЕТБУТТОНСИЗЕ ТБ

Задает размер кнопок на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает ширину (в пикселях) кнопок. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает высоту кнопок в пикселях.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

**ТБ \_ СЕТБУТТОНСИЗЕ** обычно следует вызывать после добавления кнопок.

Используйте [**ТБ \_ сетбуттонвидс**](tb-setbuttonwidth.md) , чтобы задать максимальную и минимальную допустимую ширину для кнопок перед их добавлением. Чтобы задать фактический размер кнопок, используйте **\_ сетбуттонсизе ТБ** .

## <a name="examples"></a>Примеры

В следующем примере кода устанавливается ширина кнопок 80 пикселей, а высота — 30 пикселей.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

