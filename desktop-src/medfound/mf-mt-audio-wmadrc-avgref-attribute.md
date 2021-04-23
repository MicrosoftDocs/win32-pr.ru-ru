---
description: Средняя ссылка на уровень громкости звукового файла Windows Media.
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: Атрибут MF_MT_AUDIO_WMADRC_AVGREF (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdde0bfb4c2993580d73981e9e121d1f7f18612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263623"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a><span data-ttu-id="caec9-103">\_Атрибут MF \_ Audio \_ вмадрк \_ авгреф</span><span class="sxs-lookup"><span data-stu-id="caec9-103">MF\_MT\_AUDIO\_WMADRC\_AVGREF attribute</span></span>

<span data-ttu-id="caec9-104">Средняя ссылка на уровень громкости звукового файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="caec9-104">Reference average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="caec9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="caec9-105">Data type</span></span>

<span data-ttu-id="caec9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="caec9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="caec9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="caec9-107">Remarks</span></span>

<span data-ttu-id="caec9-108">Этот атрибут применяется к типам звуковых носителей для аудиокодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="caec9-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="caec9-109">Он указывает исходный средний уровень громкости содержимого.</span><span class="sxs-lookup"><span data-stu-id="caec9-109">It specifies the original average volume level of the content.</span></span> <span data-ttu-id="caec9-110">Декодер может использовать это значение для выполнения динамического управления диапазоном.</span><span class="sxs-lookup"><span data-stu-id="caec9-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="caec9-111">Метод [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) добавляет этот атрибут к типу мультимедиа, если заголовок ASF содержит атрибут [**WM/вмадркаверажереференце**](../wmformat/wm-wmadrcaveragereference.md) .</span><span class="sxs-lookup"><span data-stu-id="caec9-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageReference**](../wmformat/wm-wmadrcaveragereference.md) attribute.</span></span> <span data-ttu-id="caec9-112">Этот атрибут описан в документации пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="caec9-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="caec9-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="caec9-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="caec9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="caec9-114">Requirements</span></span>



| <span data-ttu-id="caec9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="caec9-115">Requirement</span></span> | <span data-ttu-id="caec9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="caec9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="caec9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="caec9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="caec9-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="caec9-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="caec9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="caec9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="caec9-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="caec9-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="caec9-121">Header</span><span class="sxs-lookup"><span data-stu-id="caec9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="caec9-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="caec9-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caec9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caec9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caec9-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="caec9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="caec9-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="caec9-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="caec9-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="caec9-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="caec9-127">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="caec9-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="caec9-128">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="caec9-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
