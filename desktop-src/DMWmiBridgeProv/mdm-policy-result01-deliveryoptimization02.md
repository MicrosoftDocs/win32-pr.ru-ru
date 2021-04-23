---
title: Класс MDM_Policy_Result01_DeliveryOptimization02
description: '\_Класс политики MDM \_ Result01 \_ DeliveryOptimization02 представляет доступные политики оптимизации доставки.'
ms.assetid: 0f8a6de1-0f6c-4ee2-9235-9b5dc855f8c4
keywords:
- Класс MDM_Policy_Result01_DeliveryOptimization02
- MDM_Policy_Result01_DeliveryOptimization02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeliveryOptimization02
- MDM_Policy_Result01_DeliveryOptimization02.InstanceID
- MDM_Policy_Result01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69408228b2ed67c12de83575ddc524387498e91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801666"
---
# <a name="mdm_policy_result01_deliveryoptimization02-class"></a><span data-ttu-id="7927e-105">\_Класс политики MDM \_ Result01 \_ DeliveryOptimization02</span><span class="sxs-lookup"><span data-stu-id="7927e-105">MDM\_Policy\_Result01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="7927e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="7927e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7927e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="7927e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7927e-108">Класс **\_ политики MDM \_ Result01 \_ DeliveryOptimization02** представляет доступные политики оптимизации доставки.</span><span class="sxs-lookup"><span data-stu-id="7927e-108">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="7927e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7927e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7927e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7927e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a><span data-ttu-id="7927e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="7927e-111">Members</span></span>

<span data-ttu-id="7927e-112">Класс **\_ политики MDM \_ Result01 \_ DeliveryOptimization02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7927e-112">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="7927e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7927e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7927e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7927e-114">Properties</span></span>

<span data-ttu-id="7927e-115">Класс **\_ политики MDM \_ Result01 \_ DeliveryOptimization02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7927e-115">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7927e-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="7927e-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="7927e-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-122">докачехост</span><span class="sxs-lookup"><span data-stu-id="7927e-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7927e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="7927e-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-128">дограупид</span><span class="sxs-lookup"><span data-stu-id="7927e-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7927e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="7927e-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="7927e-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="7927e-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="7927e-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-143">DOMinBackgroundQoS</span><span class="sxs-lookup"><span data-stu-id="7927e-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="7927e-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="7927e-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="7927e-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="7927e-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="7927e-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7927e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="7927e-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7927e-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="7927e-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7927e-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7927e-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7927e-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7927e-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7927e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7927e-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7927e-170">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7927e-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7927e-171">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="7927e-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="7927e-172">Для этого класса строка имеет значение "DeliveryOptimization".</span><span class="sxs-lookup"><span data-stu-id="7927e-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="7927e-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7927e-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7927e-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7927e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7927e-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7927e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7927e-176">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7927e-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7927e-177">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="7927e-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="7927e-178">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="7927e-178">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7927e-179">Требования</span><span class="sxs-lookup"><span data-stu-id="7927e-179">Requirements</span></span>



| <span data-ttu-id="7927e-180">Требование</span><span class="sxs-lookup"><span data-stu-id="7927e-180">Requirement</span></span> | <span data-ttu-id="7927e-181">Значение</span><span class="sxs-lookup"><span data-stu-id="7927e-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7927e-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7927e-182">Minimum supported client</span></span><br/> | <span data-ttu-id="7927e-183">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7927e-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7927e-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7927e-184">Minimum supported server</span></span><br/> | <span data-ttu-id="7927e-185">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7927e-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7927e-186">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7927e-186">Namespace</span></span><br/>                | <span data-ttu-id="7927e-187">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="7927e-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="7927e-188">MOF</span><span class="sxs-lookup"><span data-stu-id="7927e-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7927e-189"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7927e-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7927e-190">DLL</span><span class="sxs-lookup"><span data-stu-id="7927e-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7927e-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7927e-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7927e-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7927e-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7927e-193">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="7927e-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

