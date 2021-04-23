---
title: DRM_DRMHeader_SubscriptionContentID
description: Атрибут DRM \_ дрмхеадер \_ СУБСКРИПТИОНКОНТЕНТИД содержит идентификатор содержимого подписки.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID формат Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987192"
---
# <a name="drm_drmheader_subscriptioncontentid"></a><span data-ttu-id="89989-104">\_Дрмхеадер \_ субскриптионконтентид DRM</span><span class="sxs-lookup"><span data-stu-id="89989-104">DRM\_DRMHeader\_SubscriptionContentID</span></span>

<span data-ttu-id="89989-105">Атрибут **DRM \_ дрмхеадер \_ субскриптионконтентид** содержит идентификатор содержимого подписки.</span><span class="sxs-lookup"><span data-stu-id="89989-105">The **DRM\_DRMHeader\_SubscriptionContentID** attribute contains the subscription content ID.</span></span>

## <a name="global-constant"></a><span data-ttu-id="89989-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="89989-106">Global Constant</span></span>

<span data-ttu-id="89989-107">g \_ всзвмдрм \_ дрмхеадер \_ субскриптионконтентид</span><span class="sxs-lookup"><span data-stu-id="89989-107">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="89989-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="89989-108">Data Type</span></span>

<span data-ttu-id="89989-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="89989-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="89989-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89989-110">Remarks</span></span>

<span data-ttu-id="89989-111">Этот атрибут имеется только в содержимом DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="89989-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="89989-112">ИДЕНТИФИКАТОР содержимого подписки является необязательным и определяется исключительно создателем содержимого.</span><span class="sxs-lookup"><span data-stu-id="89989-112">The subscription content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="89989-113">Объект модуля записи не выполняет никаких действий с этим атрибутом.</span><span class="sxs-lookup"><span data-stu-id="89989-113">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="89989-114">Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="89989-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="89989-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89989-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89989-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="89989-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




