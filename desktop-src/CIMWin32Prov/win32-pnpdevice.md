---
description: '\_Класс WMI взаимосвязей Win32 код устройства PnP связывает устройство (известное как Configuration Manager как пнпентити) и функцию, которую он выполняет.'
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Класс Win32_PnPDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a136c86c0fd0744c555af2071943d99ca8569a33ce9c59d9d22191c4a78d2a32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972044"
---
# <a name="win32_pnpdevice-class"></a>\_Класс Win32 код устройства PnP

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ код устройства PnP** связывает устройство (известное как Configuration Manager как пнпентити) и функцию, которую он выполняет. Его функция представлена подклассом логического устройства, описывающего его использование. Например, [**\_ Клавиатура Win32**](win32-keyboard.md) или экземпляр [**\_ дискдриве Win32**](win32-diskdrive.md) . Оба упоминаемых объекта представляют одно и то же базовое системное устройство. изменения, связанные с выделением ресурсов на стороне Пнпентити, будут влиять на связанное устройство.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ код устройства PnP** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ код устройства PnP** имеет следующие свойства.

<dl> <dt>

**самилемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")
</dt> </dl>

Ссылка на экземпляр [**CIM \_**](cim-logicaldevice.md) , представляющий свойства логического устройства, связанные с устройством Самонастраивающийся.

</dd> <dt>

**системелемент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ пнпентити**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ пнпентити")
</dt> </dl>

Ссылка на экземпляр [**Win32 \_ пнпентити**](win32-pnpentity.md) , представляющий устройство Самонастраивающийся, связанное с логическим устройством.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
