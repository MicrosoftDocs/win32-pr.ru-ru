---
description: Класс CIM \_ сапсапдепенденци — это ассоциация между двумя точками доступа к службе (SAPS), которая указывает, что второй SAP необходим для подключения первой SAP к своей службе.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: Класс CIM_SAPSAPDependency (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990457"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a>Класс CIM_SAPSAPDependency (поставщики WMI CIMWin32)

Класс **CIM \_ сапсапдепенденци** — это ассоциация между двумя точками доступа к службе (SAPS), которая указывает, что второй SAP необходим для подключения первой SAP к своей службе. Например, для печати на сетевом принтере точки доступа к локальным принтерам должны использовать базовые SAPs, связанные с сетью, или конечные точки протокола, чтобы отправить запрос на печать.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ сапсапдепенденци** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ сапсапдепенденци** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий необходимую точку доступа к службе.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий точку доступа службы, которая зависит от базового SAP.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ сапсапдепенденци** является производным от [**\_ зависимости CIM**](cim-dependency.md).

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

 

