---
title: Метод Модифяудитпермиссионс класса Win32_TSAccount
description: Подготавливает к установке более детализированного набора разрешений на аудит для указанной учетной записи.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Модифяудитпермиссионс
- Службы удаленных рабочих столов метода Модифяудитпермиссионс, класс Win32_TSAccount
- Класс Win32_TSAccount службы удаленных рабочих столов, метод Модифяудитпермиссионс
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892565"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a>Метод Модифяудитпермиссионс \_ класса Win32 тсаккаунт

Метод **модифяудитпермиссионс** готовится к установке более детального набора разрешений аудита для указанной учетной записи.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пермиссионмаск* \[ окне\]
</dt> <dd>

Набор [разрешений узла сеанса удаленный рабочий стол](terminal-services-permissions.md) , связываемых с указанной учетной записью. Значением этого параметра является точечный рисунок, и можно выбрать любое или все из следующих значений.

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

*Успешное завершение* \[ окне\]
</dt> <dd>

Указывает, разрешен или запрещен набор разрешений, заданный значением параметра *пермиссионмаск* .

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

## <a name="remarks"></a>Комментарии

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



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

 

