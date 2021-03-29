---
description: Этот раздел содержит свойства, принадлежащие элементу управления InkEdit.
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: Свойства InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647415"
---
# <a name="inkedit-properties"></a>Свойства InkEdit

Этот раздел содержит свойства, принадлежащие элементу управления InkEdit.



| Свойство                                                 | Описание                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Внешний вид**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Возвращает или задает значение, определяющее, выглядит ли элемент управления [InkEdit](inkedit-control-reference.md) плоским или трехмерным.<br/>                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Возвращает или задает цвет фона для элемента управления [InkEdit](inkedit-control-reference.md) .<br/>                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Возвращает или задает значение, определяющее, имеет ли элемент управления [InkEdit](inkedit-control-reference.md) границу.<br/>                                                                             |
| [**дисабленоскролл**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Возвращает или задает значение, определяющее, отключены ли полосы прокрутки в элементе управления [InkEdit](inkedit-control-reference.md) .<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Возвращает или задает атрибуты рисования для рукописного ввода, который еще должен быть нарисован на элементе управления [InkEdit](inkedit-control-reference.md) .<br/>                                                                |
| [**Активировано**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Возвращает или задает значение, определяющее, может ли элемент управления [InkEdit](inkedit-control-reference.md) отвечать на создаваемые пользователем события.<br/>                                                     |
| [**фактоид**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Возвращает или задает константу [фактоид](factoid-constants.md) , используемую объектом [**иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) для ограничения поиска результата распознавания.<br/>                  |
| [**Шрифт**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Возвращает или задает шрифт текста, отображаемого элементом управления [InkEdit](inkedit-control-reference.md) .<br/>                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Возвращает описатель окна, к которому привязан элемент управления [**инкдисп**](inkdisp-class.md) .<br/>                                                                                                      |
| [**инкинсертмоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Возвращает или задает значение, указывающее, как рукописный ввод вставляется в элемент управления [InkEdit](inkedit-control-reference.md) в виде текста или рукописного ввода.<br/>                                                |
| [**инкмоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Возвращает или задает значение, указывающее, отключена ли коллекция рукописных данных, выполняется сбор рукописных данных, а также выполняется сбор рукописных данных и жестов.<br/>                                                                |
| [**Locked**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Возвращает или задает значение, указывающее, доступен ли элемент управления [InkEdit](inkedit-control-reference.md) только для чтения или нет.<br/>                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Возвращает или задает значение, указывающее, может ли элемент управления [InkEdit](inkedit-control-reference.md) содержать максимальное количество символов и, если это так, указывает максимальное число символов.<br/> |
| [**маусеикон**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Возвращает или задает текущий пользовательский значок мыши.<br/>                                                                                                                                                 |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Возвращает или задает значение, указывающее тип указателя мыши, который появляется при наведении указателя мыши на определенную часть элемента управления [InkEdit](inkedit-control-reference.md) .<br/>                |
| [**Нескольких**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Возвращает или задает значение, указывающее, является ли это многострочным элементом управления [InkEdit](inkedit-control-reference.md) .<br/>                                                                           |
| [**рекогнитионтимеаут**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Возвращает или задает интервал времени (в миллисекундах) между последним сбором объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) и началом распознавания текста.<br/>                         |
| [**Распознаватель**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Возвращает или задает объект [**иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) , используемый для распознавания.<br/>                                                                                                    |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Возвращает или задает тип полос прокрутки, отображаемых в элементе управления [InkEdit](inkedit-control-reference.md) .<br/>                                                                                   |
| [**селалигнмент**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Возвращает или задает выравнивание, применяемое к текущему выделению или точке вставки (только во время выполнения).<br/>                                                                                            |
| [**селболд**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Возвращает или задает значение, указывающее, является ли начертание шрифта выделенного в данный момент текста в элементе управления [InkEdit](inkedit-control-reference.md) полужирным (только во время выполнения).<br/>                  |
| [**селчароффсет**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Возвращает или задает значение, указывающее, отображается ли текст в элементе управления [InkEdit](inkedit-control-reference.md) в виде надстрочного или подстрочного шрифта (только во время выполнения).<br/>                             |
| [**селколор**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Возвращает или задает цвет текста текущего выделения текста или точки вставки (только время выполнения).<br/>                                                                                               |
| [**селфонтнаме**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Возвращает или задает имя шрифта выделенного текста в элементе управления [InkEdit](inkedit-control-reference.md) (только время выполнения).<br/>                                                                |
| [**селфонтсизе**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Возвращает или задает размер шрифта выделенного текста в элементе управления [InkEdit](inkedit-control-reference.md) (только время выполнения).<br/>                                                                |
| [**селинкс**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Возвращает или задает массив внедренных объектов [**инкдисп**](inkdisp-class.md) (если они отображаются как рукописные данные), которые содержатся в текущем выделенном фрагменте.<br/>                                                      |
| [**селинксдисплаймоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Возвращает или задает значение, позволяющее переключать внешний вид выделения между рукописным вводом и текстом.<br/>                                                                                             |
| [**селиталик**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Возвращает или задает значение, указывающее, является ли начертание шрифта выделенного в данный момент текста в элементе управления [InkEdit](inkedit-control-reference.md) курсивом (только время выполнения).<br/>                |
| [**селленгс**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Возвращает или задает число символов, выбранных в элементе управления [InkEdit](inkedit-control-reference.md) (только время выполнения).<br/>                                                            |
| [**селртф**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Возвращает или задает выделенный в текущий момент текст в формате RTF в элементе управления [InkEdit](inkedit-control-reference.md) (только время выполнения).<br/>                                          |
| [**селстарт**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Возвращает или задает начальную точку текста, выбранного в текстовом поле (только во время выполнения).<br/>                                                                                               |
| [**селтекст**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Возвращает или задает выделенный текст в элементе управления [InkEdit](inkedit-control-reference.md) (только время выполнения).<br/>                                                                                 |
| [**селундерлине**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Возвращает или задает значение, указывающее, подчеркнут ли стиль шрифта выделенного в данный момент текста в элементе управления [InkEdit](inkedit-control-reference.md) (только во время выполнения).<br/>            |
| [**Состояние**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Возвращает значение, указывающее, простаивает ли элемент управления [InkEdit](inkedit-control-reference.md) , собирает рукописный ввод или распознает рукописный ввод (только время выполнения).<br/>                                       |
| [**Полнотекстовым**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Получает или задает текущий текст в текстовом поле.<br/>                                                                                                                                              |
| [**текстртф**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Возвращает или задает текст элемента управления [InkEdit](inkedit-control-reference.md) , включая все коды RTF.<br/>                                                                                     |
| [**усемаусефоринпут**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Возвращает или задает значение, указывающее, можно ли использовать мышь в качестве входного устройства.<br/>                                                                                                       |



 

 

 




