---
title: Класс MDM_Policy_Result01_Browser02
description: '\_Класс политики MDM \_ Result01 \_ Browser02 представляет доступные политики браузера. \_Класс политики MDM \_ Result01 \_ Browser02 представляет доступные политики браузера.'
ms.assetid: 06dc9f68-d9ea-4eec-93cb-1f26e8a6050d
keywords:
- Класс MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02.InstanceID
- MDM_Policy_Result01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d132c43b88b242864e248b705a0f6bca02e546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891485"
---
# <a name="mdm_policy_result01_browser02-class"></a><span data-ttu-id="2f5dc-105">\_Класс политики MDM \_ Result01 \_ Browser02</span><span class="sxs-lookup"><span data-stu-id="2f5dc-105">MDM\_Policy\_Result01\_Browser02 class</span></span>

<span data-ttu-id="2f5dc-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="2f5dc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2f5dc-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="2f5dc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2f5dc-108">Класс **\_ политики MDM \_ Result01 \_ Browser02** представляет доступные политики браузера.</span><span class="sxs-lookup"><span data-stu-id="2f5dc-108">The **MDM\_Policy\_Result01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="2f5dc-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2f5dc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5dc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f5dc-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Browser02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddressBarDropdown;
  sint32 AllowAutofill;
  sint32 AllowCookies;
  sint32 AllowDeveloperTools;
  sint32 AllowInPrivate;
  sint32 AllowMicrosoftCompatibilityList;
  sint32 AllowDoNotTrack;
  sint32 AllowFlashClickToRun;
  sint32 AllowFlash;
  sint32 AllowExtensions;
  sint32 AllowPasswordManager;
  sint32 AllowPopups;
  sint32 AllowSearchEngineCustomization;
  sint32 AllowSearchSuggestionsinAddressBar;
  sint32 AllowSmartScreen;
  sint32 AlwaysEnableBooksLibrary;
  sint32 DisableLockdownOfStartPages;
  string ConfigureAdditionalSearchEngines;
  sint32 ClearBrowsingDataOnExit;
  string EnterpriseModeSiteList;
  string EnterpriseSiteListServiceUrl;
  string Homepages;
  sint32 LockdownFavorites;
  sint32 PreventAccessToAboutFlagsInMicrosoftEdge;
  sint32 PreventLiveTileDataCollection;
  sint32 PreventFirstRunPage;
  sint32 PreventSmartScreenPromptOverride;
  sint32 PreventSmartScreenPromptOverrideForFiles;
  sint32 PreventUsingLocalHostIPAddressForWebRTC;
  string ProvisionFavorites;
  sint32 SendIntranetTraffictoInternetExplorer;
  string SetDefaultSearchEngine;
  sint32 ShowMessageWhenOpeningSitesInInternetExplorer;
  sint32 SyncFavoritesBetweenIEAndMicrosoftEdge;
};
```

## <a name="members"></a><span data-ttu-id="2f5dc-111">Члены</span><span class="sxs-lookup"><span data-stu-id="2f5dc-111">Members</span></span>

<span data-ttu-id="2f5dc-112">Класс **\_ политики MDM \_ Result01 \_ Browser02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2f5dc-112">The **MDM\_Policy\_Result01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="2f5dc-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2f5dc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f5dc-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="2f5dc-114">Properties</span></span>

<span data-ttu-id="2f5dc-115">Класс **\_ политики MDM \_ Result01 \_ Browser02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2f5dc-115">The **MDM\_Policy\_Result01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2f5dc-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="2f5dc-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="2f5dc-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="2f5dc-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="2f5dc-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="2f5dc-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="2f5dc-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="2f5dc-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="2f5dc-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="2f5dc-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="2f5dc-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="2f5dc-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="2f5dc-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="2f5dc-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="2f5dc-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="2f5dc-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-161">алвайсенаблебукслибрари</span><span class="sxs-lookup"><span data-stu-id="2f5dc-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="2f5dc-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="2f5dc-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="2f5dc-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="2f5dc-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2f5dc-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-179">Домашние страницы</span><span class="sxs-lookup"><span data-stu-id="2f5dc-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2f5dc-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f5dc-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-185">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f5dc-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f5dc-186">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="2f5dc-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="2f5dc-187">Для этого класса строка имеет значение "Browser".</span><span class="sxs-lookup"><span data-stu-id="2f5dc-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="2f5dc-188">локкдовнфаворитес</span><span class="sxs-lookup"><span data-stu-id="2f5dc-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-189">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2f5dc-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f5dc-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-194">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2f5dc-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2f5dc-195">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="2f5dc-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="2f5dc-196">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="2f5dc-196">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="2f5dc-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="2f5dc-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-198">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="2f5dc-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-201">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="2f5dc-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-204">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="2f5dc-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-207">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="2f5dc-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-210">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="2f5dc-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-213">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-215">провисионфаворитес</span><span class="sxs-lookup"><span data-stu-id="2f5dc-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="2f5dc-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-219">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="2f5dc-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-224">шовмессажевхенопенингситесининтернетексплорер</span><span class="sxs-lookup"><span data-stu-id="2f5dc-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-225">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2f5dc-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="2f5dc-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f5dc-228">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2f5dc-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f5dc-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f5dc-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f5dc-230">Требования</span><span class="sxs-lookup"><span data-stu-id="2f5dc-230">Requirements</span></span>



| <span data-ttu-id="2f5dc-231">Требование</span><span class="sxs-lookup"><span data-stu-id="2f5dc-231">Requirement</span></span> | <span data-ttu-id="2f5dc-232">Значение</span><span class="sxs-lookup"><span data-stu-id="2f5dc-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5dc-233">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f5dc-233">Minimum supported client</span></span><br/> | <span data-ttu-id="2f5dc-234">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2f5dc-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f5dc-235">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f5dc-235">Minimum supported server</span></span><br/> | <span data-ttu-id="2f5dc-236">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2f5dc-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2f5dc-237">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2f5dc-237">Namespace</span></span><br/>                | <span data-ttu-id="2f5dc-238">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="2f5dc-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="2f5dc-239">MOF</span><span class="sxs-lookup"><span data-stu-id="2f5dc-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f5dc-240"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f5dc-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f5dc-241">DLL</span><span class="sxs-lookup"><span data-stu-id="2f5dc-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f5dc-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f5dc-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f5dc-243">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f5dc-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f5dc-244">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="2f5dc-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

