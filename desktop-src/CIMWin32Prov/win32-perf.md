---
description: Базовый класс для классов счетчиков производительности Win32 \_ перфравдата и Win32 \_ перфформаттеддата.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Класс Win32_Perf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 356fdba0e2ebb7fb202f4996daa6b1929cd61fc67b028f67e8b041748306c0ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972244"
---
# <a name="win32_perf-class"></a>\_Класс производительности Win32

Базовый класс для классов счетчиков производительности [**Win32 \_ Перфравдата**](win32-perfrawdata.md) и [**Win32 \_ перфформаттеддата**](win32-perfformatteddata.md).

**Win32 \_** Производительность определяет требуемые свойства timestamp и Frequency, используемые в алгоритмах [**CounterType**](../wmisdk/countertype-qualifier.md) для классов счетчиков производительности.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

Класс **\_ производительности Win32** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ производительности Win32** имеет следующие свойства.

<dl> <dt>

**Caption**
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

</dd> <dt>

**Частота \_ перфтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Частота в тактах в секунду для свойства **Frequency \_ перфтиме** . значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Частота \_ Sys100NS**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Частота в тактах в секунду для свойства **timestamp \_ Sys100NS** (10000000).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Имя**
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

</dd> <dt>

**Метка времени \_ перфтиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка времени счетчика высокой производительности. значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Метка времени \_ Sys100NS**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение метки времени в единицах 100 нс.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ производительности Win32** является производным от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                             |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                     |
| DLL<br/>                      | <dl> <dt>WmiPerfInst.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_СТАТИСТИКАЛИНФОРМАТИОН CIM**](cim-statisticalinformation.md)
</dt> <dt>

[Классы счетчиков производительности](performance-counter-classes.md)
</dt> <dt>

[Доступ к предустановленным классам производительности WMI](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[Задачи WMI: Мониторинг производительности](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Доступ к данным о производительности в скрипте](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
