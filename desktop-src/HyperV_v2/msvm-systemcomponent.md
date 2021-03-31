---
description: Устанавливает &\# 0034; часть&\# 0034; отношение между системой и любым управляемым системным элементом, из которого она состоит.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Класс Msvm_SystemComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423694"
---
# <a name="msvm_systemcomponent-class"></a>\_Класс мсвм системкомпонент

Устанавливает отношение "часть" между системой и любым управляемым системным элементом, из которого она состоит.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ системкомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ системкомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ система CIM**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Родительский элемент в ассоциации. Это свойство наследуется от [**CIM \_ системкомпонент**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дочерний элемент в ассоциации. Это свойство наследуется от [**CIM \_ системкомпонент**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

