---
description: Конкретная версия \_ класса заданий CIM. Этот класс представляет собой универсальную выполняемую единицу работы, выполняющую создание экземпляров, например пакет или задание печати.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: Класс CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a62ab2392ce2c069aa88ebb465f7028368f30bd5432cf96559c7eebe6edb8bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813165"
---
# <a name="cim_concretejob-class"></a>\_Класс CIM конкретежоб

Конкретная версия класса [**\_ заданий CIM**](cim-job.md) . Этот класс представляет собой универсальную выполняемую единицу работы, выполняющую создание экземпляров, например пакет или задание печати.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a>Члены

Класс **CIM \_ конкретежоб** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **CIM \_ конкретежоб** содержит следующие методы.



| Метод                                                           | Описание                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Ошибка**](cim-concretejob-geterror.md)                     | Извлекает сведения об ошибке для рабочего состояния конкретного задания.<br/> |
| [**Равен**](cim-concretejob-requeststatechange.md) | Запрашивает указанное изменение состояния для конкретного задания.<br/>                    |



 

### <a name="properties"></a>Свойства

Класс **CIM \_ конкретежоб** имеет следующие свойства.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Уникально и непрозрачно определяет экземпляр этого класса в области содержащего его пространства имен.

> [!IMPORTANT]
>
> Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*
>
> *OrgID* должен включать в себя запись с правом или иным именем, которая принадлежит бизнес-сущности, определяющей **InstanceId**, или быть зарегистрированным идентификатором, который назначается распознанным глобальным центром сертификации. Этот шаблон похож на структуру имен классов схемы. Кроме того, чтобы обеспечить уникальность, первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*. Поэтому *OrgID* не должен содержать двоеточие (":").
>
> *LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.
>
> Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.
>
> Для экземпляров распределенного управления Task Force (DMTF) необходимо использовать шаблон с *OrgID* , для которого задано значение CIM.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Рабочее состояние задания и переход между этими состояниями.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Создать** (2)


</dt> <dd>

Задание никогда не запускалось.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)


</dt> <dd>

Задание переходит с состояния "новое", "приостановлено" или "служба" в состояние "работает".

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (4)


</dt> <dd>

Задание работает.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (5)


</dt> <dd>

Задание остановлено, но может быть перезапущено без проблем.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (6)


</dt> <dd>

Задание переходит в состояние "завершено", "завершено" или "уничтожено".

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (7)


</dt> <dd>

Задание выполнено нормально.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Завершено** (8)


</dt> <dd>

Задание остановлено запросом на изменение состояния завершения. Задание и все его базовые процессы завершены и могут быть перезапущены (это зависит от задания) только в качестве нового задания.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Уничтожено** (9)


</dt> <dd>

Задание остановлено запросом на изменение состояния "Kill". Базовые процессы могли быть запущены, а для освобождения ресурсов может потребоваться очистка.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Исключение** (10)


</dt> <dd>

Задание находится в ненормальном состоянии, что может указывать на состояние ошибки. Фактическое состояние может отображаться при наличии объектов, относящихся к определенному заданию.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Служба** (11)


</dt> <dd>

Задание находится в состоянии, зависящем от поставщика, которое поддерживает обнаружение проблем, разрешение или и то, и другое.

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Ожидание запроса** (12)


</dt> <dd>

Ожидание разрешения запроса клиентом.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (13.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**обязательный**](/windows/desktop/WmiSdk/standard-qualifiers), [**переопределенный**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")
</dt> </dl>

Понятное имя экземпляра. Кроме того, понятное имя можно использовать в качестве свойства для поиска или запроса.

> [!Note]  
> Имя не обязательно должно быть уникальным в пределах пространства имен.

 

</dd> <dt>

**тимебефореремовал**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Указывает время хранения завершенного задания. Значение по умолчанию — "00000000000500.000000:000" (5 минут).

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата или время последнего изменения состояния задания.

> [!Note]  
> Если состояние задания не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.

 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Задание CIM**](cim-job.md)
</dt> </dl>

 

