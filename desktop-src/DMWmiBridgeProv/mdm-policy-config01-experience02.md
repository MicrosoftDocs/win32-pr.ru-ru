---
title: Класс MDM_Policy_Config01_Experience02
description: '\_Класс политики MDM \_ Config01 \_ Experience02 представляет доступные политики взаимодействия.'
ms.assetid: 21052983-696c-4137-9c72-16ea3b4a1eb7
keywords:
- Класс MDM_Policy_Config01_Experience02
- MDM_Policy_Config01_Experience02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Experience02
- MDM_Policy_Config01_Experience02.InstanceID
- MDM_Policy_Config01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38885dbc22c51bfa9e1653f81dba38255f6ba6a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137259"
---
# <a name="mdm_policy_config01_experience02-class"></a><span data-ttu-id="ce6f8-105">\_Класс политики MDM \_ Config01 \_ Experience02</span><span class="sxs-lookup"><span data-stu-id="ce6f8-105">MDM\_Policy\_Config01\_Experience02 class</span></span>

<span data-ttu-id="ce6f8-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ce6f8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ce6f8-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ce6f8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ce6f8-108">Класс **\_ политики MDM \_ Config01 \_ Experience02** представляет доступные политики взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="ce6f8-108">The **MDM\_Policy\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="ce6f8-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ce6f8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6f8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce6f8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="ce6f8-111">Члены</span><span class="sxs-lookup"><span data-stu-id="ce6f8-111">Members</span></span>

<span data-ttu-id="ce6f8-112">Класс **\_ политики MDM \_ Config01 \_ Experience02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ce6f8-112">The **MDM\_Policy\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="ce6f8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce6f8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce6f8-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ce6f8-114">Properties</span></span>

<span data-ttu-id="ce6f8-115">Класс **\_ политики MDM \_ Config01 \_ Experience02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ce6f8-115">The **MDM\_Policy\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ce6f8-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="ce6f8-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="ce6f8-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="ce6f8-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="ce6f8-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-128">алловсавеасофоффицефилес</span><span class="sxs-lookup"><span data-stu-id="ce6f8-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce6f8-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="ce6f8-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-134">алловшарингофоффицефилес</span><span class="sxs-lookup"><span data-stu-id="ce6f8-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce6f8-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="ce6f8-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="ce6f8-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="ce6f8-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ce6f8-146">донотшовфидбаккнотификатионс</span><span class="sxs-lookup"><span data-stu-id="ce6f8-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ce6f8-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce6f8-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce6f8-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce6f8-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ce6f8-153">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="ce6f8-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="ce6f8-154">Для этого класса строка имеет значение "Experience".</span><span class="sxs-lookup"><span data-stu-id="ce6f8-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="ce6f8-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce6f8-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ce6f8-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ce6f8-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce6f8-158">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce6f8-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ce6f8-159">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="ce6f8-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="ce6f8-160">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="ce6f8-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce6f8-161">Требования</span><span class="sxs-lookup"><span data-stu-id="ce6f8-161">Requirements</span></span>



| <span data-ttu-id="ce6f8-162">Требование</span><span class="sxs-lookup"><span data-stu-id="ce6f8-162">Requirement</span></span> | <span data-ttu-id="ce6f8-163">Значение</span><span class="sxs-lookup"><span data-stu-id="ce6f8-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6f8-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce6f8-164">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6f8-165">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ce6f8-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce6f8-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce6f8-166">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6f8-167">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce6f8-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ce6f8-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ce6f8-168">Namespace</span></span><br/>                | <span data-ttu-id="ce6f8-169">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ce6f8-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ce6f8-170">MOF</span><span class="sxs-lookup"><span data-stu-id="ce6f8-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce6f8-171"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce6f8-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce6f8-172">DLL</span><span class="sxs-lookup"><span data-stu-id="ce6f8-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce6f8-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce6f8-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce6f8-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce6f8-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6f8-175">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="ce6f8-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

