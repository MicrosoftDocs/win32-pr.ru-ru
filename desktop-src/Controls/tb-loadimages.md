---
title: Сообщение TB_LOADIMAGES (Коммктрл. h)
description: Загружает определенные системой изображения кнопок в список изображений элемента управления ToolBar.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- Элементы управления Windows для TB_LOADIMAGES сообщений
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491982"
---
# <a name="tb_loadimages-message"></a>\_Сообщение ЛОАДИМАЖЕС ТБ

Загружает определенные системой изображения кнопок в список изображений элемента управления ToolBar.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор определяемого системой списка изображений для кнопки. Этому параметру можно присвоить одно из следующих значений.



| Значение                                                                                                                                                                                | Значение                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**IDB \_ хист, \_ крупный \_ Цвет**</dt> </dl> | Точечные рисунки проводника имеют большой размер.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**IDB \_ хист \_ мелкий \_ Цвет**</dt> </dl> | Точечные рисунки проводника Windows небольшого размера.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**нестандартные IDB — \_ \_ крупный \_ Цвет**</dt> </dl>    | Стандартные точечные рисунки имеют большой размер.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**неплашечный IDB по \_ \_ небольшому \_ цвету**</dt> </dl>    | Стандартные точечные рисунки небольшого размера.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**\_ \_ крупный цвет представления \_ IDB**</dt> </dl> | Просмотр точечных рисунков в большом размере.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**\_ \_ малый цвет представления \_ IDB**</dt> </dl> | Просмотр точечных рисунков в небольшом размере.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**IDB \_ хист, \_ Обычная**</dt> </dl>                 | Проводник Windows кнопки перемещения и избранные рисунки в нормальном состоянии.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**IDB \_ хист \_ Hot**</dt> </dl>                          | Кнопки перемещения в проводнике Windows и избранные рисунки в активном состоянии.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**IDB \_ хист \_ отключена**</dt> </dl>           | Кнопки перемещения в проводнике Windows и избранные рисунки в отключенном состоянии.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**\_ХИСТ IDB \_**</dt> </dl>              | Кнопки перемещения в проводнике Windows и избранные растровые изображения в нажатом состоянии.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер экземпляра. Этот параметр должен иметь значение ХИНСТ \_ коммктрл.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Число изображений в списке изображений. Возвращает нуль, если на панели инструментов нет списка изображений или если существующий список изображений пуст.

## <a name="remarks"></a>Комментарии

При подготовке структур [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) перед отправкой сообщения [**\_ аддбуттонс ТБ**](tb-addbuttons.md) необходимо использовать правильные значения индекса образа. Список значений индекса изображений для этих предустановленных точечных рисунков см. в разделе [значения индекса изображения стандартной кнопки панели инструментов](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Примеры

В следующем примере кода загружаются системные изображения с мелкими цветами.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_АДДБИТМАП ТБ**](tb-addbitmap.md)
</dt> </dl>

 

 





