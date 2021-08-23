---
title: Класс MDM_Policy_User_Config01_Desktop02
description: '\_Класс политики MDM \_ user \_ Config01 \_ Desktop02 представляет доступные политики профиля папки.'
ms.assetid: 44a60c60-bae5-44b2-b096-387c915e2692
keywords:
- Класс MDM_Policy_User_Config01_Desktop02
- MDM_Policy_User_Config01_Desktop02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Desktop02
- MDM_Policy_User_Config01_Desktop02.InstanceID
- MDM_Policy_User_Config01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd533663554ecf341530c9a6025675dbb013d0b6d6994f91550a735df434f7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694154"
---
# <a name="mdm_policy_user_config01_desktop02-class"></a>\_Класс политики MDM \_ user \_ Config01 \_ Desktop02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

\_Класс политики MDM \_ user \_ Config01 \_ Desktop02 представляет доступные политики профиля папки.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ user \_ Config01 \_ Desktop02 политики MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ user \_ Config01 \_ Desktop02 политики MDM** имеет эти свойства.

<dl> <dt>

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

[превентусерредиректионофпрофилефолдерс](/windows/client-management/mdm/policy-csp-desktop#desktop-preventuserredirectionofprofilefolders)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
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



 

