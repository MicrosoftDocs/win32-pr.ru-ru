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
ms.openlocfilehash: 18a15ff6479caa690a8645e89d9b68f4a15f523bd7cee56fedb6957e20373214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521544"
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

### <a name="properties"></a>Элемент Property

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




