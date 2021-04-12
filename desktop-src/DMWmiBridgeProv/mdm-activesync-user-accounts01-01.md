---
title: Класс MDM_ActiveSync_User_Accounts01_01
description: Класс MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01 определяет все доступные учетные записи ActiveSync.
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- Класс MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490179"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a>\_ \_ \_ Класс User Accounts01 \_ 01 MDM ActiveSync

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Класс **MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01** определяет все доступные учетные записи ActiveSync.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a>Члены

Класс **MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01** имеет эти свойства.

<dl> <dt>

[AccountIcon](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AccountName](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[AccountType](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[Доменная](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[EmailAddress](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
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

Определяет имя родительского узла.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Описывает полный путь к родительскому узлу. Для этого класса строка имеет значение "./вендор/мсфт/активесинк/"

</dd> <dt>

[Пароль](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[ServerName](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[UserName](/windows/client-management/mdm/activesync-csp#account-guid-username)
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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

