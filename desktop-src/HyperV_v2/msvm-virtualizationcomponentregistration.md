---
description: Представляет регистрацию службы на Microsoft Hyper-Vной платформе.
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
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682505"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>\_Класс мсвм виртуализатионкомпонентрегистратион

Представляет регистрацию службы на Microsoft Hyper-Vной платформе.

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

### <a name="properties"></a>Свойства

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

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ виртуализатионкомпонентрегистратион мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Окончание поддержки клиента<br/>    | Windows 8.1<br/>                                                                                  |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

