---
description: Устанавливает, что экземпляр CIM \_ ресаурцеаллокатионсеттингдата, представляющий выделение ресурсов, зависит от выделения другого ресурса.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Класс Msvm_ResourceDependentOnResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683682"
---
# <a name="msvm_resourcedependentonresource-class"></a>\_Класс мсвм ресаурцедепендентонресаурце

Устанавливает, что экземпляр [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющий выделение ресурсов, зависит от выделения другого ресурса.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ресаурцедепендентонресаурце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ ресаурцедепендентонресаурце** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ресаурцеаллокатионсеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Ресаурцеаллокатионсеттингдата CIM**](cim-resourceallocationsettingdata.md) , представляющий независимый ресурс в этой ассоциации.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ресаурцеаллокатионсеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

[**\_ Ресаурцеаллокатионсеттингдата CIM**](cim-resourceallocationsettingdata.md) , представляющий ресурс, который зависит от предшествующей задачи.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

