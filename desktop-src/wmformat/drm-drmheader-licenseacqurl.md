---
title: DRM_DRMHeader_LicenseAcqURL
description: Атрибут DRM \_ дрмхеадер \_ лиценсеаккурл содержит URL-адрес для получения лицензии для лицензии DRM версии 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL формат Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069564"
---
# <a name="drm_drmheader_licenseacqurl"></a><span data-ttu-id="c6e1c-104">\_Дрмхеадер \_ лиценсеаккурл DRM</span><span class="sxs-lookup"><span data-stu-id="c6e1c-104">DRM\_DRMHeader\_LicenseAcqURL</span></span>

<span data-ttu-id="c6e1c-105">Атрибут **DRM \_ дрмхеадер \_ лиценсеаккурл** содержит URL-адрес для получения лицензии для лицензии DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="c6e1c-105">The **DRM\_DRMHeader\_LicenseAcqURL** attribute contains the license acquisition URL for a DRM version 7 license.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c6e1c-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="c6e1c-106">Global Constant</span></span>

<span data-ttu-id="c6e1c-107">g \_ всзвмдрм \_ дрмхеадер \_ лиценсеаккурл</span><span class="sxs-lookup"><span data-stu-id="c6e1c-107">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="c6e1c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c6e1c-108">Data Type</span></span>

<span data-ttu-id="c6e1c-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="c6e1c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e1c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6e1c-110">Remarks</span></span>

<span data-ttu-id="c6e1c-111">Этот атрибут имеется только в содержимом DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="c6e1c-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="c6e1c-112">Его можно получить с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="c6e1c-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="c6e1c-113">Чтобы задать URL-адрес для получения лицензии на файл с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , необходимо использовать свойство [**\_ лиценсеаккурл DRM**](drm-licenseacqurl.md) .</span><span class="sxs-lookup"><span data-stu-id="c6e1c-113">To set the license acquisition URL on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_LicenseAcqURL**](drm-licenseacqurl.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6e1c-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6e1c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e1c-115">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="c6e1c-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




