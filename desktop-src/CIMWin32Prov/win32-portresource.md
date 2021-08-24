---
description: '\_Класс WMI портресаурце для Win32 представляет порт ввода-вывода в компьютерной системе, где работает Windows.'
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Класс Win32_PortResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 732bd1255bf216abe3654d80abcde14b1e8b1180a69d0509663a6a83a2801895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878584"
---
# <a name="win32_portresource-class"></a>\_Класс Win32 портресаурце

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ портресаурце для Win32** представляет порт ввода-вывода в компьютерной системе, где работает Windows.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ портресаурце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ портресаурце** имеет следующие свойства.

<dl> <dt>

**Псевдоним**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Configuration Manager структурные \| \_ данные ввода-вывода")
</dt> </dl>

Если **значение — true**, этот экземпляр представляет один из диапазонов с псевдонимом. Если **значение равно false**, экземпляр представляет базовый адрес порта. Базовый адрес порта — это заранее определенный адрес порта, выделенный для конкретной службы или устройства. Адрес псевдонима порта — это порт, в ответ на который устройство отвечает, как будто оно является фактическим адресом порта ввода-вывода.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).

</dd> <dt>

**кскреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Имя класса создания для системы компьютера с областями.

Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Имя системы области компьютера.

Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**ендингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,2 ")
</dt> </dl>

Конечный адрес сопоставленного ввода-вывода памяти.

Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов свойство может быть переопределено как ключевое свойство.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**стартингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**переопределить**](../wmisdk/standard-qualifiers.md) ("стартингаддресс"), [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,1 ")
</dt> </dl>

Начальный адрес сопоставленного в памяти ввода-вывода. Для свойства идентификатора ресурса оборудования необходимо задать это значение, чтобы создать сопоставленный ключ ресурса ввода-вывода.

Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ портресаурце** является производным от [**Win32 \_ системмемориресаурце**](win32-systemmemoryresource.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Системмемориресаурце Win32**](win32-systemmemoryresource.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
