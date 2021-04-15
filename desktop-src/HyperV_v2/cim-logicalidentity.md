---
description: Представляет универсальную ассоциацию между двумя управляемыми элементами, которые представляют различные аспекты одной и той же базовой сущности.
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: Класс CIM_LogicalIdentity (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662143"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a>Класс CIM_LogicalIdentity (Управление Hyper-V)

Представляет универсальную ассоциацию между двумя управляемыми элементами, которые представляют различные аспекты одной и той же базовой сущности.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ логикалидентити** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ логикалидентити** имеет следующие свойства.

<dl> <dt>

**самилемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Второй аспект ассоциации.

</dd> <dt>

**системелемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ манажеделемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Первый аспект ассоциации. Использование системы в имени свойства не ограничивает область ассоциации.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

