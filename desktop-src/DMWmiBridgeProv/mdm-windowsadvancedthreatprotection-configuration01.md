---
title: Класс MDM_WindowsAdvancedThreatProtection_Configuration01
description: Класс MDM \_ виндовсадванцедсреатпротектион \_ Configuration01 используется для определения конфигурации конечных точек защитника Windows Advanced Threat protection (WDATP).
ms.assetid: b4b2ff02-3836-4044-b8fa-d3405f433d8c
keywords:
- Класс MDM_WindowsAdvancedThreatProtection_Configuration01
- MDM_WindowsAdvancedThreatProtection_Configuration01 класс, описание
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_Configuration01
- MDM_WindowsAdvancedThreatProtection_Configuration01.InstanceID
- MDM_WindowsAdvancedThreatProtection_Configuration01.ParentID
- MDM_WindowsAdvancedThreatProtection_Configuration01.GroupIds
api_type:
- DllExport
api_location:
- Mofs\DMWmiBridgeProv.dll
ms.openlocfilehash: c6cd6689a66735790c381ac307a443c08464a379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534811"
---
# <a name="mdm_windowsadvancedthreatprotection_configuration01-class"></a><span data-ttu-id="c12df-105">\_Класс MDM виндовсадванцедсреатпротектион \_ Configuration01</span><span class="sxs-lookup"><span data-stu-id="c12df-105">MDM\_WindowsAdvancedThreatProtection\_Configuration01 class</span></span>

<span data-ttu-id="c12df-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c12df-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c12df-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c12df-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c12df-108">Класс **MDM \_ виндовсадванцедсреатпротектион \_ Configuration01** используется для определения конфигурации конечных точек защитника Windows Advanced Threat protection (WDATP).</span><span class="sxs-lookup"><span data-stu-id="c12df-108">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class is used to determine the configuration of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="c12df-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c12df-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c12df-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c12df-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_Configuration01
{
  string InstanceID;
  string ParentID;
  sint32 SampleSharing;
  string GroupIds;
  sint32 TelemetryReportingFrequency;
};
```

## <a name="members"></a><span data-ttu-id="c12df-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c12df-111">Members</span></span>

<span data-ttu-id="c12df-112">Класс **MDM \_ виндовсадванцедсреатпротектион \_ Configuration01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c12df-112">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these types of members:</span></span>

-   [<span data-ttu-id="c12df-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c12df-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c12df-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c12df-114">Properties</span></span>

<span data-ttu-id="c12df-115">Класс **MDM \_ виндовсадванцедсреатпротектион \_ Configuration01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c12df-115">The **MDM\_WindowsAdvancedThreatProtection\_Configuration01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c12df-116">**граупидс**</span><span class="sxs-lookup"><span data-stu-id="c12df-116">**GroupIds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c12df-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c12df-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c12df-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c12df-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c12df-119">TBD</span><span class="sxs-lookup"><span data-stu-id="c12df-119">TBD</span></span>

</dd> <dt>

<span data-ttu-id="c12df-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c12df-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c12df-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c12df-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c12df-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c12df-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c12df-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c12df-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c12df-124">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="c12df-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="c12df-125">Для этого класса строка имеет значение "Configuration".</span><span class="sxs-lookup"><span data-stu-id="c12df-125">For this class, the string is "Configuration".</span></span>

</dd> <dt>

<span data-ttu-id="c12df-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c12df-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c12df-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c12df-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c12df-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c12df-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c12df-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c12df-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c12df-130">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="c12df-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="c12df-131">Для этого класса строка имеет значение "./вендор/мсфт/виндовсадванцедсреатпротектион"</span><span class="sxs-lookup"><span data-stu-id="c12df-131">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="c12df-132">SampleSharing</span><span class="sxs-lookup"><span data-stu-id="c12df-132">SampleSharing</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-samplesharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c12df-133">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c12df-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c12df-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c12df-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c12df-135">телеметрирепортингфрекуенци</span><span class="sxs-lookup"><span data-stu-id="c12df-135">TelemetryReportingFrequency</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#configuration-telemetryreportingfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c12df-136">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c12df-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c12df-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c12df-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c12df-138">Требования</span><span class="sxs-lookup"><span data-stu-id="c12df-138">Requirements</span></span>



| <span data-ttu-id="c12df-139">Требование</span><span class="sxs-lookup"><span data-stu-id="c12df-139">Requirement</span></span> | <span data-ttu-id="c12df-140">Значение</span><span class="sxs-lookup"><span data-stu-id="c12df-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c12df-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c12df-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c12df-142">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c12df-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c12df-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c12df-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c12df-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c12df-144">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c12df-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c12df-145">Namespace</span></span><br/>                | <span data-ttu-id="c12df-146">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c12df-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="c12df-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c12df-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c12df-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c12df-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="c12df-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c12df-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c12df-150"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c12df-150"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c12df-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c12df-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c12df-152">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="c12df-152">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

