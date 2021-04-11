---
description: Связывает источник питания с датчиком напряжения, отслеживающим свое входное напряжение.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: Класс CIM_AssociatedSupplyVoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142085"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a>\_Класс CIM ассоЦиатедсуппливолтажесенсор

Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** связывает источник питания с датчиком напряжения, отслеживающим свое входное напряжение.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ датчик напряжения**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Датчик напряжения CIM**](cim-voltagesensor.md) , описывающий датчик напряжения.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **Источник \_ питания CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Источник питания CIM, описывающий питание, связанное с датчиком напряжения. [**\_**](cim-powersupply.md)

</dd> <dt>

**мониторингранже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает диапазон входного напряжения источника питания, измеряемый соответствующим датчиком.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Диапазон 1** (2)


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Диапазон 2** (3)


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Диапазоны 1 и 2** (4)


</dt> <dd>

Диапазон 1 и 2

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** является производным от [**CIM \_ ассоЦиатедсенсор**](cim-associatedsensor.md).

Инструментарий WMI не реализует этот класс.

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

[**\_АССОЦИАТЕДСЕНСОР CIM**](cim-associatedsensor.md)
</dt> </dl>

 

