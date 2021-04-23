---
title: Класс MDM_Policy_Config01_WindowsDefenderSecurityCenter02
description: '\_Класс политики MDM \_ Config01 \_ WindowsDefenderSecurityCenter02 представляет политики центра безопасности защитника Windows.'
ms.assetid: 406c3992-e9ed-49c5-a4c4-97d91013d416
keywords:
- Класс MDM_Policy_Config01_WindowsDefenderSecurityCenter02
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b341eb66cc5d1186a962278babce536c0050523d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891994"
---
# <a name="mdm_policy_config01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="5b551-105">\_Класс политики MDM \_ Config01 \_ WindowsDefenderSecurityCenter02</span><span class="sxs-lookup"><span data-stu-id="5b551-105">MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="5b551-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="5b551-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5b551-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="5b551-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5b551-108">\_Класс политики MDM \_ Config01 \_ WindowsDefenderSecurityCenter02 представляет политики центра безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="5b551-108">The MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="5b551-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5b551-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b551-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b551-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsDefenderSecurityCenter02
{
  string InstanceID;
  string ParentID;
  string CompanyName;
  sint32 DisableAppBrowserUI;
  sint32 DisableEnhancedNotifications;
  sint32 DisableFamilyUI;
  sint32 DisableHealthUI;
  sint32 DisableNetworkUI;
  sint32 DisableNotifications;
  sint32 DisableVirusUI;
  sint32 DisallowExploitProtectionOverride;
  string Email;
  sint32 EnableCustomizedToasts;
  sint32 EnableInAppCustomization;
  string Phone;
  string URL;
};
```

## <a name="members"></a><span data-ttu-id="5b551-111">Члены</span><span class="sxs-lookup"><span data-stu-id="5b551-111">Members</span></span>

<span data-ttu-id="5b551-112">Класс **\_ политики MDM \_ Config01 \_ WindowsDefenderSecurityCenter02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5b551-112">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="5b551-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b551-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b551-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5b551-114">Properties</span></span>

<span data-ttu-id="5b551-115">Класс **\_ политики MDM \_ Config01 \_ WindowsDefenderSecurityCenter02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5b551-115">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5b551-116">Название</span><span class="sxs-lookup"><span data-stu-id="5b551-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b551-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-119">дисаблеаппбровсеруи</span><span class="sxs-lookup"><span data-stu-id="5b551-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-122">дисаблинханцеднотификатионс</span><span class="sxs-lookup"><span data-stu-id="5b551-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-125">дисаблефамилюи</span><span class="sxs-lookup"><span data-stu-id="5b551-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-128">дисаблехеалсуи</span><span class="sxs-lookup"><span data-stu-id="5b551-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-131">дисабленетворкуи</span><span class="sxs-lookup"><span data-stu-id="5b551-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="5b551-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-137">дисаблевирусуи</span><span class="sxs-lookup"><span data-stu-id="5b551-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-140">дисалловексплоитпротектионоверриде</span><span class="sxs-lookup"><span data-stu-id="5b551-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-143">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="5b551-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b551-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-146">енаблекустомизедтоастс</span><span class="sxs-lookup"><span data-stu-id="5b551-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-149">енаблеинаппкустомизатион</span><span class="sxs-lookup"><span data-stu-id="5b551-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="5b551-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b551-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5b551-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b551-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b551-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b551-155">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b551-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5b551-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5b551-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b551-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5b551-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b551-159">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5b551-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-160">Факс</span><span class="sxs-lookup"><span data-stu-id="5b551-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b551-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5b551-163">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="5b551-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b551-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5b551-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5b551-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5b551-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b551-166">Требования</span><span class="sxs-lookup"><span data-stu-id="5b551-166">Requirements</span></span>



| <span data-ttu-id="5b551-167">Требование</span><span class="sxs-lookup"><span data-stu-id="5b551-167">Requirement</span></span> | <span data-ttu-id="5b551-168">Значение</span><span class="sxs-lookup"><span data-stu-id="5b551-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b551-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b551-169">Minimum supported client</span></span><br/> | <span data-ttu-id="5b551-170">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5b551-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5b551-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b551-171">Minimum supported server</span></span><br/> | <span data-ttu-id="5b551-172">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5b551-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5b551-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5b551-173">Namespace</span></span><br/>                | <span data-ttu-id="5b551-174">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="5b551-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5b551-175">MOF</span><span class="sxs-lookup"><span data-stu-id="5b551-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b551-176"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b551-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b551-177">DLL</span><span class="sxs-lookup"><span data-stu-id="5b551-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b551-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b551-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

