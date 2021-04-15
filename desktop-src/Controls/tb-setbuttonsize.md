---
title: Сообщение TB_SETBUTTONSIZE (Коммктрл. h)
description: Задает размер кнопок на панели инструментов.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Элементы управления Windows для TB_SETBUTTONSIZE сообщений
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
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654518"
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

## <a name="remarks"></a>Комментарии

**ТБ \_ СЕТБУТТОНСИЗЕ** обычно следует вызывать после добавления кнопок.

Используйте [**ТБ \_ сетбуттонвидс**](tb-setbuttonwidth.md) , чтобы задать максимальную и минимальную допустимую ширину для кнопок перед их добавлением. Чтобы задать фактический размер кнопок, используйте **\_ сетбуттонсизе ТБ** .

## <a name="examples"></a>Примеры

В следующем примере кода устанавливается ширина кнопок 80 пикселей, а высота — 30 пикселей.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

