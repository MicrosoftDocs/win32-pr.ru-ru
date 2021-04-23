---
title: Класс MDM_Policy_Result01_AppVirtualization02
description: '\_Класс политики MDM \_ Result01 \_ AppVirtualization02 представляет доступные политики виртуализации приложений.'
ms.assetid: fc28646f-f4b9-4648-a22d-b90d32ff888f
keywords:
- Класс MDM_Policy_Result01_AppVirtualization02
- MDM_Policy_Result01_AppVirtualization02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AppVirtualization02
- MDM_Policy_Result01_AppVirtualization02.InstanceID
- MDM_Policy_Result01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968c4718d7978bdf6770bdf8f828e6ef268cd32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491175"
---
# <a name="mdm_policy_result01_appvirtualization02-class"></a><span data-ttu-id="aafa9-105">\_Класс политики MDM \_ Result01 \_ AppVirtualization02</span><span class="sxs-lookup"><span data-stu-id="aafa9-105">MDM\_Policy\_Result01\_AppVirtualization02 class</span></span>

<span data-ttu-id="aafa9-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="aafa9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aafa9-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="aafa9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aafa9-108">\_Класс политики MDM \_ Result01 \_ AppVirtualization02 представляет доступные политики виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="aafa9-108">The MDM\_Policy\_Result01\_AppVirtualization02 class represents the available app virtualization policies.</span></span>

<span data-ttu-id="aafa9-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="aafa9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafa9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aafa9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AppVirtualization02
{
  string InstanceID;
  string ParentID;
  string AllowAppVClient;
  string AllowDynamicVirtualization;
  string AllowPackageCleanup;
  string AllowPackageScripts;
  string AllowPublishingRefreshUX;
  string AllowReportingServer;
  string AllowRoamingFileExclusions;
  string AllowRoamingRegistryExclusions;
  string AllowStreamingAutoload;
  string ClientCoexistenceAllowMigrationmode;
  string IntegrationAllowRootGlobal;
  string IntegrationAllowRootUser;
  string PublishingAllowServer1;
  string PublishingAllowServer2;
  string PublishingAllowServer3;
  string PublishingAllowServer4;
  string PublishingAllowServer5;
  string StreamingAllowCertificateFilterForClient_SSL;
  string StreamingAllowHighCostLaunch;
  string StreamingAllowLocationProvider;
  string StreamingAllowPackageInstallationRoot;
  string StreamingAllowPackageSourceRoot;
  string StreamingAllowReestablishmentInterval;
  string StreamingAllowReestablishmentRetries;
  string StreamingSharedContentStoreMode;
  string StreamingSupportBranchCache;
  string StreamingVerifyCertificateRevocationList;
  string VirtualComponentsAllowList;
};
```

## <a name="members"></a><span data-ttu-id="aafa9-111">Члены</span><span class="sxs-lookup"><span data-stu-id="aafa9-111">Members</span></span>

<span data-ttu-id="aafa9-112">Класс **\_ политики MDM \_ Result01 \_ AppVirtualization02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aafa9-112">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="aafa9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="aafa9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aafa9-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="aafa9-114">Properties</span></span>

<span data-ttu-id="aafa9-115">Класс **\_ политики MDM \_ Result01 \_ AppVirtualization02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aafa9-115">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="aafa9-116">алловаппвклиент</span><span class="sxs-lookup"><span data-stu-id="aafa9-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-119">алловдинамиквиртуализатион</span><span class="sxs-lookup"><span data-stu-id="aafa9-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-122">алловпаккажеклеануп</span><span class="sxs-lookup"><span data-stu-id="aafa9-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-125">алловпаккажескриптс</span><span class="sxs-lookup"><span data-stu-id="aafa9-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-128">алловпублишингрефрешукс</span><span class="sxs-lookup"><span data-stu-id="aafa9-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-131">алловрепортингсервер</span><span class="sxs-lookup"><span data-stu-id="aafa9-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-134">алловроамингфиликсклусионс</span><span class="sxs-lookup"><span data-stu-id="aafa9-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-137">алловроамингрегистрексклусионс</span><span class="sxs-lookup"><span data-stu-id="aafa9-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-140">алловстреамингаутолоад</span><span class="sxs-lookup"><span data-stu-id="aafa9-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-143">клиенткоексистенцеалловмигратионмоде</span><span class="sxs-lookup"><span data-stu-id="aafa9-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aafa9-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aafa9-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aafa9-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-149">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aafa9-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-150">интегратионалловрутглобал</span><span class="sxs-lookup"><span data-stu-id="aafa9-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-153">интегратионалловрутусер</span><span class="sxs-lookup"><span data-stu-id="aafa9-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aafa9-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="aafa9-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aafa9-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-159">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aafa9-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="aafa9-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="aafa9-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="aafa9-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="aafa9-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-171">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="aafa9-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-175">Стреамингалловцертификатефилтерфорклиент \_ SSL</span><span class="sxs-lookup"><span data-stu-id="aafa9-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-177">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-178">стреамингалловхигхкостлаунч</span><span class="sxs-lookup"><span data-stu-id="aafa9-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-181">стреамингалловлокатионпровидер</span><span class="sxs-lookup"><span data-stu-id="aafa9-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-183">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-184">стреамингалловпаккажеинсталлатионрут</span><span class="sxs-lookup"><span data-stu-id="aafa9-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-186">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-187">стреамингалловпаккажесаурцерут</span><span class="sxs-lookup"><span data-stu-id="aafa9-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-189">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-190">стреамингалловристаблишментинтервал</span><span class="sxs-lookup"><span data-stu-id="aafa9-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-193">стреамингалловристаблишментретриес</span><span class="sxs-lookup"><span data-stu-id="aafa9-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-195">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-196">стреамингшаредконтентсторемоде</span><span class="sxs-lookup"><span data-stu-id="aafa9-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-199">стреамингсуппортбранчкаче</span><span class="sxs-lookup"><span data-stu-id="aafa9-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-201">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-202">стреамингверифицертификатеревокатионлист</span><span class="sxs-lookup"><span data-stu-id="aafa9-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-204">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aafa9-205">виртуалкомпонентсалловлист</span><span class="sxs-lookup"><span data-stu-id="aafa9-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aafa9-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aafa9-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aafa9-207">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="aafa9-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aafa9-208">Требования</span><span class="sxs-lookup"><span data-stu-id="aafa9-208">Requirements</span></span>



| <span data-ttu-id="aafa9-209">Требование</span><span class="sxs-lookup"><span data-stu-id="aafa9-209">Requirement</span></span> | <span data-ttu-id="aafa9-210">Значение</span><span class="sxs-lookup"><span data-stu-id="aafa9-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aafa9-211">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aafa9-211">Minimum supported client</span></span><br/> | <span data-ttu-id="aafa9-212">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="aafa9-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aafa9-213">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aafa9-213">Minimum supported server</span></span><br/> | <span data-ttu-id="aafa9-214">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aafa9-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="aafa9-215">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aafa9-215">Namespace</span></span><br/>                | <span data-ttu-id="aafa9-216">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="aafa9-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="aafa9-217">MOF</span><span class="sxs-lookup"><span data-stu-id="aafa9-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aafa9-218"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aafa9-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aafa9-219">DLL</span><span class="sxs-lookup"><span data-stu-id="aafa9-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aafa9-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aafa9-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

