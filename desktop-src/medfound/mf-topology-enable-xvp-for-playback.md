---
description: Указывает, включает ли загрузчик топологии перекодированный процессор видео (КСВП). для преобразований — Включение аппаратного ускоренного преобразования цвета.
title: Атрибут MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Мфидл. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105720843"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a><span data-ttu-id="34d36-104">\_Топология MF \_ Включение \_ ксвп \_ для \_ атрибута воспроизведения</span><span class="sxs-lookup"><span data-stu-id="34d36-104">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK attribute</span></span>

<span data-ttu-id="34d36-105">Указывает, включает ли загрузчик топологии перекодированный процессор видео (КСВП).</span><span class="sxs-lookup"><span data-stu-id="34d36-105">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="34d36-106">для преобразований — Включение аппаратного ускоренного преобразования цвета.</span><span class="sxs-lookup"><span data-stu-id="34d36-106">for conversions, enabling hardware accelerated color conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="34d36-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="34d36-107">Data type</span></span>

<span data-ttu-id="34d36-108">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="34d36-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="34d36-109">Get/Set</span><span class="sxs-lookup"><span data-stu-id="34d36-109">Get/set</span></span>

<span data-ttu-id="34d36-110">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="34d36-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="34d36-111">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="34d36-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="34d36-112">Применяется к</span><span class="sxs-lookup"><span data-stu-id="34d36-112">Applies to</span></span>

[<span data-ttu-id="34d36-113">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="34d36-113">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="34d36-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34d36-114">Remarks</span></span>

<span data-ttu-id="34d36-115">Если этот атрибут задан, загрузчик топологии будет запрашивать обработчик видео при необходимости во время разрешения топологии, отличной от перекодировки.</span><span class="sxs-lookup"><span data-stu-id="34d36-115">If this attribute is set, the topology loader will pull in the video processor, if necessary, during non-transcode topology resolution.</span></span> <span data-ttu-id="34d36-116">При использовании топологии для создания собственного [имфтопологи](/windows/win32/api/mfidl/nn-mfidl-imftopology) этот атрибут указывает загрузчику использовать ксвп для преобразований вместо устаревшего цветового преобразователя, тем самым обеспечивая аппаратное преобразование цветов. устаревший цветовой конвертер — только программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="34d36-116">When you are using the topology to build your own [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) this attribute tells the loader to use XVP for conversions instead of the legacy color converter, thus enabling hardware accelerated color conversion; the legacy color converter is software-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="34d36-117">Требования</span><span class="sxs-lookup"><span data-stu-id="34d36-117">Requirements</span></span>



| <span data-ttu-id="34d36-118">Требование</span><span class="sxs-lookup"><span data-stu-id="34d36-118">Requirement</span></span> | <span data-ttu-id="34d36-119">Значение</span><span class="sxs-lookup"><span data-stu-id="34d36-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34d36-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34d36-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34d36-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="34d36-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="34d36-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34d36-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34d36-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="34d36-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="34d36-124">Header</span><span class="sxs-lookup"><span data-stu-id="34d36-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34d36-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="34d36-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34d36-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34d36-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d36-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34d36-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="34d36-128">диспетчер устройств Direct3D</span><span class="sxs-lookup"><span data-stu-id="34d36-128">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="34d36-129">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="34d36-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




