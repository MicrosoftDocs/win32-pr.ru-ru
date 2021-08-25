---
description: '\_Класс WMI взаимосвязей Win32 системтимезоне связывает компьютерную систему и часовой пояс.'
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Класс Win32_SystemTimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b94f6c6ff61acb526e972da54c55798524b39b1663dec1239e9e2dbae0110e6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827754"
---
# <a name="win32_systemtimezone-class"></a>\_Класс Win32 системтимезоне

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ системтимезоне** связывает компьютерную систему и часовой пояс.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ системтимезоне** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ системтимезоне** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Ссылка на экземпляр, представляющий компьютерную систему, отслеживающую часовой пояс системы.

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Часовой пояс Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")
</dt> </dl>

Ссылка на экземпляр, представляющий свойства часового пояса, которые отписываются в системе компьютера.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ системтимезоне** является производным от [**Win32 \_ системсеттинг**](win32-systemsetting.md).

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

[**\_Системсеттинг Win32**](win32-systemsetting.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
