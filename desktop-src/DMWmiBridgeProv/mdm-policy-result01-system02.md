---
title: Класс MDM_Policy_Result01_System02
description: '\_Класс политики MDM \_ Result01 \_ System02 представляет доступные системные политики.'
ms.assetid: 9A0D9688-9062-429F-897F-75705DC8FD79
keywords:
- Класс MDM_Policy_Result01_System02
- MDM_Policy_Result01_System02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_System02
- MDM_Policy_Result01_System02.InstanceID
- MDM_Policy_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffedc3c4e0eda857c071a3174690ad9677fd97da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802045"
---
# <a name="mdm_policy_result01_system02-class"></a><span data-ttu-id="fe961-105">\_Класс политики MDM \_ Result01 \_ System02</span><span class="sxs-lookup"><span data-stu-id="fe961-105">MDM\_Policy\_Result01\_System02 class</span></span>

<span data-ttu-id="fe961-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="fe961-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fe961-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="fe961-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fe961-108">Класс **\_ политики MDM \_ Result01 \_ System02** представляет доступные системные политики.</span><span class="sxs-lookup"><span data-stu-id="fe961-108">The **MDM\_Policy\_Result01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="fe961-109">Эти политики определяют разрешенные конфигурации системы.</span><span class="sxs-lookup"><span data-stu-id="fe961-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="fe961-110">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fe961-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe961-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe961-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_System02
{
  string InstanceID;
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

## <a name="members"></a><span data-ttu-id="fe961-112">Члены</span><span class="sxs-lookup"><span data-stu-id="fe961-112">Members</span></span>

<span data-ttu-id="fe961-113">Класс **\_ политики MDM \_ Result01 \_ System02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fe961-113">The **MDM\_Policy\_Result01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="fe961-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="fe961-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe961-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="fe961-115">Properties</span></span>

<span data-ttu-id="fe961-116">Класс **\_ политики MDM \_ Result01 \_ System02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fe961-116">The **MDM\_Policy\_Result01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fe961-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="fe961-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-118">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="fe961-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="fe961-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-124">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-126">алловфонтпровидерс</span><span class="sxs-lookup"><span data-stu-id="fe961-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-127">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="fe961-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-130">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="fe961-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-133">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="fe961-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-136">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="fe961-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-139">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-141">бутстартдриверинитиализатион</span><span class="sxs-lookup"><span data-stu-id="fe961-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fe961-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="fe961-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-145">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="fe961-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-148">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-150">дисаблесистемресторе</span><span class="sxs-lookup"><span data-stu-id="fe961-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fe961-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fe961-153">фидбаккхубалвайссаведиагностикслокалли</span><span class="sxs-lookup"><span data-stu-id="fe961-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-154">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe961-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe961-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fe961-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fe961-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe961-159">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe961-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fe961-160">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="fe961-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="fe961-161">Для этого класса строка имеет значение System.</span><span class="sxs-lookup"><span data-stu-id="fe961-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="fe961-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="fe961-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-163">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="fe961-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe961-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fe961-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fe961-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fe961-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe961-168">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe961-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fe961-169">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="fe961-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="fe961-170">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="fe961-170">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="fe961-171">телеметрипрокси</span><span class="sxs-lookup"><span data-stu-id="fe961-171">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe961-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fe961-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe961-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fe961-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe961-174">Требования</span><span class="sxs-lookup"><span data-stu-id="fe961-174">Requirements</span></span>



| <span data-ttu-id="fe961-175">Требование</span><span class="sxs-lookup"><span data-stu-id="fe961-175">Requirement</span></span> | <span data-ttu-id="fe961-176">Значение</span><span class="sxs-lookup"><span data-stu-id="fe961-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe961-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe961-177">Minimum supported client</span></span><br/> | <span data-ttu-id="fe961-178">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fe961-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe961-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe961-179">Minimum supported server</span></span><br/> | <span data-ttu-id="fe961-180">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fe961-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fe961-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fe961-181">Namespace</span></span><br/>                | <span data-ttu-id="fe961-182">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="fe961-182">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fe961-183">MOF</span><span class="sxs-lookup"><span data-stu-id="fe961-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe961-184"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe961-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe961-185">DLL</span><span class="sxs-lookup"><span data-stu-id="fe961-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe961-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe961-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe961-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe961-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe961-188">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="fe961-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

