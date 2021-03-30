---
title: Класс MDM_Policy_Result01_Experience02
description: '\_Класс политики MDM \_ Result01 \_ Experience02 представляет доступные политики взаимодействия.'
ms.assetid: c6dc2ef1-1f12-40b0-9d5f-9e886fe1e128
keywords:
- Класс MDM_Policy_Result01_Experience02
- MDM_Policy_Result01_Experience02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Experience02
- MDM_Policy_Result01_Experience02.InstanceID
- MDM_Policy_Result01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a767c96d7ee23b4dad9719fa74850b39f0759b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071170"
---
# <a name="mdm_policy_result01_experience02-class"></a><span data-ttu-id="26925-105">\_Класс политики MDM \_ Result01 \_ Experience02</span><span class="sxs-lookup"><span data-stu-id="26925-105">MDM\_Policy\_Result01\_Experience02 class</span></span>

<span data-ttu-id="26925-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="26925-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26925-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="26925-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26925-108">Класс **\_ политики MDM \_ Result01 \_ Experience02** представляет доступные политики взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="26925-108">The **MDM\_Policy\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="26925-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="26925-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26925-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26925-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="26925-111">Члены</span><span class="sxs-lookup"><span data-stu-id="26925-111">Members</span></span>

<span data-ttu-id="26925-112">Класс **\_ политики MDM \_ Result01 \_ Experience02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="26925-112">The **MDM\_Policy\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="26925-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="26925-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26925-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="26925-114">Properties</span></span>

<span data-ttu-id="26925-115">Класс **\_ политики MDM \_ Result01 \_ Experience02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="26925-115">The **MDM\_Policy\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="26925-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="26925-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="26925-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="26925-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="26925-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-128">алловсавеасофоффицефилес</span><span class="sxs-lookup"><span data-stu-id="26925-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26925-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="26925-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-134">алловшарингофоффицефилес</span><span class="sxs-lookup"><span data-stu-id="26925-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26925-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="26925-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="26925-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="26925-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26925-146">донотшовфидбаккнотификатионс</span><span class="sxs-lookup"><span data-stu-id="26925-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26925-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26925-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26925-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26925-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26925-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26925-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26925-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26925-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26925-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26925-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26925-153">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="26925-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="26925-154">Для этого класса строка имеет значение "Experience".</span><span class="sxs-lookup"><span data-stu-id="26925-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="26925-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="26925-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26925-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26925-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26925-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26925-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26925-158">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26925-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26925-159">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="26925-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="26925-160">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="26925-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26925-161">Требования</span><span class="sxs-lookup"><span data-stu-id="26925-161">Requirements</span></span>



| <span data-ttu-id="26925-162">Требование</span><span class="sxs-lookup"><span data-stu-id="26925-162">Requirement</span></span> | <span data-ttu-id="26925-163">Значение</span><span class="sxs-lookup"><span data-stu-id="26925-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26925-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26925-164">Minimum supported client</span></span><br/> | <span data-ttu-id="26925-165">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="26925-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26925-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26925-166">Minimum supported server</span></span><br/> | <span data-ttu-id="26925-167">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="26925-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="26925-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26925-168">Namespace</span></span><br/>                | <span data-ttu-id="26925-169">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="26925-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="26925-170">MOF</span><span class="sxs-lookup"><span data-stu-id="26925-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26925-171"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26925-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="26925-172">DLL</span><span class="sxs-lookup"><span data-stu-id="26925-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26925-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26925-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26925-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26925-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26925-175">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="26925-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

