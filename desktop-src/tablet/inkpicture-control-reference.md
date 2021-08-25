---
description: Элемент управления InkPicture предоставляет возможность поместить изображение в приложение и позволить пользователям добавлять рукописные данные поверх него.
ms.assetid: e9fa6807-6e2a-44ec-9b8f-a560185e4367
title: Справочник по элементу управления InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93f5727d2f3f049a579e32e5feb0ba0eaa742d2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471540"
---
# <a name="inkpicture-control-reference"></a>Справочник по элементу управления InkPicture

Элемент управления InkPicture предоставляет возможность поместить изображение в приложение и позволить пользователям добавлять рукописные данные поверх него. Он предназначен для сценариев, в которых рукописный ввод не распознается как текст, а сохраняется в виде рукописных данных.

Экземпляр элемента управления InkPicture можно создать, вызвав метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

> [!Note]  
> Элемент управления InkPicture не помечен как надежный для создания скриптов. элемент управления InkPicture не следует использовать в HTML-и ASP.NET страницах.

 

Создание элемента управления InkPicture за прозрачным элементом управления (например, GroupBox с \_ \_ набором свойств WS ex) предотвратит Сбор рукописных данных.

## <a name="members"></a>Элементы



| Перечисление                                      | Описание                                                                                              |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**инкпиктуресиземоде**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpicturesizemode) | Определяет значения, которые определяют, как фоновое изображение ведет себя внутри элемента управления InkPicture.<br/> |



 



| Событие                                                                              | Описание                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ChangeUICues**                                                                   | Не рекомендуется.<br/>                                                                                                                                                                                                                                                                                             |
| [**Откройте**](inkpicture-click.md)                                                  | Происходит, когда пользователь щелкает элемент управления InkPicture.<br/>                                                                                                                                                                                                                                                       |
| [**Событие Курсорбуттондовн**](inkpicture-cursorbuttondown.md)                      | Происходит, когда элемент управления [**InkCollector**](inkcollector-class.md) обнаруживает [**неиинккурсорбуттоный**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) объект.<br/>                                                                                                                                                         |
| [**Событие Курсорбуттонуп**](inkpicture-cursorbuttonup.md)                          | Происходит, когда элемент управления InkPicture обнаруживает [**иинккурсорбуттон**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) .<br/>                                                                                                                                                                                                  |
| [**Событие Курсордовн**](inkpicture-cursordown.md)                                  | Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.<br/>                                                                                                                                                                                                                                      |
| [**Событие Курсоринранже**](inkpicture-cursorinrange.md)                            | Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.<br/>                                                                                                                                                                                                             |
| [**Событие Курсораутофранже**](inkpicture-cursoroutofrange.md)                      | Происходит, когда курсор покидает диапазон физического обнаружения (близость) контекста планшета.<br/>                                                                                                                                                                                                           |
| [**Кнопки**](inkpicture-dblclick.md)                                            | Происходит при двойном щелчке элемента управления InkPicture.<br/> Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** . Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипедблкликк.<br/> |
| [**Событие жеста**](inkpicture-gesture.md)                                        | Происходит при распознавании жеста приложения.<br/>                                                                                                                                                                                                                                                       |
| [**\[Элемент управления InkPicture события KeyDown\]**](inkpicture-keydown.md)                 | Происходит при нажатии клавиши и в расположении вниз, пока элемент управления InkPicture находится в фокусе.<br/>                                                                                                                                                                                                           |
| [**\[Элемент управления InkPicture события KeyPress\]**](inkpicture-keypress.md)                | Происходит при нажатии клавиши, когда элемент управления InkPicture имеет фокус.<br/>                                                                                                                                                                                                                                    |
| [**\[Элемент управления InkPicture события KeyUp\]**](inkpicture-keyup.md)                     | Происходит при освобождении ключа, когда элемент управления InkPicture имеет фокус.<br/>                                                                                                                                                                                                                                   |
| [**\[Элемент управления InkPicture события MouseDown\]**](inkpicture-mousedown.md)             | Происходит при нажатии кнопки мыши, когда указатель мыши находится над элементом управления InkPicture.<br/>                                                                                                                                                                                                             |
| [**События**](inkpicture-mouseenter.md)                                        | Происходит, когда указатель мыши входит в элемент управления InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**маусеховер**](inkpicture-mousehover.md)                                        | Происходит при наведении указателя мыши на элемент управления InkPicture.<br/>                                                                                                                                                                                                                                       |
| [**MouseLeave**](inkpicture-mouseleave.md)                                        | Происходит, когда указатель мыши покидает элемент управления InkPicture.<br/>                                                                                                                                                                                                                                            |
| [**\[Элемент управления InkPicture события MouseMove\]**](inkpicture-mousemove.md)             | Происходит при перемещении указателя мыши над элементом управления InkPicture.<br/>                                                                                                                                                                                                                                     |
| [**\[Элемент управления InkPicture события MouseUp\]**](inkpicture-mouseup.md)                 | Происходит при отпускании кнопки мыши, когда указатель мыши находится над элементом управления InkPicture.<br/>                                                                                                                                                                                                            |
| [**маусевхил**](inkpicture-mousewheel.md)                                        | Происходит при движении колесика мыши, когда элемент управления InkPicture имеет фокус.<br/>                                                                                                                                                                                                                               |
| [**Событие Невинаирпаккетс**](inkpicture-newinairpackets.md)                        | Происходит при обнаружении пакета в эфире.<br/>                                                                                                                                                                                                                                                                   |
| [**Событие Невпаккетс**](inkpicture-newpackets.md)                                  | Происходит, когда элемент управления InkPicture получает пакет.<br/>                                                                                                                                                                                                                                                   |
| [**Окрашивает**](inkpicture-painted.md)                                              | Происходит при завершении перерисовки элемента управления InkPicture.<br/>                                                                                                                                                                                                                                      |
| [**Оформленные**](inkpicture-painting.md)                                            | Происходит перед перерисовкой элемента управления InkPicture.<br/>                                                                                                                                                                                                                                                    |
| [**Изменить размер**](inkpicture-resize.md)                                                | Происходит при изменении размера элемента управления InkPicture.<br/>                                                                                                                                                                                                                                                          |
| [**SelectionChanged**](inkpicture-selectionchanged.md)                            | Происходит при изменении выделения текста внутри элемента управления InkPicture, например при преобразовании в пользовательский интерфейс, процедурах вырезания и вставки или свойством [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                    |
| [**селектиончангинг**](inkpicture-selectionchanging.md)                          | Происходит при изменении выделения текста внутри элемента управления InkPicture, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                             |
| [**селектионмовед**](inkpicture-selectionmoved.md)                                | Происходит при изменении расположения текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                  |
| [**\[Элемент управления InkPicture события селектионмовинг\]**](inkpicture-selectionmoving.md) | Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                           |
| [**селектионресизед**](inkpicture-selectionresized.md)                            | Происходит при изменении размера текущего выделения, например с помощью изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                                      |
| [**селектионресизинг**](inkpicture-selectionresizing.md)                          | Происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .<br/>                                                                                               |
| [**SizeChanged**](inkpicture-sizechanged.md)                                      | Происходит после изменения размера элемента управления InkPicture, в частности после того, как изменяется значение свойства [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) или [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .<br/>                                                                                                      |
| [**сиземодечанжед**](inkpicture-sizemodechanged.md)                              | Происходит после изменения свойства [**сиземоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) элемента управления InkPicture.<br/>                                                                                                                                                                                           |
| **стилечанжед**                                                                   | Не реализован.<br/>                                                                                                                                                                                                                                                                                        |
| [**Водок**](inkpicture-stroke.md)                                                | Происходит, когда пользователь рисует новый штрих на любом планшете.<br/>                                                                                                                                                                                                                                                  |
| [**строкесделетед**](inkpicture-strokesdeleted.md)                                | Происходит после удаления объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) из свойства [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                        |
| [**строкесделетинг**](inkpicture-strokesdeleting.md)                              | Происходит перед удалением объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) из свойства [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .<br/>                                                                                                                                                                             |
| [**системколорсчанжед**](inkpicture-systemcolorschanged.md)                      | Происходит после изменения системных цветов.<br/>                                                                                                                                                                                                                                                                  |
| [**системжестуре**](inkpicture-systemgesture.md)                                  | Происходит при распознавании системного жеста.<br/>                                                                                                                                                                                                                                                             |
| [**Событие Таблетаддед**](inkpicture-tabletadded.md)                                | Происходит при добавлении планшета в систему.<br/>                                                                                                                                                                                                                                                            |
| [**Событие Таблетремовед**](inkpicture-tabletremoved.md)                            | Происходит при удалении планшета из системы.<br/>                                                                                                                                                                                                                                                        |



 



| Метод                                                                                   | Описание                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Метод Жетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-geteventinterest)                           | Возвращает значение, указывающее, имеет ли элемент управления InkPicture интерес к определенному событию.<br/>                                                                   |
| [**жетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getgesturestatus)                                  | Возвращает значение, указывающее, имеет ли элемент управления InkPicture интерес к определенному жесту приложения.<br/>                                                     |
| [**Метод Жетвиндовинпутректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-getwindowinputrectangle)             | Возвращает прямоугольник окна (в пикселях), в котором рисуются рукописные данные.<br/>                                                                                                 |
| [**хиттестселектион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-hittestselection)                                  | Возвращает член перечисления [**селектионхитресулт**](/windows/desktop/api/msinkaut/ne-msinkaut-selectionhitresult) , указывающий, какая часть выбора (если таковая имеется) была достигнута во время проверки попадания.<br/> |
| [**Метод Сеталлтаблетсмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode)                         | Позволяет элементу управления InkPicture сохранять рукописный ввод с любого планшета, подключенного к планшетному ПК.<br/>                                                                            |
| [**Метод Сетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-seteventinterest)                           | Задает значение, указывающее, имеет ли элемент управления InkPicture объект в указанном событии.<br/>                                                                        |
| SetFocus                                                                                 | Перемещает фокус на элемент управления InkPicture.<br/>                                                                                                                          |
| [**Метод Сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)                           | Задает интерес объекта InkPicture в указанном жесте приложения.<br/>                                                                                      |
| [**Метод Сетсинглетаблетинтегратедмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode) | Задает элемент управления InkPicture для получения рукописных данных только с одного планшета, подключенного к планшетному ПК. Рукописный ввод с других планшетов игнорируется.<br/>                                       |
| [**Метод Сетвиндовинпутректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setwindowinputrectangle)             | Задает прямоугольник окна для установки в координатах окна, в которых рисуются рукописные данные.<br/>                                                                            |
| шоввхатссис                                                                            | отображает выбранный раздел в файле справки, используя всплывающее окно "что это", предоставляемое справкой в 32-разрядных операционных системах Microsoft Windows (только во время разработки).<br/>           |
| зордер                                                                                   | Помещает элемент управления на передний или задний план z-порядка в его графическом уровне (только во время разработки).<br/>                                                               |



 




| Свойство | Описание | 
|----------|-------------|
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Ауторедрав, свойство</strong></a> | Возвращает или задает значение, указывающее, перерисовывается ли элемент управления InkPicture при недействительности окна (объект <a href="inkdisp-class.md"><strong>инкдисп</strong></a> , который в данный момент связан с элементом управления InkPicture, автоматически перерисовывается, когда окно, связанное с InkPicture, получает сообщение WM_PAINT).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a> | Возвращает или задает цвет фона для элемента управления InkPicture. Цвет фона по умолчанию — это цвет фона системного окна, который обычно является белым.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Коллектингинк, свойство</strong></a> | Возвращает значение, указывающее, собирает ли элемент управления InkPicture рукописный ввод (только время выполнения).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>Режиме CollectionMode</strong></a> | Возвращает или задает режим сбора, определяющий, распознаются ли рукописный ввод, жесты или рукописный ввод и жесты при записи пользователем.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor, свойство</strong></a> | Возвращает коллекцию <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>иинккурсорс</strong></a> , доступную для использования в области рукописного ввода в элементе управления InkPicture.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>кустомстрокес</strong></a> | Возвращает коллекцию <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>иинккустомстрокес</strong></a> , которая должна быть сохранена с рукописным вводом (только во время разработки).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes, свойство</strong></a> | Возвращает или задает коллекцию <a href="inkdrawingattributes-class.md"><strong>инкдравингаттрибутес</strong></a> по умолчанию, используемую при прорисовке и отображении рукописного ввода (только во время выполнения).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Десиредпаккетдескриптион, свойство</strong></a> | Возвращает или задает описание пакета для элемента управления InkPicture (только время выполнения).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Динамикрендеринг, свойство</strong></a> | Возвращает или задает значение, указывающее, будет ли элемент управления InkPicture динамически отображать рукописный ввод при его сборе.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a> | Возвращает или задает значение, указывающее, находится ли элемент управления InkPicture в режиме рукописного ввода, режиме удаления или режиме правки или выбора.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Включен</strong></a> | Возвращает или задает значение, определяющее, может ли элемент управления InkPicture отвечать на создаваемые пользователем события.<br /><blockquote>[!Note]<br />Это свойство эквивалентно свойству <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>инкенаблед</strong></a> .</blockquote><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>ерасермоде</strong></a> | Возвращает или задает значение, указывающее, удаляются ли рукописные данные по штрихам или по точкам.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>ерасервидс</strong></a> | Возвращает или задает значение, указывающее ширину кончика пера ластика.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a> | Возвращает описатель окна, к которому привязан элемент управления InkPicture. (только время выполнения)<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Рукописный ввод</strong></a> | Возвращает или задает объект <a href="inkdisp-class.md"><strong>инкдисп</strong></a> , связанный с элементом управления InkPicture (только время выполнения).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>инкенаблед</strong></a> | Возвращает или задает значение, указывающее, собирает ли элемент управления InkPicture входные данные пера (пакеты в сети Air, курсоры в пределах диапазона и т. д.).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Маргинкс, свойство</strong></a> | Возвращает или задает поле оси x вокруг прямоугольника окна в экранных координатах.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Свойство Margin</strong></a> | Возвращает или задает поле оси y вокруг прямоугольника окна в экранных координатах.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Маусеикон, свойство</strong></a> | Возвращает или задает текущий пользовательский значок мыши.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer, свойство</strong></a> | Возвращает или задает значение, указывающее тип указателя мыши, который появляется при наведении указателя мыши на определенную часть элемента управления InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Снимки</strong></a> | Возвращает графический файл, отображаемый в элементе управления InkPicture.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Свойство модуля подготовки отчетов</strong></a> | Возвращает или задает объект <a href="inkrenderer-class.md"><strong>инкрендерер</strong></a> , используемый для рисования рукописного ввода в элементе управления InkPicture (только время выполнения).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Выбор</strong></a> | Возвращает коллекцию <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">инкстрокес</a> , выбранную в данный момент в элементе управления InkPicture (только время выполнения).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a> | Возвращает или задает способ, которым элемент управления обрабатывает размещение и изменение размера изображения.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Суппорсигхконтрастинк, свойство</strong></a> | Возвращает значение, указывающее, отображаются ли рукописные данные только в одном цвете, Color = COLOR_WINDOWTEXT (из вызова Жетсистемметрикс), когда система находится в режиме высокая контрастность.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>суппорсигхконтрастселектионуи</strong></a> | Возвращает или задает значение, указывающее, отображаются ли все пользовательские интерфейсы выделения (ограничивающие прямоугольники выделения и маркеры выделения) с высокой контрастностью, когда система находится в режиме высокая контрастность.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Свойство планшета</strong></a> | Возвращает объект <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>иинктаблет</strong></a> , который в настоящее время использует элемент управления InkPicture для получения входных данных.<br /> | 




 

## <a name="remarks"></a>Комментарии

Пользовательский интерфейс времени выполнения для элемента управления InkPicture — это окно с непрозрачным фоном (один цвет, фон изображения или и то, и другое), которое содержит непрозрачные рукописные данные.

можно использовать элемент управления InkPicture для визуализации рукописного ввода в Microsoft Windows 2000, Windows Server 2003, любой выпуск Windows XP, кроме Windows XP Tablet PC edition и любой версии Windows Vista. Однако вы можете ввести рукописный ввод, принять жесты или распознать рукописный ввод только при следующих условиях:

-   рукописный ввод может быть введен и распознан, если установлен Windows Vista или XP Tablet PC Edition 2005.
-   Также можно распознать жесты.
-   рукописный ввод можно распознать как текст, если рукописный ввод создан на компьютерах с более ранними версиями Windows, если имеются распознаватели.

при использовании Windows 2000, Windows Server 2003, любого выпуска Windows xp, кроме Windows XP Tablet PC edition 2005, можно присваивать значения внешним свойствам элемента управления InkPicture, а затем копировать и вставлять рукописные данные в другие приложения. Однако значение его свойства Инкенаблед всегда будет равно **false**.

сохраненные объекты [**инкдисп**](inkdisp-class.md) можно загружать и отображать во всех выпусках Windows Vista и XP, а также в системах, где установлен только Windows XP Tablet PC Edition Software Development Kit (SDK). объекты **инкдисп** можно преобразовать в текст (распознается), если установлен Windows Vista или Windows XP Tablet PC Edition 2005.

Если операции с этим элементом управления не выполнены, возвращается юридическое значение HRESULT. При возникновении условий ошибки проверьте возвращенное значение HRESULT для ошибки.

Дополнительные сведения об элементах управления рукописного ввода см. в разделе [Рукописный ввод](ink-controls.md).

Сведения о том, какие потоки вызывают определенные события, см. [в разделе потоки, в которых может срабатывать событие](threads-on-which-an-event-can-fire.md).

Чтобы повысить производительность приложения, вручную удалите элемент управления InkPicture, когда он больше не нужен.

> [!Note]  
> Если элемент управления InkPicture накладывается на другой элемент управления, такой как **GroupBox** , для которого задано значение Transparent, то функция InkPicture не будет выполнять накопление рукописного ввода. InkPicture должен быть самым верхним элементом управления в Z-порядке или дочерним по отношению к **GroupBox**.

 

## <a name="com-implementation"></a>Реализация COM

Этот объект реализует COM-интерфейс **иинкпиктуре** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ссылка на элемент управления InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> </dl>

