---
description: Представляет состояние конфигурации параметров слияния диска для виртуальной машины.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Класс Msvm_DiskMergeSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664330"
---
# <a name="msvm_diskmergesettingdata-class"></a>\_Класс мсвм дискмержесеттингдата

Представляет состояние конфигурации параметров слияния диска для виртуальной машины.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ дискмержесеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ дискмержесеттингдата** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) и всегда имеет значение "данные параметров слияния диска".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметров слияния диска Майкрософт".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85))и всегда имеет значение "данные параметров слияния диска". Изменение этого свойства приведет к изменению свойства **ElementName** связанного производного класса [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает включенное состояние функции слияния диска.

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

**Временно отключено** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)) и всегда имеет значение "Microsoft:*GUID* \\ *девицеспеЦификдата*".

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

