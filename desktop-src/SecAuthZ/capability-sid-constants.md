---
description: Определение для хорошо известных возможностей приложений с помощью функции Аллокатеандинитиализесид.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Константы SID возможностей (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273093"
---
# <a name="capability-sid-constants"></a><span data-ttu-id="98d36-103">Константы идентификатора безопасности возможностей</span><span class="sxs-lookup"><span data-stu-id="98d36-103">Capability SID Constants</span></span>

<span data-ttu-id="98d36-104">Константы идентификаторов безопасности возможностей определяются для хорошо известных возможностей приложений с помощью функции [**аллокатеандинитиализесид**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="98d36-104">The capability SID constants define for applications well-known capabilities by using the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span>

<dl> <dt>

<span data-ttu-id="98d36-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**\_ \_ клиентский Интернет возможностей безопасности \_**</span><span class="sxs-lookup"><span data-stu-id="98d36-105"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-106">(0x00000001)</span><span class="sxs-lookup"><span data-stu-id="98d36-106">(0x00000001L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-107">У учетной записи есть доступ к Интернету с клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="98d36-107">An account has access to the Internet from a client computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**\_ \_ \_ Серверный Интернет клиента с функциями \_ безопасности**</span><span class="sxs-lookup"><span data-stu-id="98d36-108"><span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**SECURITY\_CAPABILITY\_INTERNET\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-109">(0x00000002L)</span><span class="sxs-lookup"><span data-stu-id="98d36-109">(0x00000002L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-110">У учетной записи есть доступ к Интернету с клиентских и серверных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="98d36-110">An account has access to the Internet from the client and server computers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_ \_ \_ \_ клиентский сервер частной сети с функциями \_ безопасности**</span><span class="sxs-lookup"><span data-stu-id="98d36-111"><span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**SECURITY\_CAPABILITY\_PRIVATE\_NETWORK\_CLIENT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-112">(0x00000003L)</span><span class="sxs-lookup"><span data-stu-id="98d36-112">(0x00000003L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-113">У учетной записи есть доступ к Интернету из частной сети.</span><span class="sxs-lookup"><span data-stu-id="98d36-113">An account has access to the Internet from a private network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_ \_ Библиотека изображений возможностей \_ безопасности**</span><span class="sxs-lookup"><span data-stu-id="98d36-114"><span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**SECURITY\_CAPABILITY\_PICTURES\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-115">(0x00000004L)</span><span class="sxs-lookup"><span data-stu-id="98d36-115">(0x00000004L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-116">У учетной записи есть доступ к библиотеке изображений.</span><span class="sxs-lookup"><span data-stu-id="98d36-116">An account has access to the pictures library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_ \_ Библиотека видеоматериалов по возможностям безопасности \_**</span><span class="sxs-lookup"><span data-stu-id="98d36-117"><span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**SECURITY\_CAPABILITY\_VIDEOS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-118">(0x00000005L)</span><span class="sxs-lookup"><span data-stu-id="98d36-118">(0x00000005L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-119">У учетной записи есть доступ к библиотеке видео.</span><span class="sxs-lookup"><span data-stu-id="98d36-119">An account has access to the videos library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_ \_ музыкальная библиотека возможностей безопасности \_**</span><span class="sxs-lookup"><span data-stu-id="98d36-120"><span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**SECURITY\_CAPABILITY\_MUSIC\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-121">(0x00000006L)</span><span class="sxs-lookup"><span data-stu-id="98d36-121">(0x00000006L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-122">У учетной записи есть доступ к музыкальной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="98d36-122">An account has access to the music library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**\_ \_ Библиотека документов возможностей \_ безопасности**</span><span class="sxs-lookup"><span data-stu-id="98d36-123"><span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**SECURITY\_CAPABILITY\_DOCUMENTS\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-124">(0x00000007L)</span><span class="sxs-lookup"><span data-stu-id="98d36-124">(0x00000007L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-125">У учетной записи есть доступ к библиотеке документации.</span><span class="sxs-lookup"><span data-stu-id="98d36-125">An account has access to the documentation library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_ \_ \_ Проверка подлинности Enterprise для возможностей безопасности**</span><span class="sxs-lookup"><span data-stu-id="98d36-126"><span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY\_CAPABILITY\_ENTERPRISE\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-127">(0x00000008L)</span><span class="sxs-lookup"><span data-stu-id="98d36-127">(0x00000008L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-128">Учетная запись имеет доступ к учетным данным Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="98d36-128">An account has access to the default Windows credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_ \_ \_ Сертификаты общих пользователей \_ возможностей безопасности**</span><span class="sxs-lookup"><span data-stu-id="98d36-129"><span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**SECURITY\_CAPABILITY\_SHARED\_USER\_CERTIFICATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-130">(0x00000009L)</span><span class="sxs-lookup"><span data-stu-id="98d36-130">(0x00000009L)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-131">У учетной записи есть доступ к общим сертификатам пользователей.</span><span class="sxs-lookup"><span data-stu-id="98d36-131">An account has access to the shared user certificates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="98d36-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_возможности безопасности \_ съемные \_ носители**</span><span class="sxs-lookup"><span data-stu-id="98d36-132"><span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**SECURITY\_CAPABILITY\_REMOVABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98d36-133">(0x0000000A)</span><span class="sxs-lookup"><span data-stu-id="98d36-133">(0x0000000AL)</span></span>
</dt> <dt>



<span data-ttu-id="98d36-134">У учетной записи есть доступ к съемным носителям.</span><span class="sxs-lookup"><span data-stu-id="98d36-134">An account has access to removable storage.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98d36-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98d36-135">Remarks</span></span>

<span data-ttu-id="98d36-136">При создании идентификатора безопасности возможности необходимо включить центр пакетов, \_ Центр приложений безопасности \_ \_ {0,0,0,0,0,15} , в вызове функции [**аллокатеандинитиализесид**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .</span><span class="sxs-lookup"><span data-stu-id="98d36-136">When constructing a capability SID, you need to include the package authority, SECURITY\_APP\_PACKAGE\_AUTHORITY {0,0,0,0,0,15}, in the call to the [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) function.</span></span> <span data-ttu-id="98d36-137">Кроме того, вам потребуются базовые RID и число RID для встроенных возможностей, \_ \_ Базовый \_ RID (0x00000003L) и \_ число RID встроенных возможностей \_ безопасности \_ \_ (2L).</span><span class="sxs-lookup"><span data-stu-id="98d36-137">Additionally, you need the base RID and RID count for the built-in capabilities, SECURITY\_CAPABILITY\_BASE\_RID (0x00000003L) and SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT (2L).</span></span>

## <a name="requirements"></a><span data-ttu-id="98d36-138">Требования</span><span class="sxs-lookup"><span data-stu-id="98d36-138">Requirements</span></span>



| <span data-ttu-id="98d36-139">Требование</span><span class="sxs-lookup"><span data-stu-id="98d36-139">Requirement</span></span> | <span data-ttu-id="98d36-140">Значение</span><span class="sxs-lookup"><span data-stu-id="98d36-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98d36-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98d36-141">Minimum supported client</span></span><br/> | <span data-ttu-id="98d36-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="98d36-142">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="98d36-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98d36-143">Minimum supported server</span></span><br/> | <span data-ttu-id="98d36-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="98d36-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="98d36-145">Header</span><span class="sxs-lookup"><span data-stu-id="98d36-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="98d36-146"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="98d36-146"><dt>Winnt.h</dt></span></span> </dl> |



 

