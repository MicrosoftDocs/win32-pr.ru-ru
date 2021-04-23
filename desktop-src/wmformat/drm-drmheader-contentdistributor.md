---
title: DRM_DRMHeader_ContentDistributor
description: Атрибут DRM \_ дрмхеадер \_ контентдистрибутор содержит строку идентифийинг распространителя содержимого.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor формат Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710241"
---
# <a name="drm_drmheader_contentdistributor"></a><span data-ttu-id="11890-104">\_Дрмхеадер \_ контентдистрибутор DRM</span><span class="sxs-lookup"><span data-stu-id="11890-104">DRM\_DRMHeader\_ContentDistributor</span></span>

<span data-ttu-id="11890-105">Атрибут **DRM \_ дрмхеадер \_ контентдистрибутор** содержит строку идентифийинг распространителя содержимого.</span><span class="sxs-lookup"><span data-stu-id="11890-105">The **DRM\_DRMHeader\_ContentDistributor** attribute contains a string identifiying the content distributor.</span></span>

## <a name="global-constant"></a><span data-ttu-id="11890-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="11890-106">Global Constant</span></span>

<span data-ttu-id="11890-107">g \_ всзвмдрм \_ дрмхеадер \_ контентдистрибутор</span><span class="sxs-lookup"><span data-stu-id="11890-107">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>

## <a name="data-type"></a><span data-ttu-id="11890-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="11890-108">Data Type</span></span>

<span data-ttu-id="11890-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="11890-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="11890-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11890-110">Remarks</span></span>

<span data-ttu-id="11890-111">ИДЕНТИФИКАТОР содержимого является необязательным и определяется исключительно создателем содержимого.</span><span class="sxs-lookup"><span data-stu-id="11890-111">The content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="11890-112">Объект модуля записи не выполняет никаких действий с этим атрибутом.</span><span class="sxs-lookup"><span data-stu-id="11890-112">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="11890-113">Этот атрибут имеется только в содержимом DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="11890-113">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="11890-114">Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="11890-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="11890-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11890-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11890-116">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="11890-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




