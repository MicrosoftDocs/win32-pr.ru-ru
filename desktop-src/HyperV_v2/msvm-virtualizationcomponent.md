---
description: Представляет службу платформы Hyper-V Microsoft Windows.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Класс Msvm_VirtualizationComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682507"
---
# <a name="msvm_virtualizationcomponent-class"></a>\_Класс мсвм виртуализатионкомпонент

Представляет службу платформы Hyper-V Microsoft Windows.

Следующий синтаксис представляет собой упрощенный код MOF-файл (MOF).

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуализатионкомпонент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуализатионкомпонент** имеет следующие свойства.

<dl> <dt>

**ЭТОМУ**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор **GUID** , представляющий идентификатор класса COM-объекта службы.

</dd> <dt>

**Контекст**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **экспериментальные**
</dt> </dl>

Контекст, в котором будет выполняться вновь созданный объект. Это значение передается в параметре *двклсконтекст* в [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Это свойство всегда имеет значение 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если этот экземпляр включен и может использоваться для выполнения клиентских запросов; в противном случае — **значение false**. Это свойство всегда имеет значение **true**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Строка, не зависящая от языка, которая уникально идентифицирует службу. Для предотвращения конфликтов именования предлагается следующий формат: " \| версия компонента поставщика \| ". Например, это имя представляет версию 1,0 компонента сетевого порта эмуляции Microsoft: Microsoft \| емулатеднетворкпорткомпонент \| v 1.0.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ виртуализатионкомпонент мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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



 

