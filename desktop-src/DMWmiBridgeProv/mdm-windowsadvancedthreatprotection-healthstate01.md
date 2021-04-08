---
title: Класс MDM_WindowsAdvancedThreatProtection_HealthState01
description: Класс MDM \_ виндовсадванцедсреатпротектион \_ HealthState01 используется для определения состояния работоспособности конечных точек защитника Windows Advanced Threat protection (WDATP).
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- Класс MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01 класс, описание
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989044"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a><span data-ttu-id="565de-105">\_Класс MDM виндовсадванцедсреатпротектион \_ HealthState01</span><span class="sxs-lookup"><span data-stu-id="565de-105">MDM\_WindowsAdvancedThreatProtection\_HealthState01 class</span></span>

<span data-ttu-id="565de-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="565de-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="565de-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="565de-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="565de-108">Класс **MDM \_ виндовсадванцедсреатпротектион \_ HealthState01** используется для определения состояния работоспособности конечных точек защитника Windows Advanced Threat protection (WDATP).</span><span class="sxs-lookup"><span data-stu-id="565de-108">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class is used to determine the health status of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="565de-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="565de-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="565de-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="565de-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a><span data-ttu-id="565de-111">Члены</span><span class="sxs-lookup"><span data-stu-id="565de-111">Members</span></span>

<span data-ttu-id="565de-112">Класс **MDM \_ виндовсадванцедсреатпротектион \_ HealthState01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="565de-112">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these types of members:</span></span>

-   [<span data-ttu-id="565de-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="565de-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="565de-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="565de-114">Properties</span></span>

<span data-ttu-id="565de-115">Класс **MDM \_ виндовсадванцедсреатпротектион \_ HealthState01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="565de-115">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="565de-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="565de-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="565de-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="565de-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="565de-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="565de-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="565de-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="565de-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="565de-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="565de-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="565de-121">Для этого класса строка имеет значение "HealthState".</span><span class="sxs-lookup"><span data-stu-id="565de-121">For this class, the string is "HealthState".</span></span>

</dd> <dt>

[<span data-ttu-id="565de-122">ластконнектед</span><span class="sxs-lookup"><span data-stu-id="565de-122">LastConnected</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="565de-123">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="565de-123">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="565de-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="565de-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="565de-125">OnboardingState</span><span class="sxs-lookup"><span data-stu-id="565de-125">OnboardingState</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="565de-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="565de-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="565de-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="565de-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="565de-128">OrgId</span><span class="sxs-lookup"><span data-stu-id="565de-128">OrgId</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="565de-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="565de-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="565de-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="565de-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="565de-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="565de-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="565de-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="565de-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="565de-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="565de-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="565de-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="565de-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="565de-135">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="565de-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="565de-136">Для этого класса строка имеет значение "./вендор/мсфт/виндовсадванцедсреатпротектион"</span><span class="sxs-lookup"><span data-stu-id="565de-136">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="565de-137">SenseIsRunning</span><span class="sxs-lookup"><span data-stu-id="565de-137">SenseIsRunning</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="565de-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="565de-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="565de-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="565de-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="565de-140">Требования</span><span class="sxs-lookup"><span data-stu-id="565de-140">Requirements</span></span>



| <span data-ttu-id="565de-141">Требование</span><span class="sxs-lookup"><span data-stu-id="565de-141">Requirement</span></span> | <span data-ttu-id="565de-142">Значение</span><span class="sxs-lookup"><span data-stu-id="565de-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="565de-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="565de-143">Minimum supported client</span></span><br/> | <span data-ttu-id="565de-144">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="565de-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="565de-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="565de-145">Minimum supported server</span></span><br/> | <span data-ttu-id="565de-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="565de-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="565de-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="565de-147">Namespace</span></span><br/>                | <span data-ttu-id="565de-148">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="565de-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="565de-149">MOF</span><span class="sxs-lookup"><span data-stu-id="565de-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="565de-150"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="565de-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="565de-151">DLL</span><span class="sxs-lookup"><span data-stu-id="565de-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="565de-152"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="565de-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="565de-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="565de-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="565de-154">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="565de-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

