---
description: '\_Класс WMI взаимосвязей Win32 пнпаллокатедресаурце представляет связь между логическими устройствами и системными ресурсами.'
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Класс Win32_PnPAllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896478"
---
# <a name="win32_pnpallocatedresource-class"></a>\_Класс Win32 пнпаллокатедресаурце

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ пнпаллокатедресаурце** представляет связь между логическими устройствами и системными ресурсами. Этот класс используется для обнаружения ресурсов, которые используются конкретным устройством, например запроса на прерывание (IRQ) или канала прямого доступа к памяти (DMA).

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ пнпаллокатедресаурце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ пнпаллокатедресаурце** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ системресаурце**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ системресаурце")
</dt> </dl>

Ссылка на экземпляр [**CIM \_ системресаурце**](cim-systemresource.md) , представляющий свойства системного ресурса, доступного для логического устройства. Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ пнпентити**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")
</dt> </dl>

Ссылка на экземпляр [**Win32 \_ пнпентити**](win32-pnpentity.md) , который представляет свойства логического устройства, использующего назначенные ему ресурсы системы. Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ пнпаллокатедресаурце** является производным от [**CIM \_ аллокатедресаурце**](cim-allocatedresource.md).

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

[**\_АЛЛОКАТЕДРЕСАУРЦЕ CIM**](cim-allocatedresource.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
