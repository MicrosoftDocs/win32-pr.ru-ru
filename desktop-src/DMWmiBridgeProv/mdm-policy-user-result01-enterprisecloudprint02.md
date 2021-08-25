---
title: Класс MDM_Policy_User_Result01_EnterpriseCloudPrint02
description: '\_Класс политики MDM \_ user \_ Result01 \_ EnterpriseCloudPrint02 представляет доступные политики печати в облаке.'
ms.assetid: cf830cb5-2477-4b21-9d98-9fa9989daa7f
keywords:
- Класс MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd4dcabb827a064126852768992f5126446aabe5907376434216e4fb38798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874994"
---
# <a name="mdm_policy_user_result01_enterprisecloudprint02-class"></a>\_Класс политики MDM \_ user \_ Result01 \_ EnterpriseCloudPrint02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

\_Класс политики MDM \_ user \_ Result01 \_ EnterpriseCloudPrint02 представляет доступные политики печати в облаке.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ user \_ Result01 \_ EnterpriseCloudPrint02 политики MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ user \_ Result01 \_ EnterpriseCloudPrint02 политики MDM** имеет эти свойства.

<dl> <dt>

[клаудпринтердисковерендпоинт](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[клаудпринтоаусаусорити](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[клаудпринтоаусклиентид](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[клаудпринтресаурцеид](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[дисковеримакспринтерлимит](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
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

[моприадисковериресаурцеид](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

