---
title: Метод Аддаккаунт класса Win32_TSPermissionsSetting (Факскомекс. h)
description: Метод Аддаккаунт готовится к добавлению учетной записи в терминал с указанным набором разрешений. Можно добавить пользователей, группы или компьютеры.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддаккаунт
- Службы удаленных рабочих столов метода Аддаккаунт, класс Win32_TSPermissionsSetting
- Класс Win32_TSPermissionsSetting службы удаленных рабочих столов, метод Аддаккаунт
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3bd1862dfde955d782527ca60fc0fb43ca31431ccb307574e875fe84a640655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348559"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Метод Аддаккаунт \_ класса Win32 тспермиссионссеттинг

Метод **аддаккаунт** готовится к добавлению учетной записи в терминал с указанным набором разрешений. Можно добавить пользователей, группы или компьютеры.

## <a name="syntax"></a>Синтаксис


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя_учетной_записи* \[ окне\]
</dt> <dd>

Имя учетной записи, добавляемой в терминал.

</dd> <dt>

*Пермиссионпресет* \[ окне\]
</dt> <dd>

Набор разрешений, связываемый с указанной учетной записью. Этот параметр может быть любым или любым из следующих значений. Дополнительные сведения см. в разделе [службы удаленных рабочих столов Permissions](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**Винстатион \_ Гостевой \_ доступ** (0)


</dt> <dd>

Учетная запись имеет разрешение на вход.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**Винстатион \_ \_Доступ пользователей** (1)


</dt> <dd>

учетная запись имеет следующие разрешения: вход, сведения о запросе, отправка сообщения и Подключение.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**Винстатион \_ ВСЕ \_ доступ** (2)


</dt> <dd>

Учетная запись имеет все разрешения службы удаленных рабочих столов.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Факскомекс. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тспермиссионссеттинг Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

