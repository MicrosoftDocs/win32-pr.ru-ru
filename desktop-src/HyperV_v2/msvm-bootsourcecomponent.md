---
description: Связывает бутсаурцесеттингдата Мсвм \_ с общей мсвм \_ виртуалсистемсеттингдата.
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Класс Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662597"
---
# <a name="msvm_bootsourcecomponent-class"></a>\_Класс мсвм бутсаурцекомпонент

Связывает [**\_ бутсаурцесеттингдата мсвм**](msvm-bootsourcesettingdata.md) с общей [**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md). Этот класс является производным [**от \_ компонента CIM**](/windows/desktop/CIMWin32Prov/cim-component).

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ бутсаурцекомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ бутсаурцекомпонент** имеет следующие свойства.

<dl> <dt>

**Ссылка**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажедсистемелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на родительский элемент в ассоциации. Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажедсистемелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на дочерний элемент в ассоциации. Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Компонент CIM**](cim-component.md)
</dt> <dt>

[**\_Компонент CIM**](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[**Мсвм \_ бутсаурцесеттингдата**](msvm-bootsourcesettingdata.md)
</dt> <dt>

[**Мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

