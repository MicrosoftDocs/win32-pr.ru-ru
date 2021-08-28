---
title: Идентификаторы типов элементов управления (UIAutomationClient. h)
description: В этом разделе описываются именованные константы, используемые для определения типов элементов управления модели автоматизации пользовательского интерфейса Майкрософт.
ms.assetid: 774b6078-2491-48e4-8ac3-f14dd60de862
topic_type:
- apiref
api_name:
- UIA_AppBarControlTypeId
- UIA_ButtonControlTypeId
- UIA_CalendarControlTypeId
- UIA_CheckBoxControlTypeId
- UIA_ComboBoxControlTypeId
- UIA_CustomControlTypeId
- UIA_DataGridControlTypeId
- UIA_DataItemControlTypeId
- UIA_DocumentControlTypeId
- UIA_EditControlTypeId
- UIA_GroupControlTypeId
- UIA_HeaderControlTypeId
- UIA_HeaderItemControlTypeId
- UIA_HyperlinkControlTypeId
- UIA_ImageControlTypeId
- UIA_ListControlTypeId
- UIA_ListItemControlTypeId
- UIA_MenuBarControlTypeId
- UIA_MenuControlTypeId
- UIA_MenuItemControlTypeId
- UIA_PaneControlTypeId
- UIA_ProgressBarControlTypeId
- UIA_RadioButtonControlTypeId
- UIA_ScrollBarControlTypeId
- UIA_SemanticZoomControlTypeId
- UIA_SeparatorControlTypeId
- UIA_SliderControlTypeId
- UIA_SpinnerControlTypeId
- UIA_SplitButtonControlTypeId
- UIA_StatusBarControlTypeId
- UIA_TabControlTypeId
- UIA_TabItemControlTypeId
- UIA_TableControlTypeId
- UIA_TextControlTypeId
- UIA_ThumbControlTypeId
- UIA_TitleBarControlTypeId
- UIA_ToolBarControlTypeId
- UIA_ToolTipControlTypeId
- UIA_TreeControlTypeId
- UIA_TreeItemControlTypeId
- UIA_WindowControlTypeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d488148497ae95f7b26157b043251e509f72aee577534ccccc07f9766551591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324968"
---
# <a name="control-type-identifiers"></a>Идентификаторы типов элементов управления

В этом разделе описываются именованные константы, используемые для определения типов элементов управления модели автоматизации пользовательского интерфейса Майкрософт.



| Константа/значение                                                                                                                                                                                                                                                                                                           | Описание                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_AppBarControlTypeId"></span><span id="uia_appbarcontroltypeid"></span><span id="UIA_APPBARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Аппбарконтролтипеид**</dt> <dt>50040</dt> </dl>                         | Определяет тип элемента управления [панель приложений](uiauto-supportappbarcontroltype.md) . Поддерживается начиная с Windows 8.1.<br/>                                                     |
| <span id="UIA_ButtonControlTypeId"></span><span id="uia_buttoncontroltypeid"></span><span id="UIA_BUTTONCONTROLTYPEID"></span><dl> <dt>**UIA \_ Буттонконтролтипеид**</dt> <dt>50000</dt> </dl>                         | Определяет тип элемента управления ["Кнопка"](uiauto-supportbuttoncontroltype.md) .<br/>                                                                                          |
| <span id="UIA_CalendarControlTypeId"></span><span id="uia_calendarcontroltypeid"></span><span id="UIA_CALENDARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Календарконтролтипеид**</dt> <dt>50001</dt> </dl>                 | Определяет тип элемента управления [Calendar](uiauto-supportcalendarcontroltype.md) .<br/>                                                                                      |
| <span id="UIA_CheckBoxControlTypeId"></span><span id="uia_checkboxcontroltypeid"></span><span id="UIA_CHECKBOXCONTROLTYPEID"></span><dl> <dt>**UIA \_ Чеккбоксконтролтипеид**</dt> <dt>50002</dt> </dl>                 | Определяет тип элемента управления [CheckBox](uiauto-supportcheckboxcontroltype.md) .<br/>                                                                                      |
| <span id="UIA_ComboBoxControlTypeId"></span><span id="uia_comboboxcontroltypeid"></span><span id="UIA_COMBOBOXCONTROLTYPEID"></span><dl> <dt>**UIA \_ Комбобоксконтролтипеид**</dt> <dt>50003</dt> </dl>                 | Определяет тип элемента управления [ComboBox](uiauto-supportcomboboxcontroltype.md) . <br/>                                                                                     |
| <span id="UIA_CustomControlTypeId"></span><span id="uia_customcontroltypeid"></span><span id="UIA_CUSTOMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Кустомконтролтипеид**</dt> <dt>50025</dt> </dl>                         | Определяет тип пользовательского элемента управления. Дополнительные сведения см. в разделе [пользовательские свойства, события и шаблоны элементов управления](uiauto-custompropertieseventscontrolpatterns.md). <br/> |
| <span id="UIA_DataGridControlTypeId"></span><span id="uia_datagridcontroltypeid"></span><span id="UIA_DATAGRIDCONTROLTYPEID"></span><dl> <dt>**UIA \_ Датагридконтролтипеид**</dt> <dt>50028</dt> </dl>                 | Определяет тип элемента управления [DataGrid](uiauto-supportdatagridcontroltype.md) . <br/>                                                                                     |
| <span id="UIA_DataItemControlTypeId"></span><span id="uia_dataitemcontroltypeid"></span><span id="UIA_DATAITEMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Датаитемконтролтипеид**</dt> <dt>50029</dt> </dl>                 | Определяет тип элемента управления [DataItem](uiauto-supportdataitemcontroltype.md) . <br/>                                                                                     |
| <span id="UIA_DocumentControlTypeId"></span><span id="uia_documentcontroltypeid"></span><span id="UIA_DOCUMENTCONTROLTYPEID"></span><dl> <dt>**UIA \_ Документконтролтипеид**</dt> <dt>50030</dt> </dl>                 | Определяет тип элемента управления [документом](uiauto-supportdocumentcontroltype.md) . <br/>                                                                                     |
| <span id="UIA_EditControlTypeId"></span><span id="uia_editcontroltypeid"></span><span id="UIA_EDITCONTROLTYPEID"></span><dl> <dt>**UIA \_ Едитконтролтипеид**</dt> <dt>50004</dt> </dl>                                 | Определяет тип элемента управления [Edit](uiauto-supporteditcontroltype.md) .<br/>                                                                                              |
| <span id="UIA_GroupControlTypeId"></span><span id="uia_groupcontroltypeid"></span><span id="UIA_GROUPCONTROLTYPEID"></span><dl> <dt>**UIA \_ Граупконтролтипеид**</dt> <dt>50026</dt> </dl>                             | Определяет тип элемента управления [группы](uiauto-supportgroupcontroltype.md) . <br/>                                                                                           |
| <span id="UIA_HeaderControlTypeId"></span><span id="uia_headercontroltypeid"></span><span id="UIA_HEADERCONTROLTYPEID"></span><dl> <dt>**UIA \_ Хеадерконтролтипеид**</dt> <dt>50034</dt> </dl>                         | Определяет тип элемента управления " [заголовок](uiauto-supportheadercontroltype.md) ". <br/>                                                                                         |
| <span id="UIA_HeaderItemControlTypeId"></span><span id="uia_headeritemcontroltypeid"></span><span id="UIA_HEADERITEMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Хеадеритемконтролтипеид**</dt> <dt>50035</dt> </dl>         | Определяет тип элемента управления [HeaderItem](uiauto-supportheaderitemcontroltype.md) . <br/>                                                                                 |
| <span id="UIA_HyperlinkControlTypeId"></span><span id="uia_hyperlinkcontroltypeid"></span><span id="UIA_HYPERLINKCONTROLTYPEID"></span><dl> <dt>**UIA \_ Хиперлинкконтролтипеид**</dt> <dt>50005</dt> </dl>             | Определяет тип элемента управления [Hyperlink](uiauto-supporthyperlinkcontroltype.md) . <br/>                                                                                   |
| <span id="UIA_ImageControlTypeId"></span><span id="uia_imagecontroltypeid"></span><span id="UIA_IMAGECONTROLTYPEID"></span><dl> <dt>**UIA \_ Имажеконтролтипеид**</dt> <dt>50006</dt> </dl>                             | Определяет тип элемента управления [Image](uiauto-supportimagecontroltype.md) . <br/>                                                                                           |
| <span id="UIA_ListControlTypeId"></span><span id="uia_listcontroltypeid"></span><span id="UIA_LISTCONTROLTYPEID"></span><dl> <dt>**UIA \_ Листконтролтипеид**</dt> <dt>50008</dt> </dl>                                 | Определяет тип элемента управления " [список](uiauto-supportlistcontroltype.md) ". <br/>                                                                                             |
| <span id="UIA_ListItemControlTypeId"></span><span id="uia_listitemcontroltypeid"></span><span id="UIA_LISTITEMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Листитемконтролтипеид**</dt> <dt>50007</dt> </dl>                 | Определяет тип элемента управления [ListItem](uiauto-supportlistitemcontroltype.md) . <br/>                                                                                     |
| <span id="UIA_MenuBarControlTypeId"></span><span id="uia_menubarcontroltypeid"></span><span id="UIA_MENUBARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Менубарконтролтипеид**</dt> <dt>50010</dt> </dl>                     | Определяет тип элемента управления [MenuBar](uiauto-supportmenubarcontroltype.md) . <br/>                                                                                       |
| <span id="UIA_MenuControlTypeId"></span><span id="uia_menucontroltypeid"></span><span id="UIA_MENUCONTROLTYPEID"></span><dl> <dt>**UIA \_ Менуконтролтипеид**</dt> <dt>50009</dt> </dl>                                 | Определяет тип элемента управления [Menu](uiauto-supportmenucontroltype.md) . <br/>                                                                                             |
| <span id="UIA_MenuItemControlTypeId"></span><span id="uia_menuitemcontroltypeid"></span><span id="UIA_MENUITEMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Менуитемконтролтипеид**</dt> <dt>50011</dt> </dl>                 | Определяет тип элемента управления [MenuItem](uiauto-supportmenuitemcontroltype.md) . <br/>                                                                                     |
| <span id="UIA_PaneControlTypeId"></span><span id="uia_panecontroltypeid"></span><span id="UIA_PANECONTROLTYPEID"></span><dl> <dt>**UIA \_ Панеконтролтипеид**</dt> <dt>50033</dt> </dl>                                 | Определяет тип элемента управления [Pane](uiauto-supportpanecontroltype.md) . <br/>                                                                                             |
| <span id="UIA_ProgressBarControlTypeId"></span><span id="uia_progressbarcontroltypeid"></span><span id="UIA_PROGRESSBARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Прогрессбарконтролтипеид**</dt> <dt>50012</dt> </dl>     | Определяет тип элемента управления [ProgressBar](uiauto-supportprogressbarcontroltype.md) . <br/>                                                                               |
| <span id="UIA_RadioButtonControlTypeId"></span><span id="uia_radiobuttoncontroltypeid"></span><span id="UIA_RADIOBUTTONCONTROLTYPEID"></span><dl> <dt>**UIA \_ Радиобуттонконтролтипеид**</dt> <dt>50013</dt> </dl>     | Определяет тип элемента управления [RadioButton](uiauto-supportradiobuttoncontroltype.md) . <br/>                                                                               |
| <span id="UIA_ScrollBarControlTypeId"></span><span id="uia_scrollbarcontroltypeid"></span><span id="UIA_SCROLLBARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Скроллбарконтролтипеид**</dt> <dt>50014</dt> </dl>             | Определяет тип элемента управления [ScrollBar](uiauto-supportscrollbarcontroltype.md) . <br/>                                                                                   |
| <span id="UIA_SemanticZoomControlTypeId"></span><span id="uia_semanticzoomcontroltypeid"></span><span id="UIA_SEMANTICZOOMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Семантикзумконтролтипеид**</dt> <dt>50039</dt> </dl> | Определяет тип элемента управления [семантикзум](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype) . Поддерживается начиная с Windows 8.<br/>                                       |
| <span id="UIA_SeparatorControlTypeId"></span><span id="uia_separatorcontroltypeid"></span><span id="UIA_SEPARATORCONTROLTYPEID"></span><dl> <dt>**UIA \_ Сепараторконтролтипеид**</dt> <dt>50038</dt> </dl>             | Идентифицирует тип элемента управления [separator](uiauto-supportseparatorcontroltype.md) . <br/>                                                                                   |
| <span id="UIA_SliderControlTypeId"></span><span id="uia_slidercontroltypeid"></span><span id="UIA_SLIDERCONTROLTYPEID"></span><dl> <dt>**UIA \_ Слидерконтролтипеид**</dt> <dt>50015</dt> </dl>                         | Определяет тип элемента управления " [ползунок](uiauto-supportslidercontroltype.md) ". <br/>                                                                                         |
| <span id="UIA_SpinnerControlTypeId"></span><span id="uia_spinnercontroltypeid"></span><span id="UIA_SPINNERCONTROLTYPEID"></span><dl> <dt>**UIA \_ Спиннерконтролтипеид**</dt> <dt>50016</dt> </dl>                     | Определяет тип элемента управления " [Счетчик](uiauto-supportspinnercontroltype.md) ". <br/>                                                                                       |
| <span id="UIA_SplitButtonControlTypeId"></span><span id="uia_splitbuttoncontroltypeid"></span><span id="UIA_SPLITBUTTONCONTROLTYPEID"></span><dl> <dt>**UIA \_ Сплитбуттонконтролтипеид**</dt> <dt>50031</dt> </dl>     | Определяет тип элемента управления [SplitButton](uiauto-supportsplitbuttoncontroltype.md) . <br/>                                                                               |
| <span id="UIA_StatusBarControlTypeId"></span><span id="uia_statusbarcontroltypeid"></span><span id="UIA_STATUSBARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Статусбарконтролтипеид**</dt> <dt>50017</dt> </dl>             | Определяет тип элемента управления [StatusBar](uiauto-supportstatusbarcontroltype.md) . <br/>                                                                                   |
| <span id="UIA_TabControlTypeId"></span><span id="uia_tabcontroltypeid"></span><span id="UIA_TABCONTROLTYPEID"></span><dl> <dt>**UIA \_ Табконтролтипеид**</dt> <dt>50018</dt> </dl>                                     | Определяет тип элемента управления [Tab](uiauto-supporttabcontroltype.md) . <br/>                                                                                               |
| <span id="UIA_TabItemControlTypeId"></span><span id="uia_tabitemcontroltypeid"></span><span id="UIA_TABITEMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Табитемконтролтипеид**</dt> <dt>50019</dt> </dl>                     | Определяет тип элемента управления [TabItem](uiauto-supporttabitemcontroltype.md) . <br/>                                                                                       |
| <span id="UIA_TableControlTypeId"></span><span id="uia_tablecontroltypeid"></span><span id="UIA_TABLECONTROLTYPEID"></span><dl> <dt>**UIA \_ Таблеконтролтипеид**</dt> <dt>50036</dt> </dl>                             | Определяет тип элемента управления [Table](uiauto-supporttablecontroltype.md) . <br/>                                                                                           |
| <span id="UIA_TextControlTypeId"></span><span id="uia_textcontroltypeid"></span><span id="UIA_TEXTCONTROLTYPEID"></span><dl> <dt>**UIA \_ Текстконтролтипеид**</dt> <dt>50020</dt> </dl>                                 | Определяет тип элемента управления [текстом](uiauto-supporttextcontroltype.md) . <br/>                                                                                             |
| <span id="UIA_ThumbControlTypeId"></span><span id="uia_thumbcontroltypeid"></span><span id="UIA_THUMBCONTROLTYPEID"></span><dl> <dt>**UIA \_ Сумбконтролтипеид**</dt> <dt>50027</dt> </dl>                             | Определяет тип элемента управления [Thumb](uiauto-supportthumbcontroltype.md) . <br/>                                                                                           |
| <span id="UIA_TitleBarControlTypeId"></span><span id="uia_titlebarcontroltypeid"></span><span id="UIA_TITLEBARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Титлебарконтролтипеид**</dt> <dt>50037</dt> </dl>                 | Определяет тип элемента управления " [заголовок](uiauto-supporttitlebarcontroltype.md) ". <br/>                                                                                     |
| <span id="UIA_ToolBarControlTypeId"></span><span id="uia_toolbarcontroltypeid"></span><span id="UIA_TOOLBARCONTROLTYPEID"></span><dl> <dt>**UIA \_ Тулбарконтролтипеид**</dt> <dt>50021</dt> </dl>                     | Определяет тип элемента управления [Toolbar](uiauto-supporttoolbarcontroltype.md) . <br/>                                                                                       |
| <span id="UIA_ToolTipControlTypeId"></span><span id="uia_tooltipcontroltypeid"></span><span id="UIA_TOOLTIPCONTROLTYPEID"></span><dl> <dt>**UIA \_ Тултипконтролтипеид**</dt> <dt>50022</dt> </dl>                     | Определяет тип элемента управления [ToolTip](uiauto-supporttooltipcontroltype.md) . <br/>                                                                                       |
| <span id="UIA_TreeControlTypeId"></span><span id="uia_treecontroltypeid"></span><span id="UIA_TREECONTROLTYPEID"></span><dl> <dt>**UIA \_ Триконтролтипеид**</dt> <dt>50023</dt> </dl>                                 | Определяет тип элемента управления " [дерево](uiauto-supporttreecontroltype.md) ". <br/>                                                                                             |
| <span id="UIA_TreeItemControlTypeId"></span><span id="uia_treeitemcontroltypeid"></span><span id="UIA_TREEITEMCONTROLTYPEID"></span><dl> <dt>**UIA \_ Триитемконтролтипеид**</dt> <dt>50024</dt> </dl>                 | Определяет тип элемента управления [TreeItem](uiauto-supporttreeitemcontroltype.md) . <br/>                                                                                     |
| <span id="UIA_WindowControlTypeId"></span><span id="uia_windowcontroltypeid"></span><span id="UIA_WINDOWCONTROLTYPEID"></span><dl> <dt>**UIA \_ Виндовконтролтипеид**</dt> <dt>50032</dt> </dl>                         | Определяет тип элемента управления [Window](uiauto-supportwindowcontroltype.md) . <br/>                                                                                         |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                            |
| Header<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Общие сведения о типах элементов управления автоматизации пользовательского интерфейса](uiauto-controltypesoverview.md)
</dt> <dt>

[Константы модели автоматизации пользовательского интерфейса](uiauto-entry-constants.md)
</dt> </dl>

 

