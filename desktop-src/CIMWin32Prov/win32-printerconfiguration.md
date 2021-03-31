---
description: '\_Класс WMI принтерконфигуратион для Win32 представляет конфигурацию для печатающего устройства. Сюда входят такие возможности, как разрешение, цвет, шрифты и ориентация.'
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Класс Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990696"
---
# <a name="win32_printerconfiguration-class"></a>\_Класс Win32 принтерконфигуратион

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ принтерконфигуратион для Win32** представляет конфигурацию для печатающего устройства. Сюда входят такие возможности, как разрешение, цвет, шрифты и ориентация.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ принтерконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ принтерконфигуратион** имеет следующие свойства.

<dl> <dt>

**битсперпел**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Число битов, используемых для представления цвета в этой конфигурации (бит на пиксель). Это свойство устарело. Вместо этого используйте свойства в классах [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) , чтобы определить, как представлен цвет.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Краткое текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**Разобрать по копиям**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, то печатаемые страницы должны быть упорядочены по копиям. Чтобы выполнить сортировку, необходимо напечатать весь документ перед печатью следующей копии, а не выводить на печать каждую страницу документа необходимое число раз.

Это свойство игнорируется, если драйвер принтера не поддерживает параметры сортировки.

</dd> <dt>

**Цвет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Цвет документа. Некоторые цветовые принтеры могут печататься с помощью черно-белого цвета вместо сочетания голубого, пурпурного и желтого (КМИ). Обычно это позволяет создавать более темный и яркий текст для документов. Этот параметр удобен только для цветных принтеров, поддерживающих истинную черновую печать.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Монохромный (истинный черный)

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Цвет

</dd> </dl>

</dd> <dt>

**Копии**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число печатаемых копий. Драйвер принтера должен поддерживать печать многостраничных копий.

Пример: 2

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание текущего объекта.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**DeviceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Понятное имя принтера. Это имя является уникальным для типа принтера и может быть усечено из-за ограничений строки, из которой он является производным.

Пример: PCL или HP LaserJet

</dd> <dt>

**дисплайфлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли устройство вывода цветным или монохромным, а также тип сканирования — не с чередованием или с чередованием. Это свойство устарело. Вместо этого используйте свойства дисплея, такие как свойство **дисплайтипе** класса **Win32 \_ десктопмонитор** .

</dd> <dt>

**дисплайфрекуенци**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображает частоту обновления по вертикали. Частота обновления монитора — это число перерисовок экрана в секунду (частота). Это свойство устарело. Вместо этого используйте свойства в классе [**Win32 \_ Видеоконтроллер**](win32-videocontroller.md), [**Win32 \_ десктопмонитор**](win32-desktopmonitor.md)или [**CIM \_ видеоконтроллерресолутион**](cim-videocontrollerresolution.md) .

</dd> <dt>

**дисертипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип сглаживания принтера. Это свойство может принимать стандартные значения от 1 до 5 или определенные драйвером значения от 6 до 256. Дизеринг в виде графика — это специальный метод сглаживания, который обеспечивает четко определенные границы между черным, белым и серым масштабированием. Он не подходит для изображений, которые включают непрерывное окончание интенсивности и оттенков, например отсканированных фотографий.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Без сглаживания

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Грубая кисть

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

Тонкая кисть

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**четырех**


</dt> <dd>

График

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5.0**


</dt> <dd>

Оттенки серого

</dd> </dl>

</dd> <dt>

**дриверверсион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Номер версии драйвера принтера на основе Windows. Номера версий создаются и обслуживаются производителем драйвера.

</dd> <dt>

**Дуплекс**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, печать выполняется на обеих сторонах. Если **значение равно false**, печать выполняется только на одной стороне носителя.

</dd> <dt>

**формнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Не поддерживается.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (точек на дюйм)
</dt> </dl>

Разрешение печати в точках на дюйм вдоль оси x (ширины) задания печати (аналогично устаревшему свойству **ксресолутион** ). Это значение задается, только если свойство **принткуалити** этого класса является положительным.

</dd> <dt>

**икминтент**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конкретное значение одного из трех возможных методов сопоставления цветов (целей), которые должны использоваться по умолчанию. ICM приложения устанавливают намерения, используя функции ICM. Это свойство может принимать стандартные значения от 1 до 3 или определенные драйвером значения от 4 до 256. Приложения, не использующие ICM, могут использовать это значение для определения того, как принтер обрабатывает задания цветовой печати.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Насыщенность

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Контраст

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

Точный цвет

</dd> </dl>

</dd> <dt>

**икммесод**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Как обрабатывается ICM. Для приложения, не поддерживающего ICM, это свойство определяет, включен или отключен ICM. Для ICM приложений Система проверяет это свойство, чтобы определить, какая часть системы компьютера обрабатывает поддержку ICM.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Выключено

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Windows

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

Драйвер устройства

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**четырех**


</dt> <dd>

Устройство

</dd> </dl>

</dd> <dt>

**логпикселс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Число пикселей на логический дюйм. Это устаревшее свойство допустимо только для устройств, работающих с пикселями, исключая такие устройства, как принтеры. Не существует замещающего значения, которое применяется к принтерам.

</dd> <dt>

**Мультимедиа**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип носителя, на котором печатается принтер. Свойству может быть присвоено предопределенное значение или значение, определенное драйвером, которое больше или равно 256.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Standard

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Прозрачность

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

Глянцевое

</dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Имя принтера, с которым связана эта конфигурация. Это значение соответствует свойству **Name** связанного экземпляра [**\_ принтера Win32**](win32-printer.md) .

</dd> <dt>

**Ориентация**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ориентация бумаги для печати.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Книжная

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**открыт**


</dt> <dd>

Альбомная

</dd> </dl>

</dd> <dt>

**паперленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (десятые доли миллиметра)
</dt> </dl>

Длина бумаги. Чтобы определить размер бумаги в дюймах, разделите это значение на 254.

Пример: 2794

</dd> <dt>

**паперсизе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Размер бумаги. Возможные размеры находятся в свойстве **паперсизессуппортед** соответствующего класса [**\_ принтера Win32**](win32-printer.md) .

Пример: "A4 или Letter".

</dd> <dt>

**папервидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (десятые доли миллиметра)
</dt> </dl>

Ширина бумаги. Чтобы определить размер бумаги в дюймах, разделите это значение на 254.

Пример: 2159

</dd> <dt>

**пелшеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Данное свойство не поддерживается.

</dd> <dt>

**пелсвидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Данное свойство не поддерживается.

</dd> <dt>

**PrintQuality**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Один из четырех уровней качества задания печати. Если указано положительное значение, качество измеряется в точках на дюйм.

<dt>

<span id="-1"></span>

<span id="-1"></span>**-1**


</dt> <dd>

Черновик

</dd> <dt>

<span id="-2"></span>

<span id="-2"></span>**-2**


</dt> <dd>

Низкий

</dd> <dt>

<span id="-3"></span>

<span id="-3"></span>**-3**


</dt> <dd>

Средний

</dd> <dt>

<span id="-4"></span>

<span id="-4"></span>**по 4**


</dt> <dd>

Высокий

</dd> </dl>

</dd> <dt>

**Масштабирование**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (в процентах)
</dt> </dl>

Коэффициент, на который должны масштабироваться печатаемые выходные данные. Например, масштаб 75 уменьшает вывод на печать до 3/4 ее первоначальной высоты и ширины.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Идентификатор, по которому известен текущий объект.

Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).

</dd> <dt>

**спеЦификатионверсион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Номер версии данных инициализации для устройства, связанного с принтером на основе Windows.

</dd> <dt>

**ттоптион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как должны печататься шрифты TrueType.

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Точечный рисунок** (1)


</dt> <dd>

Выводит шрифты TrueType в виде графики. Это действие по умолчанию для принтеров с матричными точками.

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Загрузка** (2)


</dt> <dd>

Скачивает шрифты TrueType в виде загружаемых шрифтов. Это действие по умолчанию для принтеров, использующих язык управления принтерами (PCL).

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Замена** (3)


</dt> <dd>

Замещает шрифты устройства для шрифтов TrueType. Это действие по умолчанию для принтеров PostScript.

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (точек на дюйм)
</dt> </dl>

Разрешение печати вдоль оси y (высота) задания печати (аналогично устаревшему свойству **иресолутион** ). Это значение задается, только если свойство **принткуалити** этого класса является положительным.

</dd> <dt>

**ксресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Это свойство устарело. Вместо этого используйте свойство **хоризонталресолутион** .

</dd> <dt>

**иресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Это свойство устарело. Вместо этого используйте свойство **вертикалресолутион** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ принтерконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).

**Обзор**

Прежде чем можно будет определить оптимальный способ распространения и использования ресурсов печати, необходимо получить подробные сведения об этих ресурсах. Например, в отделе A может быть только три принтера по сравнению с пятью принтерами в отделе б. Однако если принтеры в подразделении A могут печатать 20 страниц в минуту, а принтеры в отделе б могут печатать только 5 страниц в минуту, у пользователей в подразделении есть больше возможностей для печати. Не зная подробных сведений об этих принтерах, вы можете по ошибке завершить этот отдел а немного поработать с возможностями печати и, таким же, приобрести дополнительные принтеры, которые в итоге будут неиспользуемыми.

WMI включает два класса: [**« \_ принтер Win32**](win32-printer.md) » и « **Win32 \_ принтерконфигуратион**», которые можно использовать для получения подробных сведений обо всех принтерах, установленных на компьютере.

## <a name="examples"></a>Примеры

В следующем примере кода извлекаются сведения о принтере.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Параметр CIM**](./cim-setting.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
