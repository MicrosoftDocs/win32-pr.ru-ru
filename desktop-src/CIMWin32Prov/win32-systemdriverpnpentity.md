---
description: '\_класс WMI взаимосвязей Win32 системдриверпнпентити связывает устройство самонастраивающийся в компьютерной системе, где работает Windows, и драйвер, поддерживающий устройство самонастраивающийся.'
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Класс Win32_SystemDriverPNPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b0de9559d223db4c398387ca846be39b17566b3267c76399bdf4381cdd14e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751114"
---
# <a name="win32_systemdriverpnpentity-class"></a>\_Класс Win32 системдриверпнпентити

[класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системдриверпнпентити** связывает устройство самонастраивающийся в компьютерной системе, где работает Windows, и драйвер, поддерживающий устройство самонастраивающийся.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ системдриверпнпентити** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ системдриверпнпентити** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ пнпентити**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ пнпентити")
</dt> </dl>

Представляет самонастраивающийся устройство, управляемое драйвером.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ SystemDriver**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

[**\_ SystemDriver Win32**](win32-systemdriver.md) , который представляет драйвер, поддерживающий устройство Самонастраивающийся.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ системдриверпнпентити** является производным от [**\_ зависимости CIM**](cim-dependency.md).

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

[**\_Зависимость CIM**](cim-dependency.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
