---
description: Используется в методе Жетсуммаринформатион \_ класса мсвм виртуалсистемманажементсервице для быстрого получения общих сведений, связанных с виртуальной системой или моментальным снимком.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Класс Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650626"
---
# <a name="msvm_summaryinformationbase-class"></a>\_Класс мсвм суммаринформатионбасе

Используется в методе [**жетсуммаринформатион**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) для быстрого получения общих сведений, связанных с виртуальной системой или моментальным снимком.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ суммаринформатионбасе** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ суммаринформатионбасе** имеет следующие свойства.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время создания виртуальной системы или моментального снимка.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ манажеделемент. ElementName")
</dt> </dl>

Понятное имя виртуальной системы или моментального снимка.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние виртуальной системы или моментального снимка.

</dd> <dt>

**енханцедсессионмодестате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешены ли для узла подключения в расширенном режиме, а также если они разрешены, независимо от того, доступны ли они для виртуальной машины.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Разрешено и доступно** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Не разрешено** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Разрешено, но недоступно** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние работоспособности виртуальной системы. Это свойство является недопустимым для экземпляров [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , представляющих моментальный снимок виртуальной системы.

</dd> <dt>

**хосткомпутерсистемнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя компьютера, на котором размещена эта виртуальная машина.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ манажеделемент. InstanceId"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID — это необязательное свойство, которое можно использовать для непрозрачного и уникального определения экземпляра этого класса в области действия экземпляра пространства имен. Различные подклассы этого класса могут переопределять это свойство, чтобы сделать его обязательным, или ключ. Такие подклассы также могут изменять предпочтительные алгоритмы, чтобы обеспечить уникальность, определенную ниже.

Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма:

<OrgID>:<LocalID>

Где <OrgID> и <LocalID> разделяются двоеточием (:), а <OrgID> в месте должно быть указано уникальное имя, которое принадлежит бизнес-сущности, создающему или определяющему InstanceId или зарегистрированный идентификатор, назначенный бизнес-сущностю распознанным глобальным центром сертификации. (Это требование аналогично <Schema Name> \_ <Class Name> Структура имен классов схемы.) Кроме того, чтобы обеспечить уникальность, <OrgID> не следует включать двоеточие (:). При использовании этого алгоритма первым двоеточием, которое должно находиться в InstanceID, должен находиться в диапазоне от <OrgID> до <LocalID> .

<LocalID> выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов. Если не равно NULL и указанный выше алгоритм не используется, определяющая сущность должна гарантировать, что результирующий InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра.

Если для экземпляров, определяемых DMTF, не задано значение null, то для набора, для которого задано значение CIM, необходимо использовать "предпочтительный" алгоритм <OrgID> .

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное имя виртуальной системы или моментального снимка.

</dd> <dt>

**Примечания**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Примечания, связанные с виртуальной системой или моментальным снимком.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число виртуальных процессоров, выделенных для виртуальной системы или моментального снимка.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Текущее состояние элемента.

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое"). Для этого свойства необходимо задать значение null, если параметр **EnabledState** имеет любое значение, отличное от 1.

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** .

</dd> <dt>

**Просто**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество времени, прошедшее с момента последней загрузки виртуальной системы. Это свойство является недопустимым для экземпляров [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , представляющих моментальный снимок виртуальной системы.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Версия виртуальной системы в формате "основная. Дополнительная"; Например, "2,0".

</dd> <dt>

**виртуалсвитчнамес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")
</dt> </dl>

Строки, в которых перечислены понятные имена виртуальных коммутаторов, к которым подключена виртуальная машина.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Подтип виртуальной системы.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-v: подтип: 1** ("Microsoft: Hyper-V: подтип: 1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-v: подтип: 2** ("Microsoft: Hyper-V: подтип: 2")


</dt> <dd></dd> </dl>

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

[**\_Представление CIM**](cim-view.md)
</dt> </dl>

 

