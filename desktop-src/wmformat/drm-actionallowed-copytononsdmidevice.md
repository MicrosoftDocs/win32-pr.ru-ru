---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: Атрибут DRM \_ актионалловед \_ копитононсдмидевице указывает, разрешено ли копирование содержимого на устройство, не поддерживающее SDMI.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice формат Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069596"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a><span data-ttu-id="1ceb4-104">\_Актионалловед \_ копитононсдмидевице DRM</span><span class="sxs-lookup"><span data-stu-id="1ceb4-104">DRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

<span data-ttu-id="1ceb4-105">Атрибут **DRM \_ актионалловед \_ копитононсдмидевице** указывает, разрешено ли копирование содержимого на устройство, не поддерживающее SDMI.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-105">The **DRM\_ActionAllowed\_CopyToNonSDMIDevice** attribute indicates whether the content is allowed to be copied to a non-SDMI device</span></span>

## <a name="global-constant"></a><span data-ttu-id="1ceb4-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="1ceb4-106">Global Constant</span></span>

<span data-ttu-id="1ceb4-107">g \_ всзвмдрм \_ актионалловед \_ копитононсдмидевице</span><span class="sxs-lookup"><span data-stu-id="1ceb4-107">g\_wszWMDRM\_ActionAllowed\_CopyToNonSDMIDevice</span></span>

## <a name="data-type"></a><span data-ttu-id="1ceb4-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1ceb4-108">Data Type</span></span>

<span data-ttu-id="1ceb4-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="1ceb4-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="1ceb4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ceb4-110">Remarks</span></span>

<span data-ttu-id="1ceb4-111">Лицензии DRM для Windows Media 10 используют действие копирования для ограничения копирования на устройства.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to devices.</span></span> <span data-ttu-id="1ceb4-112">Чтобы определить, разрешено ли копирование, проверьте свойство [**\_ Актионалловед \_ Copy DRM**](drm-actionallowed-copy.md) .</span><span class="sxs-lookup"><span data-stu-id="1ceb4-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="1ceb4-113">Это свойство только для чтения, которое извлекается с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="1ceb4-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="1ceb4-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ceb4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ceb4-115">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="1ceb4-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




