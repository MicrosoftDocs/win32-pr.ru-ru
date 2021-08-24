---
description: '\_Класс WMI взаимосвязей Win32 принтерсеттинг связывает принтер и его параметры конфигурации.'
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Класс Win32_PrinterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be39a9f614ab172c75e5ddc857254cdd91ea20d1352a33071cd6fa3627132d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759384"
---
# <a name="win32_printersetting-class"></a>\_Класс Win32 принтерсеттинг

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтерсеттинг** связывает принтер и его параметры конфигурации.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ принтерсеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ принтерсеттинг** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")
</dt> </dl>

Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , представляющее свойства логического устройства, к которому можно применить параметры.

Это свойство наследуется из [**Win32 \_ девицесеттингс**](win32-devicesettings.md).

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **\_ параметр CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("параметр CIM CIM \| \_ ")
</dt> </dl>

[**\_ Параметр CIM**](cim-setting.md) , представляющий параметры, которые могут быть применены к логическому устройству.

Это свойство наследуется из [**Win32 \_ девицесеттингс**](win32-devicesettings.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ принтерсеттинг** является производным от [**Win32 \_ девицесеттингс**](win32-devicesettings.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Девицесеттингс Win32**](win32-devicesettings.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
