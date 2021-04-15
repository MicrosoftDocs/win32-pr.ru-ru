---
description: Представляет параметры для службы виртуализации, имеющейся в одной системе узла.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Класс Msvm_VirtualSystemManagementServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682485"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a>\_Класс мсвм виртуалсистемманажементсервицесеттингдата

Представляет параметры для службы виртуализации, имеющейся в одной системе узла. Свойства этого класса нельзя изменить напрямую. Клиент должен вызвать метод [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) , чтобы изменить любое из этих свойств.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемманажементсервицесеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемманажементсервицесеттингдата** имеет следующие свойства.

<dl> <dt>

**биослоккстринг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)
</dt> </dl>

Используется изготовителями оборудования для разрешения запуска операционных систем Windows, заблокированных BIOS, на виртуальной машине. Длина этой строки должна составлять ровно 32 символов.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V".

</dd> <dt>

**куррентввннаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя узла в Интернете для динамически создаваемых адресов WWN-имен, используемых для виртуальных адаптеров шины.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**дефаултекстерналдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**мсвм \_ виртуалсистемсеттингдата**](msvm-virtualsystemsettingdata.md).**Конфигуратиондатарут**")
</dt> </dl>

Корневой каталог внешних данных по умолчанию. По умолчанию "*root* \\ папка ProgramData \\ \\ \\ виртуализация Microsoft Windows".

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**дефаултвиртуалхарддисккачингмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, следует ли использовать кэширование файлов в памяти по умолчанию для дисков. Это значение может быть переопределено отдельно для каждого диска в поле **качингмоде** класса [**мсвм \_ сторажеаллокатионсеттингдата**](msvm-storageallocationsettingdata.md) .

> [!Note]  
> Добавлено в Windows 10 и Windows Server 2016.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Без кэширования** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Кэшировать родители-предки** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**дефаултвиртуалхарддискпас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к виртуальному жесткому диску по умолчанию. По умолчанию "*корневые* \\ Пользователи \\ общедоступные \\ документы — \\ виртуальные жесткие диски".

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Settings для службы управления виртуальными системами".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V". Изменение этого свойства приведет к изменению свойства **ElementName** связанного производного класса [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .

</dd> <dt>

**енханцедсессионмодинаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешен ли режим расширенного сеанса на сервере. **Значение true** указывает, что разрешено; в противном случае **false**.

**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.

</dd> <dt>

**хбалунтимеаут**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает время, в течение которого виртуальное устройство искусственного Fibre Channel будет ожидать отображения логического номера устройства (LUN) перед запуском виртуальной машины.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**хипервисоррутсчедулеренаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включен ли корневой планировщик низкоуровневой оболочки.

> [!Note]  
> Добавлено в Windows 10 версии 1709.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "Microsoft:*Host*", где *Host* — это NetBIOS-имя системы размещающего компьютера.

</dd> <dt>

**максимуммакаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный MAC-адрес для динамически создаваемых MAC-адресов.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**максимумввпнаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальный WWN-адрес для динамически создаваемых адресов WWN-имен, используемых для виртуальных адаптеров шины.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**минимуммакаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный MAC-адрес для динамически создаваемых MAC-адресов.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**минимумввпнаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Минимальный адрес WWN имени порта для динамически создаваемых адресов WWN, используемых для виртуальных адаптеров шины.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**нумаспаннинженаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, может ли память выделяться из узлов удаленного доступа к памяти неоднородным доступом (NUMA) при запуске виртуальной машины или при назначении памяти виртуальной машине с помощью динамической памяти. Это может быть одно из следующих значений.



| Значение                                                                                | Значение                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Память может выделяться как с локального, так и с удаленного узла NUMA.<br/>                   |
| <dl> <dt>**Неверно**</dt> </dl> | Память может быть выделена только из узла NUMA, назначенного виртуальной машине.<br/> |



 

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**примарйовнерконтакт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,4 ")
</dt> </dl>

Описывает, как можно достичь основного владельца системы (например, номер телефона или адрес электронной почты). По умолчанию пусто. Длина имени не может превышать 256 символов.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**примарйовнернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Общие сведения о DMTF \| 001,3 ")
</dt> </dl>

Имя основного владельца системы. По умолчанию «администраторы». Длина этого значения не может превышать 64 символов.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Доступ к классу **\_ виртуалсистемманажементсервицесеттингдата мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))
</dt> <dt>

[Классы управления виртуальной системой](virtual-system-management-classes.md)
</dt> </dl>

 

