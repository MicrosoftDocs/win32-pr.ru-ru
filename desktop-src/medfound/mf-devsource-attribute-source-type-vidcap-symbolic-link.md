---
description: Содержит символьную ссылку для драйвера видеозаписи.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: Атрибут MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155567"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a><span data-ttu-id="54153-103">\_ДЕВСАУРЦЕ MF \_ \_ тип источника \_ атрибута \_ видкап \_ символьный \_ атрибут ссылки</span><span class="sxs-lookup"><span data-stu-id="54153-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute</span></span>

<span data-ttu-id="54153-104">Содержит символьную ссылку для драйвера видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="54153-104">Contains the symbolic link for a video capture driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="54153-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="54153-105">Data type</span></span>

<span data-ttu-id="54153-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="54153-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="54153-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="54153-107">Get/set</span></span>

<span data-ttu-id="54153-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="54153-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="54153-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="54153-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="54153-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54153-110">Remarks</span></span>

<span data-ttu-id="54153-111">Используйте этот атрибут в качестве входных данных для функции [**мфкреатедевицесаурцеактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="54153-111">Use this attribute as input to the [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="54153-112">Кроме того, этот атрибут задается для объектов активации, возвращаемых следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="54153-112">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="54153-113">**мфкреатедевицесаурцеактивате**</span><span class="sxs-lookup"><span data-stu-id="54153-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="54153-114">**мфенумдевицесаурцес**</span><span class="sxs-lookup"><span data-stu-id="54153-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="54153-115">Символьная ссылка должна рассматриваться как непрозрачная строка.</span><span class="sxs-lookup"><span data-stu-id="54153-115">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="54153-116">Отображаемое понятное имя устройства содержится в атрибуте [ \_ \_ \_ понятного \_ имени атрибута MF девсаурце](mf-devsource-attribute-friendly-name.md) .</span><span class="sxs-lookup"><span data-stu-id="54153-116">The human-readable display name for a device is contained in the [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute.</span></span>

<span data-ttu-id="54153-117">\_ \_ \_ Атрибут девсаурце типа источника атрибута MF \_ \_ видкап \_ \_ может быть передан в качестве значения аргумента DevicePath функции [**сетупдиопендевицеинтерфаце**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .</span><span class="sxs-lookup"><span data-stu-id="54153-117">The MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute can be passed in as the value of the DevicePath argument of the [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) function.</span></span>

<span data-ttu-id="54153-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="54153-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="54153-119">Требования</span><span class="sxs-lookup"><span data-stu-id="54153-119">Requirements</span></span>



| <span data-ttu-id="54153-120">Требование</span><span class="sxs-lookup"><span data-stu-id="54153-120">Requirement</span></span> | <span data-ttu-id="54153-121">Значение</span><span class="sxs-lookup"><span data-stu-id="54153-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54153-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54153-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54153-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="54153-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="54153-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54153-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54153-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="54153-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="54153-126">Header</span><span class="sxs-lookup"><span data-stu-id="54153-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54153-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="54153-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54153-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54153-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54153-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54153-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="54153-130">Захват аудио- и видеоданных</span><span class="sxs-lookup"><span data-stu-id="54153-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="54153-131">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="54153-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
