---
description: '\_Класс WMI взаимосвязей Win32 меморидевицеаррай связывает устройство памяти и массив памяти, в котором он находится.'
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Класс Win32_MemoryDeviceArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895465"
---
# <a name="win32_memorydevicearray-class"></a>\_Класс Win32 меморидевицеаррай

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ меморидевицеаррай** связывает устройство памяти и массив памяти, в котором он находится.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ меморидевицеаррай** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ меморидевицеаррай** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ меморяррай**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ меморяррай")
</dt> </dl>

[**\_ Меморяррай Win32**](win32-memoryarray.md) , представляющий часть массива памяти в \_ ассоциации Win32 меморидевицеаррай.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ меморидевице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ меморидевице")
</dt> </dl>

[**\_ Меморидевице Win32**](win32-memorydevice.md) , который представляет часть устройства памяти в \_ сопоставлении Win32 меморидевицеаррай.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ меморидевицеаррай** является производным от [**\_ компонента CIM**](cim-component.md).

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

[**\_Компонент CIM**](cim-component.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

