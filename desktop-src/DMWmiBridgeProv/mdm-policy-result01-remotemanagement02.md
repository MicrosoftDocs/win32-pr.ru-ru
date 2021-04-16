---
title: Класс MDM_Policy_Result01_RemoteManagement02
description: '\_Класс политики MDM \_ Result01 \_ RemoteManagement02 представляет политики удаленного управления.'
ms.assetid: f6eb96ff-a40e-4602-a812-786d1a89bf12
keywords:
- Класс MDM_Policy_Result01_RemoteManagement02
- MDM_Policy_Result01_RemoteManagement02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteManagement02
- MDM_Policy_Result01_RemoteManagement02.InstanceID
- MDM_Policy_Result01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a60228e39c8e1d6604534c8bd052ec7d40105e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489210"
---
# <a name="mdm_policy_result01_remotemanagement02-class"></a><span data-ttu-id="f0705-105">\_Класс политики MDM \_ Result01 \_ RemoteManagement02</span><span class="sxs-lookup"><span data-stu-id="f0705-105">MDM\_Policy\_Result01\_RemoteManagement02 class</span></span>

<span data-ttu-id="f0705-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f0705-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f0705-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f0705-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f0705-108">\_Класс политики MDM \_ Result01 \_ RemoteManagement02 представляет политики удаленного управления.</span><span class="sxs-lookup"><span data-stu-id="f0705-108">The MDM\_Policy\_Result01\_RemoteManagement02 class represents the remote management policies.</span></span>

<span data-ttu-id="f0705-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f0705-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0705-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0705-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a><span data-ttu-id="f0705-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f0705-111">Members</span></span>

<span data-ttu-id="f0705-112">Класс **\_ политики MDM \_ Result01 \_ RemoteManagement02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f0705-112">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="f0705-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f0705-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0705-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f0705-114">Properties</span></span>

<span data-ttu-id="f0705-115">Класс **\_ политики MDM \_ Result01 \_ RemoteManagement02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f0705-115">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f0705-116">\_Клиент алловбасикаусентикатион</span><span class="sxs-lookup"><span data-stu-id="f0705-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-119">\_Служба алловбасикаусентикатион</span><span class="sxs-lookup"><span data-stu-id="f0705-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-122">алловкредсспаусентикатионклиент</span><span class="sxs-lookup"><span data-stu-id="f0705-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-125">алловкредсспаусентикатионсервице</span><span class="sxs-lookup"><span data-stu-id="f0705-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-128">алловремотесерверманажемент</span><span class="sxs-lookup"><span data-stu-id="f0705-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-131">\_Клиент алловуненкриптедтраффик</span><span class="sxs-lookup"><span data-stu-id="f0705-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-134">\_Служба алловуненкриптедтраффик</span><span class="sxs-lookup"><span data-stu-id="f0705-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-137">дисалловдижестаусентикатион</span><span class="sxs-lookup"><span data-stu-id="f0705-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-140">дисалловнеготиатеаусентикатионклиент</span><span class="sxs-lookup"><span data-stu-id="f0705-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-143">дисалловнеготиатеаусентикатионсервице</span><span class="sxs-lookup"><span data-stu-id="f0705-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-146">дисалловсторингофрунаскредентиалс</span><span class="sxs-lookup"><span data-stu-id="f0705-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0705-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0705-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0705-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0705-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0705-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0705-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f0705-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0705-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0705-156">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0705-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-157">спеЦифичаннелбиндингтокенхарденинглевел</span><span class="sxs-lookup"><span data-stu-id="f0705-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="f0705-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-163">турнонкомпатибилитихттплистенер</span><span class="sxs-lookup"><span data-stu-id="f0705-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0705-166">турнонкомпатибилитихттпслистенер</span><span class="sxs-lookup"><span data-stu-id="f0705-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0705-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0705-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0705-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0705-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0705-169">Требования</span><span class="sxs-lookup"><span data-stu-id="f0705-169">Requirements</span></span>



| <span data-ttu-id="f0705-170">Требование</span><span class="sxs-lookup"><span data-stu-id="f0705-170">Requirement</span></span> | <span data-ttu-id="f0705-171">Значение</span><span class="sxs-lookup"><span data-stu-id="f0705-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0705-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0705-172">Minimum supported client</span></span><br/> | <span data-ttu-id="f0705-173">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f0705-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0705-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0705-174">Minimum supported server</span></span><br/> | <span data-ttu-id="f0705-175">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0705-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f0705-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0705-176">Namespace</span></span><br/>                | <span data-ttu-id="f0705-177">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f0705-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f0705-178">MOF</span><span class="sxs-lookup"><span data-stu-id="f0705-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0705-179"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0705-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0705-180">DLL</span><span class="sxs-lookup"><span data-stu-id="f0705-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0705-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0705-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

