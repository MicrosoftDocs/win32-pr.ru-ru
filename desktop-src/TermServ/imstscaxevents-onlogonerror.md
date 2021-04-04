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
# <a name="imstscaxeventsonlogonerror-method"></a><span data-ttu-id="29450-106">Метод Имстскаксевентс:: Онлогонеррор</span><span class="sxs-lookup"><span data-stu-id="29450-106">IMsTscAxEvents::OnLogonError method</span></span>

<span data-ttu-id="29450-107">Вызывается при возникновении ошибки входа в систему или другого события входа.</span><span class="sxs-lookup"><span data-stu-id="29450-107">Called when a logon error or other logon event occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="29450-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29450-108">Syntax</span></span>


```C++
void OnLogonError(
  [in] LONG lError
);
```



## <a name="parameters"></a><span data-ttu-id="29450-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="29450-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29450-110">*леррор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29450-110">*lError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29450-111">Код ошибки входа.</span><span class="sxs-lookup"><span data-stu-id="29450-111">The logon error code.</span></span> <span data-ttu-id="29450-112">Этот список кодов не является исчерпывающим.</span><span class="sxs-lookup"><span data-stu-id="29450-112">This list of codes is not exhaustive.</span></span>

<dt>

<span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>

<span data-ttu-id="29450-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**Арбитраж \_ \_ \_ Параметры выпуклости кода** (-5 (0xFFFFFFFB))</span><span class="sxs-lookup"><span data-stu-id="29450-113"><span id="ARBITRATION_CODE_BUMP_OPTIONS"></span><span id="arbitration_code_bump_options"></span>**ARBITRATION\_CODE\_BUMP\_OPTIONS** (-5 (0xFFFFFFFB))</span></span>


</dt> <dd>

<span data-ttu-id="29450-114">Winlogon выводит диалоговое окно **состязание за сеанс** .</span><span class="sxs-lookup"><span data-stu-id="29450-114">Winlogon is displaying the **Session Contention** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>

<span data-ttu-id="29450-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**Арбитраж \_ Продолжение кода при \_ \_ входе** (-2 (0xFFFFFFFE))</span><span class="sxs-lookup"><span data-stu-id="29450-115"><span id="ARBITRATION_CODE_CONTINUE_LOGON"></span><span id="arbitration_code_continue_logon"></span>**ARBITRATION\_CODE\_CONTINUE\_LOGON** (-2 (0xFFFFFFFE))</span></span>


</dt> <dd>

<span data-ttu-id="29450-116">Winlogon продолжает процесс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="29450-116">Winlogon is continuing with the logon process.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>

<span data-ttu-id="29450-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**Арбитраж \_ \_Продолжение кода \_ прекращено** (-3 (0xFFFFFFFD))</span><span class="sxs-lookup"><span data-stu-id="29450-117"><span id="ARBITRATION_CODE_CONTINUE_TERMINATE"></span><span id="arbitration_code_continue_terminate"></span>**ARBITRATION\_CODE\_CONTINUE\_TERMINATE** (-3 (0xFFFFFFFD))</span></span>


</dt> <dd>

<span data-ttu-id="29450-118">Winlogon завершается без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="29450-118">Winlogon is ending silently.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>

<span data-ttu-id="29450-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**Арбитраж \_ \_ \_ Диалоговое окно "НЕразрешение кода** " (-6 (0xFFFFFFFA))</span><span class="sxs-lookup"><span data-stu-id="29450-119"><span id="ARBITRATION_CODE_NOPERM_DIALOG"></span><span id="arbitration_code_noperm_dialog"></span>**ARBITRATION\_CODE\_NOPERM\_DIALOG** (-6 (0xFFFFFFFA))</span></span>


</dt> <dd>

<span data-ttu-id="29450-120">Winlogon выводит диалоговое окно **нет разрешений** .</span><span class="sxs-lookup"><span data-stu-id="29450-120">Winlogon is displaying the **No Permissions** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>

<span data-ttu-id="29450-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**Арбитраж \_ \_ \_ Диалоговое окно с отклонением кода** (-7 (0xFFFFFFF9))</span><span class="sxs-lookup"><span data-stu-id="29450-121"><span id="ARBITRATION_CODE_REFUSED_DIALOG"></span><span id="arbitration_code_refused_dialog"></span>**ARBITRATION\_CODE\_REFUSED\_DIALOG** (-7 (0xFFFFFFF9))</span></span>


</dt> <dd>

<span data-ttu-id="29450-122">Winlogon выводит диалоговое окно **отказ в соединении** .</span><span class="sxs-lookup"><span data-stu-id="29450-122">Winlogon is displaying the **Disconnect Refused** dialog box.</span></span>

</dd> <dt>

<span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>

<span data-ttu-id="29450-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**Арбитраж \_ \_ \_ Параметры перенастройки кода** (-4 (0xFFFFFFFC))</span><span class="sxs-lookup"><span data-stu-id="29450-123"><span id="ARBITRATION_CODE_RECONN_OPTIONS"></span><span id="arbitration_code_reconn_options"></span>**ARBITRATION\_CODE\_RECONN\_OPTIONS** (-4 (0xFFFFFFFC))</span></span>


</dt> <dd>

<span data-ttu-id="29450-124">Winlogon отображает диалоговое окно **Повторное подключение** .</span><span class="sxs-lookup"><span data-stu-id="29450-124">Winlogon is displaying the **Reconnect** dialog box.</span></span>

</dd> <dt>

<span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>

<span data-ttu-id="29450-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**Ошибка при \_ \_ \_ Отказано в доступе к коду** (-1 (0xFFFFFFFF))</span><span class="sxs-lookup"><span data-stu-id="29450-125"><span id="ERROR_CODE_ACCESS_DENIED"></span><span id="error_code_access_denied"></span>**ERROR\_CODE\_ACCESS\_DENIED** (-1 (0xFFFFFFFF))</span></span>


</dt> <dd>

<span data-ttu-id="29450-126">Пользователю отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="29450-126">The user was denied access.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>

<span data-ttu-id="29450-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**Вход в систему \_ Неудачный \_ неправильный \_ пароль** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="29450-127"><span id="LOGON_FAILED_BAD_PASSWORD"></span><span id="logon_failed_bad_password"></span>**LOGON\_FAILED\_BAD\_PASSWORD** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="29450-128">Вход не выполнен из-за недопустимых учетных данных для входа.</span><span class="sxs-lookup"><span data-stu-id="29450-128">The logon failed because the logon credentials are not valid.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>

<span data-ttu-id="29450-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**Вход в систему \_ \_Другой сбой** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="29450-129"><span id="LOGON_FAILED_OTHER"></span><span id="logon_failed_other"></span>**LOGON\_FAILED\_OTHER** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="29450-130">Произошла другая ошибка входа или после входа.</span><span class="sxs-lookup"><span data-stu-id="29450-130">Another logon or post-logon error occurred.</span></span> <span data-ttu-id="29450-131">Клиент удаленный рабочий стол отображает экран входа для пользователя.</span><span class="sxs-lookup"><span data-stu-id="29450-131">The Remote Desktop client displays a logon screen to the user.</span></span>

</dd> <dt>

<span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>

<span data-ttu-id="29450-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**Вход в систему \_ Неудачный \_ \_ пароль обновления** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="29450-132"><span id="LOGON_FAILED_UPDATE_PASSWORD"></span><span id="logon_failed_update_password"></span>**LOGON\_FAILED\_UPDATE\_PASSWORD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="29450-133">Срок действия пароля истек.</span><span class="sxs-lookup"><span data-stu-id="29450-133">The password is expired.</span></span> <span data-ttu-id="29450-134">Чтобы продолжить вход, пользователь должен обновить свой пароль.</span><span class="sxs-lookup"><span data-stu-id="29450-134">The user must update their password to continue logging on.</span></span>

</dd> <dt>

<span id="LOGON_WARNING"></span><span id="logon_warning"></span>

<span data-ttu-id="29450-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**Вход в систему \_ ПРЕДУПРЕЖДЕНИЕ** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="29450-135"><span id="LOGON_WARNING"></span><span id="logon_warning"></span>**LOGON\_WARNING** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="29450-136">Клиент удаленный рабочий стол отображает диалоговое окно, содержащее важную информацию о пользователе.</span><span class="sxs-lookup"><span data-stu-id="29450-136">The Remote Desktop client displays a dialog box that contains important information for the user.</span></span>

</dd> <dt>

<span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>

<span data-ttu-id="29450-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**Состояние \_ \_Ограничение учетной записи** (-1073741714 (0xC000006E))</span><span class="sxs-lookup"><span data-stu-id="29450-137"><span id="STATUS_ACCOUNT_RESTRICTION"></span><span id="status_account_restriction"></span>**STATUS\_ACCOUNT\_RESTRICTION** (-1073741714 (0xC000006E))</span></span>


</dt> <dd>

<span data-ttu-id="29450-138">Имя пользователя и сведения о проверке подлинности действительны, но проверка подлинности заблокирована из-за ограничений учетной записи пользователя, например ограничений по времени суток.</span><span class="sxs-lookup"><span data-stu-id="29450-138">The user name and authentication information are valid, but authentication was blocked due to restrictions on the user account, such as time-of-day restrictions.</span></span>

</dd> <dt>

<span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>

<span data-ttu-id="29450-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**Состояние \_ \_Ошибка входа в систему** (-1073741715 (0xC000006D))</span><span class="sxs-lookup"><span data-stu-id="29450-139"><span id="STATUS_LOGON_FAILURE"></span><span id="status_logon_failure"></span>**STATUS\_LOGON\_FAILURE** (-1073741715 (0xC000006D))</span></span>


</dt> <dd>

<span data-ttu-id="29450-140">Попытка входа недопустима.</span><span class="sxs-lookup"><span data-stu-id="29450-140">The attempted logon is not valid.</span></span> <span data-ttu-id="29450-141">Это связано с неверным именем пользователя или неправильными данными проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="29450-141">This is due to either an incorrect user name or incorrect authentication information.</span></span>

</dd> <dt>

<span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>

<span data-ttu-id="29450-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**Состояние \_ ПАРОЛЬ \_ должен \_ измениться** (-1073741276 (0xC0000224))</span><span class="sxs-lookup"><span data-stu-id="29450-142"><span id="STATUS_PASSWORD_MUST_CHANGE"></span><span id="status_password_must_change"></span>**STATUS\_PASSWORD\_MUST\_CHANGE** (-1073741276 (0xC0000224))</span></span>


</dt> <dd>

<span data-ttu-id="29450-143">Срок действия пароля истек.</span><span class="sxs-lookup"><span data-stu-id="29450-143">The password is expired.</span></span> <span data-ttu-id="29450-144">Чтобы продолжить вход, пользователь должен обновить свой пароль.</span><span class="sxs-lookup"><span data-stu-id="29450-144">The user must update their password to continue logging on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29450-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29450-145">Return value</span></span>

<span data-ttu-id="29450-146">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="29450-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29450-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29450-147">Remarks</span></span>

<span data-ttu-id="29450-148">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что произошла ошибка входа в систему.</span><span class="sxs-lookup"><span data-stu-id="29450-148">Implement this method in your event sink to receive notification that a logon error has occurred.</span></span>

<span data-ttu-id="29450-149">Этот список кодов не является исчерпывающим.</span><span class="sxs-lookup"><span data-stu-id="29450-149">This list of codes is not exhaustive.</span></span>

## <a name="requirements"></a><span data-ttu-id="29450-150">Требования</span><span class="sxs-lookup"><span data-stu-id="29450-150">Requirements</span></span>



| <span data-ttu-id="29450-151">Требование</span><span class="sxs-lookup"><span data-stu-id="29450-151">Requirement</span></span> | <span data-ttu-id="29450-152">Значение</span><span class="sxs-lookup"><span data-stu-id="29450-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29450-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29450-153">Minimum supported client</span></span><br/> | <span data-ttu-id="29450-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29450-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="29450-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29450-155">Minimum supported server</span></span><br/> | <span data-ttu-id="29450-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29450-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="29450-157">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="29450-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="29450-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29450-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="29450-159">DLL</span><span class="sxs-lookup"><span data-stu-id="29450-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29450-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29450-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="29450-161">IID</span><span class="sxs-lookup"><span data-stu-id="29450-161">IID</span></span><br/>                      | <span data-ttu-id="29450-162">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="29450-162">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="29450-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29450-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29450-164">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="29450-164">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





