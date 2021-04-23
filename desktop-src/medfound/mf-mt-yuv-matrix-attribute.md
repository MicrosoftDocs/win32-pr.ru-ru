---
description: Для типов мультимедиа YUV определяет матрицу преобразования из цветового пространства Икбкр в цветовую область RGB.
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: Атрибут MF_MT_YUV_MATRIX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651132"
---
# <a name="mf_mt_yuv_matrix-attribute"></a><span data-ttu-id="a4c4e-103">\_ \_ \_ Атрибут матрицы MF MT YUV</span><span class="sxs-lookup"><span data-stu-id="a4c4e-103">MF\_MT\_YUV\_MATRIX attribute</span></span>

<span data-ttu-id="a4c4e-104">Для типов мультимедиа YUV определяет матрицу преобразования из цветового пространства И'кб'кр в цветовую область Р'Г'Б.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-104">For YUV media types, defines the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4c4e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a4c4e-105">Data type</span></span>

<span data-ttu-id="a4c4e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a4c4e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c4e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4c4e-107">Remarks</span></span>

<span data-ttu-id="a4c4e-108">Значение этого атрибута является членом перечисления [**мфвидеотрансферматрикс**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) .</span><span class="sxs-lookup"><span data-stu-id="a4c4e-108">The value of this attribute is a member of the [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) enumeration.</span></span>

<span data-ttu-id="a4c4e-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c4e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a4c4e-110">Requirements</span></span>



| <span data-ttu-id="a4c4e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a4c4e-111">Requirement</span></span> | <span data-ttu-id="a4c4e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c4e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c4e-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4c4e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c4e-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a4c4e-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a4c4e-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4c4e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c4e-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a4c4e-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a4c4e-117">Header</span><span class="sxs-lookup"><span data-stu-id="a4c4e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c4e-118"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c4e-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c4e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4c4e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c4e-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4c4e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4c4e-121">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="a4c4e-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a4c4e-122">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a4c4e-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a4c4e-123">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="a4c4e-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a4c4e-124">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="a4c4e-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4c4e-125">Расширенные сведения о цвете</span><span class="sxs-lookup"><span data-stu-id="a4c4e-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




