---
title: DRM_ActionAllowed_CopyToCD
description: Атрибут DRM \_ актионалловед \_ копитокд указывает, разрешено ли копирование содержимого на компакт-диск.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD формат Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105700805"
---
# <a name="drm_actionallowed_copytocd"></a><span data-ttu-id="6cb04-104">\_Актионалловед \_ копитокд DRM</span><span class="sxs-lookup"><span data-stu-id="6cb04-104">DRM\_ActionAllowed\_CopyToCD</span></span>

<span data-ttu-id="6cb04-105">Атрибут **DRM \_ актионалловед \_ копитокд** указывает, разрешено ли копирование содержимого на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="6cb04-105">The **DRM\_ActionAllowed\_CopyToCD** attribute indicates whether the content is allowed to be copied to a CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="6cb04-106">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="6cb04-106">Global Constant</span></span>

<span data-ttu-id="6cb04-107">g \_ всзвмдрм \_ актионалловед \_ копитокд</span><span class="sxs-lookup"><span data-stu-id="6cb04-107">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>

## <a name="data-type"></a><span data-ttu-id="6cb04-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6cb04-108">Data Type</span></span>

<span data-ttu-id="6cb04-109">**\_bool типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="6cb04-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb04-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6cb04-110">Remarks</span></span>

<span data-ttu-id="6cb04-111">Лицензии DRM для Windows Media 10 используют действие копирования для ограничения копирования на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="6cb04-111">Windows Media DRM 10 licenses use the Copy action to restrict copying to CD.</span></span> <span data-ttu-id="6cb04-112">Чтобы определить, разрешено ли копирование, проверьте свойство [**\_ Актионалловед \_ Copy DRM**](drm-actionallowed-copy.md) .</span><span class="sxs-lookup"><span data-stu-id="6cb04-112">You should check the [**DRM\_ActionAllowed\_Copy**](drm-actionallowed-copy.md) property to determine whether copying is allowed.</span></span>

<span data-ttu-id="6cb04-113">Это свойство только для чтения, которое извлекается с помощью [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="6cb04-113">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="6cb04-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cb04-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb04-115">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="6cb04-115">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




