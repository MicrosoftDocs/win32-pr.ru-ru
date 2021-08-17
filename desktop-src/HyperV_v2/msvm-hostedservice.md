---
description: Связывает службу с компьютерной системой, на которой она размещена.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Класс Msvm_HostedService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ab9ddb6326d594253ab1ef7f810140ac463c32fcb62367b03b656004b861e4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014512"
---
# <a name="msvm_hostedservice-class"></a>\_Класс мсвм HostedService

Связывает службу с компьютерной системой, на которой она размещена. Экземпляры [**мсвм \_ виртуализатионманажементсервице**](msvm-virtualsystemmanagementservice.md) можно обнаружить с помощью связи с узлом.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ HostedService** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ HostedService** имеет эти свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на систему компьютера размещения. Это свойство наследуется от [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ Служба CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на размещенную службу. Это свойство наследуется от [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ HostedService мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

См. раздел [запросы к сетевым объектам](querying-networking-objects.md).

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

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dt>

[**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[Классы управления виртуальной системой](virtual-system-management-classes.md)
</dt> </dl>

 

