---
description: Флаги профиля, определяющие параметры потока для топологии перекодирования. Флаги определяются в \_ \_ \_ \_ перечислении флагов изменения профиля MF.
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: Атрибут MF_TRANSCODE_ADJUST_PROFILE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682962"
---
# <a name="mf_transcode_adjust_profile-attribute"></a><span data-ttu-id="52d3e-104">\_ \_ Атрибут изменения профиля для ПЕРЕкодирования MF \_</span><span class="sxs-lookup"><span data-stu-id="52d3e-104">MF\_TRANSCODE\_ADJUST\_PROFILE attribute</span></span>

<span data-ttu-id="52d3e-105">Флаги профиля, определяющие параметры потока для топологии перекодирования.</span><span class="sxs-lookup"><span data-stu-id="52d3e-105">Profile flags that define the stream settings for the transcode topology.</span></span> <span data-ttu-id="52d3e-106">Флаги определяются в перечислении [**\_ \_ \_ \_ флагов изменения профиля MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .</span><span class="sxs-lookup"><span data-stu-id="52d3e-106">The flags are defined in the [**MF\_TRANSCODE\_ADJUST\_PROFILE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="52d3e-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="52d3e-107">Data type</span></span>

<span data-ttu-id="52d3e-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="52d3e-108">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="52d3e-109">Get/Set</span><span class="sxs-lookup"><span data-stu-id="52d3e-109">Get/set</span></span>

<span data-ttu-id="52d3e-110">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="52d3e-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="52d3e-111">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="52d3e-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="52d3e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52d3e-112">Remarks</span></span>

<span data-ttu-id="52d3e-113">Приложение может установить этот атрибут на уровне контейнера в профиле перекодировки.</span><span class="sxs-lookup"><span data-stu-id="52d3e-113">An application can set this attribute at the container level on the transcode profile.</span></span> <span data-ttu-id="52d3e-114">Если этот атрибут задан, функция [**мфкреатетранскодетопологи**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) изменяет атрибуты потока во время создания топологии в зависимости от указанного флага.</span><span class="sxs-lookup"><span data-stu-id="52d3e-114">If this attribute is set, the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function changes the stream attributes during topology building, depending on the specified flag.</span></span> <span data-ttu-id="52d3e-115">Например, если приложение задает флаг **\_ \_ \_ \_ по умолчанию для изменения профиля MF** , для создания профиля используются параметры потока, заданные приложением.</span><span class="sxs-lookup"><span data-stu-id="52d3e-115">For example, if the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_DEFAULT** flag, the application-specified stream settings are used to create the profile.</span></span>

<span data-ttu-id="52d3e-116">Для потока видео частота кадров обновляется на основе источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="52d3e-116">For the video stream, the frame rate is updated based on the media source.</span></span> <span data-ttu-id="52d3e-117">Если в приложении не указан режим с чередованием, профиль обновляется для использования прогрессивных кадров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="52d3e-117">If the application does not specify the interlaced mode, the profile is updated to use progressive frames by default.</span></span>

<span data-ttu-id="52d3e-118">Если в приложении указан флаг **MF Streaming \_ \_ Настройка \_ \_ \_ \_ атрибутов источника** , то отсутствующие атрибуты потока копируются из источника входного носителя в параметры потока в профиле перекодирования.</span><span class="sxs-lookup"><span data-stu-id="52d3e-118">If the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_USE\_SOURCE\_ATTRIBUTES** flag, then missing stream attributes are copied from the input media source to the stream settings in the transcode profile.</span></span>

<span data-ttu-id="52d3e-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="52d3e-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d3e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="52d3e-120">Requirements</span></span>



| <span data-ttu-id="52d3e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="52d3e-121">Requirement</span></span> | <span data-ttu-id="52d3e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="52d3e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52d3e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52d3e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="52d3e-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="52d3e-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="52d3e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52d3e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="52d3e-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="52d3e-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="52d3e-127">Header</span><span class="sxs-lookup"><span data-stu-id="52d3e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d3e-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d3e-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d3e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52d3e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d3e-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52d3e-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="52d3e-131">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="52d3e-131">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="52d3e-132">**Имфтранскодепрофиле:: Сетконтаинераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="52d3e-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




