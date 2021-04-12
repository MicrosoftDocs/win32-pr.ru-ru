---
title: DRM_BaseLicenseAcqURL
description: '\_Атрибут БАСЕЛИЦЕНСЕАККУРЛ DRM содержит частичный базовый URL-адрес, по которому приложение проигрывателя должно получить лицензию на содержимое.'
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL формат Windows Media
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133479"
---
# <a name="drm_baselicenseacqurl"></a><span data-ttu-id="5477c-104">\_БАСЕЛИЦЕНСЕАККУРЛ DRM</span><span class="sxs-lookup"><span data-stu-id="5477c-104">DRM\_BaseLicenseAcqURL</span></span>

<span data-ttu-id="5477c-105">Атрибут **\_ баселиценсеаккурл DRM** содержит частичный базовый URL-адрес, по которому приложение проигрывателя должно получить лицензию на содержимое.</span><span class="sxs-lookup"><span data-stu-id="5477c-105">The **DRM\_BaseLicenseAcqURL** attribute contains a partial, base URL to which a player application must navigate to obtain a license for the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5477c-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="5477c-106">Global Constant</span></span>

<span data-ttu-id="5477c-107">g \_ всзвмдрм \_ баселиценсеаккурл</span><span class="sxs-lookup"><span data-stu-id="5477c-107">g\_wszWMDRM\_BaseLicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="5477c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5477c-108">Data Type</span></span>

<span data-ttu-id="5477c-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="5477c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5477c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5477c-110">Remarks</span></span>

<span data-ttu-id="5477c-111">Это необязательное свойство для чтения и записи, которое задается и извлекается с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="5477c-111">This is an optional read-write property that is set and retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="5477c-112">Он предоставляется, чтобы разрешить системам распространения лицензий использовать относительные пути в свойствах URL-адреса для получения лицензий.</span><span class="sxs-lookup"><span data-stu-id="5477c-112">It is provided to enable license distribution systems to use relative paths in the license acquisition URL properties.</span></span>

<span data-ttu-id="5477c-113">После установки этого свойства все URL-адреса частичного приобретения лицензий в заголовках содержимого будут содержать базовый URL-адрес, добавляемый в начало частичного URL-адреса, чтобы сформировать полный URL-адрес для перехода к приложению проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="5477c-113">After setting this property, all partial license acquisition URLs in content headers will have the base URL added to the front of the partial URL to form a full URL for the player application to navigate to.</span></span> <span data-ttu-id="5477c-114">Вызов **ивмдрмреадер:: жетдрмпроперти** для **DRM \_ баселиценсеаккурл** будет работать только в том же сеансе, в котором она была задана.</span><span class="sxs-lookup"><span data-stu-id="5477c-114">Calling **IWMDRMReader::GetDRMProperty** for **DRM\_BaseLicenseAcqURL** will only work only in the same session as it was set.</span></span> <span data-ttu-id="5477c-115">Свойство не хранится в заголовке содержимого; Он является динамическим, и в содержимом сохраняется только относительный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5477c-115">The property is not stored in the content header; it is dynamic, and only the relative URL is stored in the content.</span></span>

## <a name="see-also"></a><span data-ttu-id="5477c-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5477c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5477c-117">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="5477c-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




