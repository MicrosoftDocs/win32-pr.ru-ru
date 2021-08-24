---
description: Связывает экземпляр выделения ресурсов с пулом ресурсов, из которого он выделяется.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Класс Msvm_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8d3913f03560262309084d99ea97b44a165944d4b71acdcac17e2a39bfd44a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148207"
---
# <a name="msvm_resourceallocationfrompool-class"></a>\_Класс мсвм ресаурцеаллокатионфромпул

Связывает экземпляр выделения ресурсов с пулом ресурсов, из которого он выделяется.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ресаурцеаллокатионфромпул** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ ресаурцеаллокатионфромпул** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **override**, **Max** (1)
</dt> </dl>

Пул ресурсов. Это свойство наследуется от [**CIM \_ ресаурцеаллокатионфромпул**](/previous-versions//cc150673(v=vs.85)).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Выделение ресурсов. Это свойство наследуется от [**CIM \_ ресаурцеаллокатионфромпул**](/previous-versions//cc150673(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ ресаурцеаллокатионфромпул мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНФРОМПУЛ CIM**](cim-resourceallocationfrompool.md)
</dt> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНФРОМПУЛ CIM**](/previous-versions//cc150673(v=vs.85))
</dt> <dt>

[**Мсвм \_ ресаурцеаллокатионфромпул (v1)**](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[Классы управления ресурсами](resource-management-classes.md)
</dt> </dl>

 

