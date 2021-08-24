---
title: Класс MDM_Firewall_PublicProfile02
description: '\_ \_ класс PublicProfile02 брандмауэра MDM используется для настройки параметров брандмауэра Защитник Windows.'
ms.assetid: 5524b931-10fa-43dc-8901-238312ecb6a8
keywords:
- Класс MDM_Firewall_PublicProfile02
- MDM_Firewall_PublicProfile02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Firewall_PublicProfile02
- MDM_Firewall_PublicProfile02.InstanceID
- MDM_Firewall_PublicProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6785607dcf02dae945b7f872ab7a98dd0d4f8de20e2f6ea7f2e5e66df2888fef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825664"
---
# <a name="mdm_firewall_publicprofile02-class"></a>\_ \_ Класс PUBLICPROFILE02 брандмауэра MDM

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

\_ \_ класс PublicProfile02 брандмауэра MDM используется для настройки параметров брандмауэра Защитник Windows.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PublicProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ PublicProfile02 брандмауэра MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ PublicProfile02 брандмауэра MDM** имеет следующие свойства.

<dl> <dt>

[алловлокалипсекполицимерже](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[алловлокалполицимерже](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[аусаппсалловусерпрефмерже](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дефаултинбаундактион](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дефаултаутбаундактион](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дисаблеинбаунднотификатионс](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дисаблестеалсмоде](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дисаблестеалсмодеипсексекуредпаккетексемптион](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дисаблеуникастреспонсестомултикастброадкаст](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[енаблефиревалл](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[глобалпортсалловусерпрефмерже](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[Экранирование](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

