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
ms.openlocfilehash: 9ab3feab1f34d0f44ce5cd0618915d8575af9e463a9ec772961c185e946ac094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963504"
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

### <a name="properties"></a>Элемент Property

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

**Caption**
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

**Windows 8.1:** это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**енаблесмбтранспорт**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включена или отключена ли возможность использования SMB в качестве транспортного типа для передачи состояния виртуальной машины между узлами Hyper-V во время миграции виртуальной системы. **Значение true** указывает, что включен. Более высокая производительность достигается, если сетевые адаптеры RDMA настроены для транспорта SMB во время динамической миграции виртуальной машины. Если **енаблесмбтранспорт** имеет значение true, значение **EnableCompression** игнорируется.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

**Windows 8.1:** это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**енаблевиртуалсистеммигратион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, включена или отключена миграция виртуальной системы. служба хранилищаная миграция всегда включена. Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) класса [**\_ виртуалсистеммигратионсервице мсвм**](msvm-virtualsystemmigrationservice.md) .

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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

