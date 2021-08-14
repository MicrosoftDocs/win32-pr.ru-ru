---
description: '\_Класс WMI взаимосвязей Win32 систембутконфигуратион связывает компьютерную систему и конфигурацию загрузки.'
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Класс Win32_SystemBootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad5b30d42e94391163a4a54836877f90415225d0ae697e719e6c088f432430cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416757"
---
# <a name="win32_systembootconfiguration-class"></a>\_Класс Win32 систембутконфигуратион

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ систембутконфигуратион** связывает компьютерную систему и конфигурацию загрузки.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ систембутконфигуратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ систембутконфигуратион** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Ссылка на экземпляр, представляющий компьютерную систему с помощью конфигурации загрузки.

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ бутконфигуратион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ бутконфигуратион")
</dt> </dl>

Ссылка на экземпляр, представляющий конфигурацию загрузки для компьютерной системы.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ систембутконфигуратион** является производным от [**Win32 \_ системсеттинг**](win32-systemsetting.md).

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

[**\_Системсеттинг Win32**](win32-systemsetting.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
