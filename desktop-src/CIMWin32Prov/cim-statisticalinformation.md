---
description: Класс CIM \_ статистикалинформатион является корневым классом для произвольной коллекции статистических данных или метрик, применимых к одному или нескольким управляемым системным элементам.
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: Класс CIM_StatisticalInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896426"
---
# <a name="cim_statisticalinformation-class"></a>\_Класс CIM статистикалинформатион

Класс **CIM \_ статистикалинформатион** является корневым классом для произвольной коллекции статистических данных или метрик, применимых к одному или нескольким управляемым системным элементам.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ статистикалинформатион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ статистикалинформатион** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое текстовое описание для статистики или метрики.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание статистики или метрики.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Метка, на которой известна статистика или метрика. При создании подклассов это свойство может быть переопределено как свойство ключа.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Инструментарий WMI не реализует этот класс. Классы WMI, производные от **CIM \_ статистикалинформатион**, см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

