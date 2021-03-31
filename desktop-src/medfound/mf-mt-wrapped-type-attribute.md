---
description: Содержит тип мультимедиа, упакованный в другой тип мультимедиа.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: Атрибут MF_MT_WRAPPED_TYPE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423526"
---
# <a name="mf_mt_wrapped_type-attribute"></a><span data-ttu-id="a473a-103">\_ \_ Атрибут типа, упакованного в формате MF \_</span><span class="sxs-lookup"><span data-stu-id="a473a-103">MF\_MT\_WRAPPED\_TYPE attribute</span></span>

<span data-ttu-id="a473a-104">Содержит тип мультимедиа, упакованный в другой тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a473a-104">Contains a media type that has been wrapped in another media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a473a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a473a-105">Data type</span></span>

<span data-ttu-id="a473a-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="a473a-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a473a-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a473a-107">Remarks</span></span>

<span data-ttu-id="a473a-108">Этот атрибут используется в функции [**мфврапмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , которая создает оболочку для типа мультимедиа внутри другого типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a473a-108">This attribute is used in the [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function, which wraps a media type inside another media type.</span></span>

<span data-ttu-id="a473a-109">Функция [**мфврапмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a473a-109">The [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function does the following:</span></span>

1.  <span data-ttu-id="a473a-110">Преобразует исходный тип мультимедиа в двоичный массив.</span><span class="sxs-lookup"><span data-stu-id="a473a-110">Converts the original media type into a binary array.</span></span>
2.  <span data-ttu-id="a473a-111">Задает атрибут **\_ типа MF MT, \_ упакованный \_** для нового типа носителя.</span><span class="sxs-lookup"><span data-stu-id="a473a-111">Sets the **MF\_MT\_WRAPPED\_TYPE** attribute on the new media type.</span></span> <span data-ttu-id="a473a-112">Значением атрибута является двоичный массив.</span><span class="sxs-lookup"><span data-stu-id="a473a-112">The value of the attribute is the binary array.</span></span>

<span data-ttu-id="a473a-113">Обычно приложения не используют этот атрибут напрямую.</span><span class="sxs-lookup"><span data-stu-id="a473a-113">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="a473a-114">Для распаковки исходного типа мультимедиа вызовите [**мфунврапмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span><span class="sxs-lookup"><span data-stu-id="a473a-114">To unwrap the original media type, call [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span></span>

<span data-ttu-id="a473a-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a473a-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a473a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a473a-116">Requirements</span></span>



| <span data-ttu-id="a473a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a473a-117">Requirement</span></span> | <span data-ttu-id="a473a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a473a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a473a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a473a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a473a-120">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a473a-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a473a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a473a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a473a-122">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a473a-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a473a-123">Header</span><span class="sxs-lookup"><span data-stu-id="a473a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a473a-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="a473a-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a473a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a473a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a473a-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a473a-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a473a-127">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="a473a-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a473a-128">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="a473a-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a473a-129">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="a473a-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a473a-130">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="a473a-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




