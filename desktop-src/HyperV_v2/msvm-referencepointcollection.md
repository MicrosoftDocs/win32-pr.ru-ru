---
description: Представляет коллекцию опорных точек виртуальной системы.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Класс Msvm_ReferencePointCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910143"
---
# <a name="msvm_referencepointcollection-class"></a>\_Класс мсвм референцепоинтколлектион

Представляет коллекцию опорных точек виртуальной системы.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ референцепоинтколлектион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ референцепоинтколлектион** имеет следующие свойства.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Уникальная идентификация объекта коллекции.

</dd> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Уровень согласованности контрольной точки.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Отказоустойчивость (1** )


</dt> <dd>

Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии сбоя.

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>С **совместимостью приложений** (2)


</dt> <dd>

Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии совместимости с приложениями.

</dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Определяемое пользователем имя коллекции. Обратите внимание, что это не обязательно должно быть уникальным.

</dd> <dt>

**хасассоЦиатедлог**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

**значение true** , если все точки ссылки на элементы имеют связанные журналы. Это допустимо только для опорных точек на основе журналов. Для опорных точек на основе RCT **хасассоЦиатедлог** имеет значение **false**. Для контрольных точек на основе журналов после удаления журнала **хасассоЦиатедлог** становится **ложным**.

</dd> <dt>

**референцепоинттипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **в**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Указывает тип контрольной точки.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**На основе журнала** (1)


</dt> <dd>

Отслеживание журнала реплики Hyper-V.

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**На основе RCT** (2)


</dt> <dd>

На основе устойчивых Отслеживание изменений виртуальных дисков.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl>

</dd> <dt>

**виртуалсистемколлектионид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ виртуалсистемколлектион**](msvm-virtualsystemcollection.md).**CollectionID**")
</dt> </dl>

Идентификатор [**\_ виртуалсистемколлектион мсвм**](msvm-virtualsystemcollection.md) , которому принадлежит данная точка ссылки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Коллекция CIM**](cim-collection.md)
</dt> </dl>

 

