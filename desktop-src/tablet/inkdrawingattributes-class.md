---
description: Представляет атрибуты, применяемые к рукописному вводу при его прорисовке.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Класс Инкдравингаттрибутес (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347905"
---
# <a name="inkdrawingattributes-class"></a>Класс Инкдравингаттрибутес

Представляет атрибуты, применяемые к рукописному вводу при его прорисовке.

**Инкдравингаттрибутес** имеет следующие типы членов:

-   [Интерфейсы](#interfaces)
-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="interfaces"></a>Интерфейсы

Класс **инкдравингаттрибутес** определяет эти интерфейсы.



| Интерфейс                 | Описание                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **иинкдравингаттрибутес** | Этот объект реализует COM-интерфейс **иинкдравингаттрибутес** .<br/> |



 

### <a name="methods"></a>Методы

Класс **инкдравингаттрибутес** содержит следующие методы.



| Метод                         | Описание                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Клонировать**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | Создает дубликат объекта [**инкдисп**](inkdisp-class.md), **инкдравингаттрибутес** или [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) .<br/> |



 

### <a name="properties"></a>Свойства

Класс **инкдравингаттрибутес** имеет следующие свойства.



| Свойство                                                                           | Тип доступа           | Описание                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Сглаживание**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | Чтение/запись<br/> | Возвращает или задает значение, указывающее, смешивается ли цвет переднего плана и фона на границе пера, чтобы увеличить гладкость рукописного штриха.<br/> |
| [**Цвет**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | Чтение/запись<br/> | Возвращает или задает цвет рукописного ввода, нарисованного с помощью этого объекта **инкдравингаттрибутес** .<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | Только для чтения<br/>  | Возвращает коллекцию определяемых приложением данных, которые хранятся в объекте **инкдравингаттрибутес** .<br/>                                                                |
| [**фиттокурве**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | Чтение/запись<br/> | Возвращает или задает значение, указывающее, отображается ли рукописный ввод в виде последовательности кривых, а не линий между точками выборки пера.<br/>                                    |
| [**Высота**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | Чтение/запись<br/> | Возвращает или задает высоту пера при рисовании рукописного ввода с помощью этого объекта **инкдравингаттрибутес** .<br/>                                                                        |
| [**игнорепрессуре**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | Чтение/запись<br/> | Возвращает или задает значение, которое указывает, расширяется ли рисуемый рукописный ввод автоматически при увеличении нажима кончика пера на поверхности планшета.<br/>                     |
| [**пентип**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | Чтение/запись<br/> | Возвращает или задает подсказку пера для использования (шарик или прямоугольник) при рисовании рукописного ввода с помощью этого объекта **инкдравингаттрибутес** .<br/>                                                       |
| [**растероператион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | Чтение/запись<br/> | Возвращает или задает, как цвет пера взаимодействует с существующими цветами фона на экране при прорисовке рукописного ввода.<br/>                                                    |
| [**Прозрачность**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | Чтение/запись<br/> | Возвращает или задает значение прозрачности рисуемого рукописного ввода. Диапазон значений от нуля (абсолютно непрозрачный) до 255 (полностью прозрачный).<br/>                                               |
| [**Ширина**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | Чтение/запись<br/> | Возвращает или задает ширину пера при рисовании рукописного ввода с помощью этого объекта **инкдравингаттрибутес** .<br/>                                                                         |



 

## <a name="remarks"></a>Комментарии

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

Эти атрибуты рисования можно связать с обводкой или курсором и указать такие параметры, как цвет, ширина и прозрачность.

Чтобы указать атрибуты рисования штриха, используйте свойство [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) . Чтобы указать атрибуты рисования всех штрихов в коллекции штрихов, вызовите метод [**модифидравингаттрибутес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Каждый объект [**InkCollector**](inkcollector-class.md) , объект [**InkOverlay**](inkoverlay-class.md) и элемент управления [InkPicture](inkpicture-control-reference.md) могут задавать различные наборы атрибутов рисования для одного и того же курсора. Используйте свойство [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) объекта [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) для получения или задания атрибутов рисования курсора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DrawingAttributes, свойство**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**DrawingAttributes, свойство**
</dt> <dt>

**DrawingAttributes, свойство**
</dt> <dt>

[**DefaultDrawingAttributes, свойство**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**DefaultDrawingAttributes, свойство**
</dt> <dt>

**DefaultDrawingAttributes, свойство**
</dt> <dt>

[**Метод Модифидравингаттрибутес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Класс Инкдисп**](inkdisp-class.md)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

