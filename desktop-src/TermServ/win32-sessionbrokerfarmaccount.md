---
title: Класс Win32_SessionBrokerFarmAccount
description: Класс Win32 \_ сессионброкерфармаккаунт больше не доступен для использования в Windows Server 2012. | Класс Win32_SessionBrokerFarmAccount
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerFarmAccount службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerFarmAccount, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b7d55f973dc19c03182a4199b64f91f9de5a0774cc8c8f9d77d67eeb715c24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422494"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>\_Класс Win32 сессионброкерфармаккаунт

\[Класс **Win32 \_ сессионброкерфармаккаунт** больше не доступен для использования в Windows Server 2012.\]

Определяет учетную запись фермы посредника сеансов.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессионброкерфармаккаунт** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ сессионброкерфармаккаунт** содержит следующие методы.



| Метод                                                      | Описание                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**делетикс**](deleteex-win32-sessionbrokerfarmaccount.md) | Удаляет учетную запись фермы.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ сессионброкерфармаккаунт** имеет следующие свойства.

<dl> <dt>

**аккаунтдомаин**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Имя домена, к которому принадлежит учетная запись фермы.

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Имя учетной записи фермы.

</dd> <dt>

**аккаунтпассворд**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Пароль учетной записи фермы.

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Первое имя участника-службы (SPN), связанное с учетной записью фермы.

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Второе имя субъекта-службы, связанное с учетной записью фермы.

</dd> <dt>

**компутерднснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

DNS-имя компьютера, связанного с учетной записью фермы.

</dd> <dt>

**фармнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя фермы посредника сеансов.

</dd> <dt>

**Вручную**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, обновляется ли пароль учетной записи вручную.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                      |
| Окончание поддержки клиента<br/>    | Ни одна версия не поддерживается<br/>                                                              |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                               |
| MOF<br/>                      | <dl> <dt>Тссдвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

