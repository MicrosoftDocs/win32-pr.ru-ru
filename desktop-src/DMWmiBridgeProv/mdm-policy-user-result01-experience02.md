---
title: Класс MDM_Policy_User_Result01_Experience02
description: '\_Класс политики MDM \_ user \_ Result01 \_ Experience02 представляет доступные политики взаимодействия.'
ms.assetid: 729dfc75-7458-426f-8173-9ba75b4ee306
keywords:
- Класс MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02.InstanceID
- MDM_Policy_User_Result01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320941108309264a2cce3be6e63edca305c1cd40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891978"
---
# <a name="mdm_policy_user_result01_experience02-class"></a>\_Класс политики MDM \_ user \_ Result01 \_ Experience02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **\_ политики MDM \_ user \_ Result01 \_ Experience02** представляет доступные политики взаимодействия.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ user \_ Result01 \_ Experience02 политики MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ user \_ Result01 \_ Experience02 политики MDM** имеет эти свойства.

<dl> <dt>

[AllowTailoredExperiencesWithDiagnosticData](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowThirdPartySuggestionsInWindowsSpotlight](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowWindowsConsumerFeatures](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowWindowsSpotlight](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowWindowsSpotlightOnActionCenter](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AllowWindowsSpotlightWindowsWelcomeExperience](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ConfigureWindowsSpotlightOnLockScreen](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
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

Определяет имя родительского узла. Для этого класса строка имеет значение "Experience".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/ресулт"

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                            |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MOF \\DMWmiBridgeProv.dll</dt> </dl> |



 

