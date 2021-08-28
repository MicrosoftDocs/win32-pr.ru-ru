---
description: '\_Класс WMI взаимосвязей Win32 компутерсистемпроцессор связывает компьютерную систему и процессор, работающий в этой системе.'
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Класс Win32_ComputerSystemProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bfaf26800a9cb75052699fcd44076f67553a4a36df0c8597b5c9c6e2855d7370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118417726"
---
# <a name="win32_computersystemprocessor-class"></a>\_Класс Win32 компутерсистемпроцессор

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ компутерсистемпроцессор** связывает компьютерную систему и процессор, работающий в этой системе.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ компутерсистемпроцессор** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ компутерсистемпроцессор** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

**Платформа Win32 \_ ComputerSystem** , описывающая свойства компьютерной системы, на которой работает процессор.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **\_ процессор Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| обработчик WMI Win32 \_ ")
</dt> </dl>

[**\_ Процессор Win32**](win32-processor.md) , описывающий свойства процессора, на котором работает компьютерная система.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ компутерсистемпроцессор** является производным от [**Win32 \_ системдевицес**](win32-systemdevices.md).

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

[**\_Системдевицес Win32**](win32-systemdevices.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

