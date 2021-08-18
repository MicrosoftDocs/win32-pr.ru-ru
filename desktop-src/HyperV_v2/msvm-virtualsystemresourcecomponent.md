---
description: представляет службу виртуального устройства платформы Hyper-V Microsoft Windows.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Класс Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0758858e9e45066cdfaddf36616c7861bbae914b12e3698665f8650c6c57d67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340174"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>\_Класс мсвм виртуалсистемресаурцекомпонент

представляет службу виртуального устройства платформы Hyper-V Microsoft Windows.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемресаурцекомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ виртуалсистемресаурцекомпонент** имеет следующие свойства.

<dl> <dt>

**аддитионалкласснамес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив строк, содержащий дополнительные классы, не связанные с взаимоассоциациями, на которые ссылается этот экземпляр **\_ виртуалсистемресаурцекомпонент мсвм** . Эти классы должны быть производными от [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) или [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ЭТОМУ**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор GUID, представляющий идентификатор класса COM-объекта службы. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Контекст**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Контекст, в котором будет выполняться вновь созданный объект. Это значение передается в параметре *двклсконтекст* в [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение 1.

</dd> <dt>

**Включен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если этот экземпляр включен и может использоваться для выполнения клиентских запросов; в противном случае — **значение false**. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)и всегда имеет значение **true**.

</dd> <dt>

**хотадд**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если этот экземпляр можно добавить в виртуальную машину с помощью горячего подключения; в противном случае — **значение false**. По умолчанию **False**.

</dd> <dt>

**хотремове**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если этот экземпляр можно удалить с виртуальной машины. в противном случае — **значение false**. По умолчанию **False**.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Строка, не зависящая от языка, которая уникально идентифицирует службу. Для предотвращения конфликтов именования предлагается следующий формат: " \| версия компонента поставщика \| ". Например, это имя представляет версию 1,0 компонента сетевого порта эмуляции Microsoft: Microsoft \| емулатеднетворкпорткомпонент \| v 1.0. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Тип**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отношение объекта WMI, описываемого здесь к виртуальному устройству.



| Значение                                                                                                                                                                                                                                                           | Значение                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"Не изменять"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton — это объект WMI верхнего уровня, который связан с виртуальным устройством 1:1 и может существовать только один раз для каждой виртуальной машины. Это значение по умолчанию.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"Многоэкземплярный"**</dt> <dt>2</dt> </dl>     | Многоэкземпляр — это объект WMI верхнего уровня, который может существовать несколько раз для каждой виртуальной машины и связан с виртуальным устройством 1:1.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Подустройство"**</dt> <dt>3</dt> </dl>                     | Подустройство — это объект WMI, который не имеет родительской ссылки, но управляется только одним виртуальным устройством, которое может существовать только один раз для каждой виртуальной машины. Однако объект WMI может существовать несколько раз.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ виртуалсистемресаурцекомпонент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

 

