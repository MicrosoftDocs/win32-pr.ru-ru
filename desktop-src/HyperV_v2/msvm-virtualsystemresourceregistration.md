---
description: Регистрирует службу, которая предоставляет объекты, относящиеся к ресурсам виртуальной машины.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Класс Msvm_VirtualSystemResourceRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540274"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a>\_Класс мсвм виртуалсистемресаурцерегистратион

Регистрирует службу, которая предоставляет объекты, относящиеся к ресурсам виртуальной машины.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемресаурцерегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемресаурцерегистратион** имеет следующие свойства.

<dl> <dt>

**Компонент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ виртуалсистемресаурцекомпонент**](msvm-virtualsystemresourcecomponent.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр, описывающий COM-объект, реализующий этот класс.

</dd> <dt>

**исрутдевице**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** , если эта регистрация указывает, является ли указанный тип ресурса корневым (или родительским) устройством для этой службы; в противном случае — **значение false**. Если **исрутдевице** имеет значение **true**, может существовать только одна регистрация. В противном случае эта регистрация представляет сопоставление с подсистемой устройства. Этому свойству всегда присвоено значение **false**.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ ресаурцетипедефинитион**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр, описывающий тип ресурса, поддерживаемый службой. Это свойство наследуется от [**мсвм \_ виртуализатионкомпонентрегистратион**](msvm-virtualizationcomponentregistration.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ виртуалсистемресаурцерегистратион мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуализатионкомпонентрегистратион**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**Мсвм \_ виртуализатионкомпонентрегистратион**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

