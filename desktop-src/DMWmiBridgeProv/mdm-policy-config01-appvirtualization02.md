---
title: Класс MDM_Policy_Config01_AppVirtualization02
description: '\_Класс политики MDM \_ Config01 \_ AppVirtualization02 настраивает доступные политики виртуализации приложений.'
ms.assetid: d270704c-8652-4f97-89f7-fcb6e68ee6fe
keywords:
- Класс MDM_Policy_Config01_AppVirtualization02
- MDM_Policy_Config01_AppVirtualization02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AppVirtualization02
- MDM_Policy_Config01_AppVirtualization02.InstanceID
- MDM_Policy_Config01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871d09b306cff2833601100d9a645cde5c59e33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135559"
---
# <a name="mdm_policy_config01_appvirtualization02-class"></a><span data-ttu-id="9e025-105">\_Класс политики MDM \_ Config01 \_ AppVirtualization02</span><span class="sxs-lookup"><span data-stu-id="9e025-105">MDM\_Policy\_Config01\_AppVirtualization02 class</span></span>

<span data-ttu-id="9e025-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9e025-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9e025-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9e025-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9e025-108">\_Класс политики MDM \_ Config01 \_ AppVirtualization02 настраивает доступные политики виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="9e025-108">The MDM\_Policy\_Config01\_AppVirtualization02 class configures the available app virtualization policies.</span></span>

<span data-ttu-id="9e025-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9e025-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e025-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e025-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AppVirtualization02
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

## <a name="members"></a><span data-ttu-id="9e025-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9e025-111">Members</span></span>

<span data-ttu-id="9e025-112">Класс **\_ политики MDM \_ Config01 \_ AppVirtualization02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9e025-112">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="9e025-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9e025-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e025-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9e025-114">Properties</span></span>

<span data-ttu-id="9e025-115">Класс **\_ политики MDM \_ Config01 \_ AppVirtualization02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9e025-115">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9e025-116">алловаппвклиент</span><span class="sxs-lookup"><span data-stu-id="9e025-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-119">алловдинамиквиртуализатион</span><span class="sxs-lookup"><span data-stu-id="9e025-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-122">алловпаккажеклеануп</span><span class="sxs-lookup"><span data-stu-id="9e025-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-125">алловпаккажескриптс</span><span class="sxs-lookup"><span data-stu-id="9e025-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-128">алловпублишингрефрешукс</span><span class="sxs-lookup"><span data-stu-id="9e025-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-131">алловрепортингсервер</span><span class="sxs-lookup"><span data-stu-id="9e025-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-134">алловроамингфиликсклусионс</span><span class="sxs-lookup"><span data-stu-id="9e025-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-137">алловроамингрегистрексклусионс</span><span class="sxs-lookup"><span data-stu-id="9e025-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-140">алловстреамингаутолоад</span><span class="sxs-lookup"><span data-stu-id="9e025-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-143">клиенткоексистенцеалловмигратионмоде</span><span class="sxs-lookup"><span data-stu-id="9e025-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e025-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9e025-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9e025-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e025-149">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9e025-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-150">интегратионалловрутглобал</span><span class="sxs-lookup"><span data-stu-id="9e025-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-153">интегратионалловрутусер</span><span class="sxs-lookup"><span data-stu-id="9e025-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e025-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9e025-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9e025-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e025-159">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9e025-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="9e025-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="9e025-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="9e025-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="9e025-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-171">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="9e025-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-175">Стреамингалловцертификатефилтерфорклиент \_ SSL</span><span class="sxs-lookup"><span data-stu-id="9e025-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-177">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-178">стреамингалловхигхкостлаунч</span><span class="sxs-lookup"><span data-stu-id="9e025-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-181">стреамингалловлокатионпровидер</span><span class="sxs-lookup"><span data-stu-id="9e025-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-183">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-184">стреамингалловпаккажеинсталлатионрут</span><span class="sxs-lookup"><span data-stu-id="9e025-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-186">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-187">стреамингалловпаккажесаурцерут</span><span class="sxs-lookup"><span data-stu-id="9e025-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-189">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-190">стреамингалловристаблишментинтервал</span><span class="sxs-lookup"><span data-stu-id="9e025-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-193">стреамингалловристаблишментретриес</span><span class="sxs-lookup"><span data-stu-id="9e025-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-195">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-196">стреамингшаредконтентсторемоде</span><span class="sxs-lookup"><span data-stu-id="9e025-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-199">стреамингсуппортбранчкаче</span><span class="sxs-lookup"><span data-stu-id="9e025-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-201">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-202">стреамингверифицертификатеревокатионлист</span><span class="sxs-lookup"><span data-stu-id="9e025-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-204">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9e025-205">виртуалкомпонентсалловлист</span><span class="sxs-lookup"><span data-stu-id="9e025-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e025-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9e025-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e025-207">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9e025-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e025-208">Требования</span><span class="sxs-lookup"><span data-stu-id="9e025-208">Requirements</span></span>



| <span data-ttu-id="9e025-209">Требование</span><span class="sxs-lookup"><span data-stu-id="9e025-209">Requirement</span></span> | <span data-ttu-id="9e025-210">Значение</span><span class="sxs-lookup"><span data-stu-id="9e025-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e025-211">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e025-211">Minimum supported client</span></span><br/> | <span data-ttu-id="9e025-212">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9e025-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e025-213">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e025-213">Minimum supported server</span></span><br/> | <span data-ttu-id="9e025-214">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9e025-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9e025-215">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9e025-215">Namespace</span></span><br/>                | <span data-ttu-id="9e025-216">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9e025-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9e025-217">MOF</span><span class="sxs-lookup"><span data-stu-id="9e025-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e025-218"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e025-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e025-219">DLL</span><span class="sxs-lookup"><span data-stu-id="9e025-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e025-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e025-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

