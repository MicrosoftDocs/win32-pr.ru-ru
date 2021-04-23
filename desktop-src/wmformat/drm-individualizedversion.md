---
title: DRM_IndividualizedVersion
description: Атрибут DRM \_ индивидуализедверсион хранится в заголовке DRM и содержит минимальную отдельную версию, необходимую для доступа к содержимому.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion формат Windows Media
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336439"
---
# <a name="drm_individualizedversion"></a><span data-ttu-id="92225-104">\_ИНДИВИДУАЛИЗЕДВЕРСИОН DRM</span><span class="sxs-lookup"><span data-stu-id="92225-104">DRM\_IndividualizedVersion</span></span>

<span data-ttu-id="92225-105">Атрибут **DRM \_ индивидуализедверсион** хранится в заголовке DRM и содержит минимальную отдельную версию, необходимую для доступа к содержимому.</span><span class="sxs-lookup"><span data-stu-id="92225-105">The **DRM\_IndividualizedVersion** attribute is stored in the DRM header and contains the minimum individualized version required to access the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="92225-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="92225-106">Global Constant</span></span>

<span data-ttu-id="92225-107">g \_ всзвмдрм \_ индивидуализедверсион</span><span class="sxs-lookup"><span data-stu-id="92225-107">g\_wszWMDRM\_IndividualizedVersion</span></span>

## <a name="data-type"></a><span data-ttu-id="92225-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="92225-108">Data Type</span></span>

<span data-ttu-id="92225-109">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="92225-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="92225-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92225-110">Remarks</span></span>

<span data-ttu-id="92225-111">Этот атрибут имеется только в содержимом DRM версии 7.</span><span class="sxs-lookup"><span data-stu-id="92225-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="92225-112">Его можно задать с помощью [**ивмдрмвритер:: сетдрматтрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) , и его можно получить при помощи [**Ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="92225-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="92225-113">Один и тот же атрибут файла можно получить с помощью [**\_ Дрмхеадер \_ индивидуализедверсион DRM**](drm-drmheader-individualizedversion.md).</span><span class="sxs-lookup"><span data-stu-id="92225-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="92225-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92225-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92225-115">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="92225-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




