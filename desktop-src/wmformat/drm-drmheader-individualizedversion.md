---
title: DRM_DRMHeader_IndividualizedVersion
description: '\_Атрибут ДРМХЕАДЕРИНДИВИДУАЛИЗЕДВЕРСИОН DRM содержит минимальную отдельную версию, необходимую для воспроизведения файла.'
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion формат Windows Media
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710235"
---
# <a name="drm_drmheader_individualizedversion"></a><span data-ttu-id="5ef1a-104">\_Дрмхеадер \_ индивидуализедверсион DRM</span><span class="sxs-lookup"><span data-stu-id="5ef1a-104">DRM\_DRMHeader\_IndividualizedVersion</span></span>

<span data-ttu-id="5ef1a-105">Атрибут **\_ дрмхеадериндивидуализедверсион DRM** содержит минимальную отдельную версию, необходимую для воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="5ef1a-105">The **DRM\_DRMHeaderIndividualizedVersion** attribute contains the minimum individualized version required to play back the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5ef1a-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="5ef1a-106">Global Constant</span></span>

<span data-ttu-id="5ef1a-107">g \_ всзвмдрм \_ дрмхеадер \_ индивидуализедверсион</span><span class="sxs-lookup"><span data-stu-id="5ef1a-107">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="5ef1a-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5ef1a-108">Data Type</span></span>

<span data-ttu-id="5ef1a-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="5ef1a-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5ef1a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ef1a-110">Remarks</span></span>

<span data-ttu-id="5ef1a-111">Этот атрибут имеется только в содержимом DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="5ef1a-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="5ef1a-112">Его можно получить с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="5ef1a-112">It can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="5ef1a-113">Чтобы задать отдельную версию (также называемую версией безопасности) для файла с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , необходимо использовать свойство [**\_ индивидуализедверсион DRM**](drm-individualizedversion.md) .</span><span class="sxs-lookup"><span data-stu-id="5ef1a-113">To set the individualized version (also called the security version) on the file using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) you must use the [**DRM\_IndividualizedVersion**](drm-individualizedversion.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ef1a-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ef1a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef1a-115">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="5ef1a-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




