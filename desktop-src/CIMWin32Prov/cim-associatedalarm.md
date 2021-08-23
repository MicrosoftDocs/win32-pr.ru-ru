---
description: '\_Зависимость АССОЦИАТЕДАЛАРМ CIM связывает сигнал с логическим устройством.'
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: Класс CIM_AssociatedAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee89533b6084999d6972da253276f1ee225dd1e517727761c893e9424f01f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439483"
---
# <a name="cim_associatedalarm-class"></a>\_Класс CIM ассоЦиатедаларм

Зависимость **\_ ассоЦиатедаларм CIM** связывает сигнал с логическим устройством.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ассоЦиатедаларм** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ ассоЦиатедаларм** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ алармдевице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Алармдевице CIM**](cim-alarmdevice.md) , содержащий сигнальное устройство.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Логическая [**модель \_ CIM**](cim-logicaldevice.md) , которая содержит логическое устройство с оповещением.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ ассоЦиатедаларм** является производным от [**\_ зависимости CIM**](cim-dependency.md).

Инструментарий WMI не реализует этот класс.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



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

 

