---
description: API-интерфейс защиты данных CNG использует следующие константы.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Константы DPAPI CNG (Нкриптпротект. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496971"
---
# <a name="cng-dpapi-constants"></a><span data-ttu-id="d6a75-103">Константы DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="d6a75-103">CNG DPAPI Constants</span></span>

<span data-ttu-id="d6a75-104">API-интерфейс защиты данных CNG использует следующие константы.</span><span class="sxs-lookup"><span data-stu-id="d6a75-104">The following constants are used by the CNG Data Protection API.</span></span>

<dl> <dt>

<span data-ttu-id="d6a75-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT \_ Descr \_ разделитель \_ и**</span><span class="sxs-lookup"><span data-stu-id="d6a75-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT\_DESCR\_DELIMITER\_AND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-106">L "И"</span><span class="sxs-lookup"><span data-stu-id="d6a75-106">L" AND "</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-107">Может использоваться для проверки строки дескриптора защиты для разделителя и.</span><span class="sxs-lookup"><span data-stu-id="d6a75-107">Can be used to test a protection descriptor string for an AND delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ Descr \_ EQUAL**</span><span class="sxs-lookup"><span data-stu-id="d6a75-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT\_DESCR\_EQUAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-109">L "="</span><span class="sxs-lookup"><span data-stu-id="d6a75-109">L"="</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-110">Может использоваться для проверки строки дескриптора защиты для знака равенства.</span><span class="sxs-lookup"><span data-stu-id="d6a75-110">Can be used to test a protection descriptor string for an equals sign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT \_ Descr \_ разделитель \_ или**</span><span class="sxs-lookup"><span data-stu-id="d6a75-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT\_DESCR\_DELIMITER\_OR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-112">L "ИЛИ"</span><span class="sxs-lookup"><span data-stu-id="d6a75-112">L" OR "</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-113">Может использоваться для проверки строки дескриптора защиты для разделителя или.</span><span class="sxs-lookup"><span data-stu-id="d6a75-113">Can be used to test a protection descriptor string for an OR delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_ \_ \_ локальный алгоритм защиты ключей \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-115">"LOCAL"</span><span class="sxs-lookup"><span data-stu-id="d6a75-115">"LOCAL"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-116">ЛОКАЛЬНЫЙ дескриптор защиты защищает содержимое для сеанса входа в систему, текущего пользователя или локального компьютера, как определено следующими константами:</span><span class="sxs-lookup"><span data-stu-id="d6a75-116">The LOCAL protection descriptor protects content to the logon session, the current user, or the local machine as identified by the following constants:</span></span>

-   <span data-ttu-id="d6a75-117">**\_ \_ \_ локальный \_ Вход в систему защиты ключей NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-117">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
-   <span data-ttu-id="d6a75-118">**\_ \_ \_ локальный \_ Пользователь защиты ключей NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-118">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
-   <span data-ttu-id="d6a75-119">**\_ \_ \_ локальный \_ компьютер защиты ключей NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-119">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**\_ \_ алгоритм защиты ключей \_ NCRYPT \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="d6a75-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-121">АВТОРИЗАЦИИ</span><span class="sxs-lookup"><span data-stu-id="d6a75-121">"SDDL"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-122">Защищает содержимое до строки SDDL (языка определения дескрипторов безопасности), содержащей сведения о дескрипторе безопасности.</span><span class="sxs-lookup"><span data-stu-id="d6a75-122">Protects content to an SDDL (Security Descriptor Definition Language) string that contains security descriptor information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_ \_ \_ ИД безопасности алгоритма защиты ключей NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="d6a75-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-124">ТРАНСЛЯЦИЮ</span><span class="sxs-lookup"><span data-stu-id="d6a75-124">"SID"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-125">Дескриптор защиты SID содержит удостоверение группы или участника.</span><span class="sxs-lookup"><span data-stu-id="d6a75-125">The SID protection descriptor contains a group or principal identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_ \_ \_ учетные данные для алгоритма защиты ключей NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="d6a75-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-127">"УЧЕТные данные"</span><span class="sxs-lookup"><span data-stu-id="d6a75-127">"WEBCREDENTIALS"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-128">Обеспечивает защиту учетных данных веб-учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6a75-128">Protects to a user's web account credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_ \_ \_ локальный \_ Вход в систему защиты ключей NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-130">входа</span><span class="sxs-lookup"><span data-stu-id="d6a75-130">"logon"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-131">Защищает содержимое в текущем сеансе входа.</span><span class="sxs-lookup"><span data-stu-id="d6a75-131">Protects content to the current logon session.</span></span> <span data-ttu-id="d6a75-132">Пользователи не смогут расшифровывать защищенное содержимое после выхода из системы или перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="d6a75-132">Users will not be able to decrypt the protected content after logoff or reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ \_ локальный \_ компьютер защиты ключей NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-134">машине</span><span class="sxs-lookup"><span data-stu-id="d6a75-134">"machine"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-135">Защищает содержимое на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d6a75-135">Protects content to the local computer.</span></span> <span data-ttu-id="d6a75-136">Все пользователи на локальном компьютере могут расшифровывать защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="d6a75-136">All users on the local computer can decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_ \_ \_ локальный \_ Пользователь защиты ключей NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-138">нажат</span><span class="sxs-lookup"><span data-stu-id="d6a75-138">"user"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-139">Защищает содержимое в текущем сеансе пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6a75-139">Protects content to the current user session.</span></span> <span data-ttu-id="d6a75-140">Только этот пользователь на локальном компьютере сможет расшифровать защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="d6a75-140">Only this user on the local computer will be able to decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_ \_ поставщик защиты ключей \_ MS**</span><span class="sxs-lookup"><span data-stu-id="d6a75-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-142">"Поставщик защиты ключей (Майкрософт)"</span><span class="sxs-lookup"><span data-stu-id="d6a75-142">"Microsoft Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-143">Представляет поставщик защиты ключей (Майкрософт), который поддерживает форматы, представленные следующими константами:</span><span class="sxs-lookup"><span data-stu-id="d6a75-143">Represents the Microsoft key protection provider which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="d6a75-144">**\_ \_ \_ ИД безопасности алгоритма защиты ключей NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="d6a75-144">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
-   <span data-ttu-id="d6a75-145">**\_ \_ \_ локальный алгоритм защиты ключей \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6a75-145">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
-   <span data-ttu-id="d6a75-146">**\_ \_ алгоритм защиты ключей \_ NCRYPT \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="d6a75-146">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6a75-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_ \_ \_ поставщик защиты ключа клиента \_ Windows**</span><span class="sxs-lookup"><span data-stu-id="d6a75-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS\_CLIENT\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a75-148">"Поставщик защиты ключа клиента Windows"</span><span class="sxs-lookup"><span data-stu-id="d6a75-148">"Windows Client Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="d6a75-149">Представляет поставщик защиты ключей (Майкрософт), доступный только на клиенте и поддерживающий форматы, представленные следующими константами:</span><span class="sxs-lookup"><span data-stu-id="d6a75-149">Represents the Microsoft key protection provider that is available only on the client and which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="d6a75-150">**\_ \_ \_ учетные данные для алгоритма защиты ключей NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="d6a75-150">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6a75-151">Требования</span><span class="sxs-lookup"><span data-stu-id="d6a75-151">Requirements</span></span>



| <span data-ttu-id="d6a75-152">Требование</span><span class="sxs-lookup"><span data-stu-id="d6a75-152">Requirement</span></span> | <span data-ttu-id="d6a75-153">Значение</span><span class="sxs-lookup"><span data-stu-id="d6a75-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a75-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6a75-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a75-155">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d6a75-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d6a75-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6a75-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a75-157">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d6a75-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d6a75-158">Header</span><span class="sxs-lookup"><span data-stu-id="d6a75-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a75-159"><dt>Нкриптпротект. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a75-159"><dt>NCryptprotect.h</dt></span></span> </dl> |



 

 




