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
ms.openlocfilehash: 15f4ef08329b3927d7e3c3328c7c2f033fb25026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891637"
---
# <a name="mdm_policy_user_config01_desktop02-class"></a>\_Класс политики MDM \_ user \_ Config01 \_ Desktop02

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

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

### <a name="properties"></a>Свойства

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

