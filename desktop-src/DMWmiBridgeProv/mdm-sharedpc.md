---
title: Класс MDM_SharedPC
description: Класс MDM \_ шаредпк используется для настройки параметров общего использования ПК.
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- Класс MDM_SharedPC
- MDM_SharedPC класс, описание
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b515e4b794e2048ab26c8e1a32bfe7d3c4b50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071154"
---
# <a name="mdm_sharedpc-class"></a><span data-ttu-id="dd347-105">\_Класс MDM шаредпк</span><span class="sxs-lookup"><span data-stu-id="dd347-105">MDM\_SharedPC class</span></span>

<span data-ttu-id="dd347-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="dd347-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd347-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="dd347-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd347-108">Класс MDM \_ шаредпк используется для настройки параметров общего использования ПК.</span><span class="sxs-lookup"><span data-stu-id="dd347-108">The MDM\_SharedPC class is used to configure settings for shared PC usage.</span></span>

<span data-ttu-id="dd347-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dd347-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd347-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd347-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a><span data-ttu-id="dd347-111">Члены</span><span class="sxs-lookup"><span data-stu-id="dd347-111">Members</span></span>

<span data-ttu-id="dd347-112">Класс **MDM \_ шаредпк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd347-112">The **MDM\_SharedPC** class has these types of members:</span></span>

-   [<span data-ttu-id="dd347-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd347-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd347-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd347-114">Properties</span></span>

<span data-ttu-id="dd347-115">Класс **MDM \_ шаредпк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd347-115">The **MDM\_SharedPC** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dd347-116">AccountModel</span><span class="sxs-lookup"><span data-stu-id="dd347-116">AccountModel</span></span>](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-119">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-119">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-120">DeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="dd347-120">DeletionPolicy</span></span>](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-123">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-123">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-124">DiskLevelCaching</span><span class="sxs-lookup"><span data-stu-id="dd347-124">DiskLevelCaching</span></span>](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-125">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-127">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-127">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-128">DiskLevelDeletion</span><span class="sxs-lookup"><span data-stu-id="dd347-128">DiskLevelDeletion</span></span>](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-131">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-131">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-132">EnableAccountManager</span><span class="sxs-lookup"><span data-stu-id="dd347-132">EnableAccountManager</span></span>](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd347-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-135">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-135">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-136">EnableSharedPCMode</span><span class="sxs-lookup"><span data-stu-id="dd347-136">EnableSharedPCMode</span></span>](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd347-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-139">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-139">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-140">InactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="dd347-140">InactiveThreshold</span></span>](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-143">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-143">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="dd347-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd347-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd347-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd347-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd347-147">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd347-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd347-148">KioskModeAUMID</span><span class="sxs-lookup"><span data-stu-id="dd347-148">KioskModeAUMID</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd347-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-151">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-151">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-152">KioskModeUserTileDisplayText</span><span class="sxs-lookup"><span data-stu-id="dd347-152">KioskModeUserTileDisplayText</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd347-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-155">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-155">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-156">MaintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="dd347-156">MaintenanceStartTime</span></span>](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-157">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-159">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-159">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-160">MaxPageFileSizeMB</span><span class="sxs-lookup"><span data-stu-id="dd347-160">MaxPageFileSizeMB</span></span>](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-161">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-161">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-163">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-163">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="dd347-164">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd347-164">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd347-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd347-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd347-167">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd347-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd347-168">RestrictLocalStorage</span><span class="sxs-lookup"><span data-stu-id="dd347-168">RestrictLocalStorage</span></span>](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-169">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd347-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-171">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-171">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-172">SetEduPolicies</span><span class="sxs-lookup"><span data-stu-id="dd347-172">SetEduPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-173">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd347-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-175">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-175">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-176">Настройки: SetPowerPolicies</span><span class="sxs-lookup"><span data-stu-id="dd347-176">SetPowerPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-177">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd347-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-179">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-179">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-180">SignInOnResume</span><span class="sxs-lookup"><span data-stu-id="dd347-180">SignInOnResume</span></span>](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-181">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dd347-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-183">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-183">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="dd347-184">SleepTimeout</span><span class="sxs-lookup"><span data-stu-id="dd347-184">SleepTimeout</span></span>](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd347-185">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd347-185">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd347-186">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd347-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dd347-187">Дополнительные сведения см. в статье [ШАРЕДПК CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="dd347-187">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd347-188">Требования</span><span class="sxs-lookup"><span data-stu-id="dd347-188">Requirements</span></span>



| <span data-ttu-id="dd347-189">Требование</span><span class="sxs-lookup"><span data-stu-id="dd347-189">Requirement</span></span> | <span data-ttu-id="dd347-190">Значение</span><span class="sxs-lookup"><span data-stu-id="dd347-190">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd347-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd347-191">Minimum supported client</span></span><br/> | <span data-ttu-id="dd347-192">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dd347-192">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dd347-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd347-193">Minimum supported server</span></span><br/> | <span data-ttu-id="dd347-194">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd347-194">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="dd347-195">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd347-195">Namespace</span></span><br/>                | <span data-ttu-id="dd347-196">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="dd347-196">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="dd347-197">MOF</span><span class="sxs-lookup"><span data-stu-id="dd347-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd347-198"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd347-198"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd347-199">DLL</span><span class="sxs-lookup"><span data-stu-id="dd347-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd347-200"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd347-200"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

