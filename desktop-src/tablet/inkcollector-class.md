---
description: Представляет объект, используемый для захвата рукописного ввода из доступных устройств планшета.
ms.assetid: 189f430e-9d00-4e29-bb8c-8ac195896793
title: Класс InkCollector (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkCollector
- InkCollector.IInkCollector
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 02ecf89a1ce8db89105ac9fa0243552efaf5218da98f6d3b0fdfbd58f874d449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718180"
---
# <a name="inkcollector-class"></a>Класс InkCollector

Представляет объект, используемый для захвата рукописного ввода из доступных устройств планшета.

Создание элемента управления **InkCollector** за прозрачным элементом управления (например, GroupBox с набором свойств **WS \_ \_ ex** ) не позволит **InkCollector** собирать рукописные данные.

**InkCollector** имеет следующие типы членов:

-   [События](#events)
-   [Интерфейсы](#interfaces)
-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="events"></a>События

Класс **InkCollector** содержит эти события.



| Событие                                                     | Описание                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**курсорбуттондовн**](inkcollector-cursorbuttondown.md) | Происходит, когда **InkCollector** обнаруживает недоступную кнопку курсора.<br/>                                                                                                                                                                             |
| [**курсорбуттонуп**](inkcollector-cursorbuttonup.md)     | Происходит, когда **InkCollector** обнаруживает кнопку курсора, которая находится в up.<br/>                                                                                                                                                                               |
| [**курсордовн**](inkcollector-cursordown.md)             | Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.<br/>                                                                                                                                                                                 |
| [**курсоринранже**](inkcollector-cursorinrange.md)       | Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.<br/>                                                                                                                                                        |
| [**курсораутофранже**](inkcollector-cursoroutofrange.md) | Происходит, когда курсор покидает диапазон физического обнаружения (близость) контекста планшета.<br/>                                                                                                                                                      |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Происходит при двойном щелчке объекта **InkCollector** .<br/>                                                                                                                                                                                         |
| [**жесты**](inkcollector-gesture.md)                   | Происходит при распознавании жеста конкретного приложения.<br/>                                                                                                                                                                                         |
| [**Вниз**](inkcollector-mousedown.md)               | Происходит при нажатии кнопки мыши, когда указатель мыши находится над объектом **InkCollector** .<br/>                                                                                                                                                   |
| [**Событие**](inkcollector-mousemove.md)               | Происходит при перемещении указателя мыши над объектом **InkCollector** .<br/>                                                                                                                                                                           |
| [**Кнопка**](inkcollector-mouseup.md)                   | Происходит при отпускании кнопки мыши, когда указатель мыши находится над объектом **InkCollector** .<br/>                                                                                                                                                  |
| [**маусевхил**](inkcollector-mousewheel.md)             | Происходит при движении колесика мыши, когда объект **InkCollector** имеет фокус.<br/>                                                                                                                                                                     |
| [**невинаирпаккетс**](inkcollector-newinairpackets.md)   | Происходит при обнаружении пакета в эфире, который происходит, когда пользователь перемещает перо рядом с планшетом, а курсор находится в окне объекта **InkCollector** , или пользователь перемещает указатель мыши в связанное окно объекта объекта **InkCollector** .<br/> |
| [**невпаккетс**](inkcollector-newpackets.md)             | Происходит, когда объект **InkCollector** получает пакеты.<br/>                                                                                                                                                                                          |
| [**Водок**](inkcollector-stroke.md)                     | Происходит, когда пользователь завершает рисование нового штриха на любом планшете.<br/>                                                                                                                                                                                  |
| [**системжестуре**](inkcollector-systemgesture.md)       | Происходит при распознавании системного жеста.<br/>                                                                                                                                                                                                        |
| [**таблетаддед**](inkcollector-tabletadded.md)           | Происходит при добавлении [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) в систему.<br/>                                                                                                                                                                                 |
| [**таблетремовед**](inkcollector-tabletremoved.md)       | Происходит при удалении [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) из системы.<br/>                                                                                                                                                                             |



 

### <a name="interfaces"></a>Интерфейсы

Класс **InkCollector** определяет эти интерфейсы.



| Интерфейс         | Описание                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **иинкколлектор** | Этот объект реализует COM-интерфейс **иинкколлектор** .<br/> |



 

### <a name="methods"></a>Методы

Класс **InkCollector** имеет следующие методы.



| Метод                                                                              | Описание                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Извлекает текущее состояние конкретного события объекта **InkCollector** , то есть независимо от того, прослушивается событие или используется ли оно.<br/>                |
| [**жетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Возвращает значение, указывающее, заинтересован ли объект **InkCollector** в определенном жесте.<br/>                                                                |
| [**жетвиндовинпутректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Извлекает прямоугольник окна в пикселях, в которых рисуется рукописный ввод.<br/>                                                                               |
| [**сеталлтаблетсмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Этот режим позволяет объекту **InkCollector** получать рукописный ввод с любого планшета, подключенного к планшетному ПК.<br/>                                              |
| [**сетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Изменяет значение, указывающее, следует ли прослушивать или использовать определенное событие.<br/>                                                            |
| [**сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Изменяет интерес объекта **InkCollector** в известном жесте.<br/>                                                                            |
| [**сетсинглетаблетинтегратедмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Этот режим позволяет объекту **InkCollector** получать рукописный ввод только с одного планшета. Рукописный ввод из других планшетов игнорируется объектом **InkCollector** .<br/> |
| [**сетвиндовинпутректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Изменяет прямоугольник окна (в пикселях), используемый для отображения рисуемых рукописных данных в окне.<br/>                                                                    |



 

### <a name="properties"></a>Свойства

Класс **InkCollector** имеет эти свойства.



| Свойство.                                                                             | Тип доступа          | Описание                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ауторедрав**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                             | Только для чтения<br/> | Возвращает или задает значение, указывающее, перерисовывает ли объект **InkCollector** рукописный ввод при недействительности окна.<br/>                                                                 |
| [**коллектингинк**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                       | Только для чтения<br/> | Возвращает значение, указывающее, рисуются ли рукописные данные в объекте **InkCollector** .<br/>                                                                                   |
| [**Режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                     | Только для чтения<br/> | Возвращает или задает режим сбора, определяющий, распознаются ли рукописный ввод, жесты или оба значения при записи пользователем.<br/>                                                                |
| [**Курсоры**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                   | Только для чтения<br/> | Возвращает коллекцию [**курсоров**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) , доступную для использования в области рукописного ввода.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/> | Только для чтения<br/> | Возвращает или задает объект [**инкдравингаттрибутес**](inkdrawingattributes-class.md) по умолчанию, который задает атрибуты рисования, используемые при прорисовке и отображении рукописного ввода.<br/> |
| [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/> | Только для чтения<br/> | Возвращает или задает интерес к аспектам пакета, связанного с рукописным вводом на объекте **InkCollector** .<br/>                                                                          |
| [**динамикрендеринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                   | Только для чтения<br/> | Возвращает или задает значение, указывающее, отображается ли рукописный ввод при прорисовке.<br/>                                                                                                       |
| [**Включен**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                   | Только для чтения<br/> | Возвращает или задает значение, указывающее, собирает ли объект **InkCollector** входные данные пера.<br/>                                                                                       |
| [**Справиться**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                       | Только для чтения<br/> | Возвращает или задает маркер окна, к которому присоединен объект **InkCollector** .<br/>                                                                                           |
| [**Рукописный ввод**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)<br/>                                           | Только для чтения<br/> | Возвращает или задает объект [**инкдисп**](inkdisp-class.md) , связанный с объектом **InkCollector** .<br/>                                                                     |
| [**маргинкс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                   | Только для чтения<br/> | Возвращает или задает поля вдоль оси x (в пикселях).<br/>                                                                                                                             |
| [**Поле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                   | Только для чтения<br/> | Возвращает или задает поля вдоль оси y (в пикселях).<br/>                                                                                                                             |
| [**маусеикон**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                               | Только для чтения<br/> | Возвращает или задает текущий пользовательский значок мыши.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                         | Только для чтения<br/> | Возвращает или задает значение, указывающее тип указателя мыши, отображаемого при наведении указателя мыши на определенную часть объекта.<br/>                                                |
| [**Обработчик**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                 | Только для чтения<br/> | Возвращает или задает объект [**инкрендерер**](inkrenderer-class.md) , используемый для рисования рукописного ввода.<br/>                                                                                        |
| [**суппорсигхконтрастинк**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>     | Только для чтения<br/> | Возвращает или задает значение, указывающее, отображаются ли рукописные данные только в одном цвете, когда система находится в высокая контрастностьном режиме.<br/>                                                           |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                        | Только для чтения<br/> | Возвращает устройство планшета, которое в настоящее время использует объект **InkCollector** для получения данных.<br/>                                                                                      |



 

## <a name="remarks"></a>Remarks

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

Объект **InkCollector** собирает только рукописные данные и жесты, вводимые в конкретное окно, с которым оно связано. Единственной целью **InkCollector** является получение рукописных данных от оборудования (например, через объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) и [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) ) и их доставка в приложение. Фактически он выступает в качестве источника, который распределяет рукописный ввод в один или несколько различных объектов [**инкдисп**](inkdisp-class.md) , которые действуют как контейнеры, содержащие распределенные рукописные данные.

Чтобы использовать объект **InkCollector**, вы создаете его, указываете, в каком окне следует собираются рисуемый рукописный ввод, и включите его. После включения он может быть настроен на получение только в одном из трех режимов (режим указывается в перечислении [**инкколлектионмоде**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) ):

-   Инконли, в котором создается объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .
-   Жестуреонли, в котором создается объект [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .
-   Инканджестуре, в котором создаются штрих, жест или, возможно, в зависимости от того, как приложение обрабатывает события.

Это означает, что при каждом перемещении курсора, находящихся в пределах диапазона планшета, объект **InkCollector** всегда собирает либо штрих, либо жест, а иногда оба. Поддержка жестов встроена с помощью распознавателя жестов Майкрософт.

Объект **InkCollector** обрабатывает все входные данные планшета. Рукописный ввод можно собирать со всех присоединенных планшетов (включая мышь) одновременно. Изменения в объектах [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) и [**иинккурсорбуттон**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton) могут привести к срабатыванию события объектом **InkCollector** .

Объект **InkCollector** также управляет списком курсоров, возникающих во время его существования. Когда **InkCollector** встречает новый курсор, событие [**курсоринранже**](inkcollector-cursorinrange.md) срабатывает с параметром *невкурсор* , установленным в значение **Variant \_ true**. Приложения используют объект **InkCollector** для управления новыми курсорами.

С определенным маркером окна может быть связано несколько элементов **InkCollector** , даже если их области коллекции, задаются в конструкторе или с помощью метода [**сетвиндовинпутректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle) , перекрываются. Однако единственным способом работы этого сценария является то, что каждый объект **InkCollector** вызывает [**сетсинглетаблетинтегратедмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) и использует уникальный планшет. Такое поведение упрощает хранение рукописных данных в отдельном объекте для каждого планшета.

Ошибка возникает, если прямоугольник ввода окна для одного включенного **инкколлекторс** (установленного с помощью свойства [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled) ) перекрывает прямоугольник ввода окна другого включенного объекта **InkCollector**.

> [!Note]  
> Перекрытие может произойти без ошибки, если только один из входных прямоугольников включен в любое известное время.

 

События [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)и [**маусевхил**](inkcollector-mousewheel.md) возвращают координаты x и y в пикселях, а не HIMETRIC единицы, связанные с пространством рукописного ввода. Это обусловлено тем, что эти события заменяют события мыши для приложений, не поддерживающих перо, и эти приложения понимают только пиксели.

> [!Note]  
> Объект **InkCollector** нельзя безопасно освободить в потоке, не являющемся ИП.

 

Чтобы повысить производительность приложения, уничтожайте объект **InkCollector** , когда он больше не нужен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Ссылка на элемент управления InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Класс Инкдисп**](inkdisp-class.md)
</dt> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[Справочник по элементу управления InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

