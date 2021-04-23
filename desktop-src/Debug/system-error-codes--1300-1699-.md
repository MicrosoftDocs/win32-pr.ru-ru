---
description: Описание кодов ошибок 1300-1699, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Коды системных ошибок (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496242"
---
# <a name="system-error-codes-1300-1699"></a><span data-ttu-id="ce714-103">Коды системных ошибок (1300-1699)</span><span class="sxs-lookup"><span data-stu-id="ce714-103">System Error Codes (1300-1699)</span></span>

> [!NOTE]
> <span data-ttu-id="ce714-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="ce714-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="ce714-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce714-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="ce714-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 1300 – 1699.</span><span class="sxs-lookup"><span data-stu-id="ce714-106">The following list describes [system error codes](system-error-codes.md) for errors 1300 to 1699.</span></span> <span data-ttu-id="ce714-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="ce714-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="ce714-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="ce714-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="ce714-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**Ошибка \_ не \_ \_ назначена всем**</span><span class="sxs-lookup"><span data-stu-id="ce714-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR\_NOT\_ALL\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-110">1300 (0x514)</span><span class="sxs-lookup"><span data-stu-id="ce714-110">1300 (0x514)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-111">Не все привилегии или группы, на которые имеются ссылки, назначены вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="ce714-111">Not all privileges or groups referenced are assigned to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**Ошибка \_ \_ не \_ сопоставлена**</span><span class="sxs-lookup"><span data-stu-id="ce714-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR\_SOME\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-113">1301 (0x515)</span><span class="sxs-lookup"><span data-stu-id="ce714-113">1301 (0x515)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-114">Не было выполнено сопоставление между именами учетных записей и идентификаторами безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-114">Some mapping between account names and security IDs was not done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**Ошибка при \_ отсутствии \_ квот \_ для \_ учетной записи**</span><span class="sxs-lookup"><span data-stu-id="ce714-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR\_NO\_QUOTAS\_FOR\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-116">1302 (0x516)</span><span class="sxs-lookup"><span data-stu-id="ce714-116">1302 (0x516)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-117">Для этой учетной записи не заданы ограничения системной квоты.</span><span class="sxs-lookup"><span data-stu-id="ce714-117">No system quota limits are specifically set for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**Ошибка \_ \_ \_ ключа сеанса локального пользователя \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR\_LOCAL\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-119">1303 (0x517)</span><span class="sxs-lookup"><span data-stu-id="ce714-119">1303 (0x517)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-120">Ключ шифрования недоступен.</span><span class="sxs-lookup"><span data-stu-id="ce714-120">No encryption key is available.</span></span> <span data-ttu-id="ce714-121">Был возвращен хорошо известный ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="ce714-121">A well-known encryption key was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**Ошибка \_ null \_ \_ пароль LM**</span><span class="sxs-lookup"><span data-stu-id="ce714-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR\_NULL\_LM\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-123">1304 (0x518)</span><span class="sxs-lookup"><span data-stu-id="ce714-123">1304 (0x518)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-124">Пароль слишком сложен для преобразования в пароль LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="ce714-124">The password is too complex to be converted to a LAN Manager password.</span></span> <span data-ttu-id="ce714-125">Возвращенный пароль LAN Manager является **пустой** строкой.</span><span class="sxs-lookup"><span data-stu-id="ce714-125">The LAN Manager password returned is a **NULL** string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**Ошибка \_ неизвестной \_ редакции**</span><span class="sxs-lookup"><span data-stu-id="ce714-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR\_UNKNOWN\_REVISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-127">1305 (0x519)</span><span class="sxs-lookup"><span data-stu-id="ce714-127">1305 (0x519)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-128">Неизвестный уровень редакции.</span><span class="sxs-lookup"><span data-stu-id="ce714-128">The revision level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**\_несоответствие редакции ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR\_REVISION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-130">1306 (0x51A)</span><span class="sxs-lookup"><span data-stu-id="ce714-130">1306 (0x51A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-131">Указывает, что два уровня редакции несовместимы.</span><span class="sxs-lookup"><span data-stu-id="ce714-131">Indicates two revision levels are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**Ошибка \_ недопустимого \_ владельца**</span><span class="sxs-lookup"><span data-stu-id="ce714-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR\_INVALID\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-133">1307 (0x51B)</span><span class="sxs-lookup"><span data-stu-id="ce714-133">1307 (0x51B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-134">Этот идентификатор безопасности нельзя назначить в качестве владельца этого объекта.</span><span class="sxs-lookup"><span data-stu-id="ce714-134">This security ID may not be assigned as the owner of this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**Ошибка \_ недопустимой \_ основной \_ группы**</span><span class="sxs-lookup"><span data-stu-id="ce714-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR\_INVALID\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-136">1308 (0x51C)</span><span class="sxs-lookup"><span data-stu-id="ce714-136">1308 (0x51C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-137">Этот идентификатор безопасности нельзя назначить в качестве основной группы объекта.</span><span class="sxs-lookup"><span data-stu-id="ce714-137">This security ID may not be assigned as the primary group of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**Ошибка \_ без \_ \_ маркера олицетворения**</span><span class="sxs-lookup"><span data-stu-id="ce714-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR\_NO\_IMPERSONATION\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-139">1309 (0x51D)</span><span class="sxs-lookup"><span data-stu-id="ce714-139">1309 (0x51D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-140">Предпринята попытка обработать токен олицетворения потоком, который в настоящее время не олицетворяет клиента.</span><span class="sxs-lookup"><span data-stu-id="ce714-140">An attempt has been made to operate on an impersonation token by a thread that is not currently impersonating a client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ОШИБКА не \_ удается \_ Отключить \_ обязательный параметр**</span><span class="sxs-lookup"><span data-stu-id="ce714-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR\_CANT\_DISABLE\_MANDATORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-142">1310 (0x51E)</span><span class="sxs-lookup"><span data-stu-id="ce714-142">1310 (0x51E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-143">Группа может быть отключена.</span><span class="sxs-lookup"><span data-stu-id="ce714-143">The group may not be disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**\_нет \_ серверов входа в систему \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR\_NO\_LOGON\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-145">1311 (0x51F)</span><span class="sxs-lookup"><span data-stu-id="ce714-145">1311 (0x51F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-146">В настоящее время нет доступных серверов входа для обслуживания запроса на вход.</span><span class="sxs-lookup"><span data-stu-id="ce714-146">There are currently no logon servers available to service the logon request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**Ошибка \_ без \_ \_ сеанса входа в систему \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR\_NO\_SUCH\_LOGON\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-148">1312 (0x520)</span><span class="sxs-lookup"><span data-stu-id="ce714-148">1312 (0x520)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-149">A specified logon session does not exist.</span><span class="sxs-lookup"><span data-stu-id="ce714-149">A specified logon session does not exist.</span></span> <span data-ttu-id="ce714-150">Возможно, он уже завершен.</span><span class="sxs-lookup"><span data-stu-id="ce714-150">It may already have been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**Ошибка \_ без \_ такой \_ привилегии**</span><span class="sxs-lookup"><span data-stu-id="ce714-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR\_NO\_SUCH\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-152">1313 (0x521)</span><span class="sxs-lookup"><span data-stu-id="ce714-152">1313 (0x521)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-153">Указанное право доступа не существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-153">A specified privilege does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**права на ошибку \_ \_ не \_ удерживаются**</span><span class="sxs-lookup"><span data-stu-id="ce714-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**ERROR\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-155">1314 (0x522)</span><span class="sxs-lookup"><span data-stu-id="ce714-155">1314 (0x522)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-156">Клиент не располагает требуемыми правами доступа.</span><span class="sxs-lookup"><span data-stu-id="ce714-156">A required privilege is not held by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**Ошибка при \_ недопустимом \_ имени учетной записи \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR\_INVALID\_ACCOUNT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-158">1315 (0x523)</span><span class="sxs-lookup"><span data-stu-id="ce714-158">1315 (0x523)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-159">Указанное имя не является правильно сформированным именем учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ce714-159">The name provided is not a properly formed account name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**Ошибка \_ пользователь \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ce714-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR\_USER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-161">1316 (0x524)</span><span class="sxs-lookup"><span data-stu-id="ce714-161">1316 (0x524)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-162">Указанная учетная запись уже существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-162">The specified account already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**Ошибка \_ без \_ такого \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="ce714-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR\_NO\_SUCH\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-164">1317 (0x525)</span><span class="sxs-lookup"><span data-stu-id="ce714-164">1317 (0x525)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-165">Указанная учетная запись не существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-165">The specified account does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**\_существует группа \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="ce714-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**ERROR\_GROUP\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-167">1318 (0x526)</span><span class="sxs-lookup"><span data-stu-id="ce714-167">1318 (0x526)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-168">Указанная группа уже существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-168">The specified group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**Ошибка \_ нет \_ такой \_ группы**</span><span class="sxs-lookup"><span data-stu-id="ce714-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR\_NO\_SUCH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-170">1319 (0x527)</span><span class="sxs-lookup"><span data-stu-id="ce714-170">1319 (0x527)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-171">Указанная группа не существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-171">The specified group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_элемент ошибки \_ в \_ группе**</span><span class="sxs-lookup"><span data-stu-id="ce714-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR\_MEMBER\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-173">1320 (0x528)</span><span class="sxs-lookup"><span data-stu-id="ce714-173">1320 (0x528)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-174">Либо указанная учетная запись пользователя уже является членом указанной группы, либо указанная группа не может быть удалена, так как она содержит элемент.</span><span class="sxs-lookup"><span data-stu-id="ce714-174">Either the specified user account is already a member of the specified group, or the specified group cannot be deleted because it contains a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**\_элемент ошибки \_ не входит \_ в \_ группу**</span><span class="sxs-lookup"><span data-stu-id="ce714-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**ERROR\_MEMBER\_NOT\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-176">1321 (0x529)</span><span class="sxs-lookup"><span data-stu-id="ce714-176">1321 (0x529)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-177">Указанная учетная запись пользователя не является членом указанной учетной записи группы.</span><span class="sxs-lookup"><span data-stu-id="ce714-177">The specified user account is not a member of the specified group account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**Ошибка \_ последнего \_ администратора**</span><span class="sxs-lookup"><span data-stu-id="ce714-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR\_LAST\_ADMIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-179">1322 (0x52A)</span><span class="sxs-lookup"><span data-stu-id="ce714-179">1322 (0x52A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-180">Эта операция запрещена, так как она может привести к отключению, удалению или невозможности входа в учетную запись администрирования.</span><span class="sxs-lookup"><span data-stu-id="ce714-180">This operation is disallowed as it could result in an administration account being disabled, deleted or unable to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ОШИБОЧный \_ \_ пароль**</span><span class="sxs-lookup"><span data-stu-id="ce714-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR\_WRONG\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-182">1323 (0x52B)</span><span class="sxs-lookup"><span data-stu-id="ce714-182">1323 (0x52B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-183">Не удалось обновить пароль.</span><span class="sxs-lookup"><span data-stu-id="ce714-183">Unable to update the password.</span></span> <span data-ttu-id="ce714-184">В качестве текущего пароля указано неверное значение.</span><span class="sxs-lookup"><span data-stu-id="ce714-184">The value provided as the current password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ОШИБКА с неправильным \_ \_ форматом \_ пароля**</span><span class="sxs-lookup"><span data-stu-id="ce714-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR\_ILL\_FORMED\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-186">1324 (0x52C)</span><span class="sxs-lookup"><span data-stu-id="ce714-186">1324 (0x52C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-187">Не удалось обновить пароль.</span><span class="sxs-lookup"><span data-stu-id="ce714-187">Unable to update the password.</span></span> <span data-ttu-id="ce714-188">Значение, указанное для нового пароля, содержит значения, недопустимые в паролях.</span><span class="sxs-lookup"><span data-stu-id="ce714-188">The value provided for the new password contains values that are not allowed in passwords.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_ограничение на пароли об ошибках \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**ERROR\_PASSWORD\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-190">1325 (0x52D)</span><span class="sxs-lookup"><span data-stu-id="ce714-190">1325 (0x52D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-191">Не удалось обновить пароль.</span><span class="sxs-lookup"><span data-stu-id="ce714-191">Unable to update the password.</span></span> <span data-ttu-id="ce714-192">Значение, указанное для нового пароля, не соответствует требованиям домена к длине, сложности или истории.</span><span class="sxs-lookup"><span data-stu-id="ce714-192">The value provided for the new password does not meet the length, complexity, or history requirements of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**Ошибка \_ при входе в систему \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR\_LOGON\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-194">1326 (0x52E)</span><span class="sxs-lookup"><span data-stu-id="ce714-194">1326 (0x52E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-195">Неправильное имя пользователя или пароль.</span><span class="sxs-lookup"><span data-stu-id="ce714-195">The user name or password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_ограничение учетной записи об ошибках \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**ERROR\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-197">1327 (0x52F)</span><span class="sxs-lookup"><span data-stu-id="ce714-197">1327 (0x52F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-198">Ограничения учетной записи запрещают вход пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="ce714-198">Account restrictions are preventing this user from signing in.</span></span> <span data-ttu-id="ce714-199">Например, пустые пароли не допускаются, время входа ограничено или применяется ограничение политики.</span><span class="sxs-lookup"><span data-stu-id="ce714-199">For example: blank passwords aren't allowed, sign-in times are limited, or a policy restriction has been enforced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**Ошибка \_ недопустимых \_ \_ часов входа**</span><span class="sxs-lookup"><span data-stu-id="ce714-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR\_INVALID\_LOGON\_HOURS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-201">1328 (0x530)</span><span class="sxs-lookup"><span data-stu-id="ce714-201">1328 (0x530)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-202">В вашей учетной записи есть ограничения по времени, которые не позволяют войти в систему прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="ce714-202">Your account has time restrictions that keep you from signing in right now.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**Ошибка \_ недопустимой \_ рабочей станции**</span><span class="sxs-lookup"><span data-stu-id="ce714-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR\_INVALID\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-204">1329 (0x531)</span><span class="sxs-lookup"><span data-stu-id="ce714-204">1329 (0x531)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-205">Этому пользователю запрещено входить на этот компьютер.</span><span class="sxs-lookup"><span data-stu-id="ce714-205">This user isn't allowed to sign in to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**\_ \_ срок действия пароля истек**</span><span class="sxs-lookup"><span data-stu-id="ce714-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERROR\_PASSWORD\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-207">1330 (0x532)</span><span class="sxs-lookup"><span data-stu-id="ce714-207">1330 (0x532)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-208">Срок действия пароля для этой учетной записи истек.</span><span class="sxs-lookup"><span data-stu-id="ce714-208">The password for this account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**\_учетная запись ошибок \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="ce714-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ERROR\_ACCOUNT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-210">1331 (0x533)</span><span class="sxs-lookup"><span data-stu-id="ce714-210">1331 (0x533)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-211">Этот пользователь не может войти в систему, так как эта учетная запись в настоящее время отключена.</span><span class="sxs-lookup"><span data-stu-id="ce714-211">This user can't sign in because this account is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**Ошибка " \_ нет \_ сопоставления"**</span><span class="sxs-lookup"><span data-stu-id="ce714-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR\_NONE\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-213">1332 (0x534)</span><span class="sxs-lookup"><span data-stu-id="ce714-213">1332 (0x534)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-214">Сопоставление между именами учетных записей и идентификаторами безопасности не выполнялось.</span><span class="sxs-lookup"><span data-stu-id="ce714-214">No mapping between account names and security IDs was done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**Ошибка \_ слишком \_ много \_ \_ запрошенных LUID**</span><span class="sxs-lookup"><span data-stu-id="ce714-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR\_TOO\_MANY\_LUIDS\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-216">1333 (0x535)</span><span class="sxs-lookup"><span data-stu-id="ce714-216">1333 (0x535)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-217">Слишком много локальных идентификаторов пользователей (LUID) запрошено за один раз.</span><span class="sxs-lookup"><span data-stu-id="ce714-217">Too many local user identifiers (LUIDs) were requested at one time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**Ошибка \_ LUID \_ исчерпана**</span><span class="sxs-lookup"><span data-stu-id="ce714-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR\_LUIDS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-219">1334 (0x536)</span><span class="sxs-lookup"><span data-stu-id="ce714-219">1334 (0x536)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-220">Больше нет доступных идентификаторов локальных пользователей (LUID).</span><span class="sxs-lookup"><span data-stu-id="ce714-220">No more local user identifiers (LUIDs) are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**Ошибка \_ недопустимого \_ \_ подцентра**</span><span class="sxs-lookup"><span data-stu-id="ce714-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR\_INVALID\_SUB\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-222">1335 (0x537)</span><span class="sxs-lookup"><span data-stu-id="ce714-222">1335 (0x537)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-223">Часть подавтора идентификатора безопасности недопустима для этого конкретного использования.</span><span class="sxs-lookup"><span data-stu-id="ce714-223">The subauthority part of a security ID is invalid for this particular use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**Ошибка \_ недопустимого \_ ACL**</span><span class="sxs-lookup"><span data-stu-id="ce714-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR\_INVALID\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-225">1336 (0x538)</span><span class="sxs-lookup"><span data-stu-id="ce714-225">1336 (0x538)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-226">Недопустимая структура списка управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="ce714-226">The access control list (ACL) structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**Ошибка \_ недопустимого \_ sid**</span><span class="sxs-lookup"><span data-stu-id="ce714-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR\_INVALID\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-228">1337 (0x539)</span><span class="sxs-lookup"><span data-stu-id="ce714-228">1337 (0x539)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-229">Недопустимая структура идентификатора безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-229">The security ID structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**Ошибка \_ недопустимых \_ \_ Descr безопасности**</span><span class="sxs-lookup"><span data-stu-id="ce714-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR\_INVALID\_SECURITY\_DESCR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-231">1338 (0x53A)</span><span class="sxs-lookup"><span data-stu-id="ce714-231">1338 (0x53A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-232">Недопустимая структура дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-232">The security descriptor structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**Ошибка при \_ неправильном \_ ACL наследования \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR\_BAD\_INHERITANCE\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-234">1340 (0x53C)</span><span class="sxs-lookup"><span data-stu-id="ce714-234">1340 (0x53C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-235">Не удалось построить наследуемый список управления доступом (ACL) или запись управления доступом (ACE).</span><span class="sxs-lookup"><span data-stu-id="ce714-235">The inherited access control list (ACL) or access control entry (ACE) could not be built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**\_сервер ошибок \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="ce714-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR\_SERVER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-237">1341 (0x53D)</span><span class="sxs-lookup"><span data-stu-id="ce714-237">1341 (0x53D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-238">Сервер в настоящее время отключен.</span><span class="sxs-lookup"><span data-stu-id="ce714-238">The server is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**\_сервер ошибок \_ не \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="ce714-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR\_SERVER\_NOT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-240">1342 (0x53E)</span><span class="sxs-lookup"><span data-stu-id="ce714-240">1342 (0x53E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-241">Сервер в настоящее время включен.</span><span class="sxs-lookup"><span data-stu-id="ce714-241">The server is currently enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**Ошибка при \_ недопустимом \_ \_ центре идентификации**</span><span class="sxs-lookup"><span data-stu-id="ce714-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR\_INVALID\_ID\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-243">1343 (0x53F)</span><span class="sxs-lookup"><span data-stu-id="ce714-243">1343 (0x53F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-244">Предоставлено недопустимое значение для центра идентификации.</span><span class="sxs-lookup"><span data-stu-id="ce714-244">The value provided was an invalid value for an identifier authority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**\_превышено выделенное место для ошибки \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERROR\_ALLOTTED\_SPACE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-246">1344 (0x540)</span><span class="sxs-lookup"><span data-stu-id="ce714-246">1344 (0x540)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-247">Больше нет доступной памяти для обновлений сведений о безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-247">No more memory is available for security information updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**Ошибка \_ недопустимых \_ \_ атрибутов группы**</span><span class="sxs-lookup"><span data-stu-id="ce714-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR\_INVALID\_GROUP\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-249">1345 (0x541)</span><span class="sxs-lookup"><span data-stu-id="ce714-249">1345 (0x541)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-250">Указанные атрибуты недопустимы или несовместимы с атрибутами группы в целом.</span><span class="sxs-lookup"><span data-stu-id="ce714-250">The specified attributes are invalid, or incompatible with the attributes for the group as a whole.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**Ошибка \_ неверного \_ уровня олицетворения \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR\_BAD\_IMPERSONATION\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-252">1346 (0x542)</span><span class="sxs-lookup"><span data-stu-id="ce714-252">1346 (0x542)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-253">Либо не обеспечен необходимый уровень олицетворения, либо уровень олицетворения недопустим.</span><span class="sxs-lookup"><span data-stu-id="ce714-253">Either a required impersonation level was not provided, or the provided impersonation level is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ОШИБКА не \_ удается \_ открыть \_ анонимную**</span><span class="sxs-lookup"><span data-stu-id="ce714-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR\_CANT\_OPEN\_ANONYMOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-255">1347 (0x543)</span><span class="sxs-lookup"><span data-stu-id="ce714-255">1347 (0x543)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-256">Не удается открыть маркер безопасности анонимного уровня.</span><span class="sxs-lookup"><span data-stu-id="ce714-256">Cannot open an anonymous level security token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**Ошибка \_ неправильного \_ \_ класса проверки**</span><span class="sxs-lookup"><span data-stu-id="ce714-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR\_BAD\_VALIDATION\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-258">1348 (0x544)</span><span class="sxs-lookup"><span data-stu-id="ce714-258">1348 (0x544)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-259">Запрошен недопустимый класс сведений о проверке.</span><span class="sxs-lookup"><span data-stu-id="ce714-259">The validation information class requested was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**Ошибка \_ неправильного \_ типа токена \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR\_BAD\_TOKEN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-261">1349 (0x545)</span><span class="sxs-lookup"><span data-stu-id="ce714-261">1349 (0x545)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-262">Тип токена не подходит для использования при его использовании.</span><span class="sxs-lookup"><span data-stu-id="ce714-262">The type of the token is inappropriate for its attempted use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**Ошибка \_ \_ при отсутствии безопасности \_ для \_ объекта**</span><span class="sxs-lookup"><span data-stu-id="ce714-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR\_NO\_SECURITY\_ON\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-264">1350 (0x546)</span><span class="sxs-lookup"><span data-stu-id="ce714-264">1350 (0x546)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-265">Не удалось выполнить операцию безопасности для объекта, который не имеет связанной безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-265">Unable to perform a security operation on an object that has no associated security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ОШИБКА не \_ удается \_ получить доступ к \_ \_ сведениям о домене**</span><span class="sxs-lookup"><span data-stu-id="ce714-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR\_CANT\_ACCESS\_DOMAIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-267">1351 (0x547)</span><span class="sxs-lookup"><span data-stu-id="ce714-267">1351 (0x547)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-268">Не удалось прочитать сведения о конфигурации из контроллера домена, так как компьютер недоступен или доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="ce714-268">Configuration information could not be read from the domain controller, either because the machine is unavailable, or access has been denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**Ошибка \_ недопустимого \_ \_ состояния сервера**</span><span class="sxs-lookup"><span data-stu-id="ce714-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR\_INVALID\_SERVER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-270">1352 (0x548)</span><span class="sxs-lookup"><span data-stu-id="ce714-270">1352 (0x548)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-271">Диспетчеру учетных записей безопасности (SAM) или локальному администратору безопасности (LSA) находилось в неправильном состоянии выполнить операцию безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-271">The security account manager (SAM) or local security authority (LSA) server was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**Ошибка \_ недопустимого \_ \_ состояния домена**</span><span class="sxs-lookup"><span data-stu-id="ce714-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR\_INVALID\_DOMAIN\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-273">1353 (0x549)</span><span class="sxs-lookup"><span data-stu-id="ce714-273">1353 (0x549)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-274">Домен находился в неправильном состоянии для выполнения операции безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-274">The domain was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**Ошибка \_ недопустимой \_ \_ роли домена**</span><span class="sxs-lookup"><span data-stu-id="ce714-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR\_INVALID\_DOMAIN\_ROLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-276">1354 (0x54A)</span><span class="sxs-lookup"><span data-stu-id="ce714-276">1354 (0x54A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-277">Эта операция разрешена только для основного контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="ce714-277">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**Ошибка \_ без \_ такого \_ домена**</span><span class="sxs-lookup"><span data-stu-id="ce714-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR\_NO\_SUCH\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-279">1355 (0x54B)</span><span class="sxs-lookup"><span data-stu-id="ce714-279">1355 (0x54B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-280">Указанный домен не существует, или к нему не удалось подключиться.</span><span class="sxs-lookup"><span data-stu-id="ce714-280">The specified domain either does not exist or could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**\_домен ошибок \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ce714-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**ERROR\_DOMAIN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-282">1356 (0x54C)</span><span class="sxs-lookup"><span data-stu-id="ce714-282">1356 (0x54C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-283">Указанный домен уже существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-283">The specified domain already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**\_ \_ превышен предел для домена с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**ERROR\_DOMAIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-285">1357 (0x54D)</span><span class="sxs-lookup"><span data-stu-id="ce714-285">1357 (0x54D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-286">Предпринята попытка превысить предельное число доменов на сервер.</span><span class="sxs-lookup"><span data-stu-id="ce714-286">An attempt was made to exceed the limit on the number of domains per server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**Ошибка \_ внутреннего \_ повреждения базы данных \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR\_INTERNAL\_DB\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-288">1358 (0x54E)</span><span class="sxs-lookup"><span data-stu-id="ce714-288">1358 (0x54E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-289">Не удалось завершить запрошенную операцию из-за катастрофического сбоя носителя или повреждения структуры данных на диске.</span><span class="sxs-lookup"><span data-stu-id="ce714-289">Unable to complete the requested operation because of either a catastrophic media failure or a data structure corruption on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ПРОИЗОШЛа \_ Внутренняя \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="ce714-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-291">1359 (0x54F)</span><span class="sxs-lookup"><span data-stu-id="ce714-291">1359 (0x54F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-292">Внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="ce714-292">An internal error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**Ошибка \_ Generic \_ не \_ сопоставлена**</span><span class="sxs-lookup"><span data-stu-id="ce714-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR\_GENERIC\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-294">1360 (0x550)</span><span class="sxs-lookup"><span data-stu-id="ce714-294">1360 (0x550)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-295">Универсальные типы доступа содержались в маске доступа, которая должна быть уже сопоставлена с неуниверсальными типами.</span><span class="sxs-lookup"><span data-stu-id="ce714-295">Generic access types were contained in an access mask which should already be mapped to nongeneric types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**Ошибка в \_ неправильном \_ формате дескриптора \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR\_BAD\_DESCRIPTOR\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-297">1361 (0x551)</span><span class="sxs-lookup"><span data-stu-id="ce714-297">1361 (0x551)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-298">Неправильный формат дескриптора безопасности (абсолютный или автономный).</span><span class="sxs-lookup"><span data-stu-id="ce714-298">A security descriptor is not in the right format (absolute or self-relative).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**Ошибка \_ при \_ входе в \_ процесс**</span><span class="sxs-lookup"><span data-stu-id="ce714-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR\_NOT\_LOGON\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-300">1362 (0x552)</span><span class="sxs-lookup"><span data-stu-id="ce714-300">1362 (0x552)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-301">Запрошенное действие ограничено только процессами входа в систему.</span><span class="sxs-lookup"><span data-stu-id="ce714-301">The requested action is restricted for use by logon processes only.</span></span> <span data-ttu-id="ce714-302">Вызывающий процесс не зарегистрирован в качестве процесса входа в систему.</span><span class="sxs-lookup"><span data-stu-id="ce714-302">The calling process has not registered as a logon process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**\_ \_ существует сеанс с ошибкой входа \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERROR\_LOGON\_SESSION\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-304">1363 (0x553)</span><span class="sxs-lookup"><span data-stu-id="ce714-304">1363 (0x553)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-305">Невозможно запустить новый сеанс входа с уже используемым ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="ce714-305">Cannot start a new logon session with an ID that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**Ошибка \_ \_ : такой \_ пакет отсутствует**</span><span class="sxs-lookup"><span data-stu-id="ce714-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR\_NO\_SUCH\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-307">1364 (0x554)</span><span class="sxs-lookup"><span data-stu-id="ce714-307">1364 (0x554)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-308">Указанный пакет проверки подлинности неизвестен.</span><span class="sxs-lookup"><span data-stu-id="ce714-308">A specified authentication package is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**Ошибка при \_ неправильном \_ \_ состоянии сеанса входа \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR\_BAD\_LOGON\_SESSION\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-310">1365 (0x555)</span><span class="sxs-lookup"><span data-stu-id="ce714-310">1365 (0x555)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-311">Сеанс входа в систему не находится в состоянии, соответствующем запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="ce714-311">The logon session is not in a state that is consistent with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**Ошибка \_ при \_ \_ конфликте сеанса входа**</span><span class="sxs-lookup"><span data-stu-id="ce714-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERROR\_LOGON\_SESSION\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-313">1366 (0x556)</span><span class="sxs-lookup"><span data-stu-id="ce714-313">1366 (0x556)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-314">Идентификатор сеанса входа уже используется.</span><span class="sxs-lookup"><span data-stu-id="ce714-314">The logon session ID is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**Ошибка \_ недопустимого \_ \_ типа входа**</span><span class="sxs-lookup"><span data-stu-id="ce714-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR\_INVALID\_LOGON\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-316">1367 (0x557)</span><span class="sxs-lookup"><span data-stu-id="ce714-316">1367 (0x557)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-317">Запрос на вход в систему содержал недопустимое значение типа входа.</span><span class="sxs-lookup"><span data-stu-id="ce714-317">A logon request contained an invalid logon type value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**Ошибка \_ не может \_ олицетворить**</span><span class="sxs-lookup"><span data-stu-id="ce714-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR\_CANNOT\_IMPERSONATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-319">1368 (0x558)</span><span class="sxs-lookup"><span data-stu-id="ce714-319">1368 (0x558)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-320">Невозможно выполнить олицетворение с помощью именованного канала, пока данные не считаны из этого канала.</span><span class="sxs-lookup"><span data-stu-id="ce714-320">Unable to impersonate using a named pipe until data has been read from that pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**Ошибка \_ рксакт \_ недопустимое \_ состояние**</span><span class="sxs-lookup"><span data-stu-id="ce714-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR\_RXACT\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-322">1369 (0x559)</span><span class="sxs-lookup"><span data-stu-id="ce714-322">1369 (0x559)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-323">Состояние транзакции поддерева реестра несовместимо с запрошенной операцией.</span><span class="sxs-lookup"><span data-stu-id="ce714-323">The transaction state of a registry subtree is incompatible with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**Ошибка \_ \_ при фиксации рксакт \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR\_RXACT\_COMMIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-325">1370 (0x55A)</span><span class="sxs-lookup"><span data-stu-id="ce714-325">1370 (0x55A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-326">Обнаружено повреждение внутренней базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-326">An internal security database corruption has been encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_Специальная \_ учетная запись ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR\_SPECIAL\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-328">1371 (0x55B)</span><span class="sxs-lookup"><span data-stu-id="ce714-328">1371 (0x55B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-329">Невозможно выполнить эту операцию с встроенными учетными записями.</span><span class="sxs-lookup"><span data-stu-id="ce714-329">Cannot perform this operation on built-in accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**\_Специальная \_ Группа ошибок**</span><span class="sxs-lookup"><span data-stu-id="ce714-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR\_SPECIAL\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-331">1372 (0x55C)</span><span class="sxs-lookup"><span data-stu-id="ce714-331">1372 (0x55C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-332">Невозможно выполнить эту операцию с этой встроенной специальной группой.</span><span class="sxs-lookup"><span data-stu-id="ce714-332">Cannot perform this operation on this built-in special group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**\_Специальный \_ пользователь ошибок**</span><span class="sxs-lookup"><span data-stu-id="ce714-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR\_SPECIAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-334">1373 (0x55D)</span><span class="sxs-lookup"><span data-stu-id="ce714-334">1373 (0x55D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-335">Невозможно выполнить эту операцию с этим встроенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="ce714-335">Cannot perform this operation on this built-in special user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**\_ \_ Основная группа участников \_ с ошибками**</span><span class="sxs-lookup"><span data-stu-id="ce714-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**ERROR\_MEMBERS\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-337">1374 (0x55E)</span><span class="sxs-lookup"><span data-stu-id="ce714-337">1374 (0x55E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-338">Невозможно удалить пользователя из группы, так как эта группа в настоящее время является основной группой пользователя.</span><span class="sxs-lookup"><span data-stu-id="ce714-338">The user cannot be removed from a group because the group is currently the user's primary group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**\_маркер ошибки \_ уже \_ \_ используется**</span><span class="sxs-lookup"><span data-stu-id="ce714-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**ERROR\_TOKEN\_ALREADY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-340">1375 (0x55F)</span><span class="sxs-lookup"><span data-stu-id="ce714-340">1375 (0x55F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-341">Токен уже используется в качестве основного токена.</span><span class="sxs-lookup"><span data-stu-id="ce714-341">The token is already in use as a primary token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**Ошибка \_ без \_ \_ псевдонима**</span><span class="sxs-lookup"><span data-stu-id="ce714-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR\_NO\_SUCH\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-343">1376 (0x560)</span><span class="sxs-lookup"><span data-stu-id="ce714-343">1376 (0x560)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-344">Указанная локальная группа не существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-344">The specified local group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**\_элемент ошибки \_ не \_ в \_ псевдониме**</span><span class="sxs-lookup"><span data-stu-id="ce714-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**ERROR\_MEMBER\_NOT\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-346">1377 (0x561)</span><span class="sxs-lookup"><span data-stu-id="ce714-346">1377 (0x561)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-347">Указанное имя учетной записи не является членом группы.</span><span class="sxs-lookup"><span data-stu-id="ce714-347">The specified account name is not a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_элемент ошибки \_ в \_ псевдониме**</span><span class="sxs-lookup"><span data-stu-id="ce714-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR\_MEMBER\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-349">1378 (0x562)</span><span class="sxs-lookup"><span data-stu-id="ce714-349">1378 (0x562)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-350">Указанное имя учетной записи уже является членом группы.</span><span class="sxs-lookup"><span data-stu-id="ce714-350">The specified account name is already a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**\_псевдоним ошибки \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ce714-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ERROR\_ALIAS\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-352">1379 (0x563)</span><span class="sxs-lookup"><span data-stu-id="ce714-352">1379 (0x563)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-353">Указанная локальная группа уже существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-353">The specified local group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**Ошибка \_ входа в систему \_ не \_ предоставлена**</span><span class="sxs-lookup"><span data-stu-id="ce714-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR\_LOGON\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-355">1380 (0x564)</span><span class="sxs-lookup"><span data-stu-id="ce714-355">1380 (0x564)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-356">Ошибка входа в систему: пользователю не был предоставлен запрошенный тип входа на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ce714-356">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**Ошибка \_ слишком \_ много \_ секретов**</span><span class="sxs-lookup"><span data-stu-id="ce714-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR\_TOO\_MANY\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-358">1381 (0x565)</span><span class="sxs-lookup"><span data-stu-id="ce714-358">1381 (0x565)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-359">Превышено максимальное число секретов, которые могут храниться в одной системе.</span><span class="sxs-lookup"><span data-stu-id="ce714-359">The maximum number of secrets that may be stored in a single system has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**\_секретный код ошибки \_ слишком \_ длинный**</span><span class="sxs-lookup"><span data-stu-id="ce714-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR\_SECRET\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-361">1382 (0x566)</span><span class="sxs-lookup"><span data-stu-id="ce714-361">1382 (0x566)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-362">Длина секрета превышает максимально допустимую.</span><span class="sxs-lookup"><span data-stu-id="ce714-362">The length of a secret exceeds the maximum length allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**Ошибка \_ внутренней \_ ошибки базы данных \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR\_INTERNAL\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-364">1383 (0x567)</span><span class="sxs-lookup"><span data-stu-id="ce714-364">1383 (0x567)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-365">Локальная база данных центра безопасности содержит внутреннюю несогласованность.</span><span class="sxs-lookup"><span data-stu-id="ce714-365">The local security authority database contains an internal inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**Ошибка \_ слишком \_ много \_ \_ идентификаторов контекста**</span><span class="sxs-lookup"><span data-stu-id="ce714-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR\_TOO\_MANY\_CONTEXT\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-367">1384 (0x568)</span><span class="sxs-lookup"><span data-stu-id="ce714-367">1384 (0x568)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-368">Во время попытки входа в систему контекст безопасности пользователя накапливает слишком много идентификаторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-368">During a logon attempt, the user's security context accumulated too many security IDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_тип ошибки \_ входа \_ не \_ предоставлен**</span><span class="sxs-lookup"><span data-stu-id="ce714-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**ERROR\_LOGON\_TYPE\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-370">1385 (0x569)</span><span class="sxs-lookup"><span data-stu-id="ce714-370">1385 (0x569)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-371">Ошибка входа в систему: пользователю не был предоставлен запрошенный тип входа на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ce714-371">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**Ошибка \_ при \_ перекрестном \_ шифровании NT \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR\_NT\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-373">1386 (0x56A)</span><span class="sxs-lookup"><span data-stu-id="ce714-373">1386 (0x56A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-374">Для изменения пароля пользователя требуется перекрестно зашифрованный пароль.</span><span class="sxs-lookup"><span data-stu-id="ce714-374">A cross-encrypted password is necessary to change a user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**Ошибка \_ без \_ такого \_ участника**</span><span class="sxs-lookup"><span data-stu-id="ce714-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR\_NO\_SUCH\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-376">1387 (0x56B)</span><span class="sxs-lookup"><span data-stu-id="ce714-376">1387 (0x56B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-377">Не удалось добавить или удалить элемент из локальной группы, так как элемент не существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-377">A member could not be added to or removed from the local group because the member does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**Ошибка \_ недопустимого \_ члена**</span><span class="sxs-lookup"><span data-stu-id="ce714-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR\_INVALID\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-379">1388 (0x56C)</span><span class="sxs-lookup"><span data-stu-id="ce714-379">1388 (0x56C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-380">Не удалось добавить нового члена в локальную группу, так как у него неправильный тип учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ce714-380">A new member could not be added to a local group because the member has the wrong account type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**Ошибка \_ слишком \_ большого числа \_ идентификаторов безопасности**</span><span class="sxs-lookup"><span data-stu-id="ce714-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR\_TOO\_MANY\_SIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-382">1389 (0x56D)</span><span class="sxs-lookup"><span data-stu-id="ce714-382">1389 (0x56D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-383">Указано слишком много идентификаторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce714-383">Too many security IDs have been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**Ошибка \_ при \_ перекрестном \_ шифровании LM \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR\_LM\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-385">1390 (0x56E)</span><span class="sxs-lookup"><span data-stu-id="ce714-385">1390 (0x56E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-386">Для изменения этого пароля пользователя требуется перекрестно зашифрованный пароль.</span><span class="sxs-lookup"><span data-stu-id="ce714-386">A cross-encrypted password is necessary to change this user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**Ошибка \_ без \_ наследования**</span><span class="sxs-lookup"><span data-stu-id="ce714-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR\_NO\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-388">1391 (0x56F)</span><span class="sxs-lookup"><span data-stu-id="ce714-388">1391 (0x56F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-389">Указывает, что список ACL не содержит наследуемых компонентов.</span><span class="sxs-lookup"><span data-stu-id="ce714-389">Indicates an ACL contains no inheritable components.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**\_файл ошибок \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="ce714-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ERROR\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-391">1392 (0x570)</span><span class="sxs-lookup"><span data-stu-id="ce714-391">1392 (0x570)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-392">Файл или каталог поврежден и не читается.</span><span class="sxs-lookup"><span data-stu-id="ce714-392">The file or directory is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**диск с ошибкой \_ \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="ce714-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR\_DISK\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-394">1393 (0x571)</span><span class="sxs-lookup"><span data-stu-id="ce714-394">1393 (0x571)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-395">Структура диска повреждена и недоступна для чтения.</span><span class="sxs-lookup"><span data-stu-id="ce714-395">The disk structure is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**Ошибка \_ без \_ \_ ключа сеанса \_ пользователя**</span><span class="sxs-lookup"><span data-stu-id="ce714-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR\_NO\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-397">1394 (0x572)</span><span class="sxs-lookup"><span data-stu-id="ce714-397">1394 (0x572)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-398">Для указанного сеанса входа в систему не существует ключа сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="ce714-398">There is no user session key for the specified logon session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**\_ \_ превышена квота лицензии на ошибку \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**ERROR\_LICENSE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-400">1395 (0x573)</span><span class="sxs-lookup"><span data-stu-id="ce714-400">1395 (0x573)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-401">Служба, к которой осуществляется доступ, лицензирована для определенного числа подключений.</span><span class="sxs-lookup"><span data-stu-id="ce714-401">The service being accessed is licensed for a particular number of connections.</span></span> <span data-ttu-id="ce714-402">В настоящее время невозможно установить больше подключений, так как служба уже может принять такое количество подключений.</span><span class="sxs-lookup"><span data-stu-id="ce714-402">No more connections can be made to the service at this time because there are already as many connections as the service can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**Ошибка \_ неправильного \_ имени целевого объекта \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR\_WRONG\_TARGET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-404">1396 (0x574)</span><span class="sxs-lookup"><span data-stu-id="ce714-404">1396 (0x574)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-405">Неверное имя целевой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ce714-405">The target account name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**Ошибка \_ взаимной \_ проверки подлинности \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR\_MUTUAL\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-407">1397 (0x575)</span><span class="sxs-lookup"><span data-stu-id="ce714-407">1397 (0x575)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-408">Сбой взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ce714-408">Mutual Authentication failed.</span></span> <span data-ttu-id="ce714-409">Пароль сервера устарел на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="ce714-409">The server's password is out of date at the domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**\_ \_ Отклонение времени ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**ERROR\_TIME\_SKEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-411">1398 (0x576)</span><span class="sxs-lookup"><span data-stu-id="ce714-411">1398 (0x576)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-412">Между клиентом и сервером существует разница между временем и (или) датой.</span><span class="sxs-lookup"><span data-stu-id="ce714-412">There is a time and/or date difference between the client and server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**Ошибка \_ текущего \_ домена \_ не \_ разрешена**</span><span class="sxs-lookup"><span data-stu-id="ce714-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR\_CURRENT\_DOMAIN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-414">1399 (0x577)</span><span class="sxs-lookup"><span data-stu-id="ce714-414">1399 (0x577)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-415">Эта операция не может быть выполнена в текущем домене.</span><span class="sxs-lookup"><span data-stu-id="ce714-415">This operation cannot be performed on the current domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**Ошибка \_ неправильного \_ \_ обработчика окна**</span><span class="sxs-lookup"><span data-stu-id="ce714-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR\_INVALID\_WINDOW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-417">1400 (0x578)</span><span class="sxs-lookup"><span data-stu-id="ce714-417">1400 (0x578)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-418">Недопустимый маркер окна.</span><span class="sxs-lookup"><span data-stu-id="ce714-418">Invalid window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера меню**</span><span class="sxs-lookup"><span data-stu-id="ce714-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR\_INVALID\_MENU\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-420">1401 (0x579)</span><span class="sxs-lookup"><span data-stu-id="ce714-420">1401 (0x579)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-421">Недопустимый маркер меню.</span><span class="sxs-lookup"><span data-stu-id="ce714-421">Invalid menu handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера курсора**</span><span class="sxs-lookup"><span data-stu-id="ce714-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR\_INVALID\_CURSOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-423">1402 (0x57A)</span><span class="sxs-lookup"><span data-stu-id="ce714-423">1402 (0x57A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-424">Недопустимый маркер курсора.</span><span class="sxs-lookup"><span data-stu-id="ce714-424">Invalid cursor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**Ошибка \_ недопустимого \_ \_ обработчика обращений**</span><span class="sxs-lookup"><span data-stu-id="ce714-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR\_INVALID\_ACCEL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-426">1403 (0x57B)</span><span class="sxs-lookup"><span data-stu-id="ce714-426">1403 (0x57B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-427">Недопустимый маркер таблицы ускорителя.</span><span class="sxs-lookup"><span data-stu-id="ce714-427">Invalid accelerator table handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**Ошибка \_ недопустимого обработчика \_ обработчика \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR\_INVALID\_HOOK\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-429">1404 (0x57C)</span><span class="sxs-lookup"><span data-stu-id="ce714-429">1404 (0x57C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-430">Недопустимый обработчик обработчика.</span><span class="sxs-lookup"><span data-stu-id="ce714-430">Invalid hook handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**Ошибка при \_ недопустимом \_ \_ обработчике DWP**</span><span class="sxs-lookup"><span data-stu-id="ce714-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR\_INVALID\_DWP\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-432">1405 (0x57D)</span><span class="sxs-lookup"><span data-stu-id="ce714-432">1405 (0x57D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-433">Недопустимый указатель на структуру расположения с несколькими окнами.</span><span class="sxs-lookup"><span data-stu-id="ce714-433">Invalid handle to a multiple-window position structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**Ошибка \_ ТЛВ \_ с \_ всчилд**</span><span class="sxs-lookup"><span data-stu-id="ce714-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR\_TLW\_WITH\_WSCHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-435">1406 (0x57E)</span><span class="sxs-lookup"><span data-stu-id="ce714-435">1406 (0x57E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-436">Не удается создать дочернее окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="ce714-436">Cannot create a top-level child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**Ошибка \_ не \_ удается \_ найти \_ класс ВНД**</span><span class="sxs-lookup"><span data-stu-id="ce714-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR\_CANNOT\_FIND\_WND\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-438">1407 (0x57F)</span><span class="sxs-lookup"><span data-stu-id="ce714-438">1407 (0x57F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-439">Не удается найти класс окна.</span><span class="sxs-lookup"><span data-stu-id="ce714-439">Cannot find window class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_окно ошибок \_ \_ другого \_ потока**</span><span class="sxs-lookup"><span data-stu-id="ce714-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**ERROR\_WINDOW\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-441">1408 (0x580)</span><span class="sxs-lookup"><span data-stu-id="ce714-441">1408 (0x580)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-442">Недопустимое окно; Он принадлежит другому потоку.</span><span class="sxs-lookup"><span data-stu-id="ce714-442">Invalid window; it belongs to other thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**\_горячая клавиша ошибки \_ уже \_ зарегистрирована**</span><span class="sxs-lookup"><span data-stu-id="ce714-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR\_HOTKEY\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-444">1409 (0X581)</span><span class="sxs-lookup"><span data-stu-id="ce714-444">1409 (0x581)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-445">Горячая клавиша уже зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="ce714-445">Hot key is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**\_класс Error \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ce714-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**ERROR\_CLASS\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-447">1410 (0x582)</span><span class="sxs-lookup"><span data-stu-id="ce714-447">1410 (0x582)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-448">Класс уже существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-448">Class already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**\_класс Error \_ \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ce714-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**ERROR\_CLASS\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-450">1411 (0x583)</span><span class="sxs-lookup"><span data-stu-id="ce714-450">1411 (0x583)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-451">Класс не существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-451">Class does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**\_класс Error \_ содержит \_ Windows**</span><span class="sxs-lookup"><span data-stu-id="ce714-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR\_CLASS\_HAS\_WINDOWS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-453">1412 (0x584)</span><span class="sxs-lookup"><span data-stu-id="ce714-453">1412 (0x584)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-454">Класс по-прежнему имеет открытые окна.</span><span class="sxs-lookup"><span data-stu-id="ce714-454">Class still has open windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**Ошибка \_ недопустимого \_ индекса**</span><span class="sxs-lookup"><span data-stu-id="ce714-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR\_INVALID\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-456">1413 (0x585)</span><span class="sxs-lookup"><span data-stu-id="ce714-456">1413 (0x585)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-457">Недопустимый индекс.</span><span class="sxs-lookup"><span data-stu-id="ce714-457">Invalid index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**Ошибка \_ неправильного \_ \_ маркера значка**</span><span class="sxs-lookup"><span data-stu-id="ce714-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR\_INVALID\_ICON\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-459">1414 (0x586)</span><span class="sxs-lookup"><span data-stu-id="ce714-459">1414 (0x586)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-460">Недопустимый маркер значка.</span><span class="sxs-lookup"><span data-stu-id="ce714-460">Invalid icon handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**Ошибка при \_ закрытии \_ индекса диалогового окна \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR\_PRIVATE\_DIALOG\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-462">1415 (0x587)</span><span class="sxs-lookup"><span data-stu-id="ce714-462">1415 (0x587)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-463">Использование закрытых слов в ДИАЛОГовых окнах.</span><span class="sxs-lookup"><span data-stu-id="ce714-463">Using private DIALOG window words.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_идентификатор списка \_ ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="ce714-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR\_LISTBOX\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-465">1416 (0x588)</span><span class="sxs-lookup"><span data-stu-id="ce714-465">1416 (0x588)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-466">Идентификатор списка не найден.</span><span class="sxs-lookup"><span data-stu-id="ce714-466">The list box identifier was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**Ошибка \_ без \_ подстановочных \_ знаков**</span><span class="sxs-lookup"><span data-stu-id="ce714-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR\_NO\_WILDCARD\_CHARACTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-468">1417 (0x589)</span><span class="sxs-lookup"><span data-stu-id="ce714-468">1417 (0x589)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-469">Подстановочные знаки не найдены.</span><span class="sxs-lookup"><span data-stu-id="ce714-469">No wildcards were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**\_буфер обмена ошибок \_ не \_ открыт**</span><span class="sxs-lookup"><span data-stu-id="ce714-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR\_CLIPBOARD\_NOT\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-471">1418 (0x58A)</span><span class="sxs-lookup"><span data-stu-id="ce714-471">1418 (0x58A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-472">В потоке не открыт буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="ce714-472">Thread does not have a clipboard open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**\_ \_ не \_ зарегистрировано сочетание клавиш для ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR\_HOTKEY\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-474">1419 (0x58B)</span><span class="sxs-lookup"><span data-stu-id="ce714-474">1419 (0x58B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-475">Горячая клавиша не зарегистрирована.</span><span class="sxs-lookup"><span data-stu-id="ce714-475">Hot key is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**окно "ошибка" \_ \_ не \_ диалоговое окно**</span><span class="sxs-lookup"><span data-stu-id="ce714-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**ERROR\_WINDOW\_NOT\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-477">1420 (0x58C)</span><span class="sxs-lookup"><span data-stu-id="ce714-477">1420 (0x58C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-478">Окно не является допустимым окном диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ce714-478">The window is not a valid dialog window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_идентификатор управления ошибками \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="ce714-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ERROR\_CONTROL\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-480">1421 (0x58D)</span><span class="sxs-lookup"><span data-stu-id="ce714-480">1421 (0x58D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-481">Идентификатор элемента управления не найден.</span><span class="sxs-lookup"><span data-stu-id="ce714-481">Control ID not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**Ошибка \_ недопустимого \_ \_ сообщения ComboBox**</span><span class="sxs-lookup"><span data-stu-id="ce714-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR\_INVALID\_COMBOBOX\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-483">1422 (0x58E)</span><span class="sxs-lookup"><span data-stu-id="ce714-483">1422 (0x58E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-484">Недопустимое сообщение для поля со списком, так как оно не имеет элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="ce714-484">Invalid message for a combo box because it does not have an edit control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**\_окно ошибок \_ не \_ ComboBox**</span><span class="sxs-lookup"><span data-stu-id="ce714-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ERROR\_WINDOW\_NOT\_COMBOBOX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-486">1423 (0x58F)</span><span class="sxs-lookup"><span data-stu-id="ce714-486">1423 (0x58F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-487">Окно не является полем со списком.</span><span class="sxs-lookup"><span data-stu-id="ce714-487">The window is not a combo box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**Ошибка \_ при \_ изменении \_ высоты**</span><span class="sxs-lookup"><span data-stu-id="ce714-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR\_INVALID\_EDIT\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-489">1424 (0x590)</span><span class="sxs-lookup"><span data-stu-id="ce714-489">1424 (0x590)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-490">Высота должна быть меньше 256.</span><span class="sxs-lookup"><span data-stu-id="ce714-490">Height must be less than 256.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**Ошибка \_ DC \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="ce714-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR\_DC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-492">1425 (0x591)</span><span class="sxs-lookup"><span data-stu-id="ce714-492">1425 (0x591)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-493">Недопустимый обработчик контекста устройства (DC).</span><span class="sxs-lookup"><span data-stu-id="ce714-493">Invalid device context (DC) handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**Ошибка \_ недопустимого \_ фильтра обработчика \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR\_INVALID\_HOOK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-495">1426 (0x592)</span><span class="sxs-lookup"><span data-stu-id="ce714-495">1426 (0x592)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-496">Недопустимый тип процедуры обработчика.</span><span class="sxs-lookup"><span data-stu-id="ce714-496">Invalid hook procedure type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**Ошибка при \_ неправильной \_ \_ процедуре фильтра**</span><span class="sxs-lookup"><span data-stu-id="ce714-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR\_INVALID\_FILTER\_PROC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-498">1427 (0x593)</span><span class="sxs-lookup"><span data-stu-id="ce714-498">1427 (0x593)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-499">Недопустимая процедура обработчика.</span><span class="sxs-lookup"><span data-stu-id="ce714-499">Invalid hook procedure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**для \_ обработчика ошибок \_ требуются \_ хмод**</span><span class="sxs-lookup"><span data-stu-id="ce714-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**ERROR\_HOOK\_NEEDS\_HMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-501">1428 (0x594)</span><span class="sxs-lookup"><span data-stu-id="ce714-501">1428 (0x594)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-502">Невозможно задать нелокальный обработчик без обработчика модуля.</span><span class="sxs-lookup"><span data-stu-id="ce714-502">Cannot set nonlocal hook without a module handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**Ошибка \_ \_ только глобального \_ ловушки**</span><span class="sxs-lookup"><span data-stu-id="ce714-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR\_GLOBAL\_ONLY\_HOOK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-504">1429 (0x595)</span><span class="sxs-lookup"><span data-stu-id="ce714-504">1429 (0x595)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-505">Эту процедуру-обработчик можно установить только глобально.</span><span class="sxs-lookup"><span data-stu-id="ce714-505">This hook procedure can only be set globally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_ \_ набор обработчиков журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR\_JOURNAL\_HOOK\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-507">1430 (0x596)</span><span class="sxs-lookup"><span data-stu-id="ce714-507">1430 (0x596)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-508">Процедура обработчика журнала уже установлена.</span><span class="sxs-lookup"><span data-stu-id="ce714-508">The journal hook procedure is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**\_обработчик ошибок \_ не \_ установлен**</span><span class="sxs-lookup"><span data-stu-id="ce714-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR\_HOOK\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-510">1431 (0x597)</span><span class="sxs-lookup"><span data-stu-id="ce714-510">1431 (0x597)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-511">Процедура-обработчик не установлена.</span><span class="sxs-lookup"><span data-stu-id="ce714-511">The hook procedure is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**Ошибка \_ недопустимого \_ сообщения о балансировке нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR\_INVALID\_LB\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-513">1432 (0x598)</span><span class="sxs-lookup"><span data-stu-id="ce714-513">1432 (0x598)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-514">Недопустимое сообщение для списка с одним выбором.</span><span class="sxs-lookup"><span data-stu-id="ce714-514">Invalid message for single-selection list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**Ошибка \_ сеткаунт \_ при \_ плохой \_ балансировке нагрузки**</span><span class="sxs-lookup"><span data-stu-id="ce714-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR\_SETCOUNT\_ON\_BAD\_LB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-516">1433 (0x599)</span><span class="sxs-lookup"><span data-stu-id="ce714-516">1433 (0x599)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-517">Балансировка нагрузки \_ сеткаунт, отправленная в список не ленивых.</span><span class="sxs-lookup"><span data-stu-id="ce714-517">LB\_SETCOUNT sent to non-lazy list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**Ошибка при \_ балансировке нагрузки \_ без \_ табуляцию**</span><span class="sxs-lookup"><span data-stu-id="ce714-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR\_LB\_WITHOUT\_TABSTOPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-519">1434 (0x59A)</span><span class="sxs-lookup"><span data-stu-id="ce714-519">1434 (0x59A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-520">Это окно списка не поддерживает позиции табуляции.</span><span class="sxs-lookup"><span data-stu-id="ce714-520">This list box does not support tab stops.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**Ошибка \_ при \_ удалении \_ объекта \_ другого \_ потока**</span><span class="sxs-lookup"><span data-stu-id="ce714-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR\_DESTROY\_OBJECT\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-522">1435 (0x59B)</span><span class="sxs-lookup"><span data-stu-id="ce714-522">1435 (0x59B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-523">Невозможно уничтожить объект, созданный другим потоком.</span><span class="sxs-lookup"><span data-stu-id="ce714-523">Cannot destroy object created by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_меню дочернего \_ окна ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**ERROR\_CHILD\_WINDOW\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-525">1436 (0x59C)</span><span class="sxs-lookup"><span data-stu-id="ce714-525">1436 (0x59C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-526">Дочерние окна не могут иметь меню.</span><span class="sxs-lookup"><span data-stu-id="ce714-526">Child windows cannot have menus.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**Ошибка \_ нет \_ системного \_ меню**</span><span class="sxs-lookup"><span data-stu-id="ce714-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR\_NO\_SYSTEM\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-528">1437 (0x59D)</span><span class="sxs-lookup"><span data-stu-id="ce714-528">1437 (0x59D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-529">Окно не имеет системного меню.</span><span class="sxs-lookup"><span data-stu-id="ce714-529">The window does not have a system menu.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**Ошибка \_ недопустимого \_ \_ стиля MSGBOX**</span><span class="sxs-lookup"><span data-stu-id="ce714-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR\_INVALID\_MSGBOX\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-531">1438 (0x59E)</span><span class="sxs-lookup"><span data-stu-id="ce714-531">1438 (0x59E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-532">Недопустимый стиль окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce714-532">Invalid message box style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**Ошибка \_ недопустимого \_ \_ значения SPI**</span><span class="sxs-lookup"><span data-stu-id="ce714-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR\_INVALID\_SPI\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-534">1439 (0x59F)</span><span class="sxs-lookup"><span data-stu-id="ce714-534">1439 (0x59F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-535">Недопустимый параметр на уровне системы (SPI \_ \* ).</span><span class="sxs-lookup"><span data-stu-id="ce714-535">Invalid system-wide (SPI\_\*) parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**\_экран ошибок \_ уже \_ заблокирован**</span><span class="sxs-lookup"><span data-stu-id="ce714-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**ERROR\_SCREEN\_ALREADY\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-537">1440 (0x5A0)</span><span class="sxs-lookup"><span data-stu-id="ce714-537">1440 (0x5A0)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-538">Экран уже заблокирован.</span><span class="sxs-lookup"><span data-stu-id="ce714-538">Screen already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**\_HWND ошибки \_ имеют \_ \_ родительский элемент diff**</span><span class="sxs-lookup"><span data-stu-id="ce714-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR\_HWNDS\_HAVE\_DIFF\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-540">1441 (0x5A1)</span><span class="sxs-lookup"><span data-stu-id="ce714-540">1441 (0x5A1)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-541">Все дескрипторы окон в структуре расположения с несколькими окнами должны иметь один и тот же родительский элемент.</span><span class="sxs-lookup"><span data-stu-id="ce714-541">All handles to windows in a multiple-window position structure must have the same parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**Ошибка \_ не \_ дочернего \_ окна**</span><span class="sxs-lookup"><span data-stu-id="ce714-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR\_NOT\_CHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-543">1442 (0x5A2)</span><span class="sxs-lookup"><span data-stu-id="ce714-543">1442 (0x5A2)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-544">Окно не является дочерним окном.</span><span class="sxs-lookup"><span data-stu-id="ce714-544">The window is not a child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**Ошибка \_ недопустимой \_ \_ команды GW**</span><span class="sxs-lookup"><span data-stu-id="ce714-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR\_INVALID\_GW\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-546">1443 (0x5A3)</span><span class="sxs-lookup"><span data-stu-id="ce714-546">1443 (0x5A3)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-547">Недопустимая \_ \* команда GW.</span><span class="sxs-lookup"><span data-stu-id="ce714-547">Invalid GW\_\* command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**Ошибка \_ недопустимого \_ \_ идентификатора потока**</span><span class="sxs-lookup"><span data-stu-id="ce714-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR\_INVALID\_THREAD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-549">1444 (0x5A4)</span><span class="sxs-lookup"><span data-stu-id="ce714-549">1444 (0x5A4)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-550">Недопустимый идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="ce714-550">Invalid thread identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ОШИБКА, \_ не \_ мдичилд \_ окно**</span><span class="sxs-lookup"><span data-stu-id="ce714-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR\_NON\_MDICHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-552">1445 (0x5A5)</span><span class="sxs-lookup"><span data-stu-id="ce714-552">1445 (0x5A5)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-553">Невозможно обработать сообщение из окна, которое не является окном многодокументного интерфейса (MDI).</span><span class="sxs-lookup"><span data-stu-id="ce714-553">Cannot process a message from a window that is not a multiple document interface (MDI) window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**\_всплывающее окно ошибки \_ уже \_ активно**</span><span class="sxs-lookup"><span data-stu-id="ce714-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR\_POPUP\_ALREADY\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-555">1446 (0x5A6)</span><span class="sxs-lookup"><span data-stu-id="ce714-555">1446 (0x5A6)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-556">Всплывающее меню уже активно.</span><span class="sxs-lookup"><span data-stu-id="ce714-556">Popup menu already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**Ошибка \_ без \_ полос прокрутки**</span><span class="sxs-lookup"><span data-stu-id="ce714-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR\_NO\_SCROLLBARS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-558">1447 (0x5A7)</span><span class="sxs-lookup"><span data-stu-id="ce714-558">1447 (0x5A7)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-559">Окно не имеет полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="ce714-559">The window does not have scroll bars.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**Ошибка \_ недопустимого \_ диапазона полосы прокрутки \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR\_INVALID\_SCROLLBAR\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-561">1448 (0x5A8)</span><span class="sxs-lookup"><span data-stu-id="ce714-561">1448 (0x5A8)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-562">Диапазон полосы прокрутки не может быть больше МАКСЛОНГ.</span><span class="sxs-lookup"><span data-stu-id="ce714-562">Scroll bar range cannot be greater than MAXLONG.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**Ошибка \_ недопустимой \_ \_ команды шоввин**</span><span class="sxs-lookup"><span data-stu-id="ce714-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR\_INVALID\_SHOWWIN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-564">1449 (0x5A9)</span><span class="sxs-lookup"><span data-stu-id="ce714-564">1449 (0x5A9)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-565">Невозможно отобразить или удалить окно указанным способом.</span><span class="sxs-lookup"><span data-stu-id="ce714-565">Cannot show or remove the window in the way specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**\_нет \_ системных \_ ресурсов**</span><span class="sxs-lookup"><span data-stu-id="ce714-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR\_NO\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-567">1450 (0x5AA)</span><span class="sxs-lookup"><span data-stu-id="ce714-567">1450 (0x5AA)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-568">Недостаточно системных ресурсов для завершения запрошенной службы.</span><span class="sxs-lookup"><span data-stu-id="ce714-568">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ОШИБКИ \_ НЕстраничных \_ системных \_ ресурсов**</span><span class="sxs-lookup"><span data-stu-id="ce714-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR\_NONPAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-570">1451 (0x5AB)</span><span class="sxs-lookup"><span data-stu-id="ce714-570">1451 (0x5AB)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-571">Недостаточно системных ресурсов для завершения запрошенной службы.</span><span class="sxs-lookup"><span data-stu-id="ce714-571">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ОШИБКИ в \_ \_ системных \_ ресурсах**</span><span class="sxs-lookup"><span data-stu-id="ce714-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERROR\_PAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-573">1452 (0x5AC)</span><span class="sxs-lookup"><span data-stu-id="ce714-573">1452 (0x5AC)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-574">Недостаточно системных ресурсов для завершения запрошенной службы.</span><span class="sxs-lookup"><span data-stu-id="ce714-574">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**Ошибка \_ в \_ \_ квоте рабочего набора**</span><span class="sxs-lookup"><span data-stu-id="ce714-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR\_WORKING\_SET\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-576">1453 (0x5AD)</span><span class="sxs-lookup"><span data-stu-id="ce714-576">1453 (0x5AD)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-577">Недостаточно квоты для завершения запрошенной службы.</span><span class="sxs-lookup"><span data-stu-id="ce714-577">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**\_Квота файла подкачки с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR\_PAGEFILE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-579">1454 (0x5AE)</span><span class="sxs-lookup"><span data-stu-id="ce714-579">1454 (0x5AE)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-580">Недостаточно квоты для завершения запрошенной службы.</span><span class="sxs-lookup"><span data-stu-id="ce714-580">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_лимит обязательств по ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**ERROR\_COMMITMENT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-582">1455 (0x5AF)</span><span class="sxs-lookup"><span data-stu-id="ce714-582">1455 (0x5AF)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-583">Файл подкачки слишком мал для завершения этой операции.</span><span class="sxs-lookup"><span data-stu-id="ce714-583">The paging file is too small for this operation to complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**пункт меню "ошибка" \_ \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="ce714-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR\_MENU\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-585">1456 (0x5B0)</span><span class="sxs-lookup"><span data-stu-id="ce714-585">1456 (0x5B0)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-586">Не удалось найти пункт меню.</span><span class="sxs-lookup"><span data-stu-id="ce714-586">A menu item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**Ошибка \_ недопустимого \_ \_ маркера клавиатуры**</span><span class="sxs-lookup"><span data-stu-id="ce714-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR\_INVALID\_KEYBOARD\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-588">1457 (0x5B1)</span><span class="sxs-lookup"><span data-stu-id="ce714-588">1457 (0x5B1)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-589">Недопустимый маркер раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ce714-589">Invalid keyboard layout handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**\_тип обработчика ошибок \_ \_ не \_ разрешен**</span><span class="sxs-lookup"><span data-stu-id="ce714-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**ERROR\_HOOK\_TYPE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-591">1458 (0x5B2)</span><span class="sxs-lookup"><span data-stu-id="ce714-591">1458 (0x5B2)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-592">Тип обработчика не разрешен.</span><span class="sxs-lookup"><span data-stu-id="ce714-592">Hook type not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**для ошибки \_ требуется \_ Interactive \_ виндовстатион**</span><span class="sxs-lookup"><span data-stu-id="ce714-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR\_REQUIRES\_INTERACTIVE\_WINDOWSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-594">1459 (0x5B3)</span><span class="sxs-lookup"><span data-stu-id="ce714-594">1459 (0x5B3)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-595">Для этой операции требуется интерактивная Командная станция.</span><span class="sxs-lookup"><span data-stu-id="ce714-595">This operation requires an interactive window station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**\_время ожидания ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**ERROR\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-597">1460 (0x5B4)</span><span class="sxs-lookup"><span data-stu-id="ce714-597">1460 (0x5B4)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-598">Эта операция возвращена, так как истек период ожидания.</span><span class="sxs-lookup"><span data-stu-id="ce714-598">This operation returned because the timeout period expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**Ошибка \_ неправильного \_ \_ обработчика монитора**</span><span class="sxs-lookup"><span data-stu-id="ce714-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR\_INVALID\_MONITOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-600">1461 (0x5B5)</span><span class="sxs-lookup"><span data-stu-id="ce714-600">1461 (0x5B5)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-601">Недопустимый обработчик монитора.</span><span class="sxs-lookup"><span data-stu-id="ce714-601">Invalid monitor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**Ошибка \_ неправильного \_ размера**</span><span class="sxs-lookup"><span data-stu-id="ce714-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR\_INCORRECT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-603">1462 (0x5B6)</span><span class="sxs-lookup"><span data-stu-id="ce714-603">1462 (0x5B6)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-604">Недопустимый аргумент размера.</span><span class="sxs-lookup"><span data-stu-id="ce714-604">Incorrect size argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**Ошибка \_ символьную ссылку, \_ класс \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="ce714-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR\_SYMLINK\_CLASS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-606">1463 (0x5B7)</span><span class="sxs-lookup"><span data-stu-id="ce714-606">1463 (0x5B7)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-607">Невозможно проследить символьную ссылку, так как ее тип отключен.</span><span class="sxs-lookup"><span data-stu-id="ce714-607">The symbolic link cannot be followed because its type is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**Ошибка \_ символьную ссылку \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="ce714-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR\_SYMLINK\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-609">1464 (0x5B8)</span><span class="sxs-lookup"><span data-stu-id="ce714-609">1464 (0x5B8)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-610">Это приложение не поддерживает текущую операцию с символической ссылкой.</span><span class="sxs-lookup"><span data-stu-id="ce714-610">This application does not support the current operation on symbolic links.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**Ошибка \_ \_ синтаксического анализа XML-кода ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR\_XML\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-612">1465 (0x5B9)</span><span class="sxs-lookup"><span data-stu-id="ce714-612">1465 (0x5B9)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-613">Windows не удалось выполнить синтаксический анализ запрошенных XML-данных.</span><span class="sxs-lookup"><span data-stu-id="ce714-613">Windows was unable to parse the requested XML data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**Ошибка \_ XMLDSIG \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR\_XMLDSIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-615">1466 (0x5BA)</span><span class="sxs-lookup"><span data-stu-id="ce714-615">1466 (0x5BA)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-616">При обработке цифровой подписи XML произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="ce714-616">An error was encountered while processing an XML digital signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**Ошибка при \_ перезапуске \_ приложения**</span><span class="sxs-lookup"><span data-stu-id="ce714-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR\_RESTART\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-618">1467 (0x5BB)</span><span class="sxs-lookup"><span data-stu-id="ce714-618">1467 (0x5BB)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-619">Это приложение необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="ce714-619">This application must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**Ошибка \_ неверной \_ Секции**</span><span class="sxs-lookup"><span data-stu-id="ce714-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR\_WRONG\_COMPARTMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-621">1468 (0x5BC)</span><span class="sxs-lookup"><span data-stu-id="ce714-621">1468 (0x5BC)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-622">Вызывающий объект сделал запрос на подключение в неверном сегменте маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ce714-622">The caller made the connection request in the wrong routing compartment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**Ошибка \_ AUTHIP \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR\_AUTHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-624">1469 (0x5BD)</span><span class="sxs-lookup"><span data-stu-id="ce714-624">1469 (0x5BD)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-625">Сбой AuthIP при попытке подключения к удаленному узлу.</span><span class="sxs-lookup"><span data-stu-id="ce714-625">There was an AuthIP failure when attempting to connect to the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**Ошибка \_ при \_ отсутствии \_ ресурсов NVRAM**</span><span class="sxs-lookup"><span data-stu-id="ce714-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR\_NO\_NVRAM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-627">1470 (0x5BE)</span><span class="sxs-lookup"><span data-stu-id="ce714-627">1470 (0x5BE)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-628">Недостаточно ресурсов NVRAM для завершения запрошенной службы.</span><span class="sxs-lookup"><span data-stu-id="ce714-628">Insufficient NVRAM resources exist to complete the requested service.</span></span> <span data-ttu-id="ce714-629">Может потребоваться перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="ce714-629">A reboot might be required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**Ошибка \_ при \_ обработке графического пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR\_NOT\_GUI\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-631">1471 (0x5BF)</span><span class="sxs-lookup"><span data-stu-id="ce714-631">1471 (0x5BF)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-632">Не удалось завершить запрошенную операцию, поскольку указанный процесс не является процессом графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ce714-632">Unable to finish the requested operation because the specified process is not a GUI process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**\_файл журнала \_ ошибок \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="ce714-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR\_EVENTLOG\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-634">1500 (0x5DC)</span><span class="sxs-lookup"><span data-stu-id="ce714-634">1500 (0x5DC)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-635">Файл журнала событий поврежден.</span><span class="sxs-lookup"><span data-stu-id="ce714-635">The event log file is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**не \_ \_ удается \_ запустить журнал событий ошибок**</span><span class="sxs-lookup"><span data-stu-id="ce714-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR\_EVENTLOG\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-637">1501 (0x5DD)</span><span class="sxs-lookup"><span data-stu-id="ce714-637">1501 (0x5DD)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-638">Не удалось открыть файл журнала событий, поэтому служба ведения журнала событий не запустилась.</span><span class="sxs-lookup"><span data-stu-id="ce714-638">No event log file could be opened, so the event logging service did not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**\_ \_ переполнение файла журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ERROR\_LOG\_FILE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-640">1502 (0x5DE)</span><span class="sxs-lookup"><span data-stu-id="ce714-640">1502 (0x5DE)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-641">Файл журнала событий заполнен.</span><span class="sxs-lookup"><span data-stu-id="ce714-641">The event log file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**\_файл журнала \_ ошибок \_ изменен**</span><span class="sxs-lookup"><span data-stu-id="ce714-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR\_EVENTLOG\_FILE\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-643">1503 (0x5DF)</span><span class="sxs-lookup"><span data-stu-id="ce714-643">1503 (0x5DF)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-644">Файл журнала событий изменился между операциями чтения.</span><span class="sxs-lookup"><span data-stu-id="ce714-644">The event log file has changed between read operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**Ошибка \_ недопустимое \_ \_ имя задачи**</span><span class="sxs-lookup"><span data-stu-id="ce714-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR\_INVALID\_TASK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-646">1550 (0x60E)</span><span class="sxs-lookup"><span data-stu-id="ce714-646">1550 (0x60E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-647">Указано недопустимое имя задачи.</span><span class="sxs-lookup"><span data-stu-id="ce714-647">The specified task name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**Ошибка при \_ недопустимом \_ \_ индексе задачи**</span><span class="sxs-lookup"><span data-stu-id="ce714-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR\_INVALID\_TASK\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-649">1551 (0x60F)</span><span class="sxs-lookup"><span data-stu-id="ce714-649">1551 (0x60F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-650">Указан недопустимый индекс задачи.</span><span class="sxs-lookup"><span data-stu-id="ce714-650">The specified task index is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**\_поток ошибок \_ уже \_ в \_ задаче**</span><span class="sxs-lookup"><span data-stu-id="ce714-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**ERROR\_THREAD\_ALREADY\_IN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-652">1552 (0x610)</span><span class="sxs-lookup"><span data-stu-id="ce714-652">1552 (0x610)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-653">Указанный поток уже присоединяется к задаче.</span><span class="sxs-lookup"><span data-stu-id="ce714-653">The specified thread is already joining a task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**Ошибка \_ при установке ошибки \_ службы \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR\_INSTALL\_SERVICE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-655">1601 (0x641)</span><span class="sxs-lookup"><span data-stu-id="ce714-655">1601 (0x641)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-656">Не удалось получить доступ к службе установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-656">The Windows Installer Service could not be accessed.</span></span> <span data-ttu-id="ce714-657">Это может произойти, если установщик Windows неправильно установлен.</span><span class="sxs-lookup"><span data-stu-id="ce714-657">This can occur if the Windows Installer is not correctly installed.</span></span> <span data-ttu-id="ce714-658">Обратитесь за помощью в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="ce714-658">Contact your support personnel for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**Ошибка при \_ установке \_ усерексит**</span><span class="sxs-lookup"><span data-stu-id="ce714-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR\_INSTALL\_USEREXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-660">1602 (0x642)</span><span class="sxs-lookup"><span data-stu-id="ce714-660">1602 (0x642)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-661">Установка отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="ce714-661">User cancelled installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**Ошибка \_ \_ при установке**</span><span class="sxs-lookup"><span data-stu-id="ce714-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR\_INSTALL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-663">1603 (0x643)</span><span class="sxs-lookup"><span data-stu-id="ce714-663">1603 (0x643)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-664">Неустранимая ошибка при установке.</span><span class="sxs-lookup"><span data-stu-id="ce714-664">Fatal error during installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**Ошибка при \_ установке \_ приостановки**</span><span class="sxs-lookup"><span data-stu-id="ce714-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR\_INSTALL\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-666">1604 (0x644)</span><span class="sxs-lookup"><span data-stu-id="ce714-666">1604 (0x644)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-667">Установка приостановлена, не завершена.</span><span class="sxs-lookup"><span data-stu-id="ce714-667">Installation suspended, incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**Ошибка \_ неизвестного \_ продукта**</span><span class="sxs-lookup"><span data-stu-id="ce714-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR\_UNKNOWN\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-669">1605 (0x645)</span><span class="sxs-lookup"><span data-stu-id="ce714-669">1605 (0x645)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-670">Это действие допустимо только для продуктов, установленных в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="ce714-670">This action is only valid for products that are currently installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**Ошибка \_ неизвестного \_ компонента**</span><span class="sxs-lookup"><span data-stu-id="ce714-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR\_UNKNOWN\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-672">1606 (0x646)</span><span class="sxs-lookup"><span data-stu-id="ce714-672">1606 (0x646)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-673">Идентификатор компонента не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="ce714-673">Feature ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**Ошибка \_ неизвестного \_ компонента**</span><span class="sxs-lookup"><span data-stu-id="ce714-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR\_UNKNOWN\_COMPONENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-675">1607 (0x647)</span><span class="sxs-lookup"><span data-stu-id="ce714-675">1607 (0x647)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-676">Идентификатор компонента не зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="ce714-676">Component ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**Ошибка \_ неизвестного \_ Свойства**</span><span class="sxs-lookup"><span data-stu-id="ce714-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR\_UNKNOWN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-678">1608 (0x648)</span><span class="sxs-lookup"><span data-stu-id="ce714-678">1608 (0x648)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-679">Неизвестное свойство.</span><span class="sxs-lookup"><span data-stu-id="ce714-679">Unknown property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**Ошибка \_ недопустимого \_ состояния обработчика \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR\_INVALID\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-681">1609 (0x649)</span><span class="sxs-lookup"><span data-stu-id="ce714-681">1609 (0x649)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-682">Недопустимое состояние обработчика.</span><span class="sxs-lookup"><span data-stu-id="ce714-682">Handle is in an invalid state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**Ошибка \_ неправильной \_ конфигурации**</span><span class="sxs-lookup"><span data-stu-id="ce714-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR\_BAD\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-684">1610 (0x64A)</span><span class="sxs-lookup"><span data-stu-id="ce714-684">1610 (0x64A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-685">Данные конфигурации для этого продукта повреждены.</span><span class="sxs-lookup"><span data-stu-id="ce714-685">The configuration data for this product is corrupt.</span></span> <span data-ttu-id="ce714-686">Обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="ce714-686">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**\_отсутствует индекс \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR\_INDEX\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-688">1611 (0x64B)</span><span class="sxs-lookup"><span data-stu-id="ce714-688">1611 (0x64B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-689">Отсутствует квалификатор компонента.</span><span class="sxs-lookup"><span data-stu-id="ce714-689">Component qualifier not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**Ошибка \_ \_ \_ отсутствия источника установки**</span><span class="sxs-lookup"><span data-stu-id="ce714-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR\_INSTALL\_SOURCE\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-691">1612 (0x64C)</span><span class="sxs-lookup"><span data-stu-id="ce714-691">1612 (0x64C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-692">Источник установки для этого продукта недоступен.</span><span class="sxs-lookup"><span data-stu-id="ce714-692">The installation source for this product is not available.</span></span> <span data-ttu-id="ce714-693">Убедитесь, что источник существует и к нему есть доступ.</span><span class="sxs-lookup"><span data-stu-id="ce714-693">Verify that the source exists and that you can access it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**Ошибка \_ при \_ установке \_ версии пакета**</span><span class="sxs-lookup"><span data-stu-id="ce714-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR\_INSTALL\_PACKAGE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-695">1613 (0x64D)</span><span class="sxs-lookup"><span data-stu-id="ce714-695">1613 (0x64D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-696">Этот установочный пакет не может быть установлен службой установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-696">This installation package cannot be installed by the Windows Installer service.</span></span> <span data-ttu-id="ce714-697">Необходимо установить пакет обновления Windows, содержащий более новую версию службы установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-697">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**При \_ удалении продукта произошла ошибка \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR\_PRODUCT\_UNINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-699">1614 (0x64E)</span><span class="sxs-lookup"><span data-stu-id="ce714-699">1614 (0x64E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-700">Удаление продукта.</span><span class="sxs-lookup"><span data-stu-id="ce714-700">Product is uninstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**Ошибка \_ неправильного \_ \_ синтаксиса запроса**</span><span class="sxs-lookup"><span data-stu-id="ce714-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR\_BAD\_QUERY\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-702">1615 (0x64F)</span><span class="sxs-lookup"><span data-stu-id="ce714-702">1615 (0x64F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-703">Синтаксис SQL Query недопустим или не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ce714-703">SQL query syntax invalid or unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**Ошибка \_ недопустимого \_ поля**</span><span class="sxs-lookup"><span data-stu-id="ce714-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR\_INVALID\_FIELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-705">1616 (0x650)</span><span class="sxs-lookup"><span data-stu-id="ce714-705">1616 (0x650)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-706">Поле записи не существует.</span><span class="sxs-lookup"><span data-stu-id="ce714-706">Record field does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**устройство с ошибкой \_ \_ удалено**</span><span class="sxs-lookup"><span data-stu-id="ce714-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**ERROR\_DEVICE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-708">1617 (0x651)</span><span class="sxs-lookup"><span data-stu-id="ce714-708">1617 (0x651)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-709">Устройство удалено.</span><span class="sxs-lookup"><span data-stu-id="ce714-709">The device has been removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**Ошибка \_ установки \_ уже \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="ce714-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR\_INSTALL\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-711">1618 (0x652)</span><span class="sxs-lookup"><span data-stu-id="ce714-711">1618 (0x652)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-712">Уже выполняется другая установка.</span><span class="sxs-lookup"><span data-stu-id="ce714-712">Another installation is already in progress.</span></span> <span data-ttu-id="ce714-713">Завершите эту установку, прежде чем продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="ce714-713">Complete that installation before proceeding with this install.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**Ошибка \_ \_ при установке \_ пакета \_ не удалось открыть**</span><span class="sxs-lookup"><span data-stu-id="ce714-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR\_INSTALL\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-715">1619 (0x653)</span><span class="sxs-lookup"><span data-stu-id="ce714-715">1619 (0x653)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-716">Не удалось открыть этот установочный пакет.</span><span class="sxs-lookup"><span data-stu-id="ce714-716">This installation package could not be opened.</span></span> <span data-ttu-id="ce714-717">Убедитесь, что пакет существует и к нему есть доступ, или обратитесь к поставщику приложения, чтобы убедиться, что это допустимый пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-717">Verify that the package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**Ошибка при \_ установке \_ пакета \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR\_INSTALL\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-719">1620 (0x654)</span><span class="sxs-lookup"><span data-stu-id="ce714-719">1620 (0x654)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-720">Не удалось открыть этот установочный пакет.</span><span class="sxs-lookup"><span data-stu-id="ce714-720">This installation package could not be opened.</span></span> <span data-ttu-id="ce714-721">Обратитесь к поставщику приложения, чтобы убедиться, что это допустимый пакет установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-721">Contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**Ошибка \_ \_ при установке пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR\_INSTALL\_UI\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-723">1621 (0x655)</span><span class="sxs-lookup"><span data-stu-id="ce714-723">1621 (0x655)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-724">Произошла ошибка при запуске пользовательского интерфейса службы установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-724">There was an error starting the Windows Installer service user interface.</span></span> <span data-ttu-id="ce714-725">Обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="ce714-725">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**Ошибка \_ при установке ошибки \_ журнала \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR\_INSTALL\_LOG\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-727">1622 (0x656)</span><span class="sxs-lookup"><span data-stu-id="ce714-727">1622 (0x656)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-728">ошибка при открытии файла журнала установки.</span><span class="sxs-lookup"><span data-stu-id="ce714-728">Error opening installation log file.</span></span> <span data-ttu-id="ce714-729">Убедитесь, что указанное расположение файла журнала существует и что вы можете записать в него.</span><span class="sxs-lookup"><span data-stu-id="ce714-729">Verify that the specified log file location exists and that you can write to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**Ошибка при \_ установке \_ языка \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="ce714-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR\_INSTALL\_LANGUAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-731">1623 (0x657)</span><span class="sxs-lookup"><span data-stu-id="ce714-731">1623 (0x657)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-732">Язык этого установочного пакета не поддерживается в вашей системе.</span><span class="sxs-lookup"><span data-stu-id="ce714-732">The language of this installation package is not supported by your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**Ошибка \_ \_ при установке преобразования \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR\_INSTALL\_TRANSFORM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-734">1624 (0x658)</span><span class="sxs-lookup"><span data-stu-id="ce714-734">1624 (0x658)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-735">Ошибка при применении преобразований.</span><span class="sxs-lookup"><span data-stu-id="ce714-735">Error applying transforms.</span></span> <span data-ttu-id="ce714-736">Убедитесь, что указаны допустимые пути преобразования.</span><span class="sxs-lookup"><span data-stu-id="ce714-736">Verify that the specified transform paths are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**Ошибка при \_ установке \_ пакета \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR\_INSTALL\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-738">1625 (0x659)</span><span class="sxs-lookup"><span data-stu-id="ce714-738">1625 (0x659)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-739">Эта установка запрещена системной политикой.</span><span class="sxs-lookup"><span data-stu-id="ce714-739">This installation is forbidden by system policy.</span></span> <span data-ttu-id="ce714-740">Обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="ce714-740">Contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**\_функция ERROR \_ не \_ вызвана**</span><span class="sxs-lookup"><span data-stu-id="ce714-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**ERROR\_FUNCTION\_NOT\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-742">1626 (0x65A)</span><span class="sxs-lookup"><span data-stu-id="ce714-742">1626 (0x65A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-743">Не удалось выполнить функцию.</span><span class="sxs-lookup"><span data-stu-id="ce714-743">Function could not be executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**Ошибка \_ \_ при выполнении функции**</span><span class="sxs-lookup"><span data-stu-id="ce714-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR\_FUNCTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-745">1627 (0x65B)</span><span class="sxs-lookup"><span data-stu-id="ce714-745">1627 (0x65B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-746">Сбой функции во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce714-746">Function failed during execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**Ошибка \_ недопустимой \_ таблицы**</span><span class="sxs-lookup"><span data-stu-id="ce714-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR\_INVALID\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-748">1628 (0x65C)</span><span class="sxs-lookup"><span data-stu-id="ce714-748">1628 (0x65C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-749">Указана недопустимая или неизвестная таблица.</span><span class="sxs-lookup"><span data-stu-id="ce714-749">Invalid or unknown table specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**\_несоответствие типов данных ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-751">1629 (0x65D)</span><span class="sxs-lookup"><span data-stu-id="ce714-751">1629 (0x65D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-752">Указан неверный тип данных.</span><span class="sxs-lookup"><span data-stu-id="ce714-752">Data supplied is of wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**\_НЕподдерживаемый \_ тип ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-754">1630 (0x65E)</span><span class="sxs-lookup"><span data-stu-id="ce714-754">1630 (0x65E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-755">Данные этого типа не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ce714-755">Data of this type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**Ошибка \_ при создании ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-757">1631 (0x65F)</span><span class="sxs-lookup"><span data-stu-id="ce714-757">1631 (0x65F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-758">Не удалось запустить службу установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-758">The Windows Installer service failed to start.</span></span> <span data-ttu-id="ce714-759">Обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="ce714-759">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**Ошибка при \_ установке \_ временного \_ недоступного для записи**</span><span class="sxs-lookup"><span data-stu-id="ce714-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR\_INSTALL\_TEMP\_UNWRITABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-761">1632 (0x660)</span><span class="sxs-lookup"><span data-stu-id="ce714-761">1632 (0x660)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-762">Временная папка находится на диске, который полон или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ce714-762">The Temp folder is on a drive that is full or is inaccessible.</span></span> <span data-ttu-id="ce714-763">Освободите место на диске или убедитесь, что у вас есть разрешение на запись во временную папку.</span><span class="sxs-lookup"><span data-stu-id="ce714-763">Free up space on the drive or verify that you have write permission on the Temp folder.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**Ошибка при \_ установке \_ платформы \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="ce714-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR\_INSTALL\_PLATFORM\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-765">1633 (0x661)</span><span class="sxs-lookup"><span data-stu-id="ce714-765">1633 (0x661)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-766">Этот установочный пакет не поддерживается этим типом процессора.</span><span class="sxs-lookup"><span data-stu-id="ce714-766">This installation package is not supported by this processor type.</span></span> <span data-ttu-id="ce714-767">Обратитесь к поставщику продукта.</span><span class="sxs-lookup"><span data-stu-id="ce714-767">Contact your product vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**Ошибка при \_ установке \_ нотусед**</span><span class="sxs-lookup"><span data-stu-id="ce714-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR\_INSTALL\_NOTUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-769">1634 (0x662)</span><span class="sxs-lookup"><span data-stu-id="ce714-769">1634 (0x662)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-770">Компонент не используется на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ce714-770">Component not used on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**\_ \_ \_ сбой при открытии пакета исправления ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR\_PATCH\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-772">1635 (0x663)</span><span class="sxs-lookup"><span data-stu-id="ce714-772">1635 (0x663)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-773">Не удалось открыть этот пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="ce714-773">This update package could not be opened.</span></span> <span data-ttu-id="ce714-774">Убедитесь, что пакет обновления существует и к нему есть доступ, или обратитесь к поставщику приложения, чтобы убедиться, что это допустимый установщик Windows пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="ce714-774">Verify that the update package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**\_ \_ Недопустимый пакет исправления ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERROR\_PATCH\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-776">1636 (0x664)</span><span class="sxs-lookup"><span data-stu-id="ce714-776">1636 (0x664)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-777">Не удалось открыть этот пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="ce714-777">This update package could not be opened.</span></span> <span data-ttu-id="ce714-778">Обратитесь к поставщику приложения, чтобы убедиться, что это допустимый установщик Windows пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="ce714-778">Contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**\_пакет ИСПРАВЛЕНИЙ \_ ошибок \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="ce714-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERROR\_PATCH\_PACKAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-780">1637 (0x665)</span><span class="sxs-lookup"><span data-stu-id="ce714-780">1637 (0x665)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-781">Этот пакет обновления не может быть обработан службой установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-781">This update package cannot be processed by the Windows Installer service.</span></span> <span data-ttu-id="ce714-782">Необходимо установить пакет обновления Windows, содержащий более новую версию службы установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-782">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_версия продукта \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR\_PRODUCT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-784">1638 (0x666)</span><span class="sxs-lookup"><span data-stu-id="ce714-784">1638 (0x666)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-785">Уже установлена другая версия этого продукта.</span><span class="sxs-lookup"><span data-stu-id="ce714-785">Another version of this product is already installed.</span></span> <span data-ttu-id="ce714-786">Установка этой версии невозможна.</span><span class="sxs-lookup"><span data-stu-id="ce714-786">Installation of this version cannot continue.</span></span> <span data-ttu-id="ce714-787">Чтобы настроить или удалить существующую версию продукта, используйте оснастку "Установка и удаление программ" на панели управления.</span><span class="sxs-lookup"><span data-stu-id="ce714-787">To configure or remove the existing version of this product, use Add/Remove Programs on the Control Panel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**Ошибка \_ Недопустимая \_ Командная \_ строка**</span><span class="sxs-lookup"><span data-stu-id="ce714-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR\_INVALID\_COMMAND\_LINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-789">1639 (0x667)</span><span class="sxs-lookup"><span data-stu-id="ce714-789">1639 (0x667)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-790">Недопустимый аргумент командной строки.</span><span class="sxs-lookup"><span data-stu-id="ce714-790">Invalid command line argument.</span></span> <span data-ttu-id="ce714-791">Подробные сведения о командной строке см. в установщик Windows пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="ce714-791">Consult the Windows Installer SDK for detailed command line help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**Ошибка \_ при \_ установке \_ запрещенного удаленного**</span><span class="sxs-lookup"><span data-stu-id="ce714-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR\_INSTALL\_REMOTE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-793">1640 (0x668)</span><span class="sxs-lookup"><span data-stu-id="ce714-793">1640 (0x668)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-794">Только администраторы имеют разрешение на добавление, удаление или настройку серверного программного обеспечения во время удаленного сеанса служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="ce714-794">Only administrators have permission to add, remove, or configure server software during a Terminal services remote session.</span></span> <span data-ttu-id="ce714-795">Если вы хотите установить или настроить программное обеспечение на сервере, обратитесь к администратору сети.</span><span class="sxs-lookup"><span data-stu-id="ce714-795">If you want to install or configure software on the server, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**Ошибка \_ при \_ перезагрузке при успешном \_ запуске**</span><span class="sxs-lookup"><span data-stu-id="ce714-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR\_SUCCESS\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-797">1641 (0x669)</span><span class="sxs-lookup"><span data-stu-id="ce714-797">1641 (0x669)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-798">Запрошенная операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="ce714-798">The requested operation completed successfully.</span></span> <span data-ttu-id="ce714-799">Система будет перезапущена, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="ce714-799">The system will be restarted so the changes can take effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**\_цель исправления \_ ошибок \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="ce714-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERROR\_PATCH\_TARGET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-801">1642 (0x66A)</span><span class="sxs-lookup"><span data-stu-id="ce714-801">1642 (0x66A)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-802">Не удается установить обновление службой установщик Windows, так как возможно, программа, которая будет обновлена, отсутствует, или обновление может обновить другую версию программы.</span><span class="sxs-lookup"><span data-stu-id="ce714-802">The upgrade cannot be installed by the Windows Installer service because the program to be upgraded may be missing, or the upgrade may update a different version of the program.</span></span> <span data-ttu-id="ce714-803">Убедитесь, что обновляемая программа существует на компьютере и что у вас есть правильное обновление.</span><span class="sxs-lookup"><span data-stu-id="ce714-803">Verify that the program to be upgraded exists on your computer and that you have the correct upgrade.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**\_пакет исправления \_ ошибок \_ отклонен**</span><span class="sxs-lookup"><span data-stu-id="ce714-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERROR\_PATCH\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-805">1643 (0x66B)</span><span class="sxs-lookup"><span data-stu-id="ce714-805">1643 (0x66B)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-806">Пакет обновления не разрешен политикой ограниченного использования программ.</span><span class="sxs-lookup"><span data-stu-id="ce714-806">The update package is not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**Ошибка при \_ установке \_ преобразования \_ отклонено**</span><span class="sxs-lookup"><span data-stu-id="ce714-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR\_INSTALL\_TRANSFORM\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-808">1644 (0x66C)</span><span class="sxs-lookup"><span data-stu-id="ce714-808">1644 (0x66C)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-809">Одна или несколько настроек не разрешены политикой ограниченного использования программ.</span><span class="sxs-lookup"><span data-stu-id="ce714-809">One or more customizations are not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**Ошибка при \_ установке \_ удаленного \_ запрещенного**</span><span class="sxs-lookup"><span data-stu-id="ce714-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR\_INSTALL\_REMOTE\_PROHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-811">1645 (0x66D)</span><span class="sxs-lookup"><span data-stu-id="ce714-811">1645 (0x66D)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-812">Установщик Windows не допускают установки из подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="ce714-812">The Windows Installer does not permit installation from a Remote Desktop Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**\_Удаление исправления \_ ошибки \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="ce714-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERROR\_PATCH\_REMOVAL\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-814">1646 (0x66E)</span><span class="sxs-lookup"><span data-stu-id="ce714-814">1646 (0x66E)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-815">Удаление пакета обновления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ce714-815">Uninstallation of the update package is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**Ошибка \_ неизвестного \_ исправления**</span><span class="sxs-lookup"><span data-stu-id="ce714-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR\_UNKNOWN\_PATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-817">1647 (0x66F)</span><span class="sxs-lookup"><span data-stu-id="ce714-817">1647 (0x66F)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-818">Обновление не применяется к этому продукту.</span><span class="sxs-lookup"><span data-stu-id="ce714-818">The update is not applied to this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**\_исправление ошибки \_ без \_ последовательности**</span><span class="sxs-lookup"><span data-stu-id="ce714-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR\_PATCH\_NO\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-820">1648 (0x670)</span><span class="sxs-lookup"><span data-stu-id="ce714-820">1648 (0x670)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-821">Не удалось найти допустимую последовательность для набора обновлений.</span><span class="sxs-lookup"><span data-stu-id="ce714-821">No valid sequence could be found for the set of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**\_Удаление исправления \_ ошибки \_ запрещено**</span><span class="sxs-lookup"><span data-stu-id="ce714-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERROR\_PATCH\_REMOVAL\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-823">1649 (0x671)</span><span class="sxs-lookup"><span data-stu-id="ce714-823">1649 (0x671)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-824">Удаление обновления запрещено политикой.</span><span class="sxs-lookup"><span data-stu-id="ce714-824">Update removal was disallowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**Ошибка \_ недопустимого \_ \_ XML-файла исправления**</span><span class="sxs-lookup"><span data-stu-id="ce714-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR\_INVALID\_PATCH\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-826">1650 (0x672)</span><span class="sxs-lookup"><span data-stu-id="ce714-826">1650 (0x672)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-827">XML-данные обновления недопустимы.</span><span class="sxs-lookup"><span data-stu-id="ce714-827">The XML update data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**Ошибка при \_ исправлении \_ управляемого \_ объявленного \_ продукта**</span><span class="sxs-lookup"><span data-stu-id="ce714-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERROR\_PATCH\_MANAGED\_ADVERTISED\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-829">1651 (0x673)</span><span class="sxs-lookup"><span data-stu-id="ce714-829">1651 (0x673)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-830">Установщик Windows не допускают обновления управляемых объявленных продуктов.</span><span class="sxs-lookup"><span data-stu-id="ce714-830">Windows Installer does not permit updating of managed advertised products.</span></span> <span data-ttu-id="ce714-831">Перед применением обновления необходимо установить по крайней мере один компонент продукта.</span><span class="sxs-lookup"><span data-stu-id="ce714-831">At least one feature of the product must be installed before applying the update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**Ошибка при \_ установке \_ службы \_ SAFEBOOT**</span><span class="sxs-lookup"><span data-stu-id="ce714-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR\_INSTALL\_SERVICE\_SAFEBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-833">1652 (0x674)</span><span class="sxs-lookup"><span data-stu-id="ce714-833">1652 (0x674)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-834">Служба установщик Windows недоступна в защищенном режиме.</span><span class="sxs-lookup"><span data-stu-id="ce714-834">The Windows Installer service is not accessible in Safe Mode.</span></span> <span data-ttu-id="ce714-835">Повторите попытку, когда компьютер не находится в защищенном режиме, или воспользуйтесь восстановлением системы, чтобы вернуть компьютер к предыдущему работоспособному состоянию.</span><span class="sxs-lookup"><span data-stu-id="ce714-835">Please try again when your computer is not in Safe Mode or you can use System Restore to return your machine to a previous good state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**Ошибка \_ при \_ быстром \_ возникновении ошибки**</span><span class="sxs-lookup"><span data-stu-id="ce714-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR\_FAIL\_FAST\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-837">1653 (0x675)</span><span class="sxs-lookup"><span data-stu-id="ce714-837">1653 (0x675)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-838">Произошло исключение с быстрым сбоем.</span><span class="sxs-lookup"><span data-stu-id="ce714-838">A fail fast exception occurred.</span></span> <span data-ttu-id="ce714-839">Обработчики исключений не будут вызываться, и процесс будет завершен немедленно.</span><span class="sxs-lookup"><span data-stu-id="ce714-839">Exception handlers will not be invoked and the process will be terminated immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce714-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**Ошибка при \_ установке \_**</span><span class="sxs-lookup"><span data-stu-id="ce714-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR\_INSTALL\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce714-841">1654 (0x676)</span><span class="sxs-lookup"><span data-stu-id="ce714-841">1654 (0x676)</span></span>
</dt> <dt>



<span data-ttu-id="ce714-842">Приложение, которое вы пытаетесь запустить, не поддерживается в этой версии Windows.</span><span class="sxs-lookup"><span data-stu-id="ce714-842">The app that you are trying to run is not supported on this version of Windows.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce714-843">Требования</span><span class="sxs-lookup"><span data-stu-id="ce714-843">Requirements</span></span>



| <span data-ttu-id="ce714-844">Требование</span><span class="sxs-lookup"><span data-stu-id="ce714-844">Requirement</span></span> | <span data-ttu-id="ce714-845">Значение</span><span class="sxs-lookup"><span data-stu-id="ce714-845">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce714-846">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce714-846">Minimum supported client</span></span><br/> | <span data-ttu-id="ce714-847">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ce714-847">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce714-848">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce714-848">Minimum supported server</span></span><br/> | <span data-ttu-id="ce714-849">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce714-849">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce714-850">Header</span><span class="sxs-lookup"><span data-stu-id="ce714-850">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce714-851"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce714-851"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce714-852">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce714-852">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce714-853">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="ce714-853">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




