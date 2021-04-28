---
description: Класс Инкдисп — представляет собранные штрихи рукописного ввода в пределах пространства рукописного ввода.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Класс Инкдисп (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4214d6b03e5823bd5012017e418066763c8132c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109992"
---
# <a name="inkdisp-class"></a>Класс Инкдисп

Представляет собранные штрихи рукописного ввода в пределах пространства рукописного ввода.

**Инкдисп** имеет следующие типы членов:

-   [События](#events)
-   [Интерфейсы](#interfaces)
-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="events"></a>События

Класс **инкдисп** содержит следующие события.



| Событие                                    | Описание                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**инкаддед**](inkdisp-inkadded.md)     | Происходит при добавлении штриха к объекту **инкдисп** .<br/>     |
| [**инкделетед**](inkdisp-inkdeleted.md) | Происходит при удалении штриха из объекта **инкдисп** .<br/> |



 

### <a name="interfaces"></a>Интерфейсы

Класс **инкдисп** определяет эти интерфейсы.



| Интерфейс    | Описание                                                       |
|:-------------|:------------------------------------------------------------------|
| **иинкдисп** | Этот объект реализует COM-интерфейс **иинкдисп** .<br/> |



 

### <a name="methods"></a>Методы

Класс **инкдисп** содержит следующие методы.



| Метод                                                                   | Описание                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддстрокесатректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | Вставляет коллекцию штрихов в объект **инкдисп** на заданном прямоугольнике.<br/>                                                                                                       |
| [**канпасте**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | Указывает, можно ли преобразовать [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) в объект **инкдисп** .<br/>                                                                                       |
| [**Усечения**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | Удаляет части штриха или коллекции штрихов, находящихся за пределами прямоугольника.<br/>                                                                                                       |
| [**клипбоардкопи**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | Копирует коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) в буфер обмена.<br/>                                                                                                           |
| [**клипбоардкопивисректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | Копирует объекты [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , содержащиеся в известном прямоугольнике, в буфер обмена.<br/>                                                               |
| [**клипбоардпасте**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | Копирует [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) из буфера обмена в объект **инкдисп** .<br/>                                                                                               |
| [**Clone (Клонировать)**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | Создает дубликат объекта **инкдисп** .<br/>                                                                                                                                                   |
| [**креатестроке**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | Создает штрих по точкам или данным пакетов.<br/>                                                                                                                                              |
| [**креатестрокес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | Создает коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) для этого объекта **инкдисп** .<br/>                                                                                                |
| [**делетестроке**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | Удаляет штрих из объекта **инкдисп** .<br/>                                                                                                                                             |
| [**делетестрокес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | Удаляет штрихи из объекта **инкдисп** .<br/>                                                                                                                                              |
| [**Метод Екстрактстрокес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | Извлекает штрихи из объекта **инкдисп** и возвращает новый объект **инкдисп** , содержащий извлеченные штрихи.<br/>                                                                       |
| [**Метод Екстрактвисректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | Вырезает или копирует штрихи из существующего объекта **класса инкдисп** и вставляет их в новый объект **класса инкдисп** , используя известный прямоугольник для определения штрихов, которые нужно извлечь.<br/> |
| [**жетбаундингбокс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | Извлекает ограничивающий прямоугольник всех штрихов в объекте **инкдисп** .<br/>                                                                                                               |
| [**хиттестЦиркле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | Извлекает коллекцию [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которая полностью находится внутри известного круга или пересекается ей.<br/>                                                  |
| [**хиттествислассо**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | Извлекает штрихи в области выделения ломаной линии.<br/>                                                                                                                                   |
| [**хиттествисректангле**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | Извлекает штрихи, содержащиеся в указанном прямоугольнике.<br/>                                                                                                                    |
| [**Загрузка**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | Заполняет новый объект **инкдисп** известными двоичными данными.<br/>                                                                                                                                |
| [**неарестпоинт**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | Извлекает [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) в объекте **инкдисп** , который является ближайшим к известной точке, при необходимости предоставляя дополнительные сведения.<br/>                       |
| [**Сохранить**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | Преобразует рукописный ввод в указанный формат и возвращает двоичные данные.<br/>                                                                                                                       |



 

### <a name="properties"></a>Свойства

Класс **инкдисп** имеет следующие свойства.



| Свойство                                                                           | Тип доступа           | Описание                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**кустомстрокес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | Только для чтения<br/>  | Возвращает коллекцию [**иинккустомстрокес**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) , которая должна быть сохранена с рукописным вводом.<br/>                             |
| [**Бит**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | Чтение/запись<br/> | Возвращает или задает значение, указывающее, был ли изменен объект **инкдисп** со времени последнего сохранения рукописного ввода.<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Только для чтения<br/>  | Возвращает коллекцию определяемых приложением данных.<br/>                                                                             |
| [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | Только для чтения<br/>  | Возвращает коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , содержащуюся в объекте **инкдисп** .<br/>                             |



 

## <a name="remarks"></a>Remarks

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

> [!Note]  
> Первый экземпляр этого объекта также приводит к созданию экземпляра GDI+. Побочный результат заключается в том, что если вы используете один объект рукописного ввода в цикле и создаете и уничтожаете его в цикле, вы заставите экземпляр GDI+ выполняться повторно. Это может привести к снижению производительности приложения. Чтобы предотвратить это, следует постоянно размещать один экземпляр объекта рукописного ввода, пока приложение использует рукописный ввод.

 

Объект **инкдисп** — это контейнер данных росчерка (Point). Данные штриха или точки, собранные пером, помещаются в объект **инкдисп** . Свойство [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) содержит данные для всех штрихов в объекте **инкдисп** .

Объект [**InkCollector**](inkcollector-class.md) , объект [**InkOverlay**](inkoverlay-class.md) и элемент управления [InkPicture](inkpicture-control-reference.md) собирают точки из входного устройства и помещают их в объект **инкдисп** . Эти объекты по сути действуют как источник, который распределяет рукописный ввод в один или несколько различных объектов **инкдисп** , которые действуют как контейнеры, содержащие распределенные рукописные данные.

Пространство для рукописного ввода — это виртуальное пространство координат, с которым сопоставляются координаты контекста планшета. Это пространство зафиксировано в системе координат HIMETRIC. В координатах рукописного пространства перемещение от 0 до 1 равно 1 HIMETRIC единице. Это сопоставление упрощает связывание нескольких объектов **инкдисп** .

Объект [**инкрендерер**](inkrenderer-class.md) управляет сопоставлениями рукописного ввода и окна отображения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[Коллекция Инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Интерфейс Иинктаблет**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

