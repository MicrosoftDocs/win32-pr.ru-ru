---
description: Класс CIM \_ компутерсистемирк представляет связь между компьютерной системой и ее доступными линиями запросов на прерывание (IRQ).
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: Класс CIM_ComputerSystemIRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655943"
---
# <a name="cim_computersystemirq-class"></a>\_Класс CIM компутерсистемирк

Класс **CIM \_ компутерсистемирк** представляет связь между компьютерной системой и ее доступными линиями запросов на прерывание (IRQ).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ компутерсистемирк** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ компутерсистемирк** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)
</dt> </dl>

Объект [**CIM \_**](cim-computersystem.md) , описывающий компьютер, связанный с IRQ.

Это свойство наследуется от [ **CIM \_ компутерсистемресаурце**](cim-computersystemresource.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **\_ IRQ CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**\_ IRQ CIM**](cim-irq.md) , описывающий IRQ компьютерной системы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ компутерсистемирк** является производным от [**CIM \_ компутерсистемресаурце**](cim-computersystemresource.md).

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

[**\_КОМПУТЕРСИСТЕМРЕСАУРЦЕ CIM**](cim-computersystemresource.md)
</dt> </dl>

 

