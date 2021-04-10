---
title: Класс MDM_Policy_Config01_DeliveryOptimization02
description: '\_Класс политики MDM \_ Config01 \_ DeliveryOptimization02 представляет доступные политики оптимизации доставки.'
ms.assetid: 10dfb751-f044-4f30-90e0-af0fcb0931fb
keywords:
- Класс MDM_Policy_Config01_DeliveryOptimization02
- MDM_Policy_Config01_DeliveryOptimization02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeliveryOptimization02
- MDM_Policy_Config01_DeliveryOptimization02.InstanceID
- MDM_Policy_Config01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb9675f87a5bf9951e125bded69ae5eb10feb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135542"
---
# <a name="mdm_policy_config01_deliveryoptimization02-class"></a><span data-ttu-id="b9c77-105">\_Класс политики MDM \_ Config01 \_ DeliveryOptimization02</span><span class="sxs-lookup"><span data-stu-id="b9c77-105">MDM\_Policy\_Config01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="b9c77-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b9c77-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b9c77-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b9c77-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b9c77-108">Класс **\_ политики MDM \_ Config01 \_ DeliveryOptimization02** представляет доступные политики оптимизации доставки.</span><span class="sxs-lookup"><span data-stu-id="b9c77-108">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="b9c77-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b9c77-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c77-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9c77-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeliveryOptimization02
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

## <a name="members"></a><span data-ttu-id="b9c77-111">Члены</span><span class="sxs-lookup"><span data-stu-id="b9c77-111">Members</span></span>

<span data-ttu-id="b9c77-112">Класс **\_ политики MDM \_ Config01 \_ DeliveryOptimization02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b9c77-112">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="b9c77-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b9c77-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9c77-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b9c77-114">Properties</span></span>

<span data-ttu-id="b9c77-115">Класс **\_ политики MDM \_ Config01 \_ DeliveryOptimization02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b9c77-115">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b9c77-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="b9c77-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="b9c77-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-122">докачехост</span><span class="sxs-lookup"><span data-stu-id="b9c77-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b9c77-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="b9c77-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-128">дограупид</span><span class="sxs-lookup"><span data-stu-id="b9c77-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b9c77-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="b9c77-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="b9c77-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="b9c77-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="b9c77-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-143">DOMinBackgroundQoS</span><span class="sxs-lookup"><span data-stu-id="b9c77-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="b9c77-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="b9c77-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="b9c77-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="b9c77-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="b9c77-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b9c77-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="b9c77-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9c77-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="b9c77-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b9c77-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b9c77-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b9c77-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b9c77-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b9c77-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b9c77-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-170">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9c77-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9c77-171">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="b9c77-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="b9c77-172">Для этого класса строка имеет значение "DeliveryOptimization".</span><span class="sxs-lookup"><span data-stu-id="b9c77-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="b9c77-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b9c77-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c77-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b9c77-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b9c77-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9c77-176">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9c77-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9c77-177">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="b9c77-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="b9c77-178">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="b9c77-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9c77-179">Требования</span><span class="sxs-lookup"><span data-stu-id="b9c77-179">Requirements</span></span>



| <span data-ttu-id="b9c77-180">Требование</span><span class="sxs-lookup"><span data-stu-id="b9c77-180">Requirement</span></span> | <span data-ttu-id="b9c77-181">Значение</span><span class="sxs-lookup"><span data-stu-id="b9c77-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c77-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9c77-182">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c77-183">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b9c77-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9c77-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9c77-184">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c77-185">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b9c77-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b9c77-186">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b9c77-186">Namespace</span></span><br/>                | <span data-ttu-id="b9c77-187">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="b9c77-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b9c77-188">MOF</span><span class="sxs-lookup"><span data-stu-id="b9c77-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9c77-189"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9c77-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9c77-190">DLL</span><span class="sxs-lookup"><span data-stu-id="b9c77-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9c77-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9c77-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9c77-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9c77-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c77-193">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="b9c77-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

