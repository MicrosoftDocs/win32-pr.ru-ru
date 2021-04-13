---
title: Структуры IKE/AuthIP
description: Структуры IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "104412632"
---
# <a name="ikeauthip-structures"></a><span data-ttu-id="c8da9-103">Структуры IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="c8da9-103">IKE/AuthIP Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c8da9-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="c8da9-104">In this section</span></span>

-   [<span data-ttu-id="c8da9-105">**\_METHOD0 проверки подлинности IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-105">**IKEEXT\_AUTHENTICATION\_METHOD0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [<span data-ttu-id="c8da9-106">**\_METHOD1 проверки подлинности IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-106">**IKEEXT\_AUTHENTICATION\_METHOD1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [<span data-ttu-id="c8da9-107">**\_METHOD2 проверки подлинности IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-107">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="c8da9-108">**\_EKUS0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-108">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="c8da9-109">**\_NAME0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-109">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="c8da9-110">**\_ \_ Корневой CONFIG0 сертификата IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-110">**IKEEXT\_CERT\_ROOT\_CONFIG0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [<span data-ttu-id="c8da9-111">**\_AUTHENTICATION0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-111">**IKEEXT\_CERTIFICATE\_AUTHENTICATION0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [<span data-ttu-id="c8da9-112">**\_AUTHENTICATION1 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-112">**IKEEXT\_CERTIFICATE\_AUTHENTICATION1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [<span data-ttu-id="c8da9-113">**\_Добавьте сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-113">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="c8da9-114">**\_CREDENTIAL0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-114">**IKEEXT\_CERTIFICATE\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [<span data-ttu-id="c8da9-115">**\_Учетные данные1 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-115">**IKEEXT\_CERTIFICATE\_CREDENTIAL1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [<span data-ttu-id="c8da9-116">**\_CRITERIA0 сертификата \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-116">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="c8da9-117">**\_ALGORITHM0 шифра IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-117">**IKEEXT\_CIPHER\_ALGORITHM0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [<span data-ttu-id="c8da9-118">**\_Общие \_ STATISTICS0и IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-118">**IKEEXT\_COMMON\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [<span data-ttu-id="c8da9-119">**\_Общие \_ STATISTICS1и IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-119">**IKEEXT\_COMMON\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [<span data-ttu-id="c8da9-120">**\_PAIR0 cookie \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-120">**IKEEXT\_COOKIE\_PAIR0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [<span data-ttu-id="c8da9-121">**\_CREDENTIAL0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-121">**IKEEXT\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [<span data-ttu-id="c8da9-122">**\_УЧЕТНЫЕ ДАННЫЕ1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-122">**IKEEXT\_CREDENTIAL1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [<span data-ttu-id="c8da9-123">**\_УЧЕТНЫЕ ДАННЫЕ2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-123">**IKEEXT\_CREDENTIAL2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [<span data-ttu-id="c8da9-124">**\_CREDENTIALS0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-124">**IKEEXT\_CREDENTIALS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [<span data-ttu-id="c8da9-125">**\_CREDENTIALS1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-125">**IKEEXT\_CREDENTIALS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [<span data-ttu-id="c8da9-126">**\_CREDENTIALS2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-126">**IKEEXT\_CREDENTIALS2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [<span data-ttu-id="c8da9-127">**\_PAIR0 учетных данных для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-127">**IKEEXT\_CREDENTIAL\_PAIR0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [<span data-ttu-id="c8da9-128">**\_PAIR1 учетных данных для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-128">**IKEEXT\_CREDENTIAL\_PAIR1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [<span data-ttu-id="c8da9-129">**\_PAIR2 учетных данных для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-129">**IKEEXT\_CREDENTIAL\_PAIR2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [<span data-ttu-id="c8da9-130">**\_AUTHENTICATION0 EAP для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-130">**IKEEXT\_EAP\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [<span data-ttu-id="c8da9-131">**\_POLICY0 EM для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-131">**IKEEXT\_EM\_POLICY0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [<span data-ttu-id="c8da9-132">**\_POLICY1 EM для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-132">**IKEEXT\_EM\_POLICY1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [<span data-ttu-id="c8da9-133">**\_POLICY2 EM для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-133">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="c8da9-134">**\_ALGORITHM0 целостность IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-134">**IKEEXT\_INTEGRITY\_ALGORITHM0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [<span data-ttu-id="c8da9-135">**\_ \_ \_ Конкретные \_ Общие \_ STATISTICS0 для IP-версии IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-135">**IKEEXT\_IP\_VERSION\_SPECIFIC\_COMMON\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [<span data-ttu-id="c8da9-136">**\_ \_ \_ Конкретные \_ Общие \_ STATISTICS1 для IP-версии IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-136">**IKEEXT\_IP\_VERSION\_SPECIFIC\_COMMON\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [<span data-ttu-id="c8da9-137">**\_IP- \_ версия IKEEXT для \_ конкретного \_ кэймодуле \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="c8da9-137">**IKEEXT\_IP\_VERSION\_SPECIFIC\_KEYMODULE\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [<span data-ttu-id="c8da9-138">**\_IP- \_ версия IKEEXT для \_ конкретного \_ кэймодуле \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="c8da9-138">**IKEEXT\_IP\_VERSION\_SPECIFIC\_KEYMODULE\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [<span data-ttu-id="c8da9-139">**IKEEXT \_ IPv6 \_ КГА \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="c8da9-139">**IKEEXT\_IPV6\_CGA\_AUTHENTICATION0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [<span data-ttu-id="c8da9-140">**IKEEXT \_ Kerberos \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="c8da9-140">**IKEEXT\_KERBEROS\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [<span data-ttu-id="c8da9-141">**IKEEXT \_ Kerberos \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="c8da9-141">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="c8da9-142">**IKEEXT \_ кэймодуле \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="c8da9-142">**IKEEXT\_KEYMODULE\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [<span data-ttu-id="c8da9-143">**IKEEXT \_ кэймодуле \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="c8da9-143">**IKEEXT\_KEYMODULE\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [<span data-ttu-id="c8da9-144">**\_Имя IKEEXT \_ CREDENTIAL0**</span><span class="sxs-lookup"><span data-stu-id="c8da9-144">**IKEEXT\_NAME\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [<span data-ttu-id="c8da9-145">**\_ \_ \_ AUTHENTICATION0а NTLM v2**</span><span class="sxs-lookup"><span data-stu-id="c8da9-145">**IKEEXT\_NTLM\_V2\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [<span data-ttu-id="c8da9-146">**\_POLICY0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-146">**IKEEXT\_POLICY0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [<span data-ttu-id="c8da9-147">**\_POLICY1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-147">**IKEEXT\_POLICY1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [<span data-ttu-id="c8da9-148">**\_POLICY2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-148">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="c8da9-149">**\_AUTHENTICATION0 с общим \_ ключом \_ для IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-149">**IKEEXT\_PRESHARED\_KEY\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [<span data-ttu-id="c8da9-150">**\_AUTHENTICATION1 с общим \_ ключом \_ для IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-150">**IKEEXT\_PRESHARED\_KEY\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [<span data-ttu-id="c8da9-151">**\_PROPOSAL0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-151">**IKEEXT\_PROPOSAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [<span data-ttu-id="c8da9-152">**\_Зарезервированные \_ AUTHENTICATION0ные IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-152">**IKEEXT\_RESERVED\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [<span data-ttu-id="c8da9-153">**\_DETAILS0 SA \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-153">**IKEEXT\_SA\_DETAILS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [<span data-ttu-id="c8da9-154">**\_DETAILS1 SA \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-154">**IKEEXT\_SA\_DETAILS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [<span data-ttu-id="c8da9-155">**\_DETAILS2 SA \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-155">**IKEEXT\_SA\_DETAILS2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [<span data-ttu-id="c8da9-156">**\_ \_ TEMPLATE0 перечисления SA для IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="c8da9-156">**IKEEXT\_SA\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [<span data-ttu-id="c8da9-157">**\_STATISTICS0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-157">**IKEEXT\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [<span data-ttu-id="c8da9-158">**\_STATISTICS1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-158">**IKEEXT\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [<span data-ttu-id="c8da9-159">**\_TRAFFIC0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="c8da9-159">**IKEEXT\_TRAFFIC0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




