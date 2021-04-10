---
description: Класс CIM \_ хостедбутсервице связывает систему размещения и службу загрузки. Так как эта связь является подклассом из CIM \_ HostedService, она наследует схему определения области или именования, определенную для службы, когда служба откладывается на ее систему размещения.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: Класс CIM_HostedBootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141731"
---
# <a name="cim_hostedbootservice-class"></a>\_Класс CIM хостедбутсервице

Класс **CIM \_ хостедбутсервице** связывает систему размещения и службу загрузки. Так как эта связь является подклассом из [**CIM \_ HostedService**](cim-hostedservice.md), она наследует схему определения области или именования, определенную для службы, когда служба откладывается на ее систему размещения.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ хостедбутсервице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ хостедбутсервице** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ система CIM**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)
</dt> </dl>

[**\_ Система CIM**](cim-system.md) , которая описывает систему размещения.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ бутсервице**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Бутсервице CIM**](cim-bootservice.md) , описывающий службу загрузки, размещенную в системе.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ хостедбутсервице** является производным от [**CIM \_ HostedService**](cim-hostedservice.md).

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

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> </dl>

 

