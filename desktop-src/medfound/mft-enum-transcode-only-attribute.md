---
description: Указывает, оптимизирован ли декодер для перекодирования, а не для воспроизведения.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: Атрибут MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423850"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a><span data-ttu-id="91550-103">\_Атрибут атрибута с перечислением \_ только для ПЕРЕкодирования MFT \_ \_</span><span class="sxs-lookup"><span data-stu-id="91550-103">MFT\_ENUM\_TRANSCODE\_ONLY\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="91550-104">Указывает, оптимизирован ли декодер для перекодирования, а не для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="91550-104">Specifies whether a decoder is optimized for transcoding rather than for playback.</span></span>

<span data-ttu-id="91550-105">В настоящее время этот атрибут применяется только к аппаратным декодерам, использующим мини-драйвер Австреам.</span><span class="sxs-lookup"><span data-stu-id="91550-105">Currently, this attribute applies only to hardware-based decoders that use the AVStream mini-driver.</span></span> <span data-ttu-id="91550-106">Атрибут хранится в реестре со сведениями о возможностях декодера.</span><span class="sxs-lookup"><span data-stu-id="91550-106">The attribute is stored in the registry under the decoder's capabilities information.</span></span> <span data-ttu-id="91550-107">Дополнительные сведения см. в документации по [**ижеткапабилитиескэй**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="91550-107">For more information, see the documentation for [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span></span>

<span data-ttu-id="91550-108">Приложения обычно не используют этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="91550-108">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="91550-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="91550-109">Data type</span></span>

<span data-ttu-id="91550-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="91550-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="91550-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91550-111">Remarks</span></span>

<span data-ttu-id="91550-112">Если эта запись реестра имеется и равна 1, функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) пропускает декодер, если только вызывающий объект не указал **флаг \_ перечисления MFT enum флага \_ \_ \_ только** в **мфтенумекс**.</span><span class="sxs-lookup"><span data-stu-id="91550-112">If this registry entry is present and equal to 1, the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function skips the decoder unless the caller specified the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in **MFTEnumEx**.</span></span>

<span data-ttu-id="91550-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="91550-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="91550-114">Требования</span><span class="sxs-lookup"><span data-stu-id="91550-114">Requirements</span></span>



| <span data-ttu-id="91550-115">Требование</span><span class="sxs-lookup"><span data-stu-id="91550-115">Requirement</span></span> | <span data-ttu-id="91550-116">Значение</span><span class="sxs-lookup"><span data-stu-id="91550-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91550-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91550-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91550-118">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="91550-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="91550-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91550-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91550-120">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="91550-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="91550-121">Header</span><span class="sxs-lookup"><span data-stu-id="91550-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91550-122"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="91550-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91550-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91550-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91550-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="91550-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="91550-125">**мфтенумекс**</span><span class="sxs-lookup"><span data-stu-id="91550-125">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
