---
title: Класс MDM_Firewall_Global02
description: '\_ \_ Класс GLOBAL02 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.'
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- Класс MDM_Firewall_Global02
- MDM_Firewall_Global02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262190"
---
# <a name="mdm_firewall_global02-class"></a>\_ \_ Класс GLOBAL02 брандмауэра MDM

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

\_ \_ Класс GLOBAL02 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ Global02 брандмауэра MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ Global02 брандмауэра MDM** имеет следующие свойства.

<dl> <dt>

[бинариверсионсуппортед](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[крлчекк](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[куррентпрофилес](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дисаблестатефулфтп](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[енаблепаккеткуеуе](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
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

[ипсецексемпт](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[оппортунистикаллиматчауссетперкм](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
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

[PolicyVersion](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[полициверсионсуппортед](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[прешаредкэйенкодинг](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[саидлетиме](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

