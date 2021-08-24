---
title: Константы и перечисления
description: справочная документация по Windows платформе ленты константы и перечисления.
ms.assetid: 8499a096-aac3-4af3-a4c9-eebf53698744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788a2dbaccbf3241d8ecad7fd315c9af870d2b0f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473740"
---
# <a name="constants-and-enumerations"></a>Константы и перечисления

справочная документация по Windows платформе ленты константы и перечисления.

### <a name="constants-and-enumerations"></a>Константы и перечисления




| Константа | Описание | 
|----------|-------------|
| <a href="/windows/desktop/windowsribbon/windowsribbon-ui-all-commands"><strong>UI_ALL_COMMANDS</strong></a><br /> | Задает константу, определяющую коллекцию команд, объявленных в файле ресурсов разметки.<br /> | 
| <a href="/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex"><strong>UI_COLLECTION_INVALIDINDEX</strong></a><br /> | Задает константу, определяющую недопустимый индекс в коллекции.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_collectionchange"><strong>UI_COLLECTIONCHANGE</strong></a><br /> | Задает значения, определяющие типы изменений, которые могут быть внесены в коллекцию.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh448736(v=vs.85)"><strong>UI_COMMANDCATEGORY</strong></a><br /> | Указывает значения, указывающие, определена ли команда во время компиляции или во время выполнения.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype"><strong>UI_COMMANDTYPE</strong></a><br /> | Задает значения, определяющие тип команды, связанной с элементом управления "лента".<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability"><strong>UI_CONTEXTAVAILABILITY</strong></a><br /> | Указывает значения, определяющие доступность <a href="windowsribbon-element-ribbon-contextualtabs.md"><strong>контекстной вкладки</strong></a>.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock"><strong>UI_CONTROLDOCK</strong></a><br /> | Указывает значения, определяющие состояние DOCKER панели быстрого доступа (QAT). <br /> | 
| <a href="/windows/desktop/api/Uiribbon/ne-uiribbon-ui_eventlocation"><strong>UI_EVENTLOCATION</strong></a><br /> | Определяет расположения, в которых могут поступать события, связанные с элементом управления "лента".<br /> | 
| <a href="/windows/desktop/api/Uiribbon/ne-uiribbon-ui_eventtype"><strong>UI_EVENTTYPE</strong></a><br /> | Определяет типы событий, связанных с <a href="windowsribbon-element-ribbon.md"><strong>лентой</strong></a>.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb"><strong>UI_EXECUTIONVERB</strong></a><br /> | Указывает значения, определяющие идентификаторы выполнения, которые сопоставляются с действиями, которые пользователь может инициировать для <a href="windowsribbon-element-command.md"><strong>команды</strong></a>. <br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize"><strong>UI_FONTDELTASIZE</strong></a><br /> | Задает значения, определяющие, должен ли размер шрифта выделенного текстового запуска увеличиваться или уменьшаться.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties"><strong>UI_FONTPROPERTIES</strong></a><br /> | Задает значения, определяющие состояние свойства шрифта <a href="windowsribbon-element-fontcontrol.md"><strong>фонтконтрол</strong></a>, например <strong>Зачеркнутый</strong>.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline"><strong>UI_FONTUNDERLINE</strong></a><br /> | Задает значения, определяющие состояние подчеркивания <a href="windowsribbon-element-fontcontrol.md"><strong>фонтконтрол</strong></a>.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition"><strong>UI_FONTVERTICALPOSITION</strong></a><br /> | Задает значения, определяющие состояние выравнивания по вертикали для <a href="windowsribbon-element-fontcontrol.md"><strong>фонтконтрол</strong></a>.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_invalidations"><strong>UI_INVALIDATIONS</strong></a><br /> | Указывает значения, определяющие аспект команды, которую необходимо сделать недействительной.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_ownership"><strong>UI_OWNERSHIP</strong></a><br /> | Указывает значения, определяющие условия владения платформой Ribbon, в которых создается изображение.<br /> | 
| <a href="/windows/desktop/api/Uiribbon/ne-uiribbon-ui_swatchcolormode"><strong>UI_SWATCHCOLORMODE</strong></a><br /> | Указывает, имеет ли образец режим нормального или монохромного.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype"><strong>UI_SWATCHCOLORTYPE</strong></a><br /> | Задает значения, определяющие способ заполнения палитры цветов в средстве выбора цвета <a href="windowsribbon-element-dropdowncolorpicker.md"><strong>дропдовнколорпиккер</strong></a> или <a href="windowsribbon-element-fontcontrol.md"><strong>Фонтконтрол</strong></a> (<strong>Цвет текста</strong> или <strong>выделение текста</strong>).<br /><blockquote>[!Note]<br />Это только рекомендации. Приложение может связать любой тип заливки с этими значениями.</blockquote><br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_viewtype"><strong>UI_VIEWTYPE</strong></a><br /> | Указывает значения, определяющие представление платформы ленты.<br /> | 
| <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_viewverb"><strong>UI_VIEWVERB</strong></a><br /> | Указывает значения, определяющие тип действия, которое необходимо выполнить в представлении платформы ленты.<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Справочник по платформе ленты](windowsribbon-reference-entry.md)
</dt> </dl>

 

