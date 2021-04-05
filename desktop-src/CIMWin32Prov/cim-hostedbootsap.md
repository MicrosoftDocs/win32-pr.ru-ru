---
description: Класс CIM \_ хостедбутсап определяет размещение единой компьютерной системы для \_ класса CIM бутсап.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: Класс CIM_HostedBootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990589"
---
# <a name="cim_hostedbootsap-class"></a>\_Класс CIM хостедбутсап

Класс **CIM \_ хостедбутсап** определяет размещение единой компьютерной системы для класса [**CIM \_ бутсап**](cim-bootsap.md) . Так как эта связь является подклассом из [**CIM \_ хостедакцесспоинт**](cim-hostedaccesspoint.md), она наследует схему определения области и именования, определенную для [**CIM \_ сервицеакцесспоинт**](cim-serviceaccesspoint.md), где точка доступа откладывается на ее систему размещения. В этом случае **CIM \_ бутсап** должен откладываться на класс [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md) размещения.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ хостедбутсап** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ хостедбутсап** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ унитарикомпутерсистем**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Унитарикомпутерсистем CIM**](cim-unitarycomputersystem.md) , описывающий единую компьютерную систему.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ бутсап**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Бутсап CIM**](cim-bootsap.md) , описывающий загрузочную систему SAP, размещенную на единой компьютерной системе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ хостедбутсап** является производным от [**CIM \_ хостедакцесспоинт**](cim-hostedaccesspoint.md).

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

[**\_ХОСТЕДАКЦЕССПОИНТ CIM**](cim-hostedaccesspoint.md)
</dt> </dl>

 

