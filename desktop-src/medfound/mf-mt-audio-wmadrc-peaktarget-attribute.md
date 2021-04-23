---
description: Целевой пиковый уровень громкости звукового файла Windows Media.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: Атрибут MF_MT_AUDIO_WMADRC_PEAKTARGET (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48391adfaa19dcc00ea4d7a30b909b4573f67222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999173"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a><span data-ttu-id="40aa6-103">\_Атрибут MF \_ Audio \_ вмадрк \_ пеактаржет</span><span class="sxs-lookup"><span data-stu-id="40aa6-103">MF\_MT\_AUDIO\_WMADRC\_PEAKTARGET attribute</span></span>

<span data-ttu-id="40aa6-104">Целевой пиковый уровень громкости звукового файла Windows Media.</span><span class="sxs-lookup"><span data-stu-id="40aa6-104">Target peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="40aa6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="40aa6-105">Data type</span></span>

<span data-ttu-id="40aa6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="40aa6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="40aa6-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40aa6-107">Remarks</span></span>

<span data-ttu-id="40aa6-108">Этот атрибут применяется к типам звуковых носителей для аудиокодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="40aa6-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="40aa6-109">Он указывает целевой пиковый уровень содержимого.</span><span class="sxs-lookup"><span data-stu-id="40aa6-109">It specifies the target peak volume level of the content.</span></span> <span data-ttu-id="40aa6-110">Декодер может использовать это значение для выполнения динамического управления диапазоном.</span><span class="sxs-lookup"><span data-stu-id="40aa6-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="40aa6-111">Метод [**имфасфконтентинфо::P арсехеадер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) добавляет этот атрибут к типу мультимедиа, если заголовок ASF содержит атрибут [**WM/вмадркпеактаржет**](../wmformat/wm-wmadrcpeaktarget.md) .</span><span class="sxs-lookup"><span data-stu-id="40aa6-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) attribute.</span></span> <span data-ttu-id="40aa6-112">Этот атрибут описан в документации пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="40aa6-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="40aa6-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="40aa6-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="40aa6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="40aa6-114">Requirements</span></span>



| <span data-ttu-id="40aa6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="40aa6-115">Requirement</span></span> | <span data-ttu-id="40aa6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="40aa6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40aa6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40aa6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="40aa6-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="40aa6-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="40aa6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40aa6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="40aa6-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="40aa6-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="40aa6-121">Header</span><span class="sxs-lookup"><span data-stu-id="40aa6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="40aa6-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="40aa6-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40aa6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40aa6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40aa6-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40aa6-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="40aa6-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="40aa6-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="40aa6-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="40aa6-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="40aa6-127">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="40aa6-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="40aa6-128">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="40aa6-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
