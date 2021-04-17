---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: Атрибут DRM \_ актионалловед \_ копитосдмидевице указывает, разрешено ли копирование содержимого на устройство SDMI.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice формат Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412464"
---
# <a name="drm_actionallowed_copytosdmidevice"></a><span data-ttu-id="7cd0f-104">\_Актионалловед \_ копитосдмидевице DRM</span><span class="sxs-lookup"><span data-stu-id="7cd0f-104">DRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

<span data-ttu-id="7cd0f-105">Атрибут **DRM \_ актионалловед \_ копитосдмидевице** указывает, разрешено ли копирование содержимого на устройство SDMI.</span><span class="sxs-lookup"><span data-stu-id="7cd0f-105">The **DRM\_ActionAllowed\_CopyToSDMIDevice** attribute indicates whether the content is allowed to be copied to an SDMI device.</span></span>

## <a name="global-constant"></a><span data-ttu-id="7cd0f-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="7cd0f-106">Global Constant</span></span>

<span data-ttu-id="7cd0f-107">g \_ всзвмдрм \_ актионалловед \_ копитосдмидевице</span><span class="sxs-lookup"><span data-stu-id="7cd0f-107">g\_wszWMDRM\_ActionAllowed\_CopyToSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="7cd0f-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7cd0f-108">Data Type</span></span>

<span data-ttu-id="7cd0f-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="7cd0f-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd0f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cd0f-110">Remarks</span></span>

<span data-ttu-id="7cd0f-111">Лицензии DRM для Windows Media 10 используют действие копирования для ограничения копирования на устройства.</span><span class="sxs-lookup"><span data-stu-id="7cd0f-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="7cd0f-112">Чтобы определить, разрешено ли копирование, проверьте свойство [**\_ Актионалловед \_ Copy DRM**](drm-actionallowed-copy.md) .</span><span class="sxs-lookup"><span data-stu-id="7cd0f-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="7cd0f-113">Это свойство только для чтения, которое извлекается с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="7cd0f-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="7cd0f-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cd0f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd0f-115">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="7cd0f-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




