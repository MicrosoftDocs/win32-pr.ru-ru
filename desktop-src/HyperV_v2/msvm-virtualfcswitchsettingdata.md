---
description: Представляет конфигурацию коммутатора виртуальной Fibre Channel.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Класс Msvm_VirtualFcSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540314"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a>\_Класс мсвм виртуалфксвитчсеттингдата

Представляет конфигурацию коммутатора виртуальной Fibre Channel.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалфксвитчсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалфксвитчсеттингдата** имеет следующие свойства.

<dl> <dt>

**аутоматикрековеряктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при сбое программного обеспечения, выполняемого виртуальной машиной. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**аутоматикшутдовнактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при завершении работы узла. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**аутоматикстартупактион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Действие, выполняемое для виртуальной машины при запуске узла. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**аутоматикстартупактионделай**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время задержки перед автоматическим запуском виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**аутоматикстартупактионсекуенценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число, указывающее относительную последовательность активации виртуальной машины при запуске главной системы. Меньшее значение указывает на более раннюю активацию. Если одна или несколько конфигураций отображают одно и то же значение, последовательность зависит от реализации. Значение 0 указывает, что последовательность зависит от реализации. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**конфигуратиондатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранится информация о конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**Файл ConfigurationFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Относительный путь и имя файла, в котором хранятся сведения о конфигурации виртуальной машины. Этот путь задается относительно свойства **конфигуратиондатарут** . Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор конфигурации. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания параметров. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

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

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**логдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранится информация журнала для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**Примечания**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указанные пользователем примечания, связанные с виртуальной машиной. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**рековерифиле**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Полный путь к файлу, в котором хранится информация, связанная с восстановлением для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**снапшотдатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**суспенддатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся сведения о приостановке виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**свапфиледатарут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к каталогу, в котором хранятся файлы подкачки для виртуальной машины. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)), но не используется.

</dd> <dt>

**виртуалсистемидентифиер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , которому принадлежат данные этого параметра. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**виртуалсистемтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает тип виртуальной машины, которую представляют данные параметров. Это свойство наследуется от [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

