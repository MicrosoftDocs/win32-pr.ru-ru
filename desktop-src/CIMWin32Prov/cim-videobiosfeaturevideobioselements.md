---
description: Класс CIM \_ видеобиосфеатуревидеобиоселементс связывает компонент Video BIOS и его объединенные элементы Video BIOS.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: Класс CIM_VideoBIOSFeatureVideoBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141422"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a>\_Класс CIM видеобиосфеатуревидеобиоселементс

Класс **CIM \_ видеобиосфеатуревидеобиоселементс** связывает компонент Video BIOS и его объединенные элементы Video BIOS.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ видеобиосфеатуревидеобиоселементс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ видеобиосфеатуревидеобиоселементс** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ видеобиосфеатуре**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

[**\_ Видеобиосфеатуре CIM**](cim-videobiosfeature.md) , описывающий функцию Video BIOS.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ видеобиоселемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ Видеобиоселемент CIM**](cim-videobioselement.md) , описывающий элемент Video BIOS, который реализует возможности, описываемые функцией Video BIOS.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ видеобиосфеатуревидеобиоселементс** является производным от [**CIM \_ софтварефеатуресофтварилементс**](cim-softwarefeaturesoftwareelements.md).

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

[**\_СОФТВАРЕФЕАТУРЕСОФТВАРИЛЕМЕНТС CIM**](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

