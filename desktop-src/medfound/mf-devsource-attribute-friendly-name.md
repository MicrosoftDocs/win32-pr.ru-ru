---
description: Указывает отображаемое имя для устройства.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692506"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a><span data-ttu-id="8a6fb-103">\_ \_ \_ Атрибут понятного имени атрибута MF девсаурце \_</span><span class="sxs-lookup"><span data-stu-id="8a6fb-103">MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME attribute</span></span>

<span data-ttu-id="8a6fb-104">Указывает отображаемое имя для устройства.</span><span class="sxs-lookup"><span data-stu-id="8a6fb-104">Specifies the display name for a device.</span></span> <span data-ttu-id="8a6fb-105">*Отображаемое имя* является удобной для чтения строкой, подходящей для вывода в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="8a6fb-105">The *display name* is a human-readable string, suitable for display in a user interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="8a6fb-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8a6fb-106">Data type</span></span>

<span data-ttu-id="8a6fb-107">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="8a6fb-107">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="8a6fb-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="8a6fb-108">Get/set</span></span>

<span data-ttu-id="8a6fb-109">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="8a6fb-109">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="8a6fb-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="8a6fb-110">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6fb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a6fb-111">Remarks</span></span>

<span data-ttu-id="8a6fb-112">Этот атрибут задается для объектов активации, возвращаемых следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="8a6fb-112">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="8a6fb-113">**мфкреатедевицесаурцеактивате**</span><span class="sxs-lookup"><span data-stu-id="8a6fb-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="8a6fb-114">**мфенумдевицесаурцес**</span><span class="sxs-lookup"><span data-stu-id="8a6fb-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="8a6fb-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="8a6fb-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6fb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8a6fb-116">Requirements</span></span>



| <span data-ttu-id="8a6fb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8a6fb-117">Requirement</span></span> | <span data-ttu-id="8a6fb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8a6fb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6fb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a6fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6fb-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8a6fb-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8a6fb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a6fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6fb-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a6fb-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8a6fb-123">Header</span><span class="sxs-lookup"><span data-stu-id="8a6fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a6fb-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a6fb-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a6fb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a6fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6fb-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a6fb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a6fb-127">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="8a6fb-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="8a6fb-128">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="8a6fb-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




