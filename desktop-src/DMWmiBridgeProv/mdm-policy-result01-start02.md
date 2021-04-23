---
title: Класс MDM_Policy_Result01_Start02
description: '\_Класс политики MDM \_ Result01 \_ Start02 представляет доступные политики начального экрана.'
ms.assetid: 997d64f9-b2be-47b8-8a84-97438e7fa842
keywords:
- Класс MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02.InstanceID
- MDM_Policy_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412e9ccecdc9f691b03a94ba5528eb6b7e3d7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071504"
---
# <a name="mdm_policy_result01_start02-class"></a><span data-ttu-id="84701-105">\_Класс политики MDM \_ Result01 \_ Start02</span><span class="sxs-lookup"><span data-stu-id="84701-105">MDM\_Policy\_Result01\_Start02 class</span></span>

<span data-ttu-id="84701-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="84701-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="84701-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="84701-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="84701-108">Класс **\_ политики MDM \_ Result01 \_ Start02** представляет доступные политики начального экрана.</span><span class="sxs-lookup"><span data-stu-id="84701-108">The **MDM\_Policy\_Result01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="84701-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="84701-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84701-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84701-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 AllowPinnedFolderVideos;
  sint32 AllowPinnedFolderSettings;
  sint32 AllowPinnedFolderPictures;
  sint32 AllowPinnedFolderPersonalFolder;
  sint32 AllowPinnedFolderNetwork;
  sint32 AllowPinnedFolderMusic;
  sint32 AllowPinnedFolderHomeGroup;
  sint32 AllowPinnedFolderFileExplorer;
  sint32 AllowPinnedFolderDownloads;
  sint32 AllowPinnedFolderDocuments;
  sint32 ForceStartSize;
  string StartLayout;
  sint32 NoPinningToTaskbar;
  string ImportEdgeAssets;
  sint32 HideUserTile;
  sint32 HideSwitchAccount;
  sint32 HideSleep;
  sint32 HideSignOut;
  sint32 HideShutDown;
  sint32 HideRestart;
  sint32 HideRecentlyAddedApps;
  sint32 HideRecentJumplists;
  sint32 HidePowerButton;
  sint32 HideLock;
  sint32 HideHibernate;
  sint32 HideFrequentlyUsedApps;
  sint32 HideChangeAccountSettings;
  sint32 HideAppList;
};
```

## <a name="members"></a><span data-ttu-id="84701-111">Члены</span><span class="sxs-lookup"><span data-stu-id="84701-111">Members</span></span>

<span data-ttu-id="84701-112">Класс **\_ политики MDM \_ Result01 \_ Start02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="84701-112">The **MDM\_Policy\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="84701-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="84701-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84701-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="84701-114">Properties</span></span>

<span data-ttu-id="84701-115">Класс **\_ политики MDM \_ Result01 \_ Start02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84701-115">The **MDM\_Policy\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="84701-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="84701-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="84701-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="84701-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="84701-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="84701-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="84701-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="84701-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="84701-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="84701-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="84701-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="84701-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="84701-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="84701-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="84701-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="84701-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="84701-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="84701-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="84701-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-168">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="84701-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="84701-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-174">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="84701-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-177">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="84701-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-180">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="84701-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-183">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="84701-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-186">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="84701-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-189">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="84701-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="84701-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84701-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84701-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84701-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84701-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84701-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84701-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84701-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84701-197">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84701-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84701-198">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="84701-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="84701-199">Для этого класса строка имеет значение Start.</span><span class="sxs-lookup"><span data-stu-id="84701-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="84701-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="84701-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-201">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="84701-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="84701-202">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84701-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="84701-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84701-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84701-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84701-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84701-206">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84701-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84701-207">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="84701-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="84701-208">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="84701-208">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="84701-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="84701-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84701-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84701-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84701-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="84701-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84701-212">Требования</span><span class="sxs-lookup"><span data-stu-id="84701-212">Requirements</span></span>



| <span data-ttu-id="84701-213">Требование</span><span class="sxs-lookup"><span data-stu-id="84701-213">Requirement</span></span> | <span data-ttu-id="84701-214">Значение</span><span class="sxs-lookup"><span data-stu-id="84701-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84701-215">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84701-215">Minimum supported client</span></span><br/> | <span data-ttu-id="84701-216">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="84701-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84701-217">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84701-217">Minimum supported server</span></span><br/> | <span data-ttu-id="84701-218">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="84701-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="84701-219">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84701-219">Namespace</span></span><br/>                | <span data-ttu-id="84701-220">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="84701-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="84701-221">MOF</span><span class="sxs-lookup"><span data-stu-id="84701-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84701-222"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84701-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84701-223">DLL</span><span class="sxs-lookup"><span data-stu-id="84701-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84701-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84701-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84701-225">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84701-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84701-226">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="84701-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

