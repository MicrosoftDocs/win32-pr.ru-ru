---
title: Сообщение TB_ADDBUTTONS (Коммктрл. h)
description: Добавляет одну или несколько кнопок на панель инструментов.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- Элементы управления Windows для TB_ADDBUTTONS сообщений
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989441"
---
# <a name="tb_addbuttons-message"></a>\_Сообщение АДДБУТТОНС ТБ

Добавляет одну или несколько кнопок на панель инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Число добавляемых кнопок.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на массив структур [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , содержащих сведения о добавляемых кнопках. Число элементов в массиве должно совпадать с кнопками, заданными параметром *wParam*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Если панель инструментов была создана с помощью функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , перед отправкой **\_ аддбуттонс ТБ** необходимо отправить на панель инструментов сообщение [**\_ буттонструктсизе**](tb-buttonstructsize.md) ТБ.

Сведения о назначении точечных рисунков кнопкам панели инструментов из одного или нескольких списков изображений см. в статье [**ТБ \_ сетимажелист**](tb-setimagelist.md) .

## <a name="examples"></a>Примеры

В следующем примере кода на панель инструментов добавляются три кнопки с использованием стандартного системного точечного рисунка для кнопок просмотра. Сообщение [**\_ Аддбитмап в ТБ**](tb-addbitmap.md) возвращает индекс первого изображения кнопки в списке изображений. Отдельные образы определяются по смещению от этого значения.


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ТБ \_ АДДБУТТОНСВ** (Юникод) и **ТБ \_ аддбуттонса** (ANSI)<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Значения индекса изображения стандартной кнопки панели инструментов**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

