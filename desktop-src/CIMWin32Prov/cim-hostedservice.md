---
description: Класс CIM \_ HostedService представляет ассоциацию между службой и системой, в которой находятся функциональные возможности.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: Класс CIM_HostedService (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655909"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a>Класс CIM_HostedService (поставщики WMI CIMWin32)

Класс **CIM \_ HostedService** представляет ассоциацию между службой и системой, в которой находятся функциональные возможности. В системе может быть размещено множество служб, которые откладываются на систему размещения. Модель не представляет службы, размещенные в нескольких системах.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ HostedService** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ HostedService** имеет эти свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ система CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Система CIM**](cim-system.md) , которая описывает систему размещения.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Служба CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

[**\_ Служба CIM**](cim-service.md) , которая описывает службу, размещенную в системе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Модель CIM \_ HostedService** является производной [**от \_ зависимости CIM**](cim-dependency.md).

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

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

