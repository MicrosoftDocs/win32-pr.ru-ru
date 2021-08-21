---
title: Сообщение TB_LOADIMAGES (Коммктрл. h)
description: Загружает определенные системой изображения кнопок в список изображений элемента управления ToolBar.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- элементы управления Windows сообщений TB_LOADIMAGES
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
ms.openlocfilehash: df2cfae5e1658dec2652eb68cae4283dd0df697ad055434f1290cc0da7c2b485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168200"
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
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <dt>**IDB \_ хист, \_ крупный \_ Цвет**</dt> </dl> | Windows Точечные рисунки обозревателя имеют большой размер.<br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <dt>**IDB \_ хист \_ мелкий \_ Цвет**</dt> </dl> | Windows Точечные рисунки в обозревателе малого размера.<br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <dt>**нестандартные IDB — \_ \_ крупный \_ Цвет**</dt> </dl>    | Стандартные точечные рисунки имеют большой размер.<br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <dt>**неплашечный IDB по \_ \_ небольшому \_ цвету**</dt> </dl>    | Стандартные точечные рисунки небольшого размера.<br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <dt>**\_ \_ крупный цвет представления \_ IDB**</dt> </dl> | Просмотр точечных рисунков в большом размере.<br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <dt>**\_ \_ малый цвет представления \_ IDB**</dt> </dl> | Просмотр точечных рисунков в небольшом размере.<br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <dt>**IDB \_ хист, \_ Обычная**</dt> </dl>                 | Windows Explorer кнопки перемещения и растровые изображения избранного в нормальном состоянии.<br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <dt>**IDB \_ хист \_ Hot**</dt> </dl>                          | Windows Проводник кнопки перемещения и избранные рисунки в активном состоянии.<br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <dt>**IDB \_ хист \_ отключена**</dt> </dl>           | Windows Кнопки перемещения в обозревателе и растровые изображения избранного в отключенном состоянии.<br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <dt>**\_ХИСТ IDB \_**</dt> </dl>              | Windows Кнопки перемещения в обозревателе и растровые изображения избранного в состоянии "в нажатии".<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Маркер экземпляра. Этот параметр должен иметь значение ХИНСТ \_ коммктрл.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Число изображений в списке изображений. Возвращает нуль, если на панели инструментов нет списка изображений или если существующий список изображений пуст.

## <a name="remarks"></a>Remarks

При подготовке структур [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) перед отправкой сообщения [**\_ аддбуттонс ТБ**](tb-addbuttons.md) необходимо использовать правильные значения индекса образа. Список значений индекса изображений для этих предустановленных точечных рисунков см. в разделе [значения индекса изображения стандартной кнопки панели инструментов](toolbar-standard-button-image-index-values.md).

## <a name="examples"></a>Примеры

В следующем примере кода загружаются системные изображения с мелкими цветами.


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_АДДБИТМАП ТБ**](tb-addbitmap.md)
</dt> </dl>

 

 





