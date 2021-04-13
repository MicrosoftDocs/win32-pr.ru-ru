---
description: '&Win32 \_ пажефилеусаже \# 8194; Класс WMI представляет файл, используемый для обработки обмена файлами виртуальной памяти в системе Win32. Сведения, содержащиеся в объектах, созданных из этого класса, указывают состояние файла подкачки во время выполнения.'
ms.assetid: 635d7bd0-3738-4092-8b76-5e9583e079a9
ms.tgt_platform: multiple
title: Класс Win32_PageFileUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileUsage
- Win32_PageFileUsage.Caption
- Win32_PageFileUsage.Description
- Win32_PageFileUsage.InstallDate
- Win32_PageFileUsage.Status
- Win32_PageFileUsage.AllocatedBaseSize
- Win32_PageFileUsage.CurrentUsage
- Win32_PageFileUsage.Name
- Win32_PageFileUsage.PeakUsage
- Win32_PageFileUsage.TempPageFile
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9885bea242a9f2b781ccb0dcac479248a9ccc538
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539224"
---
# <a name="win32_pagefileusage-class"></a>\_Класс Win32 пажефилеусаже

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ пажефилеусаже для Win32** представляет файл, используемый для обработки обмена файлами виртуальной памяти в системе Win32. Сведения, содержащиеся в объектах, созданных из этого класса, указывают состояние файла подкачки во время выполнения.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{9B3AC16A-EEE5-11d2-B13B-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileUsage : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AllocatedBaseSize;
  uint32   CurrentUsage;
  string   Name;
  uint32   PeakUsage;
  boolean  TempPageFile;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ пажефилеусаже** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ пажефилеусаже** имеет следующие свойства.

<dl> <dt>

**аллокатедбасесизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| двтоталпажефиле"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")
</dt> </dl>

Фактический объем дискового пространства, выделенный для использования с этим файлом страницы. Это значение соответствует диапазону, установленному в [**Win32 \_ пажефилесеттинг**](win32-pagefilesetting.md) в свойствах **инитиалсизе** и **MaximumSize** , которые устанавливаются при запуске системы.

Пример: 178

</dd> <dt>

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

**куррентусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus)"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")
</dt> </dl>

Объем места на диске, занятый в настоящий момент файлом подкачки.

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

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Имя файла подкачки.

Пример: "C: \\PAGEFILE.SYS"

</dd> <dt>

**пеакусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("мегабайт")
</dt> </dl>

Файл подкачки с наибольшим использованием.

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

**темппажефиле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Управление \\ \\ \\ \\ памятью диспетчер сеансов \| темппажефиле")
</dt> </dl>

**Значение true** показывает, что временный файл подкачки был создан, обычно потому, что в текущей компьютерной системе нет постоянного файла подкачки.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ пажефилеусаже** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЛОГИКАЛЕЛЕМЕНТ CIM**](cim-logicalelement.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
