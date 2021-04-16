---
title: Список атрибутов DRM
description: Список атрибутов DRM
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, управление цифровыми правами (DRM)
- Управление цифровыми правами (DRM), атрибуты
- DRM (Управление цифровыми правами), атрибуты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710157"
---
# <a name="drm-attribute-list"></a><span data-ttu-id="1198d-109">Список атрибутов DRM</span><span class="sxs-lookup"><span data-stu-id="1198d-109">DRM Attribute List</span></span>

<span data-ttu-id="1198d-110">Для удобства в следующей таблице перечислены все атрибуты файлов, связанные с DRM.</span><span class="sxs-lookup"><span data-stu-id="1198d-110">For convenience, the following table lists all the DRM-related file attributes.</span></span> <span data-ttu-id="1198d-111">(Эти атрибуты также перечислены в таблице всех атрибутов в [списке](attribute-list.md)атрибутов.)</span><span class="sxs-lookup"><span data-stu-id="1198d-111">(These attributes are also listed in the table of all attributes under [Attribute List](attribute-list.md).)</span></span>

<span data-ttu-id="1198d-112">Приложения могут устанавливать эти значения при записи файлов DRM и получать их при чтении.</span><span class="sxs-lookup"><span data-stu-id="1198d-112">Applications can set these values when writing DRM files and can retrieve them when reading.</span></span>



| <span data-ttu-id="1198d-113">Атрибут файла DRM</span><span class="sxs-lookup"><span data-stu-id="1198d-113">DRM file attribute</span></span>                                                                   | <span data-ttu-id="1198d-114">Глобальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="1198d-114">Global identifier</span></span>                             | <span data-ttu-id="1198d-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1198d-115">Data type</span></span>             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [<span data-ttu-id="1198d-116">**Идентификатор \_ CONTENTID DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-116">**DRM\_ContentID**</span></span>](drm-contentid.md)                                              | <span data-ttu-id="1198d-117">g \_ всзвмдрм идентификатор \_ ContentID</span><span class="sxs-lookup"><span data-stu-id="1198d-117">g\_wszWMDRM\_ContentID</span></span>                        | <span data-ttu-id="1198d-118">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-118">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-119">**\_Дрмхеадер \_ контентдистрибутор DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-119">**DRM\_DRMHeader\_ContentDistributor**</span></span>](drm-drmheader-contentdistributor.md)       | <span data-ttu-id="1198d-120">g \_ всзвмдрм \_ дрмхеадер \_ контентдистрибутор</span><span class="sxs-lookup"><span data-stu-id="1198d-120">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>    | <span data-ttu-id="1198d-121">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-121">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-122">**Идентификатор \_ ContentID ДРМХЕАДЕР DRM \_**</span><span class="sxs-lookup"><span data-stu-id="1198d-122">**DRM\_DRMHeader\_ContentID**</span></span>](drm-drmheader-contentid.md)                         | <span data-ttu-id="1198d-123">g \_ всзвмдрм \_ дрмхеадер идентификатор \_ ContentID</span><span class="sxs-lookup"><span data-stu-id="1198d-123">g\_wszWMDRM\_DRMHeader\_ContentID</span></span>             | <span data-ttu-id="1198d-124">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-124">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-125">**\_Дрмхеадер \_ индивидуализедверсион DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-125">**DRM\_DRMHeader\_IndividualizedVersion**</span></span>](drm-drmheader-individualizedversion.md) | <span data-ttu-id="1198d-126">g \_ всзвмдрм \_ дрмхеадер \_ индивидуализедверсион</span><span class="sxs-lookup"><span data-stu-id="1198d-126">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span> | <span data-ttu-id="1198d-127">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-127">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-128">**\_Дрмхеадер \_ KeyID DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-128">**DRM\_DRMHeader\_KeyID**</span></span>](drm-drmheader-keyid.md)                                 | <span data-ttu-id="1198d-129">g \_ всзвмдрм \_ дрмхеадер \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="1198d-129">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>                 | <span data-ttu-id="1198d-130">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-130">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-131">**\_Дрмхеадер \_ лиценсеаккурл DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-131">**DRM\_DRMHeader\_LicenseAcqURL**</span></span>](drm-drmheader-licenseacqurl.md)                 | <span data-ttu-id="1198d-132">g \_ всзвмдрм \_ дрмхеадер \_ лиценсеаккурл</span><span class="sxs-lookup"><span data-stu-id="1198d-132">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>         | <span data-ttu-id="1198d-133">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-133">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-134">**\_Дрмхеадер \_ субскриптионконтентид DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-134">**DRM\_DRMHeader\_SubscriptionContentID**</span></span>](drm-drmheader-subscriptioncontentid.md) | <span data-ttu-id="1198d-135">g \_ всзвмдрм \_ дрмхеадер \_ субскриптионконтентид</span><span class="sxs-lookup"><span data-stu-id="1198d-135">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span> | <span data-ttu-id="1198d-136">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-136">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-137">**\_ДРМХЕАДЕР DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-137">**DRM\_DRMHeader**</span></span>](drm-drmheader.md)                                              | <span data-ttu-id="1198d-138">g \_ всзвмдрм \_ дрмхеадер</span><span class="sxs-lookup"><span data-stu-id="1198d-138">g\_wszWMDRM\_DRMHeader</span></span>                        | <span data-ttu-id="1198d-139">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-139">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-140">**\_ИНДИВИДУАЛИЗЕДВЕРСИОН DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-140">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)                      | <span data-ttu-id="1198d-141">g \_ всзвмдрм \_ индивидуализедверсион</span><span class="sxs-lookup"><span data-stu-id="1198d-141">g\_wszWMDRM\_IndividualizedVersion</span></span>            | <span data-ttu-id="1198d-142">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-142">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-143">**\_KEYID DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-143">**DRM\_KeyID**</span></span>](drm-keyid.md)                                                      | <span data-ttu-id="1198d-144">g \_ всзвмдрм \_ KeyID</span><span class="sxs-lookup"><span data-stu-id="1198d-144">g\_wszWMDRM\_KeyID</span></span>                            | <span data-ttu-id="1198d-145">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-145">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-146">**\_ЛАСИГНАТУРЕЦЕРТ DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-146">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)                                  | <span data-ttu-id="1198d-147">g \_ всзвмдрм \_ ласигнатурецерт</span><span class="sxs-lookup"><span data-stu-id="1198d-147">g\_wszWMDRM\_LASignatureCert</span></span>                  | <span data-ttu-id="1198d-148">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-148">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-149">**\_ЛАСИГНАТУРЕЛИКСРВЦЕРТ DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-149">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)                      | <span data-ttu-id="1198d-150">g \_ всзвмдрм \_ ласигнатуреликсрвцерт</span><span class="sxs-lookup"><span data-stu-id="1198d-150">g\_wszWMDRM\_LASignatureLicSrvCert</span></span>            | <span data-ttu-id="1198d-151">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-151">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-152">**\_ЛАСИГНАТУРЕПРИВКЭЙ DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-152">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)                            | <span data-ttu-id="1198d-153">g \_ всзвмдрм \_ ласигнатурепривкэй</span><span class="sxs-lookup"><span data-stu-id="1198d-153">g\_wszWMDRM\_LASignaturePrivKey</span></span>               | <span data-ttu-id="1198d-154">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-154">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-155">**\_ЛАСИГНАТУРЕРУТЦЕРТ DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-155">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)                          | <span data-ttu-id="1198d-156">g \_ всзвмдрм \_ ласигнатурерутцерт</span><span class="sxs-lookup"><span data-stu-id="1198d-156">g\_wszWMDRM\_LASignatureRootCert</span></span>              | <span data-ttu-id="1198d-157">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-157">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-158">**\_ЛИЦЕНСЕАККУРЛ DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-158">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)                                      | <span data-ttu-id="1198d-159">g \_ всзвмдрм \_ лиценсеаккурл</span><span class="sxs-lookup"><span data-stu-id="1198d-159">g\_wszWMDRM\_LicenseAcqURL</span></span>                    | <span data-ttu-id="1198d-160">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-160">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="1198d-161">**\_V1LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-161">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)                                  | <span data-ttu-id="1198d-162">g \_ всзвмдрм \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="1198d-162">g\_wszWMDRM\_V1LicenseAcqURL</span></span>                  | <span data-ttu-id="1198d-163">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1198d-163">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1198d-164">См. также</span><span class="sxs-lookup"><span data-stu-id="1198d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1198d-165">**Атрибуты по типу**</span><span class="sxs-lookup"><span data-stu-id="1198d-165">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="1198d-166">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="1198d-166">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




