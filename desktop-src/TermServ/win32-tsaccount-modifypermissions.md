---
title: Метод Модифипермиссионс класса Win32_TSAccount
description: Задает разрешение для указанной учетной записи.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Модифипермиссионс
- Службы удаленных рабочих столов метода Модифипермиссионс, класс Win32_TSAccount
- Класс Win32_TSAccount службы удаленных рабочих столов, метод Модифипермиссионс
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6265290fa3604c426609f51d0518f1f6762ea02718757d86ff9ed69b10bd018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119421674"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>Метод Модифипермиссионс \_ класса Win32 тсаккаунт

Задает разрешение для указанной учетной записи.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пермиссионмаск* \[ окне\]
</dt> <dd>

[Разрешение узла сеансов удаленный рабочий стол](terminal-services-permissions.md) для установки.

Допустимые значения:

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**Винстатион \_ ЗАПРОС** (0)


</dt> <dd>

Разрешение на запрос сведений о сеансе.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Винстатион \_ SET** (1)


</dt> <dd>

Разрешение на изменение параметров соединения.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Винстатион \_ Сброс** (6)


</dt> <dd>

Разрешение на сброс или завершение сеанса или соединения.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Винстатион \_ \| \_ \_ Требуются права на виртуальные стандартные** (3)


</dt> <dd>

Разрешение на использование виртуальных каналов. Виртуальные каналы обеспечивают доступ из серверной программы к клиентским устройствам.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Винстатион \_ ТЕНЕВая копия** (4)


</dt> <dd>

Разрешение на теневое или удаленное управление сеансом другого пользователя.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Винстатион \_ Вход в систему** (5)


</dt> <dd>

Разрешение на вход в сеанс на сервере.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Винстатион \_ Выход из системы** (2)


</dt> <dd>

Разрешение на выход пользователя из сеанса.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Винстатион \_ MSG** (7)


</dt> <dd>

Разрешение на отправку сообщений в сеанс другого пользователя.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Винстатион \_ Подключение** (8)


</dt> <dd>

Разрешение на подключение к другому сеансу.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Винстатион \_ ОТКЛЮЧИТЬ** (9)


</dt> <dd>

Разрешение на отключение сеанса.

</dd> </dl> </dd> <dt>

*Разрешить* \[ окне\]
</dt> <dd>

Указывает, разрешен или запрещен ли разрешение в параметре *пермиссионмаск* .

Допустимые значения:

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Указанный набор разрешений разрешен.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Указанный набор разрешений запрещен.

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
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсаккаунт Win32**](win32-tsaccount.md)
</dt> </dl>

 

