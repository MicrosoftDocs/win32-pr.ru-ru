---
description: Представляет настроенное состояние параметров безопасности для.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Класс Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22bc30db51b103f50eaa4deed7ca6f479c5f94600fbb15ef2a6f4bb36595d159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148148"
---
# <a name="msvm_securitysettingdata-class"></a>\_Класс мсвм секуритисеттингдата

Представляет настроенное состояние параметров безопасности для виртуальной машины.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ секуритисеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ секуритисеттингдата** имеет следующие свойства.

<dl> <dt>

**датапротектионрекуестед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы запросить защиту данных для виртуальной машины. в противном случае — **значение false**. Значение по умолчанию — **false.**

</dd> <dt>

**енкриптстатеандвммигратионтраффик**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы трафик состояния и переноса виртуальной машины был зашифрован; в противном случае — **значение false**. Значение по умолчанию для вновь созданной виртуальной машины — **false**.

</dd> <dt>

**ксденаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы включить устройство хранилища ключей (КСД) для этой виртуальной машины; в противном случае — **значение false**. Недавно созданная виртуальная машина имеет значение Disable КСД.

</dd> <dt>

**шиелдингрекуестед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы запросить экранирование для виртуальной машины; в противном случае — **значение false**. Только что созданная виртуальная машина имеет первоначально запрошенное состояние экранирования **false**.

</dd> <dt>

**тпменаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы включить доверенную платформенную НОДУЛЕ (TPM) для этой виртуальной машины; в противном случае — **значение false**. У созданной виртуальной машины отключен доверенный платформенный модуль.

</dd> <dt>

**виртуализатионбаседсекуритйоптаут**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **обязательно**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**значение true** , чтобы не предлагать безопасность на основе ВИРТУАЛИЗАЦИИ виртуальной машины. в противном случае — **значение false**. Значение по умолчанию для нового состояния отказа виртуальной машины — **false**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

