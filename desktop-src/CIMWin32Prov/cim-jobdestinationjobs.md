---
description: '\_Ассоциация ЖОБДЕСТИНАТИОНЖОБС CIM описывает место отправки задания для обработки (то есть назначение задания).'
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: Класс CIM_JobDestinationJobs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5947ac9a8539227f27dbea62aeebcfbc07b14a7626e25234e3a39ee3267d81c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438434"
---
# <a name="cim_jobdestinationjobs-class"></a>\_Класс CIM жобдестинатионжобс

Ассоциация **\_ жобдестинатионжобс CIM** описывает место отправки задания для обработки (то есть назначение задания).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ жобдестинатионжобс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ жобдестинатионжобс** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ жобдестинатион**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Жобдестинатион CIM**](cim-jobdestination.md) , описывающий назначение задания, возможно, очередь.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Задание CIM** .
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Задание CIM**](cim-job.md) , описывающее задание, которое находится в очереди или назначении заданий.

</dd> </dl>

## <a name="remarks"></a>Remarks

**Модель CIM \_ Жобдестинатионжобс** является производным [**от \_ зависимости CIM**](cim-dependency.md).

Инструментарий WMI не реализует этот класс.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



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

 

