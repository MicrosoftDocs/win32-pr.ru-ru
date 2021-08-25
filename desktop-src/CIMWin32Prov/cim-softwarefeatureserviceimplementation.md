---
description: Класс CIM \_ софтварефеатуресервицеимплементатион представляет ассоциацию между службой и ее реализацией в программном обеспечении.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: Класс CIM_SoftwareFeatureServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b89be16ac5b462d9a4b10441699c6c160a91bd3ef5222b2a7cd642413c4c2081
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919204"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a>\_Класс CIM софтварефеатуресервицеимплементатион

Класс **CIM \_ софтварефеатуресервицеимплементатион** представляет ассоциацию между службой и ее реализацией в программном обеспечении. Служба может предоставляться более чем одним программным обеспечением, работающими совместно друг с другом. Кроме того, компонент программного обеспечения может предоставлять более одной службы. Если несколько функций программного обеспечения связаны с одной службой, предполагается, что элементы работают совместно, чтобы предоставить службу. При наличии различных реализаций службы каждая реализация будет создавать отдельные экземпляры объекта службы. После этого отдельные экземпляры будут иметь связи с уникальными реализациями.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ софтварефеатуресервицеимплементатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ софтварефеатуресервицеимплементатион** имеет следующие свойства.

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

Тип данных: **\_ Служба CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Служба CIM**](cim-service.md) , которая описывает зависимую службу.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ софтварефеатуресервицеимплементатион** является производным от [**\_ зависимости CIM**](cim-dependency.md).

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

 

