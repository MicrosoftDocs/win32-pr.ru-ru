---
title: Имстскаксевентс Онлогонеррор, метод
description: Вызывается при возникновении ошибки входа в систему или другого события входа.
ms.assetid: 5af9656b-f99b-4535-ab83-6ecc9bc41808
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онлогонеррор
- Службы удаленных рабочих столов метода Онлогонеррор, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онлогонеррор
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLogonError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45fe23c992f14a421c00a4feefd9c4ed95aff07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802740"
---
# <a name="imstscaxeventsonlogonerror-method"></a>Метод Имстскаксевентс:: Онлогонеррор

Вызывается при возникновении ошибки входа в систему или другого события входа.

## <a name="syntax"></a>Синтаксис


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*леррор* \[ окне\]
</dt> <dd>

Код ошибки входа. Этот список кодов не является исчерпывающим.

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Арбитраж \_ \_ \_ Параметры выпуклости кода** (-5 (0xFFFFFFFB))


</dt> <dd>

Winlogon выводит диалоговое окно **состязание за сеанс** .

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Арбитраж \_ Продолжение кода при \_ \_ входе** (-2 (0xFFFFFFFE))


</dt> <dd>

Winlogon продолжает процесс входа в систему.

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Арбитраж \_ \_Продолжение кода \_ прекращено** (-3 (0xFFFFFFFD))


</dt> <dd>

Winlogon завершается без вмешательства пользователя.

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Арбитраж \_ \_ \_ Диалоговое окно "НЕразрешение кода** " (-6 (0xFFFFFFFA))


</dt> <dd>

Winlogon выводит диалоговое окно **нет разрешений** .

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Арбитраж \_ \_ \_ Диалоговое окно с отклонением кода** (-7 (0xFFFFFFF9))


</dt> <dd>

Winlogon выводит диалоговое окно **отказ в соединении** .

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Арбитраж \_ \_ \_ Параметры перенастройки кода** (-4 (0xFFFFFFFC))


</dt> <dd>

Winlogon отображает диалоговое окно **Повторное подключение** .

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Ошибка при \_ \_ \_ Отказано в доступе к коду** (-1 (0xFFFFFFFF))


</dt> <dd>

Пользователю отказано в доступе.

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Вход в систему \_ Неудачный \_ неправильный \_ пароль** (0 (0x0))


</dt> <dd>

Вход не выполнен из-за недопустимых учетных данных для входа.

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Вход в систему \_ \_Другой сбой** (2 (0x2))


</dt> <dd>

Произошла другая ошибка входа или после входа. Клиент удаленный рабочий стол отображает экран входа для пользователя.

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Вход в систему \_ Неудачный \_ \_ пароль обновления** (1 (0x1))


</dt> <dd>

Срок действия пароля истек. Чтобы продолжить вход, пользователь должен обновить свой пароль.

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Вход в систему \_ ПРЕДУПРЕЖДЕНИЕ** (3 (0x3))


</dt> <dd>

Клиент удаленный рабочий стол отображает диалоговое окно, содержащее важную информацию о пользователе.

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Состояние \_ \_Ограничение учетной записи** (-1073741714 (0xC000006E))


</dt> <dd>

Имя пользователя и сведения о проверке подлинности действительны, но проверка подлинности заблокирована из-за ограничений учетной записи пользователя, например ограничений по времени суток.

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Состояние \_ \_Ошибка входа в систему** (-1073741715 (0xC000006D))


</dt> <dd>

Попытка входа недопустима. Это связано с неверным именем пользователя или неправильными данными проверки подлинности.

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Состояние \_ ПАРОЛЬ \_ должен \_ измениться** (-1073741276 (0xC0000224))


</dt> <dd>

Срок действия пароля истек. Чтобы продолжить вход, пользователь должен обновить свой пароль.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что произошла ошибка входа в систему.

Этот список кодов не является исчерпывающим.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





