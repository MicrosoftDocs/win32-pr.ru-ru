---
description: Этот класс представляет задание операции экспорта точки ссылки на виртуальную систему.
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Класс Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547295"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a>\_Класс мсвм виртуалсистемреференцепоинтекспортжоб

Этот класс представляет задание операции экспорта точки ссылки на виртуальную систему.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемреференцепоинтекспортжоб** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ виртуалсистемреференцепоинтекспортжоб** содержит следующие методы.



| Метод                                                                                     | Описание                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**Ошибка**](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | Извлекает ошибку.<br/>                    |
| [**жетеррорекс**](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | Извлекает дополнительные сведения об ошибке.<br/> |
| [**Равен**](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | Запрашивает изменение состояния.<br/>                |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемреференцепоинтекспортжоб** имеет следующие свойства.

<dl> <dt>

**басереференцепоинтид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID точки ссылки, используемой в качестве базы для операции экспорта.

</dd> <dt>

**Отменяемых**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли отменить задание. Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ Задание CIM**](cim-job.md)".**ErrorCode**")
</dt> </dl>

Содержит описание ошибки.

</dd> <dt>

**експортдиректори**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Расположение экспорта.

</dd> <dt>

**експортедконфигфилепас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к экспортированному файлу конфигурации.

</dd> <dt>

**експортеддискс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификаторы экземпляров виртуальных дисков, для которых были экспортированы файлы журналов.

</dd> <dt>

**експортедгуестстатефилепас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к экспортированному файлу состояния гостя.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**експортедлогфилепасс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пути к файлам журнала, которые были экспортированы.

</dd> <dt>

**експортедрунтимефилепас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к экспортированному файлу состояния среды выполнения.

</dd> <dt>

**референцепоинтид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID экспортируемой точки ссылки.

</dd> <dt>

**виртуалмачинеид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID виртуальной машины, для которой были экспортированы файлы журналов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_КОНКРЕТЕЖОБ CIM**](cim-concretejob.md)
</dt> </dl>

 

