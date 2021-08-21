---
description: представляет регистрацию службы на Microsoft Hyper-Vной платформе.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Класс Msvm_VirtualizationComponentRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c7acd111ab95f59146763e874d40c4efb411313938c94b1a4527aa1e2d08490c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146558"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>\_Класс мсвм виртуализатионкомпонентрегистратион

представляет регистрацию службы на Microsoft Hyper-Vной платформе.

Следующий синтаксис представляет собой упрощенный код MOF-файл (MOF).

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуализатионкомпонентрегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ виртуализатионкомпонентрегистратион** имеет следующие свойства.

<dl> <dt>

**Компонент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ виртуализатионкомпонент**](msvm-virtualizationcomponent.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр, описывающий COM-объект, реализующий этот класс.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ресаурцетипедефинитион**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр, описывающий тип ресурса, поддерживаемый службой.

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ виртуализатионкомпонентрегистратион мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Окончание поддержки клиента<br/>    | Windows 8.1<br/>                                                                                  |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

