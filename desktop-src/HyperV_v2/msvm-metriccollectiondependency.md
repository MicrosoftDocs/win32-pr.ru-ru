---
description: Представляет связь между двумя определениями метрик или двумя значениями метрик.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Класс Msvm_MetricCollectionDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684474"
---
# <a name="msvm_metriccollectiondependency-class"></a>\_Класс мсвм метрикколлектиондепенденци

Представляет связь между двумя определениями метрик или двумя значениями метрик.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ метрикколлектиондепенденци** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ метрикколлектиондепенденци** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий независимое определение метрики или значение метрики. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий определение метрики или значение метрики, зависящие от **предшествующей задачи**. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

