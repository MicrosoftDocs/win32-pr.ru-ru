---
description: Представляет событие, которое вызывается каждый раз при изменении свойства OperationalStatus класса Мсвм \_ ResourcePool или мсвм \_ LogicalDisk.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Класс Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 478b4617f56c73e425d833842b313767f85c385e9142314a7ca8978b5783f492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950233"
---
# <a name="msvm_storagealert-class"></a>\_Класс мсвм сторажеалерт

Представляет событие, которое вызывается каждый раз при изменении свойства **OperationalStatus** класса [**Мсвм \_ ResourcePool**](msvm-resourcepool.md) или [**мсвм \_ LogicalDisk**](msvm-logicaldisk.md) .

Следующий синтаксис упрощен из MOF-кода и включает эти свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ сторажеалерт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ сторажеалерт** имеет следующие свойства.

<dl> <dt>

**алертинжелементформат**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **моделкорреспонденце** ("CIM \_ алертиндикатион. алертингманажеделемент", "CIM \_ алертиндикатион. осералертинжелементформат")
</dt> </dl>

Задает формат свойства **алертингманажеделемент** . Формат — Цимобжектпас с форматом *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, который указывает экземпляр в схеме CIM.

Это свойство наследуется от класса **CIM \_ алертиндикатион** .

Допустимые значения:

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Цимобжектпас** (2)
</dt> </dl>

</dd> <dt>

**алертингманажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Пути WMI экземпляра, для которого создается предупреждение.

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает основную классификацию предупреждения. Возможные значения этого свойства:

<dl> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Предупреждение качества обслуживания** (3)
</dt> </dl>

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время обнаружения базового события.

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Форматированное сообщение, созданное путем объединения некоторых или всех динамических элементов, указанных в свойстве **мессажеаргументс** , со статическими элементами, однозначно идентифицируемыми свойством **MessageId** в реестре сообщений или в другом каталоге, связанном со свойством **овнинжентити** .

</dd> <dt>

**мессажеаргументс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий динамическое содержимое сообщения. Если значение **MessageId** равно 32930, аргумент в позиции 0 является **Пулидом** экземпляра [**мсвм \_ ResourcePool**](msvm-resourcepoolcomponent.md) , для которого создается предупреждение.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Однозначно определяет в области свойства **овнинжентити** формат свойства **Message** . Возможные значения этого свойства:

32930 ("недостаточное сообщение о пропускной способности пула служба хранилища)")

</dd> <dt>

**осералертинжелементформат**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая определяет значения "Other" для **алертингманажеделемент**. Это значение должно быть задано как значение, отличное от NULL, если для **алертингманажеделемент** задано значение 1 ("другое"). Для всех остальных значений **алертингманажеделемент** значение этой строки должно быть равно null.

Это свойство наследуется от класса **CIM \_ алертиндикатион** .

</dd> <dt>

**овнинжентити**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Однозначно определяет сущность, которая владеет определением формата **сообщения** , описанного в этом экземпляре. значение этого свойства всегда равно "Microsoft-Windows-Hyper-V".

"Microsoft-Windows-Hyper-V"

</dd> <dt>

**перцеиведсеверити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описывает серьезность индикации предупреждения. Возможные значения этого свойства:

<dl> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Информация** (2)
</dt> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Снижение уровня работоспособности/предупреждение** (3)
</dt> </dl>

</dd> <dt>

**пробаблекаусе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описывает возможную причину ситуации, которая привела к появлению предупреждения.

<dl> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**проблема с служба хранилища емкостью** (50)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Предыдущее оповещение сброшено** (59)
</dt> </dl>

</dd> <dt>

**пробаблекауседескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание, соответствующее значению свойства **пробаблекаусе** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Поставщик WMI Hyper-V не будет создавать события для отдельных виртуальных дисков, чтобы избежать перегрузки клиентов с событиями в случае крупномасштабных неисправностей базовых систем хранения.

когда клиент получает событие **мсвм \_ сторажеалерт** , если значение свойства **пробаблекаусе** равно 50 (проблема с емкостью служба хранилища), клиент может обнаружить, какие виртуальные диски работают вне своей политики качества обслуживания с помощью одной из следующих процедур:

-   Запросите все экземпляры [**мсвм \_ LogicalDisk**](msvm-logicaldisk.md) , которые были выделены из пула ресурсов, для которого было создано событие. Эти экземпляры **мсвм \_ LogicalDisk** связаны с пулом ресурсов через ассоциацию [**мсвм \_ елементаллокатедфромпул**](msvm-elementallocatedfrompool.md) .
-   Отфильтруйте список результатов, выбрав экземпляры, для которых параметр OperationalStatus содержит недостаточную пропускную способность.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_АЛЕРТИНДИКАТИОН CIM**](cim-alertindication.md)
</dt> <dt>

[**Мсвм \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> <dt>

[**Мсвм \_ ResourcePool**](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




