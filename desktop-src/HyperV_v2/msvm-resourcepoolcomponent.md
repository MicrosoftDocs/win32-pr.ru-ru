---
description: представляет элемент пула ресурсов платформы Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Класс Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 470317d3afd961ad74eb788ebdb70e67617749446fa4a432f40f00f43214cd92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535614"
---
# <a name="msvm_resourcepoolcomponent-class"></a>\_Класс мсвм ресаурцепулкомпонент

представляет элемент пула ресурсов платформы Microsoft Windows Hyper-V.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ресаурцепулкомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ ресаурцепулкомпонент** имеет следующие свойства.

<dl> <dt>

**аллокатионкапабилитиескласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса, производного от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) , которое описывает возможности выделения ресурсов в этом пуле.

</dd> <dt>

**ЭТОМУ**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор **GUID** , представляющий идентификатор класса COM-объекта службы. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Контекст**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Контекст, в котором будет выполняться вновь созданный объект. Это значение передается в параметре *двклсконтекст* в **CoCreateInstance**. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение 1.

</dd> <dt>

**Включен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если этот экземпляр включен и может использоваться для выполнения клиентских запросов; в противном случае — **значение false**. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение **true**.

</dd> <dt>

**макспарентпулс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное число родительских пулов ресурсов, поддерживаемых дочерним пулом.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Строка, не зависящая от языка, которая уникальным образом идентифицирует элемент. Для предотвращения конфликтов именования предлагается следующий формат: " \| версия компонента поставщика \| ". Например, это имя представляет версию 1,0 компонента сетевого порта эмуляции Microsoft: Microsoft \| емулатеднетворкпорткомпонент \| v 1.0. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).

</dd> <dt>

**фисикалдевицекласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса, производного от [**CIM source \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , который реализует физическое устройство, из которого этот пул выделяет ресурсы. Это свойство может иметь **значение NULL** , если класс виртуального устройства, выделенный из этого пула, совпадает с классом физического устройства.

</dd> <dt>

**ресаурцепулкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса, производного от [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) , который реализует пул ресурсов.

</dd> <dt>

**ресаурцепулсеттингдатакласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса, производного от значения [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)) , которое описывает параметры пула ресурсов, не связанные с выделением.

</dd> <dt>

**вмифакториклсид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор **GUID** , представляющий идентификатор класса фабрики объектов WMI компонента.

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ ресаурцепулкомпонент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Окончание поддержки клиента<br/>    | Windows 8.1<br/>                                                                                  |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуализатионкомпонент**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

