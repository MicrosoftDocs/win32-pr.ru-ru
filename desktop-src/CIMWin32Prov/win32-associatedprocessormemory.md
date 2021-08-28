---
description: '\_Класс WMI взаимосвязей Win32 ассоЦиатедпроцессормемори связывает процессор и его кэш-память.'
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Класс Win32_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8740aca290bbe116f867915fd15f4f2683bfe3b2d4c4a2e8cc731516ba8a0a09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109634"
---
# <a name="win32_associatedprocessormemory-class"></a>\_Класс Win32 ассоЦиатедпроцессормемори

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ ассоЦиатедпроцессормемори** связывает процессор и его кэш-память.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ ассоЦиатедпроцессормемори** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ ассоЦиатедпроцессормемори** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ качемемори**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ качемемори")
</dt> </dl>

[**\_ Качемемори Win32**](win32-cachememory.md) , описывающий кэш-память, доступную для процессора.

</dd> <dt>

**бусспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц")
</dt> </dl>

Скорость шины в мегагерцах (МГц) между процессором и памятью.

Это свойство наследуется от [**CIM \_ ассоЦиатедпроцессормемори**](cim-associatedprocessormemory.md).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ процессор Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| процессор Win32 WMI \_ ")
</dt> </dl>

[**\_ Процессор Win32**](win32-processor.md) , описывающий процессор, использующий кэш-память.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ ассоЦиатедпроцессормемори** является производным от [**CIM \_ ассоЦиатедпроцессормемори**](cim-associatedprocessormemory.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_АССОЦИАТЕДПРОЦЕССОРМЕМОРИ CIM**](cim-associatedprocessormemory.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

