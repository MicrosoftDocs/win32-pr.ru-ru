---
title: Класс MDM_Policy_Config01_Browser02
description: '\_Класс политики MDM \_ Config01 \_ Browser02 представляет доступные политики браузера.'
ms.assetid: 296e3be4-3bc1-4e06-9e31-532639a0b912
keywords:
- Класс MDM_Policy_Config01_Browser02
- MDM_Policy_Config01_Browser02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Browser02
- MDM_Policy_Config01_Browser02.InstanceID
- MDM_Policy_Config01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba68b4d3f6798a448447e7773dc299977c54434c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071432"
---
# <a name="mdm_policy_config01_browser02-class"></a><span data-ttu-id="9466e-105">\_Класс политики MDM \_ Config01 \_ Browser02</span><span class="sxs-lookup"><span data-stu-id="9466e-105">MDM\_Policy\_Config01\_Browser02 class</span></span>

<span data-ttu-id="9466e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9466e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9466e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9466e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9466e-108">Класс **\_ политики MDM \_ Config01 \_ Browser02** представляет доступные политики браузера.</span><span class="sxs-lookup"><span data-stu-id="9466e-108">The **MDM\_Policy\_Config01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="9466e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9466e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9466e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9466e-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Browser02
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

## <a name="members"></a><span data-ttu-id="9466e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9466e-111">Members</span></span>

<span data-ttu-id="9466e-112">Класс **\_ политики MDM \_ Config01 \_ Browser02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9466e-112">The **MDM\_Policy\_Config01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="9466e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9466e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9466e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9466e-114">Properties</span></span>

<span data-ttu-id="9466e-115">Класс **\_ политики MDM \_ Config01 \_ Browser02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9466e-115">The **MDM\_Policy\_Config01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9466e-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="9466e-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="9466e-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="9466e-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="9466e-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="9466e-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="9466e-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="9466e-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="9466e-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="9466e-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="9466e-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="9466e-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="9466e-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="9466e-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="9466e-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="9466e-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-161">алвайсенаблебукслибрари</span><span class="sxs-lookup"><span data-stu-id="9466e-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="9466e-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="9466e-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="9466e-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="9466e-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9466e-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-179">Домашние страницы</span><span class="sxs-lookup"><span data-stu-id="9466e-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9466e-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9466e-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9466e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9466e-185">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9466e-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9466e-186">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="9466e-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="9466e-187">Для этого класса строка имеет значение "Browser".</span><span class="sxs-lookup"><span data-stu-id="9466e-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="9466e-188">локкдовнфаворитес</span><span class="sxs-lookup"><span data-stu-id="9466e-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-189">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9466e-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9466e-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9466e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9466e-194">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9466e-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9466e-195">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="9466e-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="9466e-196">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="9466e-196">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="9466e-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="9466e-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-198">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="9466e-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-201">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="9466e-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-204">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="9466e-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-207">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="9466e-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-210">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="9466e-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-213">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-215">провисионфаворитес</span><span class="sxs-lookup"><span data-stu-id="9466e-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="9466e-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-219">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="9466e-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-222">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9466e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-224">шовмессажевхенопенингситесининтернетексплорер</span><span class="sxs-lookup"><span data-stu-id="9466e-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-225">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9466e-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="9466e-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9466e-228">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9466e-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9466e-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9466e-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9466e-230">Требования</span><span class="sxs-lookup"><span data-stu-id="9466e-230">Requirements</span></span>



| <span data-ttu-id="9466e-231">Требование</span><span class="sxs-lookup"><span data-stu-id="9466e-231">Requirement</span></span> | <span data-ttu-id="9466e-232">Значение</span><span class="sxs-lookup"><span data-stu-id="9466e-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9466e-233">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9466e-233">Minimum supported client</span></span><br/> | <span data-ttu-id="9466e-234">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9466e-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9466e-235">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9466e-235">Minimum supported server</span></span><br/> | <span data-ttu-id="9466e-236">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9466e-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9466e-237">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9466e-237">Namespace</span></span><br/>                | <span data-ttu-id="9466e-238">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9466e-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9466e-239">MOF</span><span class="sxs-lookup"><span data-stu-id="9466e-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9466e-240"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9466e-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9466e-241">DLL</span><span class="sxs-lookup"><span data-stu-id="9466e-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9466e-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9466e-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9466e-243">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9466e-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9466e-244">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="9466e-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

