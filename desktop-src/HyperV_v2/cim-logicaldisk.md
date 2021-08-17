---
description: Представляет непрерывный диапазон логических блоков, идентифицируемый файловой системой с помощью поля DeviceID (ключ) дисков.
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: Класс CIM_LogicalDisk (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0fccc6600e0eb5f04fd7d00360402ad85a94746e55781acbd6b1a35c7f9b94fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812109"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a>Класс CIM_LogicalDisk (Управление Hyper-V)

Представляет непрерывный диапазон логических блоков, идентифицируемый файловой системой с помощью поля **DeviceID** диска (Key). например, в Windowsной среде поле **DeviceID** содержит букву диска; в UNIXной среде она содержит путь доступа. и в среде NetWare он содержит имя тома.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ LogicalDisk** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс логического логического класса **CIM \_** имеет эти свойства.

<dl> <dt>

**намеформат**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("намеформат")
</dt> </dl>

Указывает, использует ли логическое устройство формат имени операционной системы.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Имя устройства ОС** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**наменамеспаце**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("наменамеспаце")
</dt> </dl>

Указывает, имеет ли логическое устройство то же пространство имен, что и ОС.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Пространство имен устройств ОС** (8)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_СТОРАЖЕЕКСТЕНТ CIM**](cim-storageextent.md)
</dt> </dl>

 

