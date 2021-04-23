---
title: Класс MDM_Policy_Config01_RemoteManagement02
description: Политики \_ \_ \_ удаленного управления MDM Config01 RemoteManagement02.
ms.assetid: 2eabbf72-00a4-4c61-9ae1-ff49067cb502
keywords:
- Класс MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02.InstanceID
- MDM_Policy_Config01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76aa1a04735897d0b1c8f0e16572dd124b601c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891890"
---
# <a name="mdm_policy_config01_remotemanagement02-class"></a><span data-ttu-id="e8d59-105">\_Класс политики MDM \_ Config01 \_ RemoteManagement02</span><span class="sxs-lookup"><span data-stu-id="e8d59-105">MDM\_Policy\_Config01\_RemoteManagement02 class</span></span>

<span data-ttu-id="e8d59-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e8d59-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e8d59-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e8d59-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e8d59-108">Политики \_ \_ \_ удаленного управления MDM Config01 RemoteManagement02.</span><span class="sxs-lookup"><span data-stu-id="e8d59-108">The MDM\_Policy\_Config01\_RemoteManagement02 remote management policies.</span></span>

<span data-ttu-id="e8d59-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e8d59-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d59-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8d59-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteManagement02
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

## <a name="members"></a><span data-ttu-id="e8d59-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e8d59-111">Members</span></span>

<span data-ttu-id="e8d59-112">Класс **\_ политики MDM \_ Config01 \_ RemoteManagement02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e8d59-112">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="e8d59-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8d59-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8d59-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8d59-114">Properties</span></span>

<span data-ttu-id="e8d59-115">Класс **\_ политики MDM \_ Config01 \_ RemoteManagement02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e8d59-115">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e8d59-116">\_Клиент алловбасикаусентикатион</span><span class="sxs-lookup"><span data-stu-id="e8d59-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-119">\_Служба алловбасикаусентикатион</span><span class="sxs-lookup"><span data-stu-id="e8d59-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-122">алловкредсспаусентикатионклиент</span><span class="sxs-lookup"><span data-stu-id="e8d59-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-125">алловкредсспаусентикатионсервице</span><span class="sxs-lookup"><span data-stu-id="e8d59-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-128">алловремотесерверманажемент</span><span class="sxs-lookup"><span data-stu-id="e8d59-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-131">\_Клиент алловуненкриптедтраффик</span><span class="sxs-lookup"><span data-stu-id="e8d59-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-134">\_Служба алловуненкриптедтраффик</span><span class="sxs-lookup"><span data-stu-id="e8d59-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-137">дисалловдижестаусентикатион</span><span class="sxs-lookup"><span data-stu-id="e8d59-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-140">дисалловнеготиатеаусентикатионклиент</span><span class="sxs-lookup"><span data-stu-id="e8d59-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-143">дисалловнеготиатеаусентикатионсервице</span><span class="sxs-lookup"><span data-stu-id="e8d59-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-146">дисалловсторингофрунаскредентиалс</span><span class="sxs-lookup"><span data-stu-id="e8d59-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8d59-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e8d59-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8d59-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8d59-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8d59-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e8d59-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8d59-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-156">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8d59-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-157">спеЦифичаннелбиндингтокенхарденинглевел</span><span class="sxs-lookup"><span data-stu-id="e8d59-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="e8d59-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-163">турнонкомпатибилитихттплистенер</span><span class="sxs-lookup"><span data-stu-id="e8d59-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8d59-166">турнонкомпатибилитихттпслистенер</span><span class="sxs-lookup"><span data-stu-id="e8d59-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8d59-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8d59-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8d59-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8d59-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8d59-169">Требования</span><span class="sxs-lookup"><span data-stu-id="e8d59-169">Requirements</span></span>



| <span data-ttu-id="e8d59-170">Требование</span><span class="sxs-lookup"><span data-stu-id="e8d59-170">Requirement</span></span> | <span data-ttu-id="e8d59-171">Значение</span><span class="sxs-lookup"><span data-stu-id="e8d59-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d59-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8d59-172">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d59-173">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e8d59-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8d59-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8d59-174">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d59-175">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e8d59-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e8d59-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8d59-176">Namespace</span></span><br/>                | <span data-ttu-id="e8d59-177">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e8d59-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e8d59-178">MOF</span><span class="sxs-lookup"><span data-stu-id="e8d59-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8d59-179"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8d59-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8d59-180">DLL</span><span class="sxs-lookup"><span data-stu-id="e8d59-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8d59-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8d59-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

