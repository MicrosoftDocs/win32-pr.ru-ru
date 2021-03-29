---
description: Абстрактный базовый класс для предустановленных вычисляемых классов данных.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Класс Win32_PerfFormattedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990725"
---
# <a name="win32_perfformatteddata-class"></a>\_Класс Win32 перфформаттеддата

Абстрактный базовый класс для предустановленных вычисляемых классов данных. Примером такого класса является [**Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md). Эти классы содержат вычисляемые значения, предоставляемые [поставщиком данных о производительности](../wmisdk/formatted-performance-data-provider.md)с высокой производительностью.

Следующий синтаксис упрощен из MOF-кода и показывает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ перфформаттеддата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ перфформаттеддата** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Краткое текстовое описание для статистики или метрики.

Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание статистики или метрики.

Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).

</dd> <dt>

**Frequency, \_ объект**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Частота в тактах в секунду для свойства **\_ объекта timestamp** . При наличии подклассов поставщик определяет это свойство.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Частота \_ перфтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Частота в тактах в секунду для свойства **Frequency \_ перфтиме** . Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Частота \_ Sys100NS**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Частота в тактах в секунду для свойства **timestamp \_ Sys100NS** (10000000).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Метка, на которой известна статистика или метрика. При создании подклассов это свойство может быть переопределено как свойство ключа.

Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).

</dd> <dt>

**\_Объект timestamp**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отметка времени, определяемая объектом. Поставщик определяет его свойство.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Метка времени \_ перфтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка времени счетчика высокой производительности. Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).

</dd> <dt>

**Метка времени \_ Sys100NS**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение метки времени в единицах 100 нс.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ перфформаттеддата** является производным от [**Win32 \_ Perf**](win32-perf.md), который является производным от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md). Класс находится в **корневом пространстве имен \\ CIMV2** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                             |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Производительность \_ Win32**](win32-perf.md)
</dt> <dt>

[Классы счетчиков производительности](performance-counter-classes.md)
</dt> <dt>

[Доступ к предустановленным классам производительности WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Доступ к данным о производительности в скрипте](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
