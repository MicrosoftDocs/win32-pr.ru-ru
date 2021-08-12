---
description: Класс CIM \_ логикалдискбаседонпартитион связывает логический диск с разделом диска, на котором он находится.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: Класс CIM_LogicalDiskBasedOnPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27e0805d4fa3a4a59d59423b30b3644e78ccc6138509b2b0f71cdecb435ffc7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679876"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a>\_Класс CIM логикалдискбаседонпартитион

Класс **CIM \_ логикалдискбаседонпартитион** связывает логический диск с разделом диска, на котором он находится.

Например, диск C может находиться в разделе на локальном физическом носителе, что указывает на то, что логический диск не может охватывать более одной секции. Если логический диск может охватывать более одной секции, логический диск основан на конфигурации RAID (например, зеркальном или чередующемся наборе). В этом случае логический диск основан на томе хранилища. Чтобы предотвратить неправильное использование ассоциации **\_ логикалдискбаседонпартитион CIM** , квалификатор **Max (1)** помещается в ссылку **Antecedent** на раздел диска.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ логикалдискбаседонпартитион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ логикалдискбаседонпартитион** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ дискпартитион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Дискпартитион CIM**](cim-diskpartition.md) , описывающий раздел диска.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ LogicalDisk**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Логический [**\_ логический диск CIM**](cim-logicaldisk.md) , описывающий логические диски, созданные на основе секции.

</dd> <dt>

**ендингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает конец высокоуровневого экстента в хранилище нижнего уровня. Это свойство полезно при сопоставлении несмежных экстентов с группировкой более высокого уровня.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).

</dd> <dt>

**стартингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает начало экстента высокого уровня в хранилище нижнего уровня.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **CIM \_ логикалдискбаседонпартитион** является производным от [**CIM \_ BasedOn**](cim-basedon.md).

Инструментарий WMI не реализует этот класс. Классы, производные от **CIM \_ логикалдискбаседонпартитион**, см. в разделе [Классы Win32](win32-provider.md).

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

[**\_BASEDON CIM**](cim-basedon.md)
</dt> </dl>

 

