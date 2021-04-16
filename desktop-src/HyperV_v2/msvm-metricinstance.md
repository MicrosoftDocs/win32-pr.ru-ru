---
description: Представляет ассоциацию объектов значений метрик с их определениями метрик.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Класс Msvm_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683384"
---
# <a name="msvm_metricinstance-class"></a>\_Класс мсвм метриЦинстанце

Представляет ассоциацию объектов значений метрик с их определениями метрик. Эта Ассоциация связывает экземпляр [**мсвм \_ басеметриквалуе**](msvm-basemetricvalue.md) с его [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md).

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ метриЦинстанце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ метриЦинстанце** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: * * * * CIM \_ манажеделемент * * * *
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md) , представляющий определения метрик.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: * * * * CIM \_ манажеделемент * * * *
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ басеметриквалуе**](msvm-basemetricvalue.md) , представляющий метрики, зависящие от **предшествующей задачи**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




