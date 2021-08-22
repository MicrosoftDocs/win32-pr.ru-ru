---
description: Представляет объект, который удобен для сценариев заметок, в которых пользователи не связаны с распознаванием рукописного ввода, а зависят от размера, формы, цвета и положения рукописного ввода.
ms.assetid: 61191ab3-075e-458b-9e0f-4bc255687b3c
title: Класс InkOverlay (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkOverlay
- InkOverlay.IInkOverlay
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d1a818c1fef9006abad2dd31da5a41f43aeb3df9a9b75d348d8987938abfcea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967123"
---
# <a name="inkoverlay-class"></a>Класс InkOverlay

Представляет объект, который удобен для сценариев заметок, в которых пользователи не связаны с распознаванием рукописного ввода, а зависят от размера, формы, цвета и положения рукописного ввода.

Создание элемента управления **InkOverlay** за прозрачным элементом управления (например, GroupBox с \_ \_ набором свойств WS ex) предотвратит Сбор рукописных данных на **InkOverlay** .

В **InkOverlay** имеются следующие типы членов:

-   [События](#events)
-   [Интерфейсы](#interfaces)
-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="events"></a>События

Класс **InkOverlay** имеет эти события.



| Событие                                                     | Описание                                                                                                                                                                                                                                               |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**курсорбуттондовн**](inkcollector-cursorbuttondown.md) | Происходит, когда **InkOverlay** обнаруживает недоступную кнопку курсора.<br/>                                                                                                                                                                           |
| [**курсорбуттонуп**](inkcollector-cursorbuttonup.md)     | Происходит, когда **InkOverlay** обнаруживает нажатую кнопку курсора.<br/>                                                                                                                                                                             |
| [**курсордовн**](inkcollector-cursordown.md)             | Происходит, когда подсказка курсора обращается к поверхности планшета в дигитайзере.<br/>                                                                                                                                                                             |
| [**курсоринранже**](inkcollector-cursorinrange.md)       | Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.<br/>                                                                                                                                                    |
| [**курсораутофранже**](inkcollector-cursoroutofrange.md) | Происходит, когда курсор покидает диапазон физического обнаружения (близость) контекста планшета.<br/>                                                                                                                                                  |
| [**DoubleClick**](inkcollector-doubleclick.md)           | Происходит при двойном щелчке объекта **InkOverlay** .<br/>                                                                                                                                                                                       |
| [**жесты**](inkcollector-gesture.md)                   | Происходит при распознавании жеста конкретного приложения.<br/>                                                                                                                                                                                     |
| [**Вниз**](inkcollector-mousedown.md)               | Происходит при нажатии кнопки мыши, когда указатель мыши находится над объектом **InkOverlay** .<br/>                                                                                                                                                 |
| [**Событие**](inkcollector-mousemove.md)               | Происходит при перемещении указателя мыши над объектом **InkOverlay** .<br/>                                                                                                                                                                         |
| [**Кнопка**](inkcollector-mouseup.md)                   | Происходит при отпускании кнопки мыши, когда указатель мыши находится над объектом **InkOverlay** .<br/>                                                                                                                                                |
| [**маусевхил**](inkcollector-mousewheel.md)             | Происходит при движении колесика мыши, когда объект **InkOverlay** имеет фокус.<br/>                                                                                                                                                                   |
| [**невинаирпаккетс**](inkcollector-newinairpackets.md)   | Происходит при обнаружении пакета в эфире, который происходит, когда пользователь перемещает перо рядом с планшетом, а курсор находится в окне объекта **InkOverlay** , или пользователь перемещает указатель мыши в связанное окно объекта объекта **InkOverlay** .<br/> |
| [**невпаккетс**](inkcollector-newpackets.md)             | Происходит, когда объект **InkOverlay** получает пакеты.<br/>                                                                                                                                                                                        |
| [**Окрашивает**](inkoverlay-painted.md)                     | Происходит при завершении перерисовки объекта **InkOverlay** .<br/>                                                                                                                                                                          |
| [**Оформленные**](inkoverlay-painting.md)                   | Происходит перед перерисовкой объекта **InkOverlay** .<br/>                                                                                                                                                                                        |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)   | Происходит при изменении выделения рукописных данных в элементе управления, например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                       |
| [**селектиончангинг**](inkoverlay-selectionchanging.md) | Происходит при изменении выделения рукописных данных в элементе управления, например при выполнении изменений в пользовательском интерфейсе, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                |
| [**селектионмовед**](inkoverlay-selectionmoved.md)       | Происходит при изменении расположения текущего выделения, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                         |
| [**селектионмовинг**](inkoverlay-selectionmoving.md)     | Происходит, когда расположение текущего выделения собирается измениться, например, посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                  |
| [**селектионресизед**](inkoverlay-selectionresized.md)   | Происходит при изменении размера текущего выделения, например с помощью изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                             |
| [**селектионресизинг**](inkoverlay-selectionresizing.md) | Происходит, когда размер текущего выделения собирается измениться, например посредством изменений пользовательского интерфейса, процедур копирования и вставки или свойства [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .<br/>                                      |
| [**Водок**](inkcollector-stroke.md)                     | Происходит, когда пользователь завершает рисование нового штриха на любом планшете.<br/>                                                                                                                                                                              |
| [**строкесделетед**](inkoverlay-strokesdeleted.md)       | Происходит после удаления штрихов из свойства [**рукописного ввода**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                      |
| [**строкесделетинг**](inkoverlay-strokesdeleting.md)     | Происходит перед удалением штрихов из свойства [**рукописного ввода**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .<br/>                                                                                                                                                           |
| [**системжестуре**](inkcollector-systemgesture.md)       | Происходит при распознавании системного жеста.<br/>                                                                                                                                                                                                    |
| [**таблетаддед**](inkcollector-tabletadded.md)           | Происходит при добавлении [**иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) в систему.<br/>                                                                                                                                                                        |
| [**таблетремовед**](inkcollector-tabletremoved.md)       | Происходит при удалении [**планшета**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) из системы.<br/>                                                                                                                                                                         |



 

### <a name="interfaces"></a>Интерфейсы

Класс **InkOverlay** определяет эти интерфейсы.



| Интерфейс       | Описание                                                          |
|:----------------|:---------------------------------------------------------------------|
| **иинковерлай** | Этот объект реализует COM-интерфейс **иинковерлай** .<br/> |



 

### <a name="methods"></a>Методы

Класс **InkOverlay** имеет следующие методы.



| Метод                                                                              | Описание                                                                                                                                                |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw)                                                     | Задает прямоугольник, в котором необходимо перерисовать рукописный ввод в объекте **InkOverlay** .<br/>                                                                   |
| [**жетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-geteventinterest)                           | Возвращает текущее состояние конкретного события объекта **InkOverlay** , то есть независимо от того, прослушивается событие или используется ли оно.<br/>                |
| [**жетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus)                           | Возвращает значение, указывающее, заинтересован ли объект **InkOverlay** в определенном жесте.<br/>                                                                |
| [**жетвиндовинпутректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getwindowinputrectangle)             | Извлекает прямоугольник окна в пикселях, в которых рисуется рукописный ввод.<br/>                                                                           |
| [**хиттестселектион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-hittestselection)                             | Определяет, какая часть выделения была достигнута во время проверки попадания.<br/>                                                                             |
| [**сеталлтаблетсмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode)                         | Этот режим позволяет объекту **InkOverlay** получать рукописный ввод с любого планшета, подключенного к планшетному ПК.<br/>                                            |
| [**сетевентинтерест**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-seteventinterest)                           | Указывает, следует ли прослушивать или использовать определенное событие.<br/>                                                                                   |
| [**сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)                           | Задает интерес к объекту **InkOverlay** в известном жесте.<br/>                                                                              |
| [**сетсинглетаблетинтегратедмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode) | Этот режим позволяет объекту **InkOverlay** получать рукописные данные только с одного планшета. Рукописный ввод из других планшетов игнорируется объектом **InkOverlay** .<br/> |
| [**сетвиндовинпутректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle)             | Задает прямоугольник окна (в пикселях), используемый для отображения рисуемых рукописных данных в окне.<br/>                                                                    |



 

### <a name="properties"></a>Свойства

Класс **InkOverlay** имеет эти свойства.



| Свойство                                                                                       | Тип доступа           | Описание                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аттачмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode)<br/>                                         | Чтение/запись<br/> | Возвращает или задает значение, указывающее, присоединен ли объект **InkOverlay** позади или перед известным окном.<br/>                                                       |
| [**ауторедрав**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)<br/>                                       | Чтение/запись<br/> | Возвращает или задает значение, указывающее, будет ли **InkOverlay** перерисовывать рукописный ввод при недействительности окна.<br/>                                                                   |
| [**коллектингинк**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink)<br/>                                 | Только для чтения<br/>  | Возвращает значение, указывающее, рисуются ли рукописные данные в объекте **InkOverlay** .<br/>                                                                                     |
| [**Режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode)<br/>                               | Чтение/запись<br/> | Возвращает или задает режим сбора, определяющий, распознаются ли рукописный ввод, жесты или оба значения при записи пользователем.<br/>                                                                |
| [**Курсоры**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors)<br/>                                             | Только для чтения<br/>  | Возвращает коллекцию [**курсоров**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors) , доступную для использования в области рукописного ввода.<br/>                                                                                |
| [**DefaultDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)<br/>           | Чтение/запись<br/> | Возвращает или задает объект [**инкдравингаттрибутес**](inkdrawingattributes-class.md) по умолчанию, который задает атрибуты рисования, используемые при прорисовке и отображении рукописного ввода.<br/> |
| [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)<br/>           | Чтение/запись<br/> | Возвращает или задает интерес к аспектам пакета, связанного с рукописным вводом объекта **InkOverlay** .<br/>                                                                            |
| [**динамикрендеринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering)<br/>                             | Чтение/запись<br/> | Возвращает или задает значение, указывающее, отображается ли рукописный ввод при прорисовке.<br/>                                                                                                       |
| [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)<br/>                                       | Чтение/запись<br/> | Возвращает или задает значение, указывающее, находится ли **InkOverlay** в режиме рукописного ввода, режиме удаления или в режиме выбора/правки.<br/>                                                          |
| [**Включен**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled)<br/>                                             | Чтение/запись<br/> | Возвращает или задает значение, указывающее, собирает ли объект **InkOverlay** входные данные пера.<br/>                                                                                         |
| [**ерасермоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)<br/>                                         | Чтение/запись<br/> | Возвращает или задает значение, указывающее, удаляются ли рукописные данные по штрихам или по точкам.<br/>                                                                                                  |
| [**ерасервидс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_eraserwidth)<br/>                                       | Чтение/запись<br/> | Возвращает или задает значение, указывающее ширину кончика пера ластика.<br/>                                                                                                              |
| [**Справиться**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd)<br/>                                                 | Чтение/запись<br/> | Возвращает или задает маркер окна, к которому присоединен объект **InkOverlay** .<br/>                                                                                             |
| [**Рукописный ввод**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_ink)<br/>                                                       | Чтение/запись<br/> | Возвращает или задает объект [**инкдисп**](inkdisp-class.md) , связанный с объектом **InkOverlay** .<br/>                                                                       |
| [**маргинкс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx)<br/>                                             | Чтение/запись<br/> | Возвращает или задает поля вдоль оси x (в пикселях).<br/>                                                                                                                             |
| [**Поле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy)<br/>                                             | Чтение/запись<br/> | Возвращает или задает поля вдоль оси y (в пикселях).<br/>                                                                                                                             |
| [**маусеикон**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon)<br/>                                         | Чтение/запись<br/> | Возвращает или задает текущий пользовательский значок мыши.<br/>                                                                                                                                       |
| [**MousePointer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer)<br/>                                   | Чтение/запись<br/> | Возвращает или задает значение, указывающее тип указателя мыши, отображаемого при наведении указателя мыши на определенную часть объекта.<br/>                                                |
| [**Обработчик**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)<br/>                                           | Чтение/запись<br/> | Возвращает или задает объект [**инкрендерер**](inkrenderer-class.md) , используемый для рисования рукописного ввода.<br/>                                                                                        |
| [**Выбор**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)<br/>                                           | Чтение/запись<br/> | Возвращает или задает коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , выбранную в данный момент в элементе управления **InkOverlay** .<br/>                                                 |
| [**суппорсигхконтрастинк**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink)<br/>               | Чтение/запись<br/> | Возвращает или задает значение, указывающее, отображаются ли рукописные данные только в одном цвете, когда система находится в высокая контрастностьном режиме.<br/>                                                           |
| [**суппорсигхконтрастселектионуи**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_supporthighcontrastselectionui)<br/> | Чтение/запись<br/> | Возвращает или задает значение, указывающее, будет ли весь пользовательский интерфейс выделения отображаться в режиме высокой контрастности, если система находится в высокая контрастностьном.<br/>                                                  |
| [**Tablet**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_tablet)<br/>                                                  | Только для чтения<br/>  | Возвращает устройство планшета, которое в настоящее время использует объект **InkOverlay** для получения входных данных.<br/>                                                                                        |



 

## <a name="mfc-implementation-notes"></a>Заметки о реализации MFC

Если вы присоединяете объект InkOverlay к объекту CView, освободите объект InkOverlay в ответ на сообщение WM \_ destroy, как показано в следующем примере:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="remarks"></a>Remarks

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

Объект **InkOverlay** хорошо подходит для создания заметок и создания базовых кривых. Основным предполагаемым использованием этого объекта является отображение рукописных данных в виде рукописных данных.

Как правило, Пользовательский интерфейс времени выполнения для этого объекта является прозрачным окном с непрозрачным рукописным вводом.

События [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), [**MouseUp**](inkcollector-mouseup.md)и [**маусевхил**](inkcollector-mousewheel.md) возвращают координаты x и координаты y в пикселях, а не HIMETRIC единицы, связанные с пространством рукописного ввода. Это обусловлено тем, что эти события заменяют события мыши для приложений, не поддерживающих перо, и эти приложения понимают только пиксели.

> [!Caution]  
> Если вы настраиваете свойство [**аттачмоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode) объекта **InkOverlay** на onfront, создайте объект **InkOverlay** в потоке, в котором выполняется форма. Приложение может перестать отвечать, если объект **InkOverlay** создан в другом потоке, а его свойство **аттачмоде** имеет значение onfront.

 

> [!Note]  
> Объект **InkOverlay** нельзя безопасно освободить в потоке, не являющемся ИП.

 

Чтобы повысить производительность приложения, удалите объект **InkOverlay** , когда он больше не нужен.

Если вы присоединяете объект InkOverlay к объекту CView, освободите объект InkOverlay в ответ на сообщение WM \_ destroy, как показано в следующем примере:


```C++
BOOL CRecognitionAlternatesSampleCppView::OnWndMsg(UINT msg, WPARAM wp, PARAM lp, LRESULT *pLR)
{
    if(WM_DESTROY == msg)
        m_spInkOverlay.Release();
    return CView::OnWndMsg(msg, wp, lp, pLR);
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс InkCollector**](inkcollector-class.md)
</dt> <dt>

[Справочник по элементу управления InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[Ссылка на элемент управления InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

