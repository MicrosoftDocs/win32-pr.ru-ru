---
description: Указывает, является ли источник видеозаписи аппаратным устройством или программным устройством.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647237"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a><span data-ttu-id="16da1-103">\_ \_ Тип источника атрибута MF девсаурце \_ \_ \_ видкап \_ \_ атрибут источника оборудования</span><span class="sxs-lookup"><span data-stu-id="16da1-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_HW\_SOURCE attribute</span></span>

<span data-ttu-id="16da1-104">Указывает, является ли источник видеозаписи аппаратным устройством или программным устройством.</span><span class="sxs-lookup"><span data-stu-id="16da1-104">Specifies whether a video capture source is a hardware device or a software device.</span></span>

## <a name="data-type"></a><span data-ttu-id="16da1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="16da1-105">Data type</span></span>

<span data-ttu-id="16da1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="16da1-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="16da1-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="16da1-107">Get/set</span></span>

<span data-ttu-id="16da1-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="16da1-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="16da1-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="16da1-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="16da1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16da1-110">Remarks</span></span>

<span data-ttu-id="16da1-111">Если значение равно **true**, источником захвата является аппаратное устройство.</span><span class="sxs-lookup"><span data-stu-id="16da1-111">If the value is **TRUE**, the capture source is a hardware device.</span></span> <span data-ttu-id="16da1-112">Если значение равно **false**, это программное устройство.</span><span class="sxs-lookup"><span data-stu-id="16da1-112">If the value is **FALSE**, it is a software device.</span></span> <span data-ttu-id="16da1-113">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="16da1-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="16da1-114">Этот атрибут задается для объектов активации, возвращаемых следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="16da1-114">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="16da1-115">**мфкреатедевицесаурцеактивате**</span><span class="sxs-lookup"><span data-stu-id="16da1-115">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="16da1-116">**мфенумдевицесаурцес**</span><span class="sxs-lookup"><span data-stu-id="16da1-116">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="16da1-117">Атрибут применяется только к устройствам записи видео.</span><span class="sxs-lookup"><span data-stu-id="16da1-117">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="16da1-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="16da1-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="16da1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="16da1-119">Requirements</span></span>



| <span data-ttu-id="16da1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="16da1-120">Requirement</span></span> | <span data-ttu-id="16da1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="16da1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16da1-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16da1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16da1-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="16da1-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="16da1-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16da1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16da1-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="16da1-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="16da1-126">Header</span><span class="sxs-lookup"><span data-stu-id="16da1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="16da1-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="16da1-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16da1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16da1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16da1-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16da1-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="16da1-130">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="16da1-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="16da1-131">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="16da1-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




