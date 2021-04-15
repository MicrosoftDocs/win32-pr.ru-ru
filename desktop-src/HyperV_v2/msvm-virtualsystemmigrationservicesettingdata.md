---
description: Представляет параметры для службы миграции виртуальной системы на узле.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Класс Msvm_VirtualSystemMigrationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662233"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a>\_Класс мсвм виртуалсистеммигратионсервицесеттингдата

Представляет параметры для службы миграции виртуальной системы на узле. Свойства этого класса нельзя изменить напрямую. Клиент должен вызвать метод **мсвм \_ Виртуалсистеммигратионсервице. модифисервицесеттингс** , чтобы изменить любое из этих свойств.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистеммигратионсервицесеттингдата** имеет следующие свойства.

<dl> <dt>

**AuthenticationType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает механизм проверки подлинности, используемый для сетевых подключений миграции виртуальной системы. Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

**CredSSP** (0)


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

**Kerberos** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включен или отключен сжатие трафика динамической миграции. Значение true указывает, что включен.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**енаблесмбтранспорт**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включена или отключена ли возможность использования SMB в качестве транспортного типа для передачи состояния виртуальной машины между узлами Hyper-V во время миграции виртуальной системы. **Значение true** указывает, что включен. Более высокая производительность достигается, если сетевые адаптеры RDMA настроены для транспорта SMB во время динамической миграции виртуальной машины. Если **енаблесмбтранспорт** имеет значение true, значение **EnableCompression** игнорируется.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**енаблевиртуалсистеммигратион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включена или отключена миграция виртуальной системы. Миграция хранилища всегда включена. Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**максимумактивесторажемигратион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает максимальное количество разрешенных миграций Active Storage. Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .

</dd> <dt>

**максимумактивевиртуалсистеммигратион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает максимальное разрешенное количество активных миграций виртуальной системы. Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .

</dd> </dl>

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

