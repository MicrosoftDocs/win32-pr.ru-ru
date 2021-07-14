---
description: Сообщает метаданные и буфер маски для фоновой маски сегментации, которая различает фон и передний план видеокадра.
title: Атрибут MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK (Мфапи. h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691865"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a><span data-ttu-id="161fd-103">\_ \_ \_ \_ Атрибут маски фона кадра записи \_ MF</span><span class="sxs-lookup"><span data-stu-id="161fd-103">MF\_CAPTURE\_METADATA\_FRAME\_BACKGROUND\_MASK attribute</span></span>

<span data-ttu-id="161fd-104">Сообщает метаданные и буфер маски для фоновой маски сегментации, которая различает фон и передний план видеокадра.</span><span class="sxs-lookup"><span data-stu-id="161fd-104">Reports the metadata and mask buffer for a background segmentation mask that distinguishes between the background and foreground of a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="161fd-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="161fd-105">Data type</span></span>

<span data-ttu-id="161fd-106">**ОБЪЕКТЕ**</span><span class="sxs-lookup"><span data-stu-id="161fd-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="161fd-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="161fd-107">Remarks</span></span>

<span data-ttu-id="161fd-108">Данными, переданными по этому атрибуту, является структура [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) , содержащая сведения об измерениях фоновой маски, а также о покрытии фрейма, от которого она выводится, это кадр, выводимый потоком.</span><span class="sxs-lookup"><span data-stu-id="161fd-108">The data carried by this attribute is a [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) structure that contains information about the dimensions of the background mask as well as its coverage of the frame it is inferred from, which is the frame that is outputted by the stream.</span></span> <span data-ttu-id="161fd-109">Он также содержит непрерывный буфер, представляющий маску, используемую приложением для определения того, какие пиксели считаются частью переднего плана или фона.</span><span class="sxs-lookup"><span data-stu-id="161fd-109">It also carries a contiguous buffer representing the mask to be leveraged by the consuming app to define which pixels are considered part of the foreground or background.</span></span> <span data-ttu-id="161fd-110">Масштабирование и корреляция координат изображения маски, относящейся к кадру, обрабатываются приложением, которое использует приложение.</span><span class="sxs-lookup"><span data-stu-id="161fd-110">The scaling and image coordinate correlation of the mask regarding the frame is handled by the consuming app.</span></span> 

## <a name="requirements"></a><span data-ttu-id="161fd-111">Требования</span><span class="sxs-lookup"><span data-stu-id="161fd-111">Requirements</span></span>



| <span data-ttu-id="161fd-112">Требование</span><span class="sxs-lookup"><span data-stu-id="161fd-112">Requirement</span></span> | <span data-ttu-id="161fd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="161fd-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="161fd-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="161fd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="161fd-115">Windows 22000t сборки</span><span class="sxs-lookup"><span data-stu-id="161fd-115">Windows Build 22000t</span></span><br/>                          |
| <span data-ttu-id="161fd-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="161fd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="161fd-117">Windows Сборка 22000</span><span class="sxs-lookup"><span data-stu-id="161fd-117">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="161fd-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="161fd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="161fd-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="161fd-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="161fd-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="161fd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="161fd-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="161fd-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="161fd-122">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="161fd-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="161fd-123">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="161fd-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="161fd-124">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="161fd-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="161fd-125">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="161fd-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 




