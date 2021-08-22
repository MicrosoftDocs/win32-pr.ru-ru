---
description: Связывает два управляемых элемента, которые представляют различные аспекты одной и той же базовой сущности.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Класс Msvm_LogicalIdentity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 12ee48b85ae11b10a24bab35001baa45c8382105158050d110eb7448a8e883e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148367"
---
# <a name="msvm_logicalidentity-class"></a>\_Класс мсвм логикалидентити

Связывает два управляемых элемента, которые представляют различные аспекты одной и той же базовой сущности. Этот класс является производным от [**CIM \_ логикалидентити**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ логикалидентити** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ логикалидентити** имеет следующие свойства.

<dl> <dt>

**самилемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ логикалелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на альтернативный аспект системной сущности.

</dd> <dt>

**системелемент**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ логикалелемент**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на один аспект логического элемента.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЛОГИКАЛИДЕНТИТИ CIM**](cim-logicalidentity.md)
</dt> <dt>

[**\_ЛОГИКАЛИДЕНТИТИ CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

