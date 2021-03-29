---
description: Этот атрибут указывает дополнительную защиту, предлагаемую центром доверенного видео (OTA), если соединитель не поддерживает выходную защиту.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Атрибут MFPROTECTION_CONSTRICTVIDEO_NOOPM (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991428"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a><span data-ttu-id="6629b-103">МФПРОТЕКТИОН \_ констриктвидео \_ нупм, атрибут</span><span class="sxs-lookup"><span data-stu-id="6629b-103">MFPROTECTION\_CONSTRICTVIDEO\_NOOPM attribute</span></span>

<span data-ttu-id="6629b-104">Этот атрибут указывает дополнительную защиту, предлагаемую центром доверенного видео (OTA), если соединитель не поддерживает выходную защиту.</span><span class="sxs-lookup"><span data-stu-id="6629b-104">This attribute specifies additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="6629b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6629b-105">Data type</span></span>

<span data-ttu-id="6629b-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="6629b-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="6629b-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6629b-107">Remarks</span></span>

<span data-ttu-id="6629b-108">Это дополнительная защита, предоставляемая беспроводным центром управления видео (OTA), если соединитель не поддерживает выходную защиту (см.[**имфаутпуттрустаусорити**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span><span class="sxs-lookup"><span data-stu-id="6629b-108">This is an additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection (see [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span></span> <span data-ttu-id="6629b-109">В этом случае OTA может предложить такую защиту, которая действует так же, как и защита [мфпротектион \_ констриктвидео](mfprotection-constrictvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="6629b-109">In this case the OTA may offer this protection whose effect is the same as the [MFPROTECTION\_CONSTRICTVIDEO](mfprotection-constrictvideo.md) protection.</span></span> <span data-ttu-id="6629b-110">Это определено, чтобы избежать путаницы с предыдущими вызовами [**имфаутпутполици:: женератерекуиредсчемас**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) взаимодействия, в которых \_ для определения псевдо-соединителя диспетчера окон настольных систем используется защита мфпротектион констриктвидео.</span><span class="sxs-lookup"><span data-stu-id="6629b-110">This is defined to avoid confusion with previous calls to [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions where the presence of MFPROTECTION\_CONSTRICTVIDEO protection was used to help identify the desktop window manager pseudo-connector.</span></span>

## <a name="requirements"></a><span data-ttu-id="6629b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6629b-111">Requirements</span></span>



| <span data-ttu-id="6629b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6629b-112">Requirement</span></span> | <span data-ttu-id="6629b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6629b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6629b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6629b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6629b-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6629b-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6629b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6629b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6629b-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6629b-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6629b-118">Header</span><span class="sxs-lookup"><span data-stu-id="6629b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6629b-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6629b-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6629b-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6629b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6629b-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6629b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




