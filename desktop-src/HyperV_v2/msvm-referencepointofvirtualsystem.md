---
description: Связывает виртуалсистемреференцепоинт Мсвм \_ с соответствующими \_ объектами мсвм виртуалсистем.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Класс Msvm_ReferencePointOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d9224e0ce51608904f7cf2459dc3d1341d84dd005bd8fe4daee5707d22b38163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789594"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a>\_Класс мсвм референцепоинтофвиртуалсистем

Связывает [**\_ виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) с соответствующими объектами [**мсвм \_ виртуалсистем**](msvm-virtualsystemresourcecomponent.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ референцепоинтофвиртуалсистем** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ референцепоинтофвиртуалсистем** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ ComputerSystem**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Объект [**\_ ComputerSystem мсвм**](msvm-computersystem.md) , представляющий независимый объект в этой ассоциации.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **мсвм \_ виртуалсистемреференцепоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Виртуалсистемреференцепоинт мсвм**](msvm-virtualsystemreferencepoint.md) , представляющий объект, который зависит от **предшествующей задачи**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

