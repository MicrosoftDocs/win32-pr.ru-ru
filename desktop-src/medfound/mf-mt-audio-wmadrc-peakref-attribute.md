---
description: Эталонный пиковый уровень громкости звукового файла Windows Media.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: Атрибут MF_MT_AUDIO_WMADRC_PEAKREF (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544346"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a><span data-ttu-id="bbc83-103">\_Атрибут MF \_ Audio \_ вмадрк \_ пеакреф</span><span class="sxs-lookup"><span data-stu-id="bbc83-103">MF\_MT\_AUDIO\_WMADRC\_PEAKREF attribute</span></span>

<span data-ttu-id="bbc83-104">Эталонный пиковый уровень громкости звукового файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bbc83-104">Reference peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="bbc83-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bbc83-105">Data type</span></span>

<span data-ttu-id="bbc83-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bbc83-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc83-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbc83-107">Remarks</span></span>

<span data-ttu-id="bbc83-108">Этот атрибут применяется к типам звуковых носителей для аудиокодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bbc83-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="bbc83-109">Он указывает исходный пиковый уровень содержимого.</span><span class="sxs-lookup"><span data-stu-id="bbc83-109">It specifies the original peak volume level of the content.</span></span> <span data-ttu-id="bbc83-110">Декодер может использовать это значение для выполнения динамического управления диапазоном.</span><span class="sxs-lookup"><span data-stu-id="bbc83-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="bbc83-111">Метод [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) добавляет этот атрибут к типу мультимедиа, если заголовок ASF содержит атрибут [**WM/вмадркпеакреференце**](../wmformat/wm-wmadrcpeakreference.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc83-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) attribute.</span></span> <span data-ttu-id="bbc83-112">Этот атрибут описан в документации пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="bbc83-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="bbc83-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="bbc83-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc83-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bbc83-114">Requirements</span></span>



| <span data-ttu-id="bbc83-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bbc83-115">Requirement</span></span> | <span data-ttu-id="bbc83-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bbc83-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc83-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbc83-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc83-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="bbc83-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="bbc83-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbc83-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc83-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="bbc83-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bbc83-121">Header</span><span class="sxs-lookup"><span data-stu-id="bbc83-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbc83-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc83-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbc83-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbc83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc83-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bbc83-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bbc83-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="bbc83-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bbc83-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bbc83-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="bbc83-127">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="bbc83-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="bbc83-128">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="bbc83-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
