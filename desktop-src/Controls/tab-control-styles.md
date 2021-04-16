---
title: Стили элемента управления Tab (Коммктрл. h)
description: В этом разделе перечислены поддерживаемые стили элементов управления вкладки.
ms.assetid: a01a6609-b02e-4ada-afa0-ed5ad8dde0d6
topic_type:
- apiref
api_name:
- TCS_BOTTOM
- TCS_BUTTONS
- TCS_FIXEDWIDTH
- TCS_FLATBUTTONS
- TCS_FOCUSNEVER
- TCS_FOCUSONBUTTONDOWN
- TCS_FORCEICONLEFT
- TCS_FORCELABELLEFT
- TCS_HOTTRACK
- TCS_MULTILINE
- TCS_MULTISELECT
- TCS_OWNERDRAWFIXED
- TCS_RAGGEDRIGHT
- TCS_RIGHT
- TCS_RIGHTJUSTIFY
- TCS_SCROLLOPPOSITE
- TCS_SINGLELINE
- TCS_TABS
- TCS_TOOLTIPS
- TCS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352864fe71b5efc39529109bafb3bdc49cee68e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657192"
---
# <a name="tab-control-styles"></a>Стили элемента управления Tab

В этом разделе перечислены поддерживаемые стили элементов управления вкладки.



| Константа                                                                                                                                                                              | Описание                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**TCS \_ снизу**</dt> </dl>                                  | [Версия 4,70](common-control-versions.md). Вкладки отображаются в нижней части элемента управления. Это значение равно TCS \_ right. Этот стиль не поддерживается, если используется ComCtl32.dll версии 6.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**\_кнопки TCS**</dt> </dl>                               | Вкладки отображаются как кнопки, и границы вокруг области отображения не отображаются.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**TCS \_ FIXEDWIDTH**</dt> </dl>                      | Все вкладки имеют одинаковую ширину. Этот стиль нельзя сочетать с TCS \_ ригхтжустифи Style.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**TCS \_ флатбуттонс**</dt> </dl>                   | [Версия 4,71](common-control-versions.md). Выбранные вкладки отображаются с отступом в фоновом режиме, в то время как другие вкладки находятся на той же плоскости, что и фон. Этот стиль влияет только на элементы управления "Вкладка" с помощью \_ кнопки TCS.<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**TCS \_ фокусневер**</dt> </dl>                      | Элемент управления "Вкладка" не получает фокус ввода при щелчке.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**TCS \_ фокусонбуттондовн**</dt> </dl> | Элемент управления "Вкладка" получает фокус ввода при щелчке.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**TCS \_ форцеиконлефт**</dt> </dl>             | Значки вычисляются по левому краю каждой вкладки фиксированная ширина. Этот стиль можно использовать только с \_ стилем TCS FIXEDWIDTH.<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**TCS \_ форцелабеллефт**</dt> </dl>          | Метки вычисляются по левому краю каждой вкладки фиксированная ширина; то есть метка отображается сразу справа от значка, а не по центру. Этот стиль можно использовать только с \_ стилем TCS FIXEDWIDTH, и он подразумевает \_ стиль TCS форцеиконлефт.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**TCS \_ хоттракк**</dt> </dl>                            | [Версия 4,70](common-control-versions.md). Элементы под указателем автоматически выделяются. Чтобы проверить, включено ли оперативное отслеживание, вызовите [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**\_Многострочный TCS**</dt> </dl>                         | При необходимости отображается несколько строк вкладок, поэтому все вкладки отображаются одновременно.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**TCS \_**</dt> </dl>                   | [Версия 4,70](common-control-versions.md). Можно выбрать несколько вкладок, удерживая нажатой клавишу CTRL. Этот стиль следует использовать с \_ стилем кнопок TCS.<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**TCS \_ овнердравфиксед**</dt> </dl>          | Родительское окно отвечает за вкладки рисования.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**TCS \_ RAGGEDRIGHT**</dt> </dl>                   | Строки вкладок не будут растягиваться для заполнения всей ширины элемента управления. Этот стиль используется по умолчанию.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS \_ вправо**</dt> </dl>                                     | [Версия 4,70](common-control-versions.md). Вкладки отображаются вертикально справа от элементов управления, использующих \_ вертикальный стиль TCS. Это значение равно TCS \_ Bottom. Этот стиль не поддерживается, если используются визуальные стили.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**TCS \_ ригхтжустифи**</dt> </dl>                | При необходимости ширина каждой вкладки увеличивается, чтобы каждая строка вкладок заполнила всю ширину элемента управления "Вкладка". Этот стиль окна игнорируется, если \_ не задан также многострочный стиль TCS.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**TCS \_ скроллоппосите**</dt> </dl>          | [Версия 4,70](common-control-versions.md). Ненужные вкладки прокручиваются к противоположной стороне элемента управления при выборе вкладки.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**TCS \_ SINGLELINE**</dt> </dl>                      | Отображается только одна строка вкладок. При необходимости пользователь может выполнить прокрутку для просмотра дополнительных вкладок. Этот стиль используется по умолчанию.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**TCS \_ вкладки**</dt> </dl>                                        | Вкладки отображаются в виде вкладок, а граница отображается вокруг области отображения. Этот стиль используется по умолчанию.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**\_подсказки TCS**</dt> </dl>                            | С элементом управления "Вкладка" связан элемент управления ToolTip. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TCS \_ по вертикали**</dt> </dl>                            | [Версия 4,70](common-control-versions.md). В левой части элемента управления отображаются вкладки с текстом, отображаемым вертикально. Этот стиль допустим только при использовании в \_ многострочном стиле TCS. Чтобы вкладки отображались справа от элемента управления, также используйте \_ стиль TCS right. Этот стиль не поддерживается, если используется ComCtl32.dll версии 6.<br/> |



## <a name="remarks"></a>Комментарии

После создания элемента управления можно изменить следующие стили.

-   TCS \_ снизу
-   \_кнопки TCS
-   TCS \_ FIXEDWIDTH
-   TCS \_ флатбуттонс
-   TCS \_ форцеиконлефт
-   TCS \_ форцелабеллефт
-   \_Многострочный TCS
-   TCS \_ овнердравфиксед
-   TCS \_ RAGGEDRIGHT
-   TCS \_ вправо
-   TCS \_ по вертикали

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Коммктрл. h</dt> </dl> |



 

