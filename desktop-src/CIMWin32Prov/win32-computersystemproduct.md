---
description: Представляет продукт. Сюда входят программное обеспечение и оборудование, используемые в данной компьютерной системе.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Класс Win32_ComputerSystemProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47312acde8f346ac4ac3b2260fe06a2a5270610f9b7265da2b627a4c92fb4b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119294034"
---
# <a name="win32_computersystemproduct-class"></a>\_Класс Win32 компутерсистемпродукт

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ компутерсистемпродукт для Win32** представляет продукт. Сюда входят программное обеспечение и оборудование, используемые в данной компьютерной системе.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ компутерсистемпродукт** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ компутерсистемпродукт** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое текстовое описание продукта.

Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание продукта.

Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).

</dd> <dt>

**IdentifyingNumber**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,4 в DMTF
</dt> </dl>

Идентификация продукта, например серийный номер программного обеспечения, номер кристалла микросхемы оборудования или (для некоммерческих продуктов) номер проекта.

Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,2 в DMTF
</dt> </dl>

Часто используемое название продукта.

Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).

</dd> <dt>

**скунумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Сведения о единицах складского учета продукта (SKU).

Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).

</dd> <dt>

**UUID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 1 \| UUID")
</dt> </dl>

Универсальный уникальный идентификатор (UUID) для этого продукта. UUID — это 128-разрядный идентификатор, который гарантированно отличается от других созданных UUID. Если UUID недоступен, используется UUID всех нулей.

это значение берется из элемента **UUID** структуры **Сведения о системе** в сведениях SMBIOS.

</dd> <dt>

**поставщик**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,1 в DMTF
</dt> </dl>

Название поставщика продукта или сущность, которая продает продукт (изготовитель, Торговый посредник, поставщик вычислительной техники и т. д.).

Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Значение ComponentID \| 001,3 в DMTF
</dt> </dl>

Сведения о версии продукта.

Это свойство наследуется [**от \_ продукта CIM**](cim-product.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ компутерсистемпродукт** является производным от [**\_ продукта CIM**](cim-product.md).

## <a name="examples"></a>Примеры

Пример [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell в коллекции TechNet использует для получения списка нерабочего оборудования, использующего инструментарий WMI, в **Win32 \_ компутерсистемпродукт** .

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

[**\_Продукт CIM**](cim-product.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

