---
title: Метод Жеттстолсконнективитистатус класса Win32_TerminalServiceSetting
description: Определяет состояние подключения между службы удаленных рабочих столов и сервером лицензирования.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеттстолсконнективитистатус
- Службы удаленных рабочих столов метода Жеттстолсконнективитистатус, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жеттстолсконнективитистатус
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491340"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Метод Жеттстолсконнективитистатус \_ класса Win32 терминалсервицесеттинг

Определяет состояние подключения между службы удаленных рабочих столов и сервером лицензирования.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя сервера* \[ окне\]
</dt> <dd>

Имя сервера лицензирования, для которого проверяется состояние подключения.

</dd> <dt>

*Тстолсконнективитистатус* \[ заполняет\]
</dt> <dd>

Значение, указывающее состояние подключения сервера лицензирования. Это может быть одно из следующих значений.

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Лат \_ Неизвестный \_ для подключения** (0)


</dt> <dd>

Невозможно определить состояние подключения.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Лат \_ Подсоединенная \_ допустимая \_ WS08R2** (1)


</dt> <dd>

Службы удаленных рабочих столов может подключиться к серверу лицензирования Windows Server 2008 R2.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Лат \_ Подсоединенная \_ допустимая \_ WS08** (2)


</dt> <dd>

Службы удаленных рабочих столов может подключиться к серверу лицензий Windows Server 2008.

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Лат \_ Несоответствие ПОДКЛЮЧАЕМого \_ бета-версии \_ RTM \_** (3)


</dt> <dd>

Службы удаленных рабочих столов может подключиться к серверу лицензирования, но на одном из серверов работает бета-версия операционной системы.

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Лат \_ Версия с ПОДКЛЮЧЕНИЕм \_ более ранней \_ версии** (4)


</dt> <dd>

Службы удаленных рабочих столов может подключиться к серверу лицензирования, но существует несовместимость между сервером лицензирования и сервером службы удаленных рабочих столов узла.

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Лат \_ СОЕДИНЕНИЕ \_ не \_ в \_ тскграуп** (5)


</dt> <dd>

Групповая политика безопасности включена на сервере лицензирования, но службы удаленных рабочих столов не является частью групповой политики.

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Лат \_ НЕ \_ подсоединено** (6)


</dt> <dd>

Службы удаленных рабочих столов не удается подключиться к серверу лицензирования.

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Лат \_ \_Неизвестная \_ достоверность** (7)


</dt> <dd>

Сервер лицензирования может быть подключен к, но не удается определить допустимость соединения.

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Лат \_ ПОДКЛЮЧЕНИЕ \_ \_ разрешено, но доступ \_ запрещен** (8)


</dt> <dd>

Службы удаленных рабочих столов может подключиться к серверу лицензирования, но учетная запись пользователя не имеет прав администратора на сервере лицензирования.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Лат \_ Подсоединенная \_ допустимая \_ WS08R2 \_ VDI** (9)


</dt> <dd>

Службы удаленных рабочих столов может подключаться к серверу инфраструктуры виртуальных рабочих столов Windows Server 2008 R2 (VDI).

**Windows Server 2008 R2:** Это значение не поддерживается до Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Лат \_ Возможность подключения \_ \_ не \_ поддерживается** (10)


</dt> <dd>

Эта функция не поддерживается.

**Windows server 2008 R2 и Windows server 2008 R2 с пакетом обновления 1 (SP1):** Это значение не поддерживается до Windows Server 2012.

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Лат \_ Подсоединенная \_ допустимая \_ Ls** (11)


</dt> <dd>

Сервер лицензирования является допустимым.

**Windows server 2008 R2 и Windows server 2008 R2 с пакетом обновления 1 (SP1):** Это значение не поддерживается до Windows Server 2012.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                       |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Терминалсервицесеттинг Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





