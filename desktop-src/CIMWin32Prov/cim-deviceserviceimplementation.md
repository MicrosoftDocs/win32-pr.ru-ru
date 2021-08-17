---
description: Класс CIM \_ девицесервицеимплементатион представляет ассоциацию между службой и ее реализацией.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: Класс CIM_DeviceServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14ab52a8075a9982d9e14f87b130b7b85a7b18badb9adab58e609acd0ee9662b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924514"
---
# <a name="cim_deviceserviceimplementation-class"></a>\_Класс CIM девицесервицеимплементатион

Класс **CIM \_ девицесервицеимплементатион** представляет ассоциацию между службой и ее реализацией. Если несколько устройств связаны с одной службой, эти элементы работают совместно, чтобы предоставить службу. При наличии различных реализаций службы каждая реализация приводит к отдельным экземплярам объекта службы.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ девицесервицеимплементатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ девицесервицеимплементатион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Служба CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Служба CIM**](cim-service.md) , которая описывает службу, реализованную с помощью логического устройства.

</dd> </dl>

## <a name="remarks"></a>Remarks

Инструментарий WMI не реализует этот класс.

Класс **CIM \_ девицесервицеимплементатион** является производным от [**\_ зависимости CIM**](cim-dependency.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

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
</dt> </dl>

 

