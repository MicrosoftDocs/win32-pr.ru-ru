---
title: Класс MDM_Policy_Config01_System02
description: '\_Класс политики MDM \_ Config01 \_ System02 представляет доступные системные политики.'
ms.assetid: 0C3E21DF-309C-4AF3-8682-E921BF45BDEF
keywords:
- Класс MDM_Policy_ConfigSource01_System02
- MDM_Policy_ConfigSource01_System02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_ConfigSource01_System02
- MDM_Policy_ConfigSource01_System02.InstanceID
- MDM_Policy_ConfigSource01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45ae8061b3e383abdd075d461d5b6dc2c46a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802405"
---
# <a name="mdm_policy_config01_system02-class"></a><span data-ttu-id="9f2cc-105">\_Класс политики MDM \_ Config01 \_ System02</span><span class="sxs-lookup"><span data-stu-id="9f2cc-105">MDM\_Policy\_Config01\_System02 class</span></span>

<span data-ttu-id="9f2cc-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f2cc-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9f2cc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9f2cc-108">Класс **\_ политики MDM \_ Config01 \_ System02** представляет доступные системные политики.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-108">The **MDM\_Policy\_Config01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="9f2cc-109">Эти политики определяют разрешенные конфигурации системы.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="9f2cc-110">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2cc-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f2cc-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_System02
{
  string InstanceID = "System";
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a><span data-ttu-id="9f2cc-112">Члены</span><span class="sxs-lookup"><span data-stu-id="9f2cc-112">Members</span></span>

<span data-ttu-id="9f2cc-113">Класс **\_ политики MDM \_ ConfigSource01 \_ System02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9f2cc-113">The **MDM\_Policy\_ConfigSource01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="9f2cc-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f2cc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f2cc-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f2cc-115">Properties</span></span>

<span data-ttu-id="9f2cc-116">Класс **\_ политики MDM \_ ConfigSource01 \_ System02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-116">The **MDM\_Policy\_ConfigSource01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9f2cc-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="9f2cc-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-118">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="9f2cc-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="9f2cc-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-124">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-126">алловфонтпровидерс</span><span class="sxs-lookup"><span data-stu-id="9f2cc-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-127">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="9f2cc-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-130">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="9f2cc-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-133">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="9f2cc-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-136">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="9f2cc-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-139">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-141">бутстартдриверинитиализатион</span><span class="sxs-lookup"><span data-stu-id="9f2cc-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="9f2cc-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-145">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="9f2cc-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-148">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-150">дисаблесистемресторе</span><span class="sxs-lookup"><span data-stu-id="9f2cc-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9f2cc-153">фидбаккхубалвайссаведиагностикслокалли</span><span class="sxs-lookup"><span data-stu-id="9f2cc-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-154">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f2cc-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f2cc-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-159">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f2cc-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f2cc-160">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="9f2cc-161">Для этого класса строка имеет значение System.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="9f2cc-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="9f2cc-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-163">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9f2cc-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f2cc-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-168">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f2cc-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f2cc-169">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="9f2cc-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="9f2cc-170">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="9f2cc-170">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

<span data-ttu-id="9f2cc-171">"./Вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="9f2cc-171">"./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="9f2cc-172">телеметрипрокси</span><span class="sxs-lookup"><span data-stu-id="9f2cc-172">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f2cc-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f2cc-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f2cc-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9f2cc-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f2cc-175">Требования</span><span class="sxs-lookup"><span data-stu-id="9f2cc-175">Requirements</span></span>



| <span data-ttu-id="9f2cc-176">Требование</span><span class="sxs-lookup"><span data-stu-id="9f2cc-176">Requirement</span></span> | <span data-ttu-id="9f2cc-177">Значение</span><span class="sxs-lookup"><span data-stu-id="9f2cc-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2cc-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f2cc-178">Minimum supported client</span></span><br/> | <span data-ttu-id="9f2cc-179">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9f2cc-179">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f2cc-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f2cc-180">Minimum supported server</span></span><br/> | <span data-ttu-id="9f2cc-181">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9f2cc-181">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9f2cc-182">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9f2cc-182">Namespace</span></span><br/>                | <span data-ttu-id="9f2cc-183">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9f2cc-183">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9f2cc-184">MOF</span><span class="sxs-lookup"><span data-stu-id="9f2cc-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f2cc-185"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f2cc-185"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f2cc-186">DLL</span><span class="sxs-lookup"><span data-stu-id="9f2cc-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f2cc-187"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f2cc-187"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2cc-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f2cc-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2cc-189">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="9f2cc-189">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

