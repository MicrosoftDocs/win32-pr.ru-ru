---
description: Связывает экземпляр выделенного ресурса с пулом ресурсов, из которого он был выделен.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Класс Msvm_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a68731bec7ae7ab8126fa6b76305257d4333f06012e619cd7a3c9a90bcc69283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148536"
---
# <a name="msvm_elementallocatedfrompool-class"></a>\_Класс мсвм елементаллокатедфромпул

Связывает экземпляр выделенного ресурса с пулом ресурсов, из которого он был выделен.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ елементаллокатедфромпул** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ елементаллокатедфромпул** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **override**, **Max** (1)
</dt> </dl>

Пул ресурсов. Это свойство наследуется от [**CIM \_ елементаллокатедфромпул**](/previous-versions//cc150668(v=vs.85)).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ логикалелемент**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Выделенный ресурс. Это свойство наследуется от [**CIM \_ елементаллокатедфромпул**](/previous-versions//cc150668(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ елементаллокатедфромпул мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ЕЛЕМЕНТАЛЛОКАТЕДФРОМПУЛ CIM**](cim-elementallocatedfrompool.md)
</dt> <dt>

[**\_ЕЛЕМЕНТАЛЛОКАТЕДФРОМПУЛ CIM**](/previous-versions//cc150668(v=vs.85))
</dt> <dt>

[**Мсвм \_ елементаллокатедфромпул (v1)**](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[Классы управления ресурсами](resource-management-classes.md)
</dt> </dl>

 

