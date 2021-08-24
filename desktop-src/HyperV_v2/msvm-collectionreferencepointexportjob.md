---
description: Этот класс представляет задание операции экспорта точки ссылки на коллекцию.
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Класс Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3baf6405f160401b3a2fe8024861d92560484a513e1c55436f9e149e92daed7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681914"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a>\_Класс мсвм коллектионреференцепоинтекспортжоб

Этот класс представляет задание операции экспорта точки ссылки на коллекцию.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектионреференцепоинтекспортжоб** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ коллектионреференцепоинтекспортжоб** содержит следующие методы.



| Метод                                                                                  | Описание                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**Ошибка**](msvm-collectionreferencepointexportjob-geterror.md)                     | Возвращает ошибку.<br/>                     |
| [**жетеррорекс**](msvm-collectionreferencepointexportjob-geterrorex.md)                 | Извлекает дополнительные сведения об ошибке.<br/> |
| [**Равен**](msvm-collectionreferencepointexportjob-requeststatechange.md) | Запрашивает изменение состояния.<br/>                |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ коллектионреференцепоинтекспортжоб** имеет следующие свойства.

<dl> <dt>

**басереференцепоинтграупид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID точки ссылки коллекции, которая используется в качестве базы в експортоператион.

</dd> <dt>

**Отменяемых**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли отменить задание. Значение этого свойства не гарантирует, что запрос на отмену задания будет выполнен.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID группы виртуальных машин, для которой верикспортед файлы журналов.

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

**експортедконфигфилепасс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к экспортированному файлу конфигурации виртуальной машины.

</dd> <dt>

**експортеддискс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификаторы экземпляров виртуальных дисков, для которых были экспортированы файлы журналов.

</dd> <dt>

**експортедгуестстатефилепасс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к экспортированному файлу состояния гостя виртуальной машины.

> [!Note]  
> добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**експортедлогфилепасс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пути к файлам журнала, которые были экспортированы.

</dd> <dt>

**експортедрунтимефилепасс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к экспортированному файлу состояния среды выполнения виртуальной машины.

</dd> <dt>

**референцепоинтграупид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID для экспортируемой точки ссылки коллекции.

</dd> <dt>

**виртуалмачинеид**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID виртуальных машин, для которых была выполнена операция экспорта.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_КОНКРЕТЕЖОБ CIM**](cim-concretejob.md)
</dt> </dl>

 

