---
description: Представляет связь между объектом CIM сторажеекстент более высокого уровня \_ и объектом CIM сторажеекстент более низкого уровня \_ . Например, объект CIM \_ протектедспацеекстент является частью \_ объекта фисикалекстент CIM.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Класс CIM_BasedOn (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd07a329388d1c4883674bc86f9cadf648746487ea44769141d91e90548722c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995770"
---
# <a name="cim_basedon-class-hyper-v-management"></a>Класс CIM_BasedOn (Управление Hyper-V)

Представляет связь между объектом **CIM \_ сторажеекстент** более высокого уровня и объектом **CIM \_ сторажеекстент** более низкого уровня. Например, объект [**CIM \_ протектедспацеекстент**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) является частью объекта [**\_ фисикалекстент CIM**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ BasedOn** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ BasedOn** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сторажеекстент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Объект **CIM \_ сторажеекстент** нижнего уровня.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сторажеекстент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Объект **CIM \_ сторажеекстент** более высокого уровня.

</dd> <dt>

**ендингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес, указывающий, где в хранилище нижнего уровня заканчивается объект **CIM \_ сторажеекстент** более высокого уровня. Это свойство полезно при сопоставлении несмежных объектов **CIM \_ сторажеекстент** с группировкой более высокого уровня.

</dd> <dt>

**ордериндекс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Индекс, который используется для указания порядка сопоставлений **CIM \_ BasedOn** в коллекции; в противном случае — значение 0 указывает на отсутствие порядка. **Модель CIM \_ Экземпляры BasedOn** с одинаковым зависимым значением должны располагать уникальными значениями в свойстве **ордериндекс** . Наименьшее значение **ордериндекс** указывает первый элемент коллекции.

Примером использования этого свойства является определение чередующегося массива RAID-0 из 3 дисков. Результирующий массив RAID — это область хранения, которая зависит от экстентов хранения, описывающих каждый из трех дисков. Значение **ордериндекс** каждой ассоциации **CIM \_ BasedOn** из ЭКСТЕНТов диска в массив RAID можно указать как 1, 2 и 3, чтобы указать порядок, в котором экстенты дисков используются для доступа к данным RAID.

</dd> <dt>

**стартингаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес, который указывает, где в хранилище нижнего уровня начинается объект **CIM \_ сторажеекстент** высшего уровня.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

