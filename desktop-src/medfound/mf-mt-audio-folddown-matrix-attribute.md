---
description: Указывает, каким образом звуковой декодер должен преобразовать многоканальный звук в стерео вывод. Этот процесс также называется свертыванием.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Атрибут MF_MT_AUDIO_FOLDDOWN_MATRIX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683120"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a><span data-ttu-id="af5e5-104">\_ \_ \_ \_ Атрибут матрицы фолддовн MF Audio</span><span class="sxs-lookup"><span data-stu-id="af5e5-104">MF\_MT\_AUDIO\_FOLDDOWN\_MATRIX attribute</span></span>

<span data-ttu-id="af5e5-105">Указывает, каким образом звуковой декодер должен преобразовать многоканальный звук в стерео вывод.</span><span class="sxs-lookup"><span data-stu-id="af5e5-105">Specifies how an audio decoder should transform multichannel audio to stereo output.</span></span> <span data-ttu-id="af5e5-106">Этот процесс также называется *свертыванием*.</span><span class="sxs-lookup"><span data-stu-id="af5e5-106">This process is also called *fold-down*.</span></span>

## <a name="data-type"></a><span data-ttu-id="af5e5-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="af5e5-107">Data type</span></span>

<span data-ttu-id="af5e5-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="af5e5-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="af5e5-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af5e5-109">Remarks</span></span>

<span data-ttu-id="af5e5-110">Этот атрибут применяется к типам звуковых носителей.</span><span class="sxs-lookup"><span data-stu-id="af5e5-110">This attribute applies to audio media types.</span></span>

<span data-ttu-id="af5e5-111">Значение этого атрибута является структурой [**\_ матрицы мффолддовн**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .</span><span class="sxs-lookup"><span data-stu-id="af5e5-111">The value of this attribute is an [**MFFOLDDOWN\_MATRIX**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) structure.</span></span>

<span data-ttu-id="af5e5-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="af5e5-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5e5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="af5e5-113">Requirements</span></span>



| <span data-ttu-id="af5e5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="af5e5-114">Requirement</span></span> | <span data-ttu-id="af5e5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="af5e5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af5e5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af5e5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="af5e5-117">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="af5e5-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="af5e5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af5e5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="af5e5-119">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="af5e5-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="af5e5-120">Header</span><span class="sxs-lookup"><span data-stu-id="af5e5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="af5e5-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="af5e5-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af5e5-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af5e5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5e5-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af5e5-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="af5e5-124">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="af5e5-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="af5e5-125">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="af5e5-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="af5e5-126">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="af5e5-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="af5e5-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="af5e5-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




