---
description: Представляет доступные поставщики для репликации.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Класс Msvm_ReplicationProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c865cb14ee8f34eb4950bfa4d7e3aac1ea15d113ab8f579614f10e3041e98cc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130424"
---
# <a name="msvm_replicationprovider-class"></a>\_Класс мсвм репликатионпровидер

Представляет доступные поставщики для репликации.

Следующий синтаксис упрощен из MOF-кода и включает эти наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ репликатионпровидер** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ репликатионпровидер** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement). Для этого объекта значение равно:

"Поставщик репликации"

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement). Для внешних поставщиков это значение предоставляется. Для размещения встроенного поставщика на узле используется значение:

"Поставщик репликации виртуальных машин для узла Hyper-V"

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя для поставщика конечной точки. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

Для размещения встроенного поставщика на узле этому свойству всегда присваивается значение:

"Поставщик репликации виртуальных машин для узла Hyper-V"

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Идентификатор экземпляра WMI, который идентифицирует поставщик. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement). Это свойство имеет формат "Microsoft: <Host-Machine-Name>\\ репликатионпровидер \\<поставщик-имя>".

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Глобальный уникальный идентификатор (GUID) поставщика, который идентифицирует поставщик конечной точки. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

В случае с внешним поставщиком это свойство является идентификатором CLSID объекта класса COM поставщика. Для размещения встроенного поставщика на узле это свойство имеет фиксированное значение:

"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение:

<dl> <dt>

<span id="S_OK"></span><span id="s_ok"></span>**С \_ ОК** (2)
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

Для включения отношения репликации можно использовать любой из доступных поставщиков и класс [**мсвм \_ репликатионрелатионшип**](msvm-replicationrelationship.md) . По умолчанию Hyper-V выбирает встроенный узел для поставщика узла, который можно изменить во время создания репликации. Служба управления Hyper-V взаимодействует с внешним поставщиком с помощью COM.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**](cim-managedsystemelement.md)
</dt> <dt>

[**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

