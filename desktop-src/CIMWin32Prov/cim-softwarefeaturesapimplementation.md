---
description: Класс CIM \_ софтварефеатуресапимплементатион представляет связь между точкой доступа к службе (SAP) и ее реализацией в программном обеспечении.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Класс CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ca763199f346936431671d99190595455cc4142d78e749183bcbf5183fc65995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119817834"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a>\_Класс CIM софтварефеатуресапимплементатион

Класс **CIM \_ софтварефеатуресапимплементатион** представляет связь между точкой доступа к службе (SAP) и ее реализацией в программном обеспечении. SAP может предоставляться несколькими программными компонентами для взаимодействия друг с другом. Кроме того, программная функция может предоставлять более одного SAP. Если многие функции программного обеспечения связаны с одним SAP, предполагается, что элементы работают совместно, чтобы предоставить точку доступа. При наличии различных реализаций SAP каждая реализация будет создавать отдельные экземпляры объекта SAP. После этого отдельные экземпляры будут иметь связи с уникальными реализациями.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ софтварефеатуресапимплементатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ софтварефеатуресапимплементатион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ софтварефеатуре**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Софтварефеатуре CIM**](cim-softwarefeature.md) , описывающий функцию предшествующего программного обеспечения.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий зависимую точку доступа службы.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ софтварефеатуресапимплементатион** является производным от [**\_ зависимости CIM**](cim-dependency.md).

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



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

