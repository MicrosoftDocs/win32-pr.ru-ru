---
title: DRM_IsDRMCached
description: Свойство DRM \_ исдрмкачед указывает, хранятся ли на локальном компьютере сведения о лицензии DRM версии 1.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached формат Windows Media
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 185a8b2c94ca5ec517eb1a781262e3f988001a01
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105672253"
---
# <a name="drm_isdrmcached"></a><span data-ttu-id="04a4c-104">\_ИСДРМКАЧЕД DRM</span><span class="sxs-lookup"><span data-stu-id="04a4c-104">DRM\_IsDRMCached</span></span>

<span data-ttu-id="04a4c-105">Свойство **DRM \_ исдрмкачед** указывает, хранятся ли на локальном компьютере сведения о лицензии DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="04a4c-105">The **DRM\_IsDRMCached** property indicates whether DRM version 1 license information has been stored on the local machine.</span></span>

## <a name="global-constant"></a><span data-ttu-id="04a4c-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="04a4c-106">Global Constant</span></span>

<span data-ttu-id="04a4c-107">g \_ всзвмдрм \_ исдрмкачед</span><span class="sxs-lookup"><span data-stu-id="04a4c-107">g\_wszWMDRM\_IsDRMCached</span></span>

## <a name="data-type"></a><span data-ttu-id="04a4c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="04a4c-108">Data Type</span></span>

<span data-ttu-id="04a4c-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="04a4c-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="04a4c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04a4c-110">Remarks</span></span>

<span data-ttu-id="04a4c-111">Это свойство только для чтения, которое извлекается с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="04a4c-111">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="04a4c-112">Это **справедливо** , если URL-адрес получения лицензии совпадает с одним из двух известных URL-адресов, используемых для приобретения локальной лицензии в DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="04a4c-112">It is **TRUE** when the license acquisition URL matches one of two know URLs used for local license acquisition in DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="04a4c-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04a4c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a4c-114">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="04a4c-114">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




