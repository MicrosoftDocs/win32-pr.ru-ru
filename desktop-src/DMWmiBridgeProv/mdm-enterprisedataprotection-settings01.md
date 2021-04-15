---
title: Класс MDM_EnterpriseDataProtection_Settings01
description: Класс MDM \_ ентерприседатапротектион \_ Settings01 используется для настройки параметров Windows Information Protection (WIP) (прежнее название — защита корпоративных данных).
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- Класс MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491958"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a>\_Класс MDM ентерприседатапротектион \_ Settings01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ ентерприседатапротектион \_ Settings01** используется для настройки параметров Windows Information Protection (WIP) (прежнее название — защита корпоративных данных). Дополнительные сведения о WIP см. в статье [Защита корпоративных данных с помощью защиты корпоративных данных (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ ентерприседатапротектион \_ Settings01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ ентерприседатапротектион \_ Settings01** имеет следующие свойства.

<dl> <dt>

[алловазурермсфоредп](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[алловусердекриптион](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[датарековерицертификате](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **октетстринг**
</dt> </dl>

</dd> <dt>

[едпенфорцементлевел](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[едпшовиконс](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ентерприсепротектеддомаиннамес](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Settings".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/ентерприседатапротектион"

</dd> <dt>

[ревокеонуненролл](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[рмстемплатеидфоредп](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[смбаутоенкриптедфиликстенсионс](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

