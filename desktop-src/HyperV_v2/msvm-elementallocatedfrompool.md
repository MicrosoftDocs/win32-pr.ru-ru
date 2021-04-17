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
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683856"
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

### <a name="properties"></a>Свойства

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

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ елементаллокатедфромпул мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
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

 

