---
description: Представляет ассоциацию, в которой \_ экземпляр CIM ресаурцеаллокатионсеттингдата выделяется из пула ресурсов.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: Класс CIM_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999034"
---
# <a name="cim_resourceallocationfrompool-class"></a>\_Класс CIM ресаурцеаллокатионфромпул

Представляет ассоциацию, в которой экземпляр [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) выделяется из пула ресурсов.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ресаурцеаллокатионфромпул** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ ресаурцеаллокатионфромпул** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ResourcePool**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Пул ресурсов.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ ресаурцеаллокатионсеттингдата**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Данные о выделении ресурсов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

