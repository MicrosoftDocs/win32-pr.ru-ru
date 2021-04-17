---
description: Представляет задание печати, созданное приложением Windows. Любая единица работы, созданная командой print приложения, работающей на компьютере, работающем под управлением операционной системы Windows, является потомком или членом этого класса.
ms.assetid: d884acba-e1b2-4d24-9b55-15d175a163d9
ms.tgt_platform: multiple
title: Класс Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob
- Win32_PrintJob.Caption
- Win32_PrintJob.Description
- Win32_PrintJob.InstallDate
- Win32_PrintJob.Name
- Win32_PrintJob.Status
- Win32_PrintJob.ElapsedTime
- Win32_PrintJob.JobStatus
- Win32_PrintJob.Notify
- Win32_PrintJob.Owner
- Win32_PrintJob.Priority
- Win32_PrintJob.StartTime
- Win32_PrintJob.TimeSubmitted
- Win32_PrintJob.UntilTime
- Win32_PrintJob.Color
- Win32_PrintJob.DataType
- Win32_PrintJob.Document
- Win32_PrintJob.DriverName
- Win32_PrintJob.HostPrintQueue
- Win32_PrintJob.JobId
- Win32_PrintJob.PagesPrinted
- Win32_PrintJob.PaperLength
- Win32_PrintJob.PaperSize
- Win32_PrintJob.PaperWidth
- Win32_PrintJob.Parameters
- Win32_PrintJob.PrintProcessor
- Win32_PrintJob.Size
- Win32_PrintJob.StatusMask
- Win32_PrintJob.TotalPages
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f56034161a9313eed1b7d302ab790d153c0ee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655985"
---
# <a name="win32_printjob-class"></a>\_Класс Win32 PrintJob

[Класс WMI](../wmisdk/retrieving-a-class.md) для **Win32 \_ PrintJob** представляет задание печати, созданное приложением Windows. Любая единица работы, созданная командой print приложения, работающей на компьютере, работающем под управлением операционной системы Windows, является потомком или членом этого класса.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_PrintJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Color;
  string   DataType;
  string   Document;
  string   DriverName;
  string   HostPrintQueue;
  uint32   JobId;
  uint32   PagesPrinted;
  uint32   PaperLength;
  string   PaperSize;
  uint32   PaperWidth;
  string   Parameters;
  string   PrintProcessor;
  uint32   Size;
  uint32   StatusMask;
  uint32   TotalPages;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ PrintJob** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ PrintJob** содержит следующие методы.



| Метод                                                  | Описание                       |
|:--------------------------------------------------------|:----------------------------------|
| [**Пауза**](pause-method-in-class-win32-printjob.md)   | Приостанавливает задание печати.<br/>    |
| [**Возобновить**](resume-method-in-class-win32-printjob.md) | Возобновляет задание печати.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ PrintJob** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Цвет**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, указывающая, печатается ли документ в цвете или монохромный режим. Некоторые цветные принтеры имеют возможность печати с использованием черного цвета, а не сочетания желтого, голубого и пурпурного цветов. Истинный черный цвет обычно создает более темный и яркий текст для документов. Этот параметр удобен только для цветных принтеров, поддерживающих истинную черновую печать.

Значения качества производительности:

<dl><span id="_Color_"></span><span id="_color_"></span><span id="_COLOR_"></span><dt>

**Color**
</dt><span id="_Monochrome_"></span><span id="_monochrome_"></span><span id="_MONOCHROME_"></span><dt>

**Монохромная**
</dt> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Формат данных для этого задания печати. Это предписывает драйверу принтера преобразовать данные (общий текст, PostScript или PCL) перед печатью или распечатать его в необработанном формате (для графики и изображений).

Пример: "TEXT"

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Document**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя задания печати. Пользователь видит это имя при просмотре документов, ожидающих печати.

Пример: "Microsoft Word-Review.doc"

</dd> <dt>

**Имя_драйвера**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя драйвера принтера, используемого для задания печати.

</dd> <dt>

**елапседтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время выполнения задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**хостпринткуеуе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя компьютера, на котором создано задание печати.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Указывает, когда был установлен объект. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор задания. Он используется другими методами в качестве маркера для задания печати на принтере.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, представляющая состояние задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов это свойство может быть переопределено как свойство ключа.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Уведомление**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пользователь получает уведомление о завершении задания или сбое.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**Владелец**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пользователь, отправивший задание.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**пажеспринтед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число печатаемых страниц. Это значение может быть равно 0 (нулю), если задание печати не содержит сведений о разделителях страниц.

</dd> <dt>

**паперленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (десятые доли миллиметра).
</dt> </dl>

Длина бумаги.

Пример: 2794

</dd> <dt>

**паперсизе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Размер бумаги, используемой для печати задания. Значение является одним из возможных размеров бумаги для принтера, указанного в свойстве **паперсизессуппортед** класса [**\_ принтеров Win32**](win32-printer.md) .

</dd> <dt>

**папервидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (десятые доли миллиметра).
</dt> </dl>

Ширина бумаги.

Пример: 2159

</dd> <dt>

**Параметры**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Необязательные параметры для отправки в обработчик заданий печати. Дополнительные сведения см. в описании свойства **принтпроцессор** .

</dd> <dt>

**принтпроцессор**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Служба обработчика печати, используемая для обработки задания печати. Обработчик принтера работает вместе с драйвером принтера для предоставления дополнительных преобразований данных принтера для принтера и может использоваться для предоставления специальных параметров, таких как страница заголовка для задания.

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Важность выполнения задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**Размер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) (в байтах)
</dt> </dl>

Размер задания печати.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время начала задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Строка, указывающая текущее состояние объекта. Можно определить операционное и нерабочее состояние. Оперативное состояние может включать "ОК", "деградация" и "пред Fail". "Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).

Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание". "Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> <dt>

**статусмаск**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Битовая карта возможных состояний, связанных с этим заданием печати.

<dt>

1 (0x1)
</dt> <dd>

Пауза

</dd> <dt>

2 (0x2)
</dt> <dd>

Ошибка

</dd> <dt>

4 (0x4)
</dt> <dd>

Удаление

</dd> <dt>

8 (0x8)
</dt> <dd>

Печати

</dd> <dt>

16 (0x10)
</dt> <dd>

Печать

</dd> <dt>

32 (0x20)
</dt> <dd>

Автономная миграция

</dd> <dt>

64 (0x40)
</dt> <dd>

Бумага

</dd> <dt>

128 (0x80)
</dt> <dd>

Отпечатан

</dd> <dt>

256 (0x100)
</dt> <dd>

Удаленная

</dd> <dt>

512 (0x200)
</dt> <dd>

Заблокированный \_ девк

</dd> <dt>

1024 (0x400)
</dt> <dd>

\_Заявка на вмешательство пользователя \_

</dd> <dt>

2048 (0x800)
</dt> <dd>

Перезагрузить

</dd> </dl>

</dd> <dt>

**тимесубмиттед**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время отправки задания.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> <dt>

**TotalPages**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество страниц, необходимых для выполнения задания. Это значение может быть равно 0 (нулю), если задание печати не содержит сведений о разделителях страниц.

</dd> <dt>

**унтилтиме**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время, когда задание является недопустимым или должно быть остановлено.

Это свойство наследуется [**от \_ задания CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ PrintJob** является производным от [**\_ задания CIM**](cim-job.md).

## <a name="examples"></a>Примеры

В следующем примере кода VBScript описывается получение статистики заданий принтера из экземпляров **Win32 \_ PrintJob**.


```VB
Set PrintJobSet = GetObject("winmgmts:").InstancesOf ("Win32_PrintJob")

If (PrintJobSet.Count = 0) Then WScript.Echo "No print jobs!"
for each PrintJob in PrintJobSet
 WScript.Echo PrintJob.Name
 WScript.Echo PrintJob.JobId
 WScript.Echo PrintJob.Status
 WScript.Echo PrintJob.TotalPages
 Wscript.Echo ""
next
```



В следующем образце кода Perl описывается получение статистики заданий принтера из экземпляров **Win32 \_ PrintJob**.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($PrintJobset, $PrintJob);
eval {$PrintJobset = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 InstancesOf ("Win32_PrintJob") };
if (!$@ && defined $PrintJobset)
{
 if ($PrintJobset->{Count} == 0 ) 
 {
  print "\nNo print jobs!\n";
 }

 foreach $PrintJob (in $PrintJobset)
 {
  print $PrintJob->{Name} , "\n";
  print $PrintJob->{JobId} , "\n";
  print $PrintJob->{Status} , "\n";
  print $PrintJob->{TotalPages} , "\n";
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
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

[**\_Задание CIM**](./cim-job.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
