---
description: Описание кодов ошибок 6000-8199, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Коды системных ошибок (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896145"
---
# <a name="system-error-codes-6000-8199"></a><span data-ttu-id="eb676-103">Коды системных ошибок (6000-8199)</span><span class="sxs-lookup"><span data-stu-id="eb676-103">System Error Codes (6000-8199)</span></span>

> [!NOTE]
> <span data-ttu-id="eb676-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb676-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="eb676-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb676-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="eb676-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) (ошибки 6000 – 8199).</span><span class="sxs-lookup"><span data-stu-id="eb676-106">The following list describes [system error codes](system-error-codes.md) (errors 6000 to 8199).</span></span> <span data-ttu-id="eb676-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="eb676-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="eb676-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="eb676-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="eb676-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**Ошибка \_ шифрования \_ при ошибке**</span><span class="sxs-lookup"><span data-stu-id="eb676-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR\_ENCRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-110">6000 (0x1770)</span><span class="sxs-lookup"><span data-stu-id="eb676-110">6000 (0x1770)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-111">Указанный файл не может быть зашифрован.</span><span class="sxs-lookup"><span data-stu-id="eb676-111">The specified file could not be encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_сбой при расшифровке ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR\_DECRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-113">6001 (0x1771)</span><span class="sxs-lookup"><span data-stu-id="eb676-113">6001 (0x1771)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-114">Не удалось расшифровать указанный файл.</span><span class="sxs-lookup"><span data-stu-id="eb676-114">The specified file could not be decrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**файл с ОШИБКАми \_ \_ зашифрован**</span><span class="sxs-lookup"><span data-stu-id="eb676-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ERROR\_FILE\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-116">6002 (0x1772)</span><span class="sxs-lookup"><span data-stu-id="eb676-116">6002 (0x1772)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-117">Указанный файл зашифрован, и пользователь не может его расшифровать.</span><span class="sxs-lookup"><span data-stu-id="eb676-117">The specified file is encrypted and the user does not have the ability to decrypt it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**Ошибка \_ без \_ \_ политики восстановления**</span><span class="sxs-lookup"><span data-stu-id="eb676-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR\_NO\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-119">6003 (0x1773)</span><span class="sxs-lookup"><span data-stu-id="eb676-119">6003 (0x1773)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-120">Для этой системы не настроена допустимая политика восстановления шифрования.</span><span class="sxs-lookup"><span data-stu-id="eb676-120">There is no valid encryption recovery policy configured for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**Ошибка \_ без \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="eb676-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR\_NO\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-122">6004 (0x1774)</span><span class="sxs-lookup"><span data-stu-id="eb676-122">6004 (0x1774)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-123">Необходимый для этой системы драйвер шифрования не загружен.</span><span class="sxs-lookup"><span data-stu-id="eb676-123">The required encryption driver is not loaded for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**произошла ошибка \_ \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="eb676-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR\_WRONG\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-125">6005 (0x1775)</span><span class="sxs-lookup"><span data-stu-id="eb676-125">6005 (0x1775)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-126">Файл был зашифрован с использованием другого драйвера шифрования, чем в настоящий момент загружен.</span><span class="sxs-lookup"><span data-stu-id="eb676-126">The file was encrypted with a different encryption driver than is currently loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**Ошибка \_ без \_ \_ ключей пользователей**</span><span class="sxs-lookup"><span data-stu-id="eb676-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR\_NO\_USER\_KEYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-128">6006 (0x1776)</span><span class="sxs-lookup"><span data-stu-id="eb676-128">6006 (0x1776)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-129">Для пользователя не определены ключи EFS.</span><span class="sxs-lookup"><span data-stu-id="eb676-129">There are no EFS keys defined for the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**\_файл ошибок \_ не \_ зашифрован**</span><span class="sxs-lookup"><span data-stu-id="eb676-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ERROR\_FILE\_NOT\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-131">6007 (0x1777)</span><span class="sxs-lookup"><span data-stu-id="eb676-131">6007 (0x1777)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-132">Указанный файл не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="eb676-132">The specified file is not encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**Ошибка \_ при \_ экспорте \_ формата**</span><span class="sxs-lookup"><span data-stu-id="eb676-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR\_NOT\_EXPORT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-134">6008 (0x1778)</span><span class="sxs-lookup"><span data-stu-id="eb676-134">6008 (0x1778)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-135">Указанный файл не находится в определенном формате экспорта EFS.</span><span class="sxs-lookup"><span data-stu-id="eb676-135">The specified file is not in the defined EFS export format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**Ошибка \_ файл \_ только для чтения \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ERROR\_FILE\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-137">6009 (0x1779)</span><span class="sxs-lookup"><span data-stu-id="eb676-137">6009 (0x1779)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-138">Указанный файл доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="eb676-138">The specified file is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**Ошибка \_ dir. \_ EFS \_ запрещена**</span><span class="sxs-lookup"><span data-stu-id="eb676-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR\_DIR\_EFS\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-140">6010 (0x177A)</span><span class="sxs-lookup"><span data-stu-id="eb676-140">6010 (0x177A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-141">Для этого каталога отключено шифрование.</span><span class="sxs-lookup"><span data-stu-id="eb676-141">The directory has been disabled for encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**Ошибка \_ " \_ сервер EFS \_ не является \_ доверенным"**</span><span class="sxs-lookup"><span data-stu-id="eb676-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR\_EFS\_SERVER\_NOT\_TRUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-143">6011 (0x177B)</span><span class="sxs-lookup"><span data-stu-id="eb676-143">6011 (0x177B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-144">Сервер не является доверенным для удаленной операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="eb676-144">The server is not trusted for remote encryption operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**Ошибка \_ неправильной \_ \_ политики восстановления**</span><span class="sxs-lookup"><span data-stu-id="eb676-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR\_BAD\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-146">6012 (0x177C)</span><span class="sxs-lookup"><span data-stu-id="eb676-146">6012 (0x177C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-147">Политика восстановления, настроенная для этой системы, содержит недопустимый сертификат восстановления.</span><span class="sxs-lookup"><span data-stu-id="eb676-147">Recovery policy configured for this system contains invalid recovery certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**Ошибка \_ \_ \_ \_ слишком \_ большой размер BLOB-объекта алгоритма EFS**</span><span class="sxs-lookup"><span data-stu-id="eb676-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR\_EFS\_ALG\_BLOB\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-149">6013 (0x177D)</span><span class="sxs-lookup"><span data-stu-id="eb676-149">6013 (0x177D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-150">Алгоритму шифрования, используемому в исходном файле, требуется больший буфер ключа, чем тот, который находится в целевом файле.</span><span class="sxs-lookup"><span data-stu-id="eb676-150">The encryption algorithm used on the source file needs a bigger key buffer than the one on the destination file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**\_том ошибок \_ не \_ поддерживает \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="eb676-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERROR\_VOLUME\_NOT\_SUPPORT\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-152">6014 (0x177E)</span><span class="sxs-lookup"><span data-stu-id="eb676-152">6014 (0x177E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-153">Раздел диска не поддерживает шифрование файлов.</span><span class="sxs-lookup"><span data-stu-id="eb676-153">The disk partition does not support file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**Ошибка \_ EFS \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="eb676-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR\_EFS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-155">6015 (0x177F)</span><span class="sxs-lookup"><span data-stu-id="eb676-155">6015 (0x177F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-156">Этот компьютер отключен для шифрования файлов.</span><span class="sxs-lookup"><span data-stu-id="eb676-156">This machine is disabled for file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**Ошибка \_ \_ \_ не поддерживает версию \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="eb676-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR\_EFS\_VERSION\_NOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-158">6016 (0x1780)</span><span class="sxs-lookup"><span data-stu-id="eb676-158">6016 (0x1780)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-159">Для расшифровки этого зашифрованного файла требуется более новая система.</span><span class="sxs-lookup"><span data-stu-id="eb676-159">A newer system is required to decrypt this encrypted file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**Ошибка \_ CS \_ ENCRYPTION \_ Недопустимый \_ \_ ответ сервера**</span><span class="sxs-lookup"><span data-stu-id="eb676-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR\_CS\_ENCRYPTION\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-161">6017 (0x1781)</span><span class="sxs-lookup"><span data-stu-id="eb676-161">6017 (0x1781)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-162">Удаленный сервер отправил недопустимый ответ для открываемого файла с шифрованием на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="eb676-162">The remote server sent an invalid response for a file being opened with Client Side Encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**Ошибка \_ CS \_ ENCRYPTION \_ неподдерживаемый \_ сервер**</span><span class="sxs-lookup"><span data-stu-id="eb676-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR\_CS\_ENCRYPTION\_UNSUPPORTED\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-164">6018 (0x1782)</span><span class="sxs-lookup"><span data-stu-id="eb676-164">6018 (0x1782)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-165">Шифрование на стороне клиента не поддерживается удаленным сервером, хотя оно требует его поддержки.</span><span class="sxs-lookup"><span data-stu-id="eb676-165">Client Side Encryption is not supported by the remote server even though it claims to support it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**Ошибка \_ CS \_ Шифрование \_ существующего \_ зашифрованного \_ файла**</span><span class="sxs-lookup"><span data-stu-id="eb676-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_EXISTING\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-167">6019 (0x1783)</span><span class="sxs-lookup"><span data-stu-id="eb676-167">6019 (0x1783)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-168">Файл зашифрован и должен быть открыт в режиме шифрования на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="eb676-168">File is encrypted and should be opened in Client Side Encryption mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**Ошибка \_ CS \_ Шифрование \_ нового \_ зашифрованного \_ файла**</span><span class="sxs-lookup"><span data-stu-id="eb676-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_NEW\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-170">6020 (0x1784)</span><span class="sxs-lookup"><span data-stu-id="eb676-170">6020 (0x1784)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-171">Создается новый зашифрованный файл, и необходимо указать $EFS.</span><span class="sxs-lookup"><span data-stu-id="eb676-171">A new encrypted file is being created and a $EFS needs to be provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**Ошибка \_ CS \_ \_ File Encryption \_ не является \_ CSE**</span><span class="sxs-lookup"><span data-stu-id="eb676-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR\_CS\_ENCRYPTION\_FILE\_NOT\_CSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-173">6021 (0x1785)</span><span class="sxs-lookup"><span data-stu-id="eb676-173">6021 (0x1785)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-174">Клиент SMB запросил CSE ФСКТЛ в файле, отличном от CSE.</span><span class="sxs-lookup"><span data-stu-id="eb676-174">The SMB client requested a CSE FSCTL on a non-CSE file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**\_Политика шифрования \_ ошибок \_ запрещает \_ операцию**</span><span class="sxs-lookup"><span data-stu-id="eb676-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR\_ENCRYPTION\_POLICY\_DENIES\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-176">6022 (0x1786)</span><span class="sxs-lookup"><span data-stu-id="eb676-176">6022 (0x1786)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-177">Запрошенная операция заблокирована политикой.</span><span class="sxs-lookup"><span data-stu-id="eb676-177">The requested operation was blocked by policy.</span></span> <span data-ttu-id="eb676-178">Для получения дополнительных сведений обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="eb676-178">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**Ошибка \_ не \_ \_ найдены серверы \_ браузера**</span><span class="sxs-lookup"><span data-stu-id="eb676-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR\_NO\_BROWSER\_SERVERS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-180">6118 (0x17E6)</span><span class="sxs-lookup"><span data-stu-id="eb676-180">6118 (0x17E6)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-181">Список серверов для этой Рабочей группы в настоящее время недоступен.</span><span class="sxs-lookup"><span data-stu-id="eb676-181">The list of servers for this workgroup is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED \_ E \_ Service \_ Not \_ LocalSystem**</span><span class="sxs-lookup"><span data-stu-id="eb676-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED\_E\_SERVICE\_NOT\_LOCALSYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-183">6200 (0x1838)</span><span class="sxs-lookup"><span data-stu-id="eb676-183">6200 (0x1838)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-184">Служба планировщик задач должна быть настроена для правильной работы в системной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="eb676-184">The Task Scheduler service must be configured to run in the System account to function properly.</span></span> <span data-ttu-id="eb676-185">Отдельные задачи могут быть настроены для работы в других учетных записях.</span><span class="sxs-lookup"><span data-stu-id="eb676-185">Individual tasks may be configured to run in other accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**\_ \_ Недопустимый сектор журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**ERROR\_LOG\_SECTOR\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-187">6600 (0x19C8)</span><span class="sxs-lookup"><span data-stu-id="eb676-187">6600 (0x19C8)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-188">Служба журнала обнаружила недопустимый сектор журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-188">Log service encountered an invalid log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**\_ \_ \_ Недопустимый контроль четности для сектора журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**ERROR\_LOG\_SECTOR\_PARITY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-190">6601 (0x19C9)</span><span class="sxs-lookup"><span data-stu-id="eb676-190">6601 (0x19C9)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-191">Служба журнала обнаружила сектор журнала с недопустимым контролем четности блоков.</span><span class="sxs-lookup"><span data-stu-id="eb676-191">Log service encountered a log sector with invalid block parity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**повторное \_ \_ сопоставление сектора журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**ERROR\_LOG\_SECTOR\_REMAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-193">6602 (0x19CA)</span><span class="sxs-lookup"><span data-stu-id="eb676-193">6602 (0x19CA)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-194">Служба журнала обнаружила повторно сопоставленный сектор журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-194">Log service encountered a remapped log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**\_неполный \_ блок журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**ERROR\_LOG\_BLOCK\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-196">6603 (0x19CB)</span><span class="sxs-lookup"><span data-stu-id="eb676-196">6603 (0x19CB)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-197">Служба журнала обнаружила частичный или неполный блок журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-197">Log service encountered a partial or incomplete log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ Недопустимый \_ диапазон журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**ERROR\_LOG\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-199">6604 (0x19CC)</span><span class="sxs-lookup"><span data-stu-id="eb676-199">6604 (0x19CC)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-200">Служба журнала обнаружила попытки доступа к данным за пределами активного диапазона журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-200">Log service encountered an attempt access data outside the active log range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**\_ \_ исчерпаны блоки журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**ERROR\_LOG\_BLOCKS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-202">6605 (0x19CD)</span><span class="sxs-lookup"><span data-stu-id="eb676-202">6605 (0x19CD)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-203">Буферы для пользователя службы журнала исчерпаны.</span><span class="sxs-lookup"><span data-stu-id="eb676-203">Log service user marshalling buffers are exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**\_ \_ \_ Недопустимый контекст \_ чтения журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**ERROR\_LOG\_READ\_CONTEXT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-205">6606 (0x19CE)</span><span class="sxs-lookup"><span data-stu-id="eb676-205">6606 (0x19CE)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-206">Служба журнала обнаружила операцию чтения из области маршалирования с недопустимым контекстом чтения.</span><span class="sxs-lookup"><span data-stu-id="eb676-206">Log service encountered an attempt read from a marshalling area with an invalid read context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**\_ \_ Недопустимый ПЕРЕЗАПУСК журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**ERROR\_LOG\_RESTART\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-208">6607 (0x19CF)</span><span class="sxs-lookup"><span data-stu-id="eb676-208">6607 (0x19CF)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-209">Служба журнала обнаружила недопустимую область перезапуска журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-209">Log service encountered an invalid log restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_ \_ версия блока журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR\_LOG\_BLOCK\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-211">6608 (0x19D0)</span><span class="sxs-lookup"><span data-stu-id="eb676-211">6608 (0x19D0)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-212">Служба журнала обнаружила недопустимую версию блока журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-212">Log service encountered an invalid log block version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**\_ \_ Недопустимый блок журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**ERROR\_LOG\_BLOCK\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-214">6609 (0x19D1)</span><span class="sxs-lookup"><span data-stu-id="eb676-214">6609 (0x19D1)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-215">Служба журнала обнаружила недопустимый блок журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-215">Log service encountered an invalid log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**\_ \_ \_ Недопустимый режим \_ чтения журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**ERROR\_LOG\_READ\_MODE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-217">6610 (0x19D2)</span><span class="sxs-lookup"><span data-stu-id="eb676-217">6610 (0x19D2)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-218">Служба журнала обнаружила попытку чтения журнала с недопустимым режимом чтения.</span><span class="sxs-lookup"><span data-stu-id="eb676-218">Log service encountered an attempt to read the log with an invalid read mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**\_журнал ошибок \_ без \_ перезагрузки**</span><span class="sxs-lookup"><span data-stu-id="eb676-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**ERROR\_LOG\_NO\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-220">6611 (0x19D3)</span><span class="sxs-lookup"><span data-stu-id="eb676-220">6611 (0x19D3)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-221">Служба журнала обнаружила поток журнала без области перезапуска.</span><span class="sxs-lookup"><span data-stu-id="eb676-221">Log service encountered a log stream with no restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**\_ \_ повреждение МЕТАДАННЫХ журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**ERROR\_LOG\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-223">6612 (0x19D4)</span><span class="sxs-lookup"><span data-stu-id="eb676-223">6612 (0x19D4)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-224">Служба журнала обнаружила поврежденный файл метаданных.</span><span class="sxs-lookup"><span data-stu-id="eb676-224">Log service encountered a corrupted metadata file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**\_ \_ недопустимые метаданные журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**ERROR\_LOG\_METADATA\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-226">6613 (0x19D5)</span><span class="sxs-lookup"><span data-stu-id="eb676-226">6613 (0x19D5)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-227">Служба журнала обнаружила файл метаданных, который не удалось создать с помощью файловой системы журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-227">Log service encountered a metadata file that could not be created by the log file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**\_несоответствие \_ МЕТАДАННЫХ журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**ERROR\_LOG\_METADATA\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-229">6614 (0x19D6)</span><span class="sxs-lookup"><span data-stu-id="eb676-229">6614 (0x19D6)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-230">Служба журнала обнаружила файл метаданных с непоследовательными данными.</span><span class="sxs-lookup"><span data-stu-id="eb676-230">Log service encountered a metadata file with inconsistent data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**\_ \_ недопустимое резервирование журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**ERROR\_LOG\_RESERVATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-232">6615 (0x19D7)</span><span class="sxs-lookup"><span data-stu-id="eb676-232">6615 (0x19D7)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-233">Служба журнала обнаружила попытку ошибочного выделения или удаления пространства резервирования.</span><span class="sxs-lookup"><span data-stu-id="eb676-233">Log service encountered an attempt to erroneous allocate or dispose reservation space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**журнал ошибок "не \_ \_ удается \_ Удалить"**</span><span class="sxs-lookup"><span data-stu-id="eb676-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR\_LOG\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-235">6616 (0x19D8)</span><span class="sxs-lookup"><span data-stu-id="eb676-235">6616 (0x19D8)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-236">Службе журнала не удается удалить файл журнала или контейнер файловой системы.</span><span class="sxs-lookup"><span data-stu-id="eb676-236">Log service cannot delete log file or file system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**\_ \_ \_ Превышено ограничение \_ контейнера журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**ERROR\_LOG\_CONTAINER\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-238">6617 (0x19D9)</span><span class="sxs-lookup"><span data-stu-id="eb676-238">6617 (0x19D9)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-239">Служба журналов достигла максимально допустимого контейнера, выделенного файлу журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-239">Log service has reached the maximum allowable containers allocated to a log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**Журнал \_ ошибок \_ \_ , начало \_ журнала**</span><span class="sxs-lookup"><span data-stu-id="eb676-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**ERROR\_LOG\_START\_OF\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-241">6618 (0x19DA)</span><span class="sxs-lookup"><span data-stu-id="eb676-241">6618 (0x19DA)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-242">Служба журнала попыталась выполнить чтение или запись в обратном направлении после начала журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-242">Log service has attempted to read or write backward past the start of the log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**\_Политика журнала \_ ошибок \_ уже \_ установлена**</span><span class="sxs-lookup"><span data-stu-id="eb676-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**ERROR\_LOG\_POLICY\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-244">6619 (0x19DB)</span><span class="sxs-lookup"><span data-stu-id="eb676-244">6619 (0x19DB)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-245">Не удалось установить политику журнала, так как уже существует политика того же типа.</span><span class="sxs-lookup"><span data-stu-id="eb676-245">Log policy could not be installed because a policy of the same type is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**\_Политика журнала \_ ошибок \_ не \_ установлена**</span><span class="sxs-lookup"><span data-stu-id="eb676-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**ERROR\_LOG\_POLICY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-247">6620 (0x19DC)</span><span class="sxs-lookup"><span data-stu-id="eb676-247">6620 (0x19DC)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-248">Рассматриваемая политика журнала не была установлена во время запроса.</span><span class="sxs-lookup"><span data-stu-id="eb676-248">Log policy in question was not installed at the time of the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**\_ \_ Недопустимая политика журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**ERROR\_LOG\_POLICY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-250">6621 (0x19DD)</span><span class="sxs-lookup"><span data-stu-id="eb676-250">6621 (0x19DD)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-251">В журнале установлен недопустимый набор политик.</span><span class="sxs-lookup"><span data-stu-id="eb676-251">The installed set of policies on the log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_ \_ конфликт политик журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**ERROR\_LOG\_POLICY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-253">6622 (0x19DE)</span><span class="sxs-lookup"><span data-stu-id="eb676-253">6622 (0x19DE)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-254">Не удалось завершить операцию из-за политики для рассматриваемого журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-254">A policy on the log in question prevented the operation from completing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_ \_ закрепленный \_ \_ ЗАКЛЮЧИТЕЛЬный фрагмент журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**ERROR\_LOG\_PINNED\_ARCHIVE\_TAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-256">6623 (0x19DF)</span><span class="sxs-lookup"><span data-stu-id="eb676-256">6623 (0x19DF)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-257">Не удается освободить пространство журнала, так как журнал закреплен с помощью заключительного фрагмента архива.</span><span class="sxs-lookup"><span data-stu-id="eb676-257">Log space cannot be reclaimed because the log is pinned by the archive tail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**\_ \_ несуществующая запись журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**ERROR\_LOG\_RECORD\_NONEXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-259">6624 (0x19E0)</span><span class="sxs-lookup"><span data-stu-id="eb676-259">6624 (0x19E0)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-260">Запись журнала не является записью в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-260">Log record is not a record in the log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_ \_ \_ недопустимые зарезервированные записи журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**ERROR\_LOG\_RECORDS\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-262">6625 (0x19E1)</span><span class="sxs-lookup"><span data-stu-id="eb676-262">6625 (0x19E1)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-263">Количество зарезервированных записей журнала или недопустимая Коррекция количества зарезервированных записей журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-263">Number of reserved log records or the adjustment of the number of reserved log records is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**\_ \_ \_ недопустимое зарезервированное пространство журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ERROR\_LOG\_SPACE\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-265">6626 (0x19E2)</span><span class="sxs-lookup"><span data-stu-id="eb676-265">6626 (0x19E2)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-266">Зарезервированное пространство журнала или корректировка пространства журнала недействительны.</span><span class="sxs-lookup"><span data-stu-id="eb676-266">Reserved log space or the adjustment of the log space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**\_ \_ Недопустимый конец журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**ERROR\_LOG\_TAIL\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-268">6627 (0x19E3)</span><span class="sxs-lookup"><span data-stu-id="eb676-268">6627 (0x19E3)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-269">Новый или существующий архивный хвост или база активного журнала недействительна.</span><span class="sxs-lookup"><span data-stu-id="eb676-269">An new or existing archive tail or base of the active log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**\_журнал ошибок \_ полон**</span><span class="sxs-lookup"><span data-stu-id="eb676-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**ERROR\_LOG\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-271">6628 (0x19E4)</span><span class="sxs-lookup"><span data-stu-id="eb676-271">6628 (0x19E4)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-272">Место в журнале исчерпано.</span><span class="sxs-lookup"><span data-stu-id="eb676-272">Log space is exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**Ошибка \_ \_ не удалось \_ изменить размер \_ журнала**</span><span class="sxs-lookup"><span data-stu-id="eb676-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR\_COULD\_NOT\_RESIZE\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-274">6629 (0x19E5)</span><span class="sxs-lookup"><span data-stu-id="eb676-274">6629 (0x19E5)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-275">Не удалось установить запрошенный размер журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-275">The log could not be set to the requested size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**\_немультиплексированный журнал ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**ERROR\_LOG\_MULTIPLEXED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-277">6630 (0x19E6)</span><span class="sxs-lookup"><span data-stu-id="eb676-277">6630 (0x19E6)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-278">Журнал мультиплексен, прямая запись в физический журнал запрещена.</span><span class="sxs-lookup"><span data-stu-id="eb676-278">Log is multiplexed, no direct writes to the physical log is allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**\_ \_ Выделенный Журнал ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**ERROR\_LOG\_DEDICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-280">6631 (0x19E7)</span><span class="sxs-lookup"><span data-stu-id="eb676-280">6631 (0x19E7)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-281">Не удалось выполнить операцию, так как журнал является выделенным журналом.</span><span class="sxs-lookup"><span data-stu-id="eb676-281">The operation failed because the log is a dedicated log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_ \_ \_ не \_ выполняется архивация \_ журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-283">6632 (0x19E8)</span><span class="sxs-lookup"><span data-stu-id="eb676-283">6632 (0x19E8)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-284">Для операции требуется контекст архива.</span><span class="sxs-lookup"><span data-stu-id="eb676-284">The operation requires an archive context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ выполняется архивация \_ журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-286">6633 (0x19E9)</span><span class="sxs-lookup"><span data-stu-id="eb676-286">6633 (0x19E9)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-287">Выполняется архивация журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-287">Log archival is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**журнал ошибок " \_ \_ эфемерный"**</span><span class="sxs-lookup"><span data-stu-id="eb676-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR\_LOG\_EPHEMERAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-289">6634 (0x19EA)</span><span class="sxs-lookup"><span data-stu-id="eb676-289">6634 (0x19EA)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-290">Для операции требуется невременный журнал, но журнал является эфемерным.</span><span class="sxs-lookup"><span data-stu-id="eb676-290">The operation requires a non-ephemeral log, but the log is ephemeral.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**\_ \_ \_ недостаточно контейнеров для журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**ERROR\_LOG\_NOT\_ENOUGH\_CONTAINERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-292">6635 (0x19EB)</span><span class="sxs-lookup"><span data-stu-id="eb676-292">6635 (0x19EB)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-293">В журнале должно быть по крайней мере два контейнера, прежде чем они могут быть считаны или записаны в.</span><span class="sxs-lookup"><span data-stu-id="eb676-293">The log must have at least two containers before it can be read from or written to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**\_Клиент журнала \_ ошибок \_ уже \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="eb676-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**ERROR\_LOG\_CLIENT\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-295">6636 (0x19EC)</span><span class="sxs-lookup"><span data-stu-id="eb676-295">6636 (0x19EC)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-296">Клиент журнала уже зарегистрирован в потоке.</span><span class="sxs-lookup"><span data-stu-id="eb676-296">A log client has already registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**\_Клиент журнала \_ ошибок \_ не \_ зарегистрирован**</span><span class="sxs-lookup"><span data-stu-id="eb676-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**ERROR\_LOG\_CLIENT\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-298">6637 (0x19ED)</span><span class="sxs-lookup"><span data-stu-id="eb676-298">6637 (0x19ED)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-299">Клиент журнала не зарегистрирован в потоке.</span><span class="sxs-lookup"><span data-stu-id="eb676-299">A log client has not been registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ выполняется полный обработчик \_ \_ журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR\_LOG\_FULL\_HANDLER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-301">6638 (0x19EE)</span><span class="sxs-lookup"><span data-stu-id="eb676-301">6638 (0x19EE)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-302">Уже выполнен запрос на обработку условия переполнения журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-302">A request has already been made to handle the log full condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**\_ \_ \_ сбой чтения контейнера журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR\_LOG\_CONTAINER\_READ\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-304">6639 (0x19EF)</span><span class="sxs-lookup"><span data-stu-id="eb676-304">6639 (0x19EF)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-305">Служба журнала обнаружила ошибку при попытке чтения из контейнера журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-305">Log service encountered an error when attempting to read from a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**\_ \_ \_ сбой записи контейнера журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR\_LOG\_CONTAINER\_WRITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-307">6640 (0x19F0)</span><span class="sxs-lookup"><span data-stu-id="eb676-307">6640 (0x19F0)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-308">Служба журнала обнаружила ошибку при попытке записи в контейнер журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-308">Log service encountered an error when attempting to write to a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**\_ \_ \_ не удалось открыть контейнер журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR\_LOG\_CONTAINER\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-310">6641 (0x19F1)</span><span class="sxs-lookup"><span data-stu-id="eb676-310">6641 (0x19F1)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-311">Служба журнала обнаружила ошибку при попыток открыть контейнер журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-311">Log service encountered an error when attempting open a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**\_ \_ \_ недопустимое состояние контейнера журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ERROR\_LOG\_CONTAINER\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-313">6642 (0x19F2)</span><span class="sxs-lookup"><span data-stu-id="eb676-313">6642 (0x19F2)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-314">Служба журнала обнаружила недопустимое состояние контейнера при выполнении запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="eb676-314">Log service encountered an invalid container state when attempting a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**\_ \_ недопустимое состояние журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ERROR\_LOG\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-316">6643 (0x19F3)</span><span class="sxs-lookup"><span data-stu-id="eb676-316">6643 (0x19F3)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-317">Служба журнала находится в неправильном состоянии для выполнения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="eb676-317">Log service is not in the correct state to perform a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**\_ \_ закрепленный журнал ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**ERROR\_LOG\_PINNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-319">6644 (0x19F4)</span><span class="sxs-lookup"><span data-stu-id="eb676-319">6644 (0x19F4)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-320">Не удается освободить место в журнале, так как журнал закреплен.</span><span class="sxs-lookup"><span data-stu-id="eb676-320">Log space cannot be reclaimed because the log is pinned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_ \_ \_ сбой при записи метаданных журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR\_LOG\_METADATA\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-322">6645 (0x19F5)</span><span class="sxs-lookup"><span data-stu-id="eb676-322">6645 (0x19F5)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-323">Сбой при записи метаданных журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-323">Log metadata flush failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**журнал ошибок — \_ \_ несовместимость \_ безопасности**</span><span class="sxs-lookup"><span data-stu-id="eb676-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**ERROR\_LOG\_INCONSISTENT\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-325">6646 (0x19F6)</span><span class="sxs-lookup"><span data-stu-id="eb676-325">6646 (0x19F6)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-326">Безопасность журнала и его контейнеров не согласуется.</span><span class="sxs-lookup"><span data-stu-id="eb676-326">Security on the log and its containers is inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**Ошибка \_ \_ при присоединении \_ записи журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR\_LOG\_APPENDED\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-328">6647 (0x19F7)</span><span class="sxs-lookup"><span data-stu-id="eb676-328">6647 (0x19F7)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-329">Записи были добавлены в журнал или были внесены изменения в резервирование, но журнал не может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="eb676-329">Records were appended to the log or reservation changes were made, but the log could not be flushed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ зафиксированное \_ РЕЗЕРВИРОВАНие журнала ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**ERROR\_LOG\_PINNED\_RESERVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-331">6648 (0x19F8)</span><span class="sxs-lookup"><span data-stu-id="eb676-331">6648 (0x19F8)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-332">Журнал закреплен из-за резервирования, использующего большую часть пространства журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-332">The log is pinned due to reservation consuming most of the log space.</span></span> <span data-ttu-id="eb676-333">Освободите зарезервированные записи, чтобы освободить место.</span><span class="sxs-lookup"><span data-stu-id="eb676-333">Free some reserved records to make space available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**Ошибка \_ недопустимой \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR\_INVALID\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-335">6700 (0x1A2C)</span><span class="sxs-lookup"><span data-stu-id="eb676-335">6700 (0x1A2C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-336">Недопустимый маркер транзакции, связанный с этой операцией.</span><span class="sxs-lookup"><span data-stu-id="eb676-336">The transaction handle associated with this operation is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**\_неактивная Ошибка транзакции \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR\_TRANSACTION\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-338">6701 (0x1A2D)</span><span class="sxs-lookup"><span data-stu-id="eb676-338">6701 (0x1A2D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-339">Запрошенная операция была выполнена в контексте транзакции, которая больше не активна.</span><span class="sxs-lookup"><span data-stu-id="eb676-339">The requested operation was made in the context of a transaction that is no longer active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**\_ \_ Недопустимый запрос ошибки транзакции \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR\_TRANSACTION\_REQUEST\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-341">6702 (0x1A2E)</span><span class="sxs-lookup"><span data-stu-id="eb676-341">6702 (0x1A2E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-342">Запрошенная операция недопустима для объекта транзакции в его текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="eb676-342">The requested operation is not valid on the Transaction object in its current state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ОШИБОЧная \_ транзакция \_ не \_ запрошена**</span><span class="sxs-lookup"><span data-stu-id="eb676-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ERROR\_TRANSACTION\_NOT\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-344">6703 (0x1A2F)</span><span class="sxs-lookup"><span data-stu-id="eb676-344">6703 (0x1A2F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-345">Вызывающий объект вызвал API ответа, но ответ не ожидается, так как TM не выдавала соответствующий запрос вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="eb676-345">The caller has called a response API, but the response is not expected because the TM did not issue the corresponding request to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**транзакция с ошибкой \_ \_ уже \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="eb676-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**ERROR\_TRANSACTION\_ALREADY\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-347">6704 (0x1A30)</span><span class="sxs-lookup"><span data-stu-id="eb676-347">6704 (0x1A30)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-348">Выполнение запрошенной операции слишком поздно, так как транзакция уже прервана.</span><span class="sxs-lookup"><span data-stu-id="eb676-348">It is too late to perform the requested operation, since the Transaction has already been aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**транзакция с ошибкой \_ \_ уже \_ зафиксирована**</span><span class="sxs-lookup"><span data-stu-id="eb676-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**ERROR\_TRANSACTION\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-350">6705 (0x1A31)</span><span class="sxs-lookup"><span data-stu-id="eb676-350">6705 (0x1A31)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-351">Выполнение запрошенной операции слишком поздно, так как транзакция уже была зафиксирована.</span><span class="sxs-lookup"><span data-stu-id="eb676-351">It is too late to perform the requested operation, since the Transaction has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**Ошибка \_ \_ при инициализации \_ TM**</span><span class="sxs-lookup"><span data-stu-id="eb676-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR\_TM\_INITIALIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-353">6706 (0x1A32)</span><span class="sxs-lookup"><span data-stu-id="eb676-353">6706 (0x1A32)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-354">Не удалось успешно инициализировать диспетчер транзакций.</span><span class="sxs-lookup"><span data-stu-id="eb676-354">The Transaction Manager was unable to be successfully initialized.</span></span> <span data-ttu-id="eb676-355">Транзакционные операции не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="eb676-355">Transacted operations are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ОШИБКИ \_ RESOURCEMANAGER \_ только для чтения \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR\_RESOURCEMANAGER\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-357">6707 (0x1A33)</span><span class="sxs-lookup"><span data-stu-id="eb676-357">6707 (0x1A33)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-358">Указанный ResourceManager не внес изменений или обновлений в ресурс в этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-358">The specified ResourceManager made no changes or updates to the resource under this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ОШИБОЧная \_ транзакция \_ не \_ присоединена**</span><span class="sxs-lookup"><span data-stu-id="eb676-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR\_TRANSACTION\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-360">6708 (0x1A34)</span><span class="sxs-lookup"><span data-stu-id="eb676-360">6708 (0x1A34)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-361">Диспетчер ресурсов попытался подготовить транзакцию, которая не была успешно присоединена.</span><span class="sxs-lookup"><span data-stu-id="eb676-361">The resource manager has attempted to prepare a transaction that it has not successfully joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**Существует некоторая транзакция с ошибкой \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR\_TRANSACTION\_SUPERIOR\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-363">6709 (0x1A35)</span><span class="sxs-lookup"><span data-stu-id="eb676-363">6709 (0x1A35)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-364">Объект транзакции уже имеет старший зачисление, и вызывающая сторона попыталась выполнить операцию, которая создала новый старший.</span><span class="sxs-lookup"><span data-stu-id="eb676-364">The Transaction object already has a superior enlistment, and the caller attempted an operation that would have created a new superior.</span></span> <span data-ttu-id="eb676-365">Разрешается только один старший связующий элемент.</span><span class="sxs-lookup"><span data-stu-id="eb676-365">Only a single superior enlistment is allow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**Ошибка \_ \_ протокол CRM \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="eb676-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR\_CRM\_PROTOCOL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-367">6710 (0x1A36)</span><span class="sxs-lookup"><span data-stu-id="eb676-367">6710 (0x1A36)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-368">Диспетчер ресурсов попытался зарегистрировать уже существующий протокол.</span><span class="sxs-lookup"><span data-stu-id="eb676-368">The RM tried to register a protocol that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**Ошибка \_ \_ при распространении \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR\_TRANSACTION\_PROPAGATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-370">6711 (0x1A37)</span><span class="sxs-lookup"><span data-stu-id="eb676-370">6711 (0x1A37)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-371">Сбой при попытке распространения транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-371">The attempt to propagate the Transaction failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**Ошибка \_ \_ \_ не \_ найдена протокол CRM**</span><span class="sxs-lookup"><span data-stu-id="eb676-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR\_CRM\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-373">6712 (0x1A38)</span><span class="sxs-lookup"><span data-stu-id="eb676-373">6712 (0x1A38)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-374">Запрошенный протокол распространения не зарегистрирован в качестве CRM.</span><span class="sxs-lookup"><span data-stu-id="eb676-374">The requested propagation protocol was not registered as a CRM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**\_Недопустимый Сбой транзакции \_ Маршалловы в \_ \_ буфере**</span><span class="sxs-lookup"><span data-stu-id="eb676-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR\_TRANSACTION\_INVALID\_MARSHALL\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-376">6713 (0x1A39)</span><span class="sxs-lookup"><span data-stu-id="eb676-376">6713 (0x1A39)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-377">Буфер, переданный в Пуштрансактион или Пуллтрансактион, имеет недопустимый формат.</span><span class="sxs-lookup"><span data-stu-id="eb676-377">The buffer passed in to PushTransaction or PullTransaction is not in a valid format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**Ошибка \_ \_ \_ \_ недопустимой текущей транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR\_CURRENT\_TRANSACTION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-379">6714 (0x1A3A)</span><span class="sxs-lookup"><span data-stu-id="eb676-379">6714 (0x1A3A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-380">Текущий контекст транзакции, связанный с потоком, не является допустимым маркером для объекта транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-380">The current transaction context associated with the thread is not a valid handle to a transaction object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_ \_ не \_ удалось найти ТРАНЗАКЦИю с ошибками**</span><span class="sxs-lookup"><span data-stu-id="eb676-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**ERROR\_TRANSACTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-382">6715 (0x1A3B)</span><span class="sxs-lookup"><span data-stu-id="eb676-382">6715 (0x1A3B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-383">Не удалось открыть указанный объект транзакции, так как он не найден.</span><span class="sxs-lookup"><span data-stu-id="eb676-383">The specified Transaction object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**\_ \_ не \_ удалось найти RESOURCEMANAGER "ошибка"**</span><span class="sxs-lookup"><span data-stu-id="eb676-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR\_RESOURCEMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-385">6716 (0x1A3C)</span><span class="sxs-lookup"><span data-stu-id="eb676-385">6716 (0x1A3C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-386">Не удалось открыть указанный объект ResourceManager, так как он не найден.</span><span class="sxs-lookup"><span data-stu-id="eb676-386">The specified ResourceManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ не удалось найти зачисление ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR\_ENLISTMENT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-388">6717 (0x1A3D)</span><span class="sxs-lookup"><span data-stu-id="eb676-388">6717 (0x1A3D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-389">Не удалось открыть указанный объект зачислений, поскольку он не найден.</span><span class="sxs-lookup"><span data-stu-id="eb676-389">The specified Enlistment object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**Ошибка \_ диспетчеров транзакций \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="eb676-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-391">6718 (0x1A3E)</span><span class="sxs-lookup"><span data-stu-id="eb676-391">6718 (0x1A3E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-392">Не удалось открыть указанный объект диспетчер транзакций, так как он не найден.</span><span class="sxs-lookup"><span data-stu-id="eb676-392">The specified TransactionManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**Ошибка \_ диспетчеров транзакций \_ не в \_ сети**</span><span class="sxs-lookup"><span data-stu-id="eb676-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-394">6719 (0x1A3F)</span><span class="sxs-lookup"><span data-stu-id="eb676-394">6719 (0x1A3F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-395">Не удалось создать или открыть указанный объект, так как связанный с ним диспетчер транзакций не находится в режиме "в сети".</span><span class="sxs-lookup"><span data-stu-id="eb676-395">The object specified could not be created or opened, because its associated TransactionManager is not online.</span></span> <span data-ttu-id="eb676-396">Диспетчер транзакций должен быть полностью подключен к сети путем вызова Рековертрансактионманажер для восстановления до конца своего файла журнала, прежде чем можно будет открыть объекты в его транзакциях или пространствах имен ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="eb676-396">The TransactionManager must be brought fully Online by calling RecoverTransactionManager to recover to the end of its LogFile before objects in its Transaction or ResourceManager namespaces can be opened.</span></span> <span data-ttu-id="eb676-397">Кроме того, ошибки при записи в файл журнала могут привести к тому, что диспетчер транзакций перейдет в режим «вне сети».</span><span class="sxs-lookup"><span data-stu-id="eb676-397">In addition, errors in writing records to its LogFile can cause a TransactionManager to go offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**Ошибка \_ при \_ \_ конфликте имен при восстановлении транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR\_TRANSACTIONMANAGER\_RECOVERY\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-399">6720 (0x1A40)</span><span class="sxs-lookup"><span data-stu-id="eb676-399">6720 (0x1A40)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-400">Указанному диспетчеру транзакций не удалось создать объекты, содержащиеся в его файле журнала, в пространстве имен OB.</span><span class="sxs-lookup"><span data-stu-id="eb676-400">The specified TransactionManager was unable to create the objects contained in its logfile in the Ob namespace.</span></span> <span data-ttu-id="eb676-401">Поэтому диспетчеру транзакций не удалось выполнить восстановление.</span><span class="sxs-lookup"><span data-stu-id="eb676-401">Therefore, the TransactionManager was unable to recover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**Ошибка \_ \_ не является \_ корневой транзакцией**</span><span class="sxs-lookup"><span data-stu-id="eb676-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR\_TRANSACTION\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-403">6721 (0x1A41)</span><span class="sxs-lookup"><span data-stu-id="eb676-403">6721 (0x1A41)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-404">Не удалось завершить вызов для создания старшего прикрепления для этого объекта транзакции, так как объект транзакции, указанный для прикрепления, является подчиненной ветвью транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-404">The call to create a superior Enlistment on this Transaction object could not be completed, because the Transaction object specified for the enlistment is a subordinate branch of the Transaction.</span></span> <span data-ttu-id="eb676-405">Только корень транзакции можно прикрепить в качестве руководителя.</span><span class="sxs-lookup"><span data-stu-id="eb676-405">Only the root of the Transaction can be enlisted on as a superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**\_ \_ срок действия объекта транзакции с ошибкой \_ истек**</span><span class="sxs-lookup"><span data-stu-id="eb676-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR\_TRANSACTION\_OBJECT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-407">6722 (0x1A42)</span><span class="sxs-lookup"><span data-stu-id="eb676-407">6722 (0x1A42)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-408">Так как связанный диспетчер транзакций или диспетчер ресурсов был закрыт, этот маркер больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="eb676-408">Because the associated transaction manager or resource manager has been closed, the handle is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ОШИБОЧный \_ ответ на транзакцию \_ \_ не \_ прикреплен**</span><span class="sxs-lookup"><span data-stu-id="eb676-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR\_TRANSACTION\_RESPONSE\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-410">6723 (0x1A43)</span><span class="sxs-lookup"><span data-stu-id="eb676-410">6723 (0x1A43)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-411">Указанная операция не может быть выполнена для этого старшего прикрепления, так как зачисление не было создано с соответствующим ответом завершения в Нотификатионмаск.</span><span class="sxs-lookup"><span data-stu-id="eb676-411">The specified operation could not be performed on this Superior enlistment, because the enlistment was not created with the corresponding completion response in the NotificationMask.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**\_ \_ \_ слишком \_ длинная запись транзакции с ошибкой**</span><span class="sxs-lookup"><span data-stu-id="eb676-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**ERROR\_TRANSACTION\_RECORD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-413">6724 (0x1A44)</span><span class="sxs-lookup"><span data-stu-id="eb676-413">6724 (0x1A44)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-414">Не удалось выполнить указанную операцию, так как запись, которая была записана в журнал, слишком длинная.</span><span class="sxs-lookup"><span data-stu-id="eb676-414">The specified operation could not be performed, because the record that would be logged was too long.</span></span> <span data-ttu-id="eb676-415">Это может произойти из-за двух условий: слишком много зачислений в этой транзакции или объединенный Рековеринформатион, регистрируемый от имени этих зачислений, слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="eb676-415">This can occur because of two conditions: either there are too many Enlistments on this Transaction, or the combined RecoveryInformation being logged on behalf of those Enlistments is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**Ошибка \_ неявной \_ транзакции \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="eb676-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR\_IMPLICIT\_TRANSACTION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-417">6725 (0x1A45)</span><span class="sxs-lookup"><span data-stu-id="eb676-417">6725 (0x1A45)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-418">Неявная транзакция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb676-418">Implicit transaction are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**\_ \_ нарушение целостности транзакции при ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR\_TRANSACTION\_INTEGRITY\_VIOLATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-420">6726 (0x1A46)</span><span class="sxs-lookup"><span data-stu-id="eb676-420">6726 (0x1A46)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-421">Диспетчеру транзакций ядра пришлось прервать или забыть транзакцию, так как она блокировала ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="eb676-421">The kernel transaction manager had to abort or forget the transaction because it blocked forward progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**Ошибка \_ при \_ несоответствии удостоверения в диспетчере транзакций \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR\_TRANSACTIONMANAGER\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-423">6727 (0x1A47)</span><span class="sxs-lookup"><span data-stu-id="eb676-423">6727 (0x1A47)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-424">Переданное удостоверение диспетчером транзакций не соответствует записанному в файле журнала диспетчером транзакций.</span><span class="sxs-lookup"><span data-stu-id="eb676-424">The TransactionManager identity that was supplied did not match the one recorded in the TransactionManager's log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**Ошибка \_ RM \_ не может \_ быть \_ заморожена \_ для \_ моментального снимка**</span><span class="sxs-lookup"><span data-stu-id="eb676-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR\_RM\_CANNOT\_BE\_FROZEN\_FOR\_SNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-426">6728 (0x1A48)</span><span class="sxs-lookup"><span data-stu-id="eb676-426">6728 (0x1A48)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-427">Невозможно продолжить операцию создания моментального снимка, так как диспетчер ресурсов транзакций не может зафиксироваться в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="eb676-427">This snapshot operation cannot continue because a transactional resource manager cannot be frozen in its current state.</span></span> <span data-ttu-id="eb676-428">Повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="eb676-428">Please try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**\_ \_ должна \_ WRITETHROUGHся транзакция с ошибкой**</span><span class="sxs-lookup"><span data-stu-id="eb676-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR\_TRANSACTION\_MUST\_WRITETHROUGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-430">6729 (0x1A49)</span><span class="sxs-lookup"><span data-stu-id="eb676-430">6729 (0x1A49)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-431">Не удается прикрепить транзакцию к указанному Енлистментмаск, так как транзакция уже завершила этап предварительной подготовки.</span><span class="sxs-lookup"><span data-stu-id="eb676-431">The transaction cannot be enlisted on with the specified EnlistmentMask, because the transaction has already completed the PrePrepare phase.</span></span> <span data-ttu-id="eb676-432">Чтобы гарантировать правильность, ResourceManager необходимо переключиться в режим сквозной записи и прекратить кэширование данных в рамках этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-432">In order to ensure correctness, the ResourceManager must switch to a write- through mode and cease caching data within this transaction.</span></span> <span data-ttu-id="eb676-433">Прикрепление только к последующим этапам транзакций может выполняться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eb676-433">Enlisting for only subsequent transaction phases may still succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**Ошибка \_ \_ \_ нестаршая транзакция**</span><span class="sxs-lookup"><span data-stu-id="eb676-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR\_TRANSACTION\_NO\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-435">6730 (0x1A4A)</span><span class="sxs-lookup"><span data-stu-id="eb676-435">6730 (0x1A4A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-436">Транзакция не имеет старшего прикрепления.</span><span class="sxs-lookup"><span data-stu-id="eb676-436">The transaction does not have a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**\_возможна ошибка эвристического \_ повреждения \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERROR\_HEURISTIC\_DAMAGE\_POSSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-438">6731 (0x1A4B)</span><span class="sxs-lookup"><span data-stu-id="eb676-438">6731 (0x1A4B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-439">Попытка зафиксировать транзакцию завершена, но возможно, что часть дерева транзакций не была успешно зафиксирована из-за эвристики.</span><span class="sxs-lookup"><span data-stu-id="eb676-439">The attempt to commit the Transaction completed, but it is possible that some portion of the transaction tree did not commit successfully due to heuristics.</span></span> <span data-ttu-id="eb676-440">Поэтому возможно, что некоторые данные, измененные в транзакции, не зафиксированы, что приводит к несогласованности транзакций.</span><span class="sxs-lookup"><span data-stu-id="eb676-440">Therefore it is possible that some data modified in the transaction may not have committed, resulting in transactional inconsistency.</span></span> <span data-ttu-id="eb676-441">По возможности проверьте согласованность связанных данных.</span><span class="sxs-lookup"><span data-stu-id="eb676-441">If possible, check the consistency of the associated data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**Ошибка при \_ \_ КОНФЛИКТе транзакций**</span><span class="sxs-lookup"><span data-stu-id="eb676-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR\_TRANSACTIONAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-443">6800 (0x1A90)</span><span class="sxs-lookup"><span data-stu-id="eb676-443">6800 (0x1A90)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-444">Функция попыталась использовать имя, зарезервированное для использования другой транзакцией.</span><span class="sxs-lookup"><span data-stu-id="eb676-444">The function attempted to use a name that is reserved for use by another transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**Ошибка \_ RM \_ не \_ активна**</span><span class="sxs-lookup"><span data-stu-id="eb676-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR\_RM\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-446">6801 (0x1A91)</span><span class="sxs-lookup"><span data-stu-id="eb676-446">6801 (0x1A91)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-447">Поддержка транзакций в указанном диспетчере ресурсов не запущена или была завершена из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb676-447">Transaction support within the specified resource manager is not started or was shut down due to an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**\_метаданные ошибки \_ RM \_ повреждены**</span><span class="sxs-lookup"><span data-stu-id="eb676-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR\_RM\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-449">6802 (0x1A92)</span><span class="sxs-lookup"><span data-stu-id="eb676-449">6802 (0x1A92)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-450">Метаданные RM повреждены.</span><span class="sxs-lookup"><span data-stu-id="eb676-450">The metadata of the RM has been corrupted.</span></span> <span data-ttu-id="eb676-451">RM не будет работать.</span><span class="sxs-lookup"><span data-stu-id="eb676-451">The RM will not function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**\_Каталог ошибок \_ не \_ RM**</span><span class="sxs-lookup"><span data-stu-id="eb676-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR\_DIRECTORY\_NOT\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-453">6803 (0x1A93)</span><span class="sxs-lookup"><span data-stu-id="eb676-453">6803 (0x1A93)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-454">Указанный каталог не содержит Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="eb676-454">The specified directory does not contain a resource manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**Неподдерживаемые транзакции с ОШИБКАми \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**ERROR\_TRANSACTIONS\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-456">6805 (0x1A95)</span><span class="sxs-lookup"><span data-stu-id="eb676-456">6805 (0x1A95)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-457">Удаленный сервер или общая папка не поддерживает транзакционные файловые операции.</span><span class="sxs-lookup"><span data-stu-id="eb676-457">The remote server or share does not support transacted file operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**\_ \_ \_ Недопустимый размер журнала \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ERROR\_LOG\_RESIZE\_INVALID\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-459">6806 (0x1A96)</span><span class="sxs-lookup"><span data-stu-id="eb676-459">6806 (0x1A96)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-460">Запрошенный размер журнала недопустим.</span><span class="sxs-lookup"><span data-stu-id="eb676-460">The requested log size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**\_объект Error \_ \_ больше не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="eb676-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**ERROR\_OBJECT\_NO\_LONGER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-462">6807 (0x1A97)</span><span class="sxs-lookup"><span data-stu-id="eb676-462">6807 (0x1A97)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-463">Объект (файл, поток, ссылка), соответствующий этому маркеру, был удален откатом точки сохранения транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-463">The object (file, stream, link) corresponding to the handle has been deleted by a Transaction Savepoint Rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ не найдена мини – версия потока \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="eb676-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-465">6808 (0x1A98)</span><span class="sxs-lookup"><span data-stu-id="eb676-465">6808 (0x1A98)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-466">Указанная мини для файла не найдена для этого файла транзакций, открытых в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="eb676-466">The specified file miniversion was not found for this transacted file open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**\_ \_ Недопустимая мини – версия потока ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-468">6809 (0x1A99)</span><span class="sxs-lookup"><span data-stu-id="eb676-468">6809 (0x1A99)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-469">Указанная мини – версия файла найдена, но стала недействительной.</span><span class="sxs-lookup"><span data-stu-id="eb676-469">The specified file miniversion was found but has been invalidated.</span></span> <span data-ttu-id="eb676-470">Наиболее вероятной причиной является откат точки сохранения транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-470">Most likely cause is a transaction savepoint rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**Ошибка \_ мини, \_ недоступная \_ из \_ указанной \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR\_MINIVERSION\_INACCESSIBLE\_FROM\_SPECIFIED\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-472">6810 (0x1A9A)</span><span class="sxs-lookup"><span data-stu-id="eb676-472">6810 (0x1A9A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-473">Мини-версия может быть открыта только в контексте транзакции, создавшей ее.</span><span class="sxs-lookup"><span data-stu-id="eb676-473">A miniversion may only be opened in the context of the transaction that created it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ОШИБКА не \_ удается \_ Открыть мини – версию \_ \_ с \_ \_ намерением изменения**</span><span class="sxs-lookup"><span data-stu-id="eb676-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR\_CANT\_OPEN\_MINIVERSION\_WITH\_MODIFY\_INTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-475">6811 (0x1A9B)</span><span class="sxs-lookup"><span data-stu-id="eb676-475">6811 (0x1A9B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-476">Невозможно открыть мини-версию с доступом на изменение.</span><span class="sxs-lookup"><span data-stu-id="eb676-476">It is not possible to open a miniversion with modify access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ОШИБКА не \_ удается \_ создать \_ Дополнительные \_ потоковые \_ миниверсионс**</span><span class="sxs-lookup"><span data-stu-id="eb676-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR\_CANT\_CREATE\_MORE\_STREAM\_MINIVERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-478">6812 (0x1A9C)</span><span class="sxs-lookup"><span data-stu-id="eb676-478">6812 (0x1A9C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-479">Невозможно создать дополнительные миниверсионс для этого потока.</span><span class="sxs-lookup"><span data-stu-id="eb676-479">It is not possible to create any more miniversions for this stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии версии удаленного файла \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR\_REMOTE\_FILE\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-481">6814 (0x1A9E)</span><span class="sxs-lookup"><span data-stu-id="eb676-481">6814 (0x1A9E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-482">Удаленный сервер отправил несоответствующий номер версии или FID для файла, открытого с помощью транзакций.</span><span class="sxs-lookup"><span data-stu-id="eb676-482">The remote server sent mismatching version number or Fid for a file opened with transactions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**\_обработчик ошибок \_ \_ больше не \_ действителен**</span><span class="sxs-lookup"><span data-stu-id="eb676-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**ERROR\_HANDLE\_NO\_LONGER\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-484">6815 (0x1A9F)</span><span class="sxs-lookup"><span data-stu-id="eb676-484">6815 (0x1A9F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-485">Этот маркер был аннулирован транзакцией.</span><span class="sxs-lookup"><span data-stu-id="eb676-485">The handle has been invalidated by a transaction.</span></span> <span data-ttu-id="eb676-486">Наиболее вероятная причина — наличие сопоставления памяти для файла или открытого обработчика после завершения или отката транзакции до точки сохранения.</span><span class="sxs-lookup"><span data-stu-id="eb676-486">The most likely cause is the presence of memory mapping on a file or an open handle when the transaction ended or rolled back to savepoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**Ошибка \_ без \_ \_ метаданных TxF**</span><span class="sxs-lookup"><span data-stu-id="eb676-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR\_NO\_TXF\_METADATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-488">6816 (0x1AA0)</span><span class="sxs-lookup"><span data-stu-id="eb676-488">6816 (0x1AA0)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-489">В файле нет метаданных транзакций.</span><span class="sxs-lookup"><span data-stu-id="eb676-489">There is no transaction metadata on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**\_ \_ обнаружено повреждение журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**ERROR\_LOG\_CORRUPTION\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-491">6817 (0x1AA1)</span><span class="sxs-lookup"><span data-stu-id="eb676-491">6817 (0x1AA1)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-492">Данные журнала повреждены.</span><span class="sxs-lookup"><span data-stu-id="eb676-492">The log data is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**Ошибка \_ не \_ удается \_ восстановить \_ с \_ открытым маркером**</span><span class="sxs-lookup"><span data-stu-id="eb676-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR\_CANT\_RECOVER\_WITH\_HANDLE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-494">6818 (0x1AA2)</span><span class="sxs-lookup"><span data-stu-id="eb676-494">6818 (0x1AA2)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-495">Невозможно восстановить файл, так как на нем еще открыт обработчик.</span><span class="sxs-lookup"><span data-stu-id="eb676-495">The file can't be recovered because there is a handle still open on it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**Ошибка \_ RM \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="eb676-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR\_RM\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-497">6819 (0x1AA3)</span><span class="sxs-lookup"><span data-stu-id="eb676-497">6819 (0x1AA3)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-498">Результат транзакции недоступен, так как диспетчер ресурсов, ответственный за него, был отключен.</span><span class="sxs-lookup"><span data-stu-id="eb676-498">The transaction outcome is unavailable because the resource manager responsible for it has disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**\_зачисление ошибок \_ не является \_ старшим**</span><span class="sxs-lookup"><span data-stu-id="eb676-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR\_ENLISTMENT\_NOT\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-500">6820 (0x1AA4)</span><span class="sxs-lookup"><span data-stu-id="eb676-500">6820 (0x1AA4)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-501">Запрос был отклонен, так как зачисление в вопросе не является старшим прикреплением.</span><span class="sxs-lookup"><span data-stu-id="eb676-501">The request was rejected because the enlistment in question is not a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**восстановление после ошибок \_ \_ не \_ требуется**</span><span class="sxs-lookup"><span data-stu-id="eb676-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**ERROR\_RECOVERY\_NOT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-503">6821 (0x1AA5)</span><span class="sxs-lookup"><span data-stu-id="eb676-503">6821 (0x1AA5)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-504">Транзакционный диспетчер ресурсов уже согласован.</span><span class="sxs-lookup"><span data-stu-id="eb676-504">The transactional resource manager is already consistent.</span></span> <span data-ttu-id="eb676-505">Восстановление не требуется.</span><span class="sxs-lookup"><span data-stu-id="eb676-505">Recovery is not needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**Ошибка \_ RM \_ уже \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="eb676-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR\_RM\_ALREADY\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-507">6822 (0x1AA6)</span><span class="sxs-lookup"><span data-stu-id="eb676-507">6822 (0x1AA6)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-508">Диспетчер ресурсов транзакций уже запущен.</span><span class="sxs-lookup"><span data-stu-id="eb676-508">The transactional resource manager has already been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**\_ \_ неустойчивое удостоверение файла ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**ERROR\_FILE\_IDENTITY\_NOT\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-510">6823 (0x1AA7)</span><span class="sxs-lookup"><span data-stu-id="eb676-510">6823 (0x1AA7)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-511">Файл нельзя открыть транзакционно, так как его удостоверение зависит от результата неразрешенной транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-511">The file cannot be opened transactionally, because its identity depends on the outcome of an unresolved transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ОШИБКА не \_ удается \_ ПРЕрвать \_ транзакционную \_ зависимость**</span><span class="sxs-lookup"><span data-stu-id="eb676-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR\_CANT\_BREAK\_TRANSACTIONAL\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-513">6824 (0x1AA8)</span><span class="sxs-lookup"><span data-stu-id="eb676-513">6824 (0x1AA8)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-514">Невозможно выполнить операцию, поскольку другая транзакция зависит от того факта, что это свойство не изменится.</span><span class="sxs-lookup"><span data-stu-id="eb676-514">The operation cannot be performed because another transaction is depending on the fact that this property will not change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ОШИБКА не \_ удается \_ перекрестно \_ \_ границы RM**</span><span class="sxs-lookup"><span data-stu-id="eb676-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR\_CANT\_CROSS\_RM\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-516">6825 (0x1AA9)</span><span class="sxs-lookup"><span data-stu-id="eb676-516">6825 (0x1AA9)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-517">Операция будет затрагивать один файл с двумя диспетчерами ресурсов транзакций и, следовательно, не будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="eb676-517">The operation would involve a single file with two transactional resource managers and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**Ошибка \_ TxF \_ dir \_ не \_ пуста**</span><span class="sxs-lookup"><span data-stu-id="eb676-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR\_TXF\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-519">6826 (0x1AAA)</span><span class="sxs-lookup"><span data-stu-id="eb676-519">6826 (0x1AAA)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-520">Для выполнения этой операции каталог $Txf должен быть пустым.</span><span class="sxs-lookup"><span data-stu-id="eb676-520">The $Txf directory must be empty for this operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_нет проблем с НЕсомнительными \_ транзакциями \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERROR\_INDOUBT\_TRANSACTIONS\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-522">6827 (0x1AAB)</span><span class="sxs-lookup"><span data-stu-id="eb676-522">6827 (0x1AAB)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-523">Операция оставляет диспетчер ресурсов транзакций в несогласованном состоянии и, следовательно, не разрешается.</span><span class="sxs-lookup"><span data-stu-id="eb676-523">The operation would leave a transactional resource manager in an inconsistent state and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**Ошибка \_ TM \_ volatile**</span><span class="sxs-lookup"><span data-stu-id="eb676-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR\_TM\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-525">6828 (0x1AAC)</span><span class="sxs-lookup"><span data-stu-id="eb676-525">6828 (0x1AAC)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-526">Не удалось выполнить операцию, так как диспетчер транзакций не имеет журнала.</span><span class="sxs-lookup"><span data-stu-id="eb676-526">The operation could not be completed because the transaction manager does not have a log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**\_ \_ срок действия таймера отката ошибки \_ истек**</span><span class="sxs-lookup"><span data-stu-id="eb676-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR\_ROLLBACK\_TIMER\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-528">6829 (0x1AAD)</span><span class="sxs-lookup"><span data-stu-id="eb676-528">6829 (0x1AAD)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-529">Не удалось запланировать откат, так как ранее запланированный откат уже выполнен или поставлен в очередь на выполнение.</span><span class="sxs-lookup"><span data-stu-id="eb676-529">A rollback could not be scheduled because a previously scheduled rollback has already executed or been queued for execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**Ошибка \_ при \_ \_ повреждении атрибута TxF**</span><span class="sxs-lookup"><span data-stu-id="eb676-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR\_TXF\_ATTRIBUTE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-531">6830 (0x1AAE)</span><span class="sxs-lookup"><span data-stu-id="eb676-531">6830 (0x1AAE)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-532">Атрибут метаданных транзакций для файла или каталога поврежден и недоступен для чтения.</span><span class="sxs-lookup"><span data-stu-id="eb676-532">The transactional metadata attribute on the file or directory is corrupt and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**Ошибка \_ EFS \_ не \_ разрешена \_ в \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR\_EFS\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-534">6831 (0x1AAF)</span><span class="sxs-lookup"><span data-stu-id="eb676-534">6831 (0x1AAF)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-535">Не удалось выполнить операцию шифрования, так как транзакция активна.</span><span class="sxs-lookup"><span data-stu-id="eb676-535">The encryption operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**Ошибка при \_ открытии транзакции \_ \_ \_ запрещено**</span><span class="sxs-lookup"><span data-stu-id="eb676-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR\_TRANSACTIONAL\_OPEN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-537">6832 (0x1AB0)</span><span class="sxs-lookup"><span data-stu-id="eb676-537">6832 (0x1AB0)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-538">Этот объект не может быть открыт в транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-538">This object is not allowed to be opened in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**\_ \_ сбой при росте журнала ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR\_LOG\_GROWTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-540">6833 (0x1AB1)</span><span class="sxs-lookup"><span data-stu-id="eb676-540">6833 (0x1AB1)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-541">Сбой при создании пространства в журнале диспетчера ресурсов транзакций.</span><span class="sxs-lookup"><span data-stu-id="eb676-541">An attempt to create space in the transactional resource manager's log failed.</span></span> <span data-ttu-id="eb676-542">Состояние сбоя записано в журнал событий.</span><span class="sxs-lookup"><span data-stu-id="eb676-542">The failure status has been recorded in the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**Ошибка при \_ \_ сопоставлении \_ неподдерживаемой удаленной транзакции сопоставления \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR\_TRANSACTED\_MAPPING\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-544">6834 (0x1AB2)</span><span class="sxs-lookup"><span data-stu-id="eb676-544">6834 (0x1AB2)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-545">Сопоставление памяти (создание сопоставленного раздела) удаленный файл в транзакции не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb676-545">Memory mapping (creating a mapped section) a remote file under a transaction is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**Ошибка \_ \_ \_ уже имеется метаданные \_ TxF**</span><span class="sxs-lookup"><span data-stu-id="eb676-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR\_TXF\_METADATA\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-547">6835 (0x1AB3)</span><span class="sxs-lookup"><span data-stu-id="eb676-547">6835 (0x1AB3)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-548">Метаданные транзакции уже существуют в этом файле и не могут быть заменены.</span><span class="sxs-lookup"><span data-stu-id="eb676-548">Transaction metadata is already present on this file and cannot be superseded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**\_ \_ \_ \_ не заданы обратные вызовы области транзакций с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR\_TRANSACTION\_SCOPE\_CALLBACKS\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-550">6836 (0x1AB4)</span><span class="sxs-lookup"><span data-stu-id="eb676-550">6836 (0x1AB4)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-551">Не удалось указать область транзакции, так как обработчик области не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="eb676-551">A transaction scope could not be entered because the scope handler has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_ \_ требуется \_ специальное продвижение для транзакции с ошибками**</span><span class="sxs-lookup"><span data-stu-id="eb676-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR\_TRANSACTION\_REQUIRED\_PROMOTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-553">6837 (0x1AB5)</span><span class="sxs-lookup"><span data-stu-id="eb676-553">6837 (0x1AB5)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-554">Требуется продвижение, чтобы разрешить диспетчеру ресурсов прикрепить, но для транзакции было задано значение "запретить".</span><span class="sxs-lookup"><span data-stu-id="eb676-554">Promotion was required in order to allow the resource manager to enlist, but the transaction was set to disallow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**Ошибка \_ не может \_ выполнить \_ файл \_ в \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR\_CANNOT\_EXECUTE\_FILE\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-556">6838 (0x1AB6)</span><span class="sxs-lookup"><span data-stu-id="eb676-556">6838 (0x1AB6)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-557">Этот файл открыт для изменения в неразрешенной транзакции и может быть открыт для выполнения только транзакционным агентом чтения.</span><span class="sxs-lookup"><span data-stu-id="eb676-557">This file is open for modification in an unresolved transaction and may be opened for execute only by a transacted reader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ОШИБОЧные \_ транзакции \_ не \_ заморожены**</span><span class="sxs-lookup"><span data-stu-id="eb676-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ERROR\_TRANSACTIONS\_NOT\_FROZEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-559">6839 (0x1AB7)</span><span class="sxs-lookup"><span data-stu-id="eb676-559">6839 (0x1AB7)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-560">Запрос на разморозку замороженных транзакций был проигнорирован, так как транзакции ранее не были заморожены.</span><span class="sxs-lookup"><span data-stu-id="eb676-560">The request to thaw frozen transactions was ignored because transactions had not previously been frozen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**\_ \_ выполняется замораживание транзакций \_ с \_ ошибками**</span><span class="sxs-lookup"><span data-stu-id="eb676-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR\_TRANSACTION\_FREEZE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-562">6840 (0x1AB8)</span><span class="sxs-lookup"><span data-stu-id="eb676-562">6840 (0x1AB8)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-563">Транзакции нельзя зафиксировать, так как уже выполняется заморозка.</span><span class="sxs-lookup"><span data-stu-id="eb676-563">Transactions cannot be frozen because a freeze is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**Ошибка \_ не является \_ томом моментальных снимков \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR\_NOT\_SNAPSHOT\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-565">6841 (0x1AB9)</span><span class="sxs-lookup"><span data-stu-id="eb676-565">6841 (0x1AB9)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-566">Целевой том не является томом моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="eb676-566">The target volume is not a snapshot volume.</span></span> <span data-ttu-id="eb676-567">Эта операция допустима только для тома, подключенного в качестве моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="eb676-567">This operation is only valid on a volume mounted as a snapshot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**не обнаружена \_ \_ точка сохранения \_ с \_ открытыми \_ файлами**</span><span class="sxs-lookup"><span data-stu-id="eb676-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR\_NO\_SAVEPOINT\_WITH\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-569">6842 (0x1ABA)</span><span class="sxs-lookup"><span data-stu-id="eb676-569">6842 (0x1ABA)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-570">Не удалось выполнить операцию точки сохранения, так как файлы открыты в транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-570">The savepoint operation failed because files are open on the transaction.</span></span> <span data-ttu-id="eb676-571">Это не разрешено.</span><span class="sxs-lookup"><span data-stu-id="eb676-571">This is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**\_ \_ Восстановление потерянных данных об ошибках \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERROR\_DATA\_LOST\_REPAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-573">6843 (0x1ABB)</span><span class="sxs-lookup"><span data-stu-id="eb676-573">6843 (0x1ABB)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-574">Windows обнаружила повреждение в файле, и этот файл был восстановлен.</span><span class="sxs-lookup"><span data-stu-id="eb676-574">Windows has discovered corruption in a file, and that file has since been repaired.</span></span> <span data-ttu-id="eb676-575">Возможно, произошла потери данных.</span><span class="sxs-lookup"><span data-stu-id="eb676-575">Data loss may have occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**\_ \_ \_ \_ в транзакции не РАЗРЕШЕНо разреженных ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR\_SPARSE\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-577">6844 (0x1ABC)</span><span class="sxs-lookup"><span data-stu-id="eb676-577">6844 (0x1ABC)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-578">Не удалось выполнить операцию разрежения, так как в файле активна транзакция.</span><span class="sxs-lookup"><span data-stu-id="eb676-578">The sparse operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**Ошибка \_ с \_ \_ несоответствием удостоверений TM**</span><span class="sxs-lookup"><span data-stu-id="eb676-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR\_TM\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-580">6845 (0x1ABD)</span><span class="sxs-lookup"><span data-stu-id="eb676-580">6845 (0x1ABD)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-581">Не удалось вызвать для создания объекта диспетчер транзакций, так как удостоверение TM, хранящееся в файле журнала, не совпадает с удостоверением TM, переданным в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="eb676-581">The call to create a TransactionManager object failed because the Tm Identity stored in the logfile does not match the Tm Identity that was passed in as an argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**Ошибка в \_ разделе с плавающей ошибкой \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR\_FLOATED\_SECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-583">6846 (0x1ABE)</span><span class="sxs-lookup"><span data-stu-id="eb676-583">6846 (0x1ABE)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-584">Предпринята попытка ввода-вывода для объекта раздела, который был перемещен в результате завершения транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-584">I/O was attempted on a section object that has been floated as a result of a transaction ending.</span></span> <span data-ttu-id="eb676-585">Нет допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="eb676-585">There is no valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**Ошибка \_ не может \_ принять \_ транзакционную \_ работу**</span><span class="sxs-lookup"><span data-stu-id="eb676-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR\_CANNOT\_ACCEPT\_TRANSACTED\_WORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-587">6847 (0x1ABF)</span><span class="sxs-lookup"><span data-stu-id="eb676-587">6847 (0x1ABF)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-588">Диспетчер ресурсов транзакций в настоящее время не может принять транзакционную работу из-за временной ситуации, такой как нехватка ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb676-588">The transactional resource manager cannot currently accept transacted work due to a transient condition such as low resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**Ошибка \_ не может \_ прерывать \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR\_CANNOT\_ABORT\_TRANSACTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-590">6848 (0x1AC0)</span><span class="sxs-lookup"><span data-stu-id="eb676-590">6848 (0x1AC0)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-591">Диспетчер ресурсов транзакций имел слишком много транактионсных невыполненных запросов, которые не удалось прервать.</span><span class="sxs-lookup"><span data-stu-id="eb676-591">The transactional resource manager had too many tranactions outstanding that could not be aborted.</span></span> <span data-ttu-id="eb676-592">Работа диспетчера ресурсов транзакций завершена.</span><span class="sxs-lookup"><span data-stu-id="eb676-592">The transactional resource manger has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ОШИБКИ \_ поврежденных \_ кластеров**</span><span class="sxs-lookup"><span data-stu-id="eb676-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR\_BAD\_CLUSTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-594">6849 (0x1AC1)</span><span class="sxs-lookup"><span data-stu-id="eb676-594">6849 (0x1AC1)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-595">Не удалось выполнить операцию из-за поврежденных кластеров на диске.</span><span class="sxs-lookup"><span data-stu-id="eb676-595">The operation could not be completed due to bad clusters on disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_Сжатие ошибок \_ не \_ разрешено \_ в \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**ERROR\_COMPRESSION\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-597">6850 (0x1AC2)</span><span class="sxs-lookup"><span data-stu-id="eb676-597">6850 (0x1AC2)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-598">Не удалось выполнить операцию сжатия, так как в файле активна транзакция.</span><span class="sxs-lookup"><span data-stu-id="eb676-598">The compression operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**Ошибка \_ \_ "грязный том"**</span><span class="sxs-lookup"><span data-stu-id="eb676-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR\_VOLUME\_DIRTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-600">6851 (0x1AC3)</span><span class="sxs-lookup"><span data-stu-id="eb676-600">6851 (0x1AC3)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-601">Не удалось выполнить операцию, так как том изменен.</span><span class="sxs-lookup"><span data-stu-id="eb676-601">The operation could not be completed because the volume is dirty.</span></span> <span data-ttu-id="eb676-602">Запустите Chkdsk и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="eb676-602">Please run chkdsk and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**Ошибка \_ \_ \_ при отслеживании ссылок \_ в \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR\_NO\_LINK\_TRACKING\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-604">6852 (0x1AC4)</span><span class="sxs-lookup"><span data-stu-id="eb676-604">6852 (0x1AC4)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-605">Не удалось выполнить операцию отслеживания ссылок, так как транзакция активна.</span><span class="sxs-lookup"><span data-stu-id="eb676-605">The link tracking operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_операция \_ с ошибкой не \_ поддерживается \_ в \_ транзакции**</span><span class="sxs-lookup"><span data-stu-id="eb676-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**ERROR\_OPERATION\_NOT\_SUPPORTED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-607">6853 (0x1AC5)</span><span class="sxs-lookup"><span data-stu-id="eb676-607">6853 (0x1AC5)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-608">Эта операция не может быть выполнена в транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-608">This operation cannot be performed in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**\_маркер с истекшим сроком действия \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR\_EXPIRED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-610">6854 (0x1AC6)</span><span class="sxs-lookup"><span data-stu-id="eb676-610">6854 (0x1AC6)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-611">Этот маркер больше не связан с его транзакцией.</span><span class="sxs-lookup"><span data-stu-id="eb676-611">The handle is no longer properly associated with its transaction.</span></span> <span data-ttu-id="eb676-612">Возможно, он был открыт в транзакционном диспетчере ресурсов, который затем был принудительно перезапущен.</span><span class="sxs-lookup"><span data-stu-id="eb676-612">It may have been opened in a transactional resource manager that was subsequently forced to restart.</span></span> <span data-ttu-id="eb676-613">Закройте этот обработчик и откройте новый.</span><span class="sxs-lookup"><span data-stu-id="eb676-613">Please close the handle and open a new one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ОШИБОЧная \_ транзакция \_ не \_ прикреплена**</span><span class="sxs-lookup"><span data-stu-id="eb676-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR\_TRANSACTION\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-615">6855 (0x1AC7)</span><span class="sxs-lookup"><span data-stu-id="eb676-615">6855 (0x1AC7)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-616">Не удалось выполнить указанную операцию, так как диспетчер ресурсов не прикреплен к транзакции.</span><span class="sxs-lookup"><span data-stu-id="eb676-616">The specified operation could not be performed because the resource manager is not enlisted in the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**Ошибка \_ CTX \_ \_ \_ недопустимое имя винстатион**</span><span class="sxs-lookup"><span data-stu-id="eb676-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR\_CTX\_WINSTATION\_NAME\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-618">7001 (0x1B59)</span><span class="sxs-lookup"><span data-stu-id="eb676-618">7001 (0x1B59)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-619">Указано недопустимое имя сеанса.</span><span class="sxs-lookup"><span data-stu-id="eb676-619">The specified session name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**Ошибка \_ CTX \_ недопустимых \_ PD**</span><span class="sxs-lookup"><span data-stu-id="eb676-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR\_CTX\_INVALID\_PD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-621">7002 (0x1B5A)</span><span class="sxs-lookup"><span data-stu-id="eb676-621">7002 (0x1B5A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-622">Указан недопустимый драйвер протокола.</span><span class="sxs-lookup"><span data-stu-id="eb676-622">The specified protocol driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**Ошибка \_ CTX \_ PD \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="eb676-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR\_CTX\_PD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-624">7003 (0x1B5B)</span><span class="sxs-lookup"><span data-stu-id="eb676-624">7003 (0x1B5B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-625">Указанный драйвер протокола не найден в системном пути.</span><span class="sxs-lookup"><span data-stu-id="eb676-625">The specified protocol driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**Ошибка \_ CTX \_ WD \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="eb676-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR\_CTX\_WD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-627">7004 (0x1B5C)</span><span class="sxs-lookup"><span data-stu-id="eb676-627">7004 (0x1B5C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-628">Указанный драйвер подключения терминала не найден в системном пути.</span><span class="sxs-lookup"><span data-stu-id="eb676-628">The specified terminal connection driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**Ошибка \_ CTX. \_ не удается \_ создать \_ запись в журнале событий \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR\_CTX\_CANNOT\_MAKE\_EVENTLOG\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-630">7005 (0x1B5D)</span><span class="sxs-lookup"><span data-stu-id="eb676-630">7005 (0x1B5D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-631">Не удалось создать раздел реестра для ведения журнала событий для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="eb676-631">A registry key for event logging could not be created for this session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**Ошибка \_ CTX \_ \_ конфликт имен \_ служб**</span><span class="sxs-lookup"><span data-stu-id="eb676-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR\_CTX\_SERVICE\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-633">7006 (0x1B5E)</span><span class="sxs-lookup"><span data-stu-id="eb676-633">7006 (0x1B5E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-634">Служба с таким именем уже существует в системе.</span><span class="sxs-lookup"><span data-stu-id="eb676-634">A service with the same name already exists on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**Ошибка \_ CTX \_ \_ Ожидание закрытия**</span><span class="sxs-lookup"><span data-stu-id="eb676-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR\_CTX\_CLOSE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-636">7007 (0x1B5F)</span><span class="sxs-lookup"><span data-stu-id="eb676-636">7007 (0x1B5F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-637">В сеансе ожидается операция закрытия.</span><span class="sxs-lookup"><span data-stu-id="eb676-637">A close operation is pending on the session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**Ошибка \_ CTX \_ No \_ аутбуф**</span><span class="sxs-lookup"><span data-stu-id="eb676-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR\_CTX\_NO\_OUTBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-639">7008 (0x1B60)</span><span class="sxs-lookup"><span data-stu-id="eb676-639">7008 (0x1B60)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-640">Свободные буферы вывода недоступны.</span><span class="sxs-lookup"><span data-stu-id="eb676-640">There are no free output buffers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**Ошибка \_ CTX \_ . \_ \_ не \_ найден INF-файл модема**</span><span class="sxs-lookup"><span data-stu-id="eb676-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR\_CTX\_MODEM\_INF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-642">7009 (0x1B61)</span><span class="sxs-lookup"><span data-stu-id="eb676-642">7009 (0x1B61)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-643">МОДЕМ. INF-файл не найден.</span><span class="sxs-lookup"><span data-stu-id="eb676-643">The MODEM.INF file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**Ошибка \_ CTX \_ Недопустимая \_ модемнаме**</span><span class="sxs-lookup"><span data-stu-id="eb676-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR\_CTX\_INVALID\_MODEMNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-645">7010 (0x1B62)</span><span class="sxs-lookup"><span data-stu-id="eb676-645">7010 (0x1B62)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-646">Имя модема не найдено в файле MODEM. INF.</span><span class="sxs-lookup"><span data-stu-id="eb676-646">The modem name was not found in MODEM.INF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**Ошибка \_ при \_ \_ отклике модема CTX \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-648">7011 (0x1B63)</span><span class="sxs-lookup"><span data-stu-id="eb676-648">7011 (0x1B63)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-649">Модем не принял отправленную ему команду.</span><span class="sxs-lookup"><span data-stu-id="eb676-649">The modem did not accept the command sent to it.</span></span> <span data-ttu-id="eb676-650">Убедитесь, что имя настроенного модема соответствует подключенному модему.</span><span class="sxs-lookup"><span data-stu-id="eb676-650">Verify that the configured modem name matches the attached modem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**Ошибка \_ CTX \_ \_ время ожидания ответа модема \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-652">7012 (0x1B64)</span><span class="sxs-lookup"><span data-stu-id="eb676-652">7012 (0x1B64)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-653">Модем не ответил на отправленную ему команду.</span><span class="sxs-lookup"><span data-stu-id="eb676-653">The modem did not respond to the command sent to it.</span></span> <span data-ttu-id="eb676-654">Убедитесь, что модем правильно подключен и включен.</span><span class="sxs-lookup"><span data-stu-id="eb676-654">Verify that the modem is properly cabled and powered on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**Ошибка \_ CTX \_ ответа модема \_ \_ нет \_ несущей**</span><span class="sxs-lookup"><span data-stu-id="eb676-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_CARRIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-656">7013 (0x1B65)</span><span class="sxs-lookup"><span data-stu-id="eb676-656">7013 (0x1B65)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-657">Произошла ошибка обнаружения несущей или она была удалена из-за отключения.</span><span class="sxs-lookup"><span data-stu-id="eb676-657">Carrier detect has failed or carrier has been dropped due to disconnect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**Ошибка \_ , \_ CTX \_ ответ модема \_ No \_ диалтоне**</span><span class="sxs-lookup"><span data-stu-id="eb676-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-659">7014 (0x1B66)</span><span class="sxs-lookup"><span data-stu-id="eb676-659">7014 (0x1B66)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-660">Гудок не обнаружен в течение необходимого времени.</span><span class="sxs-lookup"><span data-stu-id="eb676-660">Dial tone not detected within the required time.</span></span> <span data-ttu-id="eb676-661">Убедитесь, что телефонный кабель правильно подключен и работает.</span><span class="sxs-lookup"><span data-stu-id="eb676-661">Verify that the phone cable is properly attached and functional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**Ошибка \_ ctx, что \_ ответ модема \_ \_ занят**</span><span class="sxs-lookup"><span data-stu-id="eb676-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-663">7015 (0x1B67)</span><span class="sxs-lookup"><span data-stu-id="eb676-663">7015 (0x1B67)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-664">Сигнал занятости обнаружен на удаленном веб-сайте при обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="eb676-664">Busy signal detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**Ошибка \_ CTX \_ ответа модема \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-666">7016 (0x1B68)</span><span class="sxs-lookup"><span data-stu-id="eb676-666">7016 (0x1B68)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-667">Речь обнаружено на удаленном веб-сайте при обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="eb676-667">Voice detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**Ошибка \_ CTX \_ TD \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR\_CTX\_TD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-669">7017 (0x1B69)</span><span class="sxs-lookup"><span data-stu-id="eb676-669">7017 (0x1B69)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-670">Ошибка драйвера транспорта.</span><span class="sxs-lookup"><span data-stu-id="eb676-670">Transport driver error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**Ошибка \_ CTX \_ винстатион \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="eb676-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR\_CTX\_WINSTATION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-672">7022 (0x1B6E)</span><span class="sxs-lookup"><span data-stu-id="eb676-672">7022 (0x1B6E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-673">Не удается найти указанный сеанс.</span><span class="sxs-lookup"><span data-stu-id="eb676-673">The specified session cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**Ошибка \_ CTX \_ винстатион \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="eb676-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR\_CTX\_WINSTATION\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-675">7023 (0x1B6F)</span><span class="sxs-lookup"><span data-stu-id="eb676-675">7023 (0x1B6F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-676">Указанное имя сеанса уже используется.</span><span class="sxs-lookup"><span data-stu-id="eb676-676">The specified session name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**Ошибка \_ CTX \_ винстатион \_ Busy**</span><span class="sxs-lookup"><span data-stu-id="eb676-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR\_CTX\_WINSTATION\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-678">7024 (0x1B70)</span><span class="sxs-lookup"><span data-stu-id="eb676-678">7024 (0x1B70)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-679">Задача, которую вы пытаетесь выполнить, не может быть завершена, так как службы удаленных рабочих столов в данный момент занят.</span><span class="sxs-lookup"><span data-stu-id="eb676-679">The task you are trying to do can't be completed because Remote Desktop Services is currently busy.</span></span> <span data-ttu-id="eb676-680">Повторите попытку через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="eb676-680">Please try again in a few minutes.</span></span> <span data-ttu-id="eb676-681">Другие пользователи по-прежнему должны иметь возможность войти в систему.</span><span class="sxs-lookup"><span data-stu-id="eb676-681">Other users should still be able to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**Ошибка \_ CTXного \_ \_ \_ видеорежима**</span><span class="sxs-lookup"><span data-stu-id="eb676-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR\_CTX\_BAD\_VIDEO\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-683">7025 (0x1B71)</span><span class="sxs-lookup"><span data-stu-id="eb676-683">7025 (0x1B71)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-684">Предпринята попытка подключения к сеансу, видео режим которого не поддерживается текущим клиентом.</span><span class="sxs-lookup"><span data-stu-id="eb676-684">An attempt has been made to connect to a session whose video mode is not supported by the current client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**Ошибка \_ CTX \_ графика \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR\_CTX\_GRAPHICS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-686">7035 (0x1B7B)</span><span class="sxs-lookup"><span data-stu-id="eb676-686">7035 (0x1B7B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-687">Приложение попыталось включить графический режим DOS.</span><span class="sxs-lookup"><span data-stu-id="eb676-687">The application attempted to enable DOS graphics mode.</span></span> <span data-ttu-id="eb676-688">Графический режим DOS не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb676-688">DOS graphics mode is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**Ошибка \_ CTX \_ входа \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="eb676-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR\_CTX\_LOGON\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-690">7037 (0x1B7D)</span><span class="sxs-lookup"><span data-stu-id="eb676-690">7037 (0x1B7D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-691">Права на интерактивный вход отключены.</span><span class="sxs-lookup"><span data-stu-id="eb676-691">Your interactive logon privilege has been disabled.</span></span> <span data-ttu-id="eb676-692">Обратитесь за помощью к администратору.</span><span class="sxs-lookup"><span data-stu-id="eb676-692">Please contact your administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**Ошибка \_ CTX \_ не \_ консоль**</span><span class="sxs-lookup"><span data-stu-id="eb676-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR\_CTX\_NOT\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-694">7038 (0x1B7E)</span><span class="sxs-lookup"><span data-stu-id="eb676-694">7038 (0x1B7E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-695">Запрошенную операцию можно выполнить только в системной консоли.</span><span class="sxs-lookup"><span data-stu-id="eb676-695">The requested operation can be performed only on the system console.</span></span> <span data-ttu-id="eb676-696">Чаще всего это вызвано драйвером или системной библиотекой DLL, для которой необходим прямой доступ к консоли.</span><span class="sxs-lookup"><span data-stu-id="eb676-696">This is most often the result of a driver or system DLL requiring direct console access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**Ошибка \_ CTX \_ \_ \_ время ожидания запроса клиента**</span><span class="sxs-lookup"><span data-stu-id="eb676-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR\_CTX\_CLIENT\_QUERY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-698">7040 (0x1B80)</span><span class="sxs-lookup"><span data-stu-id="eb676-698">7040 (0x1B80)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-699">Клиенту не удалось ответить на сообщение подключения к серверу.</span><span class="sxs-lookup"><span data-stu-id="eb676-699">The client failed to respond to the server connect message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**Ошибка \_ при \_ \_ отключении консоли CTX**</span><span class="sxs-lookup"><span data-stu-id="eb676-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR\_CTX\_CONSOLE\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-701">7041 (0x1B81)</span><span class="sxs-lookup"><span data-stu-id="eb676-701">7041 (0x1B81)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-702">Отключение сеанса консоли не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb676-702">Disconnecting the console session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**Ошибка \_ CTX \_ \_ Подключение консоли**</span><span class="sxs-lookup"><span data-stu-id="eb676-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR\_CTX\_CONSOLE\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-704">7042 (0x1B82)</span><span class="sxs-lookup"><span data-stu-id="eb676-704">7042 (0x1B82)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-705">Повторное подключение отключенного сеанса к консоли не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb676-705">Reconnecting a disconnected session to the console is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**Ошибка \_ CTX \_ теневой копии \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR\_CTX\_SHADOW\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-707">7044 (0x1B84)</span><span class="sxs-lookup"><span data-stu-id="eb676-707">7044 (0x1B84)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-708">Запрос на удаленное управление другим сеансом был отклонен.</span><span class="sxs-lookup"><span data-stu-id="eb676-708">The request to control another session remotely was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**Ошибка \_ CTX \_ \_ отказа в доступе винстатион \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR\_CTX\_WINSTATION\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-710">7045 (0x1B85)</span><span class="sxs-lookup"><span data-stu-id="eb676-710">7045 (0x1B85)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-711">Отказано в доступе к запрошенному сеансу.</span><span class="sxs-lookup"><span data-stu-id="eb676-711">The requested session access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**Ошибка \_ CTX \_ Недопустимый \_ WD**</span><span class="sxs-lookup"><span data-stu-id="eb676-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR\_CTX\_INVALID\_WD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-713">7049 (0x1B89)</span><span class="sxs-lookup"><span data-stu-id="eb676-713">7049 (0x1B89)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-714">Указан недопустимый драйвер подключения терминала.</span><span class="sxs-lookup"><span data-stu-id="eb676-714">The specified terminal connection driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**Ошибка \_ CTX \_ теневой копии \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR\_CTX\_SHADOW\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-716">7050 (0x1B8A)</span><span class="sxs-lookup"><span data-stu-id="eb676-716">7050 (0x1B8A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-717">Не удается управлять запрошенным сеансом удаленно.</span><span class="sxs-lookup"><span data-stu-id="eb676-717">The requested session cannot be controlled remotely.</span></span> <span data-ttu-id="eb676-718">Это может быть вызвано тем, что сеанс отключен или в данный момент пользователь не вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="eb676-718">This may be because the session is disconnected or does not currently have a user logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**Ошибка \_ CTX \_ теневой копии \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="eb676-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR\_CTX\_SHADOW\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-720">7051 (0x1B8B)</span><span class="sxs-lookup"><span data-stu-id="eb676-720">7051 (0x1B8B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-721">Запрошенный сеанс не настроен на разрешение удаленного управления.</span><span class="sxs-lookup"><span data-stu-id="eb676-721">The requested session is not configured to allow remote control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**Ошибка \_ \_ \_ \_ при использовании клиентской лицензии CTX \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-723">7052 (0x1B8C)</span><span class="sxs-lookup"><span data-stu-id="eb676-723">7052 (0x1B8C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-724">Запрос на подключение к этому серверу терминалов отклонен.</span><span class="sxs-lookup"><span data-stu-id="eb676-724">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="eb676-725">Номер клиентской лицензии сервера терминалов сейчас используется другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="eb676-725">Your Terminal Server client license number is currently being used by another user.</span></span> <span data-ttu-id="eb676-726">Обратитесь к системному администратору, чтобы получить уникальный номер лицензии.</span><span class="sxs-lookup"><span data-stu-id="eb676-726">Please call your system administrator to obtain a unique license number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**Ошибка \_ CTX \_ клиентской \_ лицензии \_ не \_ задана**</span><span class="sxs-lookup"><span data-stu-id="eb676-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-728">7053 (0x1B8D)</span><span class="sxs-lookup"><span data-stu-id="eb676-728">7053 (0x1B8D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-729">Запрос на подключение к этому серверу терминалов отклонен.</span><span class="sxs-lookup"><span data-stu-id="eb676-729">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="eb676-730">Номер клиентской лицензии сервера терминалов не был введен для этой копии клиента сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="eb676-730">Your Terminal Server client license number has not been entered for this copy of the Terminal Server client.</span></span> <span data-ttu-id="eb676-731">Обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="eb676-731">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**Ошибка \_ CTX \_ Лицензия \_ \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="eb676-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR\_CTX\_LICENSE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-733">7054 (0x1B8E)</span><span class="sxs-lookup"><span data-stu-id="eb676-733">7054 (0x1B8E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-734">Число подключений к этому компьютеру ограничено, и все подключения сейчас используются.</span><span class="sxs-lookup"><span data-stu-id="eb676-734">The number of connections to this computer is limited and all connections are in use right now.</span></span> <span data-ttu-id="eb676-735">Попробуйте подключиться позже или обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="eb676-735">Try connecting later or contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**Ошибка \_ CTX \_ Лицензия \_ клиента \_ недействительна**</span><span class="sxs-lookup"><span data-stu-id="eb676-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR\_CTX\_LICENSE\_CLIENT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-737">7055 (0x1B8F)</span><span class="sxs-lookup"><span data-stu-id="eb676-737">7055 (0x1B8F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-738">Используемый клиент не имеет лицензии на использование этой системы.</span><span class="sxs-lookup"><span data-stu-id="eb676-738">The client you are using is not licensed to use this system.</span></span> <span data-ttu-id="eb676-739">Запрос на вход запрещен.</span><span class="sxs-lookup"><span data-stu-id="eb676-739">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**Ошибка \_ CTX \_ \_ срок действия лицензии истек**</span><span class="sxs-lookup"><span data-stu-id="eb676-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR\_CTX\_LICENSE\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-741">7056 (0x1B90)</span><span class="sxs-lookup"><span data-stu-id="eb676-741">7056 (0x1B90)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-742">Срок действия системной лицензии истек.</span><span class="sxs-lookup"><span data-stu-id="eb676-742">The system license has expired.</span></span> <span data-ttu-id="eb676-743">Запрос на вход запрещен.</span><span class="sxs-lookup"><span data-stu-id="eb676-743">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**Ошибка \_ CTX \_ теневой копии \_ не \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="eb676-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR\_CTX\_SHADOW\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-745">7057 (0x1B91)</span><span class="sxs-lookup"><span data-stu-id="eb676-745">7057 (0x1B91)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-746">Не удалось завершить удаленное управление, так как указанный сеанс в настоящее время не управляется удаленно.</span><span class="sxs-lookup"><span data-stu-id="eb676-746">Remote control could not be terminated because the specified session is not currently being remotely controlled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**Ошибка \_ CTX \_ теневой копии \_ , завершенной \_ \_ \_ изменением режима**</span><span class="sxs-lookup"><span data-stu-id="eb676-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR\_CTX\_SHADOW\_ENDED\_BY\_MODE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-748">7058 (0x1B92)</span><span class="sxs-lookup"><span data-stu-id="eb676-748">7058 (0x1B92)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-749">Удаленное управление консолью прервано, так как был изменен режим экрана.</span><span class="sxs-lookup"><span data-stu-id="eb676-749">The remote control of the console was terminated because the display mode was changed.</span></span> <span data-ttu-id="eb676-750">Изменение режима просмотра в сеансе удаленного управления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb676-750">Changing the display mode in a remote control session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**\_Превышено число активаций ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**ERROR\_ACTIVATION\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-752">7059 (0x1B93)</span><span class="sxs-lookup"><span data-stu-id="eb676-752">7059 (0x1B93)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-753">Активация уже была сброшена максимально допустимое количество раз для этой установки.</span><span class="sxs-lookup"><span data-stu-id="eb676-753">Activation has already been reset the maximum number of times for this installation.</span></span> <span data-ttu-id="eb676-754">Таймер активации не будет сброшен.</span><span class="sxs-lookup"><span data-stu-id="eb676-754">Your activation timer will not be cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**Ошибка \_ CTX \_ винстатионс \_ Disabled**</span><span class="sxs-lookup"><span data-stu-id="eb676-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR\_CTX\_WINSTATIONS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-756">7060 (0x1B94)</span><span class="sxs-lookup"><span data-stu-id="eb676-756">7060 (0x1B94)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-757">Удаленные имена входа в настоящее время отключены.</span><span class="sxs-lookup"><span data-stu-id="eb676-757">Remote logins are currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**Ошибка \_ CTX \_ . \_ требуется уровень шифрования \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR\_CTX\_ENCRYPTION\_LEVEL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-759">7061 (0x1B95)</span><span class="sxs-lookup"><span data-stu-id="eb676-759">7061 (0x1B95)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-760">У вас нет нужного уровня шифрования для доступа к этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="eb676-760">You do not have the proper encryption level to access this Session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**Ошибка \_ \_ \_ при использовании сеанса \_ CTX**</span><span class="sxs-lookup"><span data-stu-id="eb676-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR\_CTX\_SESSION\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-762">7062 (0x1B96)</span><span class="sxs-lookup"><span data-stu-id="eb676-762">7062 (0x1B96)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-763">Пользователь% s \\ \\ % s в данный момент вошел в систему на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="eb676-763">The user %s\\\\%s is currently logged on to this computer.</span></span> <span data-ttu-id="eb676-764">Только текущий пользователь или администратор может войти на этот компьютер.</span><span class="sxs-lookup"><span data-stu-id="eb676-764">Only the current user or an administrator can log on to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**Ошибка \_ CTX \_ без \_ принудительного \_ выхода**</span><span class="sxs-lookup"><span data-stu-id="eb676-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR\_CTX\_NO\_FORCE\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-766">7063 (0x1B97)</span><span class="sxs-lookup"><span data-stu-id="eb676-766">7063 (0x1B97)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-767">Пользователь% s \\ \\ % s уже вошел в консоль этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="eb676-767">The user %s\\\\%s is already logged on to the console of this computer.</span></span> <span data-ttu-id="eb676-768">У вас нет разрешения на вход в систему в данный момент.</span><span class="sxs-lookup"><span data-stu-id="eb676-768">You do not have permission to log in at this time.</span></span> <span data-ttu-id="eb676-769">Чтобы устранить эту проблему, обратитесь в% s \\ \\ % s и выйдите из системы.</span><span class="sxs-lookup"><span data-stu-id="eb676-769">To resolve this issue, contact %s\\\\%s and have them log off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**Ошибка \_ при \_ ограничении учетной записи CTX \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR\_CTX\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-771">7064 (0x1B98)</span><span class="sxs-lookup"><span data-stu-id="eb676-771">7064 (0x1B98)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-772">Не удалось войти в систему из-за ограничений учетной записи.</span><span class="sxs-lookup"><span data-stu-id="eb676-772">Unable to log you on because of an account restriction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**Ошибка \_ \_ протокола RDP \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR\_RDP\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-774">7065 (0x1B99)</span><span class="sxs-lookup"><span data-stu-id="eb676-774">7065 (0x1B99)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-775">Компонент протокола RDP %2 обнаружил ошибку в потоке протокола и отключил клиент.</span><span class="sxs-lookup"><span data-stu-id="eb676-775">The RDP protocol component %2 detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**Ошибка \_ CTX \_ CDM \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="eb676-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR\_CTX\_CDM\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-777">7066 (0x1B9A)</span><span class="sxs-lookup"><span data-stu-id="eb676-777">7066 (0x1B9A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-778">Служба сопоставления клиентских дисков подключена к терминальному подключению.</span><span class="sxs-lookup"><span data-stu-id="eb676-778">The Client Drive Mapping Service Has Connected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**Ошибка \_ CTX \_ CDM \_ Disconnect**</span><span class="sxs-lookup"><span data-stu-id="eb676-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR\_CTX\_CDM\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-780">7067 (0x1B9B)</span><span class="sxs-lookup"><span data-stu-id="eb676-780">7067 (0x1B9B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-781">Служба сопоставления клиентских дисков отключена на терминальном подключении.</span><span class="sxs-lookup"><span data-stu-id="eb676-781">The Client Drive Mapping Service Has Disconnected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**Ошибка \_ CTX \_ \_ уровня безопасности \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR\_CTX\_SECURITY\_LAYER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-783">7068 (0x1B9C)</span><span class="sxs-lookup"><span data-stu-id="eb676-783">7068 (0x1B9C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-784">Уровень безопасности сервера терминалов обнаружил ошибку в потоке протокола и отключил клиента.</span><span class="sxs-lookup"><span data-stu-id="eb676-784">The Terminal Server security layer detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ОШИБКИ \_ \_ несовместимых \_ сеансов TS**</span><span class="sxs-lookup"><span data-stu-id="eb676-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR\_TS\_INCOMPATIBLE\_SESSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-786">7069 (0x1B9D)</span><span class="sxs-lookup"><span data-stu-id="eb676-786">7069 (0x1B9D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-787">Целевой сеанс несовместим с текущим сеансом.</span><span class="sxs-lookup"><span data-stu-id="eb676-787">The target session is incompatible with the current session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**Ошибка \_ \_ подсистемы видеоподсистемы TS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR\_TS\_VIDEO\_SUBSYSTEM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-789">7070 (0x1B9E)</span><span class="sxs-lookup"><span data-stu-id="eb676-789">7070 (0x1B9E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-790">Windows не удается подключиться к сеансу из-за проблемы в подсистеме Windows.</span><span class="sxs-lookup"><span data-stu-id="eb676-790">Windows can't connect to your session because a problem occurred in the Windows video subsystem.</span></span> <span data-ttu-id="eb676-791">Повторите попытку подключения позже или обратитесь за помощью к администратору сервера.</span><span class="sxs-lookup"><span data-stu-id="eb676-791">Try connecting again later, or contact the server administrator for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_ \_ неправильная \_ последовательность API \_ для FRS Err**</span><span class="sxs-lookup"><span data-stu-id="eb676-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS\_ERR\_INVALID\_API\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-793">8001 (0x1F41)</span><span class="sxs-lookup"><span data-stu-id="eb676-793">8001 (0x1F41)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-794">API службы репликации файлов был вызван неправильно.</span><span class="sxs-lookup"><span data-stu-id="eb676-794">The file replication service API was called incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**\_служба FRS Err \_ starting \_ Service**</span><span class="sxs-lookup"><span data-stu-id="eb676-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS\_ERR\_STARTING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-796">8002 (0x1F42)</span><span class="sxs-lookup"><span data-stu-id="eb676-796">8002 (0x1F42)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-797">Не удается запустить службу репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="eb676-797">The file replication service cannot be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**\_служба FRS Err \_ останавливает \_ службу**</span><span class="sxs-lookup"><span data-stu-id="eb676-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS\_ERR\_STOPPING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-799">8003 (0x1F43)</span><span class="sxs-lookup"><span data-stu-id="eb676-799">8003 (0x1F43)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-800">Не удается остановить службу репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="eb676-800">The file replication service cannot be stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ внутренний API FRS \_ Err**</span><span class="sxs-lookup"><span data-stu-id="eb676-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS\_ERR\_INTERNAL\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-802">8004 (0x1F44)</span><span class="sxs-lookup"><span data-stu-id="eb676-802">8004 (0x1F44)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-803">API службы репликации файлов прервал запрос.</span><span class="sxs-lookup"><span data-stu-id="eb676-803">The file replication service API terminated the request.</span></span> <span data-ttu-id="eb676-804">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-804">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**\_Внутренняя ошибка \_ FRS**</span><span class="sxs-lookup"><span data-stu-id="eb676-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS\_ERR\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-806">8005 (0x1F45)</span><span class="sxs-lookup"><span data-stu-id="eb676-806">8005 (0x1F45)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-807">Служба репликации файлов завершила запрос.</span><span class="sxs-lookup"><span data-stu-id="eb676-807">The file replication service terminated the request.</span></span> <span data-ttu-id="eb676-808">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-808">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_канал связи \_ службы FRS Err \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS\_ERR\_SERVICE\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-810">8006 (0x1F46)</span><span class="sxs-lookup"><span data-stu-id="eb676-810">8006 (0x1F46)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-811">Не удается связаться со службой репликации файлов.</span><span class="sxs-lookup"><span data-stu-id="eb676-811">The file replication service cannot be contacted.</span></span> <span data-ttu-id="eb676-812">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-812">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**Ошибка FRS при \_ \_ нехватке \_ Priv**</span><span class="sxs-lookup"><span data-stu-id="eb676-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS\_ERR\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-814">8007 (0x1F47)</span><span class="sxs-lookup"><span data-stu-id="eb676-814">8007 (0x1F47)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-815">Служба репликации файлов не может удовлетворить запрос, так как у пользователя недостаточно привилегий.</span><span class="sxs-lookup"><span data-stu-id="eb676-815">The file replication service cannot satisfy the request because the user has insufficient privileges.</span></span> <span data-ttu-id="eb676-816">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-816">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**\_ \_ Проверка подлинности FRS Err**</span><span class="sxs-lookup"><span data-stu-id="eb676-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS\_ERR\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-818">8008 (0x1F48)</span><span class="sxs-lookup"><span data-stu-id="eb676-818">8008 (0x1F48)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-819">Службе репликации файлов не удается удовлетворить запрос, так как проверка подлинности RPC недоступна.</span><span class="sxs-lookup"><span data-stu-id="eb676-819">The file replication service cannot satisfy the request because authenticated RPC is not available.</span></span> <span data-ttu-id="eb676-820">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-820">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**\_ \_ недостаточный родительский элемент FRS Err \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS\_ERR\_PARENT\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-822">8009 (0x1F49)</span><span class="sxs-lookup"><span data-stu-id="eb676-822">8009 (0x1F49)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-823">Службе репликации файлов не удается удовлетворить запрос, так как у пользователя недостаточно привилегий на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="eb676-823">The file replication service cannot satisfy the request because the user has insufficient privileges on the domain controller.</span></span> <span data-ttu-id="eb676-824">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-824">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ родительская \_ Проверка подлинности FRS Err**</span><span class="sxs-lookup"><span data-stu-id="eb676-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS\_ERR\_PARENT\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-826">8010 (0x1F4A)</span><span class="sxs-lookup"><span data-stu-id="eb676-826">8010 (0x1F4A)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-827">Службе репликации файлов не удается удовлетворить запрос, так как проверка подлинности RPC недоступна на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="eb676-827">The file replication service cannot satisfy the request because authenticated RPC is not available on the domain controller.</span></span> <span data-ttu-id="eb676-828">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-828">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**\_ \_ дочерний элемент FRS Err \_ с \_ родительским \_ каналом**</span><span class="sxs-lookup"><span data-stu-id="eb676-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS\_ERR\_CHILD\_TO\_PARENT\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-830">8011 (0x1F4B)</span><span class="sxs-lookup"><span data-stu-id="eb676-830">8011 (0x1F4B)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-831">Службе репликации файлов не удается связаться со службой репликации файлов на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="eb676-831">The file replication service cannot communicate with the file replication service on the domain controller.</span></span> <span data-ttu-id="eb676-832">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-832">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ Err \_ Parent \_ to \_ Дочерний \_ канал связи**</span><span class="sxs-lookup"><span data-stu-id="eb676-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS\_ERR\_PARENT\_TO\_CHILD\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-834">8012 (0x1F4C)</span><span class="sxs-lookup"><span data-stu-id="eb676-834">8012 (0x1F4C)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-835">Службе репликации файлов на контроллере домена не удается связаться со службой репликации файлов на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="eb676-835">The file replication service on the domain controller cannot communicate with the file replication service on this computer.</span></span> <span data-ttu-id="eb676-836">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-836">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_ \_ Заполнение SYSVOL Err FRS \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS\_ERR\_SYSVOL\_POPULATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-838">8013 (0x1F4D)</span><span class="sxs-lookup"><span data-stu-id="eb676-838">8013 (0x1F4D)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-839">Службе репликации файлов не удается заполнить системный том из-за внутренней ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb676-839">The file replication service cannot populate the system volume because of an internal error.</span></span> <span data-ttu-id="eb676-840">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-840">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ время ожидания заполнения SYSVOL Err \_ FRS**</span><span class="sxs-lookup"><span data-stu-id="eb676-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS\_ERR\_SYSVOL\_POPULATE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-842">8014 (0x1F4E)</span><span class="sxs-lookup"><span data-stu-id="eb676-842">8014 (0x1F4E)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-843">Службе репликации файлов не удается заполнить системный том из-за внутреннего времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="eb676-843">The file replication service cannot populate the system volume because of an internal timeout.</span></span> <span data-ttu-id="eb676-844">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-844">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**Служба \_ FRS \_ Err \_ SYSVOL \_ занята**</span><span class="sxs-lookup"><span data-stu-id="eb676-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS\_ERR\_SYSVOL\_IS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-846">8015 (0x1F4F)</span><span class="sxs-lookup"><span data-stu-id="eb676-846">8015 (0x1F4F)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-847">Службе репликации файлов не удается обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="eb676-847">The file replication service cannot process the request.</span></span> <span data-ttu-id="eb676-848">Системный том занят с помощью предыдущего запроса.</span><span class="sxs-lookup"><span data-stu-id="eb676-848">The system volume is busy with a previous request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**Репликация \_ SYSVOL Err FRS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS\_ERR\_SYSVOL\_DEMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-850">8016 (0x1F50)</span><span class="sxs-lookup"><span data-stu-id="eb676-850">8016 (0x1F50)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-851">Службе репликации файлов не удается отключить репликацию системного тома из-за внутренней ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb676-851">The file replication service cannot stop replicating the system volume because of an internal error.</span></span> <span data-ttu-id="eb676-852">В журнале событий могут быть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb676-852">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eb676-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_ \_ Недопустимый \_ параметр службы FRS Err \_**</span><span class="sxs-lookup"><span data-stu-id="eb676-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS\_ERR\_INVALID\_SERVICE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb676-854">8017 (0x1F51)</span><span class="sxs-lookup"><span data-stu-id="eb676-854">8017 (0x1F51)</span></span>
</dt> <dt>



<span data-ttu-id="eb676-855">Служба репликации файлов обнаружила недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="eb676-855">The file replication service detected an invalid parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb676-856">Требования</span><span class="sxs-lookup"><span data-stu-id="eb676-856">Requirements</span></span>



| <span data-ttu-id="eb676-857">Требование</span><span class="sxs-lookup"><span data-stu-id="eb676-857">Requirement</span></span> | <span data-ttu-id="eb676-858">Значение</span><span class="sxs-lookup"><span data-stu-id="eb676-858">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb676-859">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb676-859">Minimum supported client</span></span><br/> | <span data-ttu-id="eb676-860">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="eb676-860">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eb676-861">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb676-861">Minimum supported server</span></span><br/> | <span data-ttu-id="eb676-862">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb676-862">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb676-863">Header</span><span class="sxs-lookup"><span data-stu-id="eb676-863">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb676-864"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb676-864"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb676-865">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb676-865">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb676-866">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="eb676-866">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




