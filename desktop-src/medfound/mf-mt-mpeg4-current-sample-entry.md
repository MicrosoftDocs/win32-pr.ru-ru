---
description: Задает текущую запись в поле Образец описания для типа носителя MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Атрибут MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647495"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a><span data-ttu-id="76893-103">\_ \_ \_ Текущий \_ пример \_ атрибута записи MF MT MPEG4</span><span class="sxs-lookup"><span data-stu-id="76893-103">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY attribute</span></span>

<span data-ttu-id="76893-104">Задает текущую запись в поле Образец описания для типа носителя MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="76893-104">Specifies the current entry in the sample description box for an MPEG-4 media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="76893-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="76893-105">Data type</span></span>

<span data-ttu-id="76893-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="76893-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="76893-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="76893-107">Get/set</span></span>

<span data-ttu-id="76893-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="76893-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="76893-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="76893-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="76893-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="76893-110">Applies to</span></span>

[<span data-ttu-id="76893-111">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="76893-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="76893-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76893-112">Remarks</span></span>

<span data-ttu-id="76893-113">В файле MP4 или 3GP в поле Описание примера описывается кодировка, используемая для потока в файле.</span><span class="sxs-lookup"><span data-stu-id="76893-113">In an MP4 or 3GP file, the sample description box describes the encoding used for a stream in the file.</span></span> <span data-ttu-id="76893-114">В поле Описание образца может содержаться несколько записей.</span><span class="sxs-lookup"><span data-stu-id="76893-114">The sample description box can contain multiple entries.</span></span> <span data-ttu-id="76893-115">Этот атрибут указывает, какую запись использовать.</span><span class="sxs-lookup"><span data-stu-id="76893-115">This attribute specifies which entry to use.</span></span> <span data-ttu-id="76893-116">Значение — это Отсчитываемый от нуля индекс в списке.</span><span class="sxs-lookup"><span data-stu-id="76893-116">The value is a zero-based index into the list.</span></span>

<span data-ttu-id="76893-117">В настоящее время единственным поддерживаемым значением является 0.</span><span class="sxs-lookup"><span data-stu-id="76893-117">Currently, the only supported value is 0.</span></span> <span data-ttu-id="76893-118">Атрибут был определен для будущего расширения.</span><span class="sxs-lookup"><span data-stu-id="76893-118">The attribute has been defined for future extensibility.</span></span>

<span data-ttu-id="76893-119">Источник файла MPEG-4 всегда задает значение 0.</span><span class="sxs-lookup"><span data-stu-id="76893-119">The MPEG-4 file source always sets the value to 0.</span></span> <span data-ttu-id="76893-120">Приемники файлов MP4 и 3GP игнорируют значение этого атрибута, если оно имеется.</span><span class="sxs-lookup"><span data-stu-id="76893-120">The MP4 and 3GP file sinks ignore the value of this attribute if it is present.</span></span>

<span data-ttu-id="76893-121">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="76893-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="76893-122">Требования</span><span class="sxs-lookup"><span data-stu-id="76893-122">Requirements</span></span>



| <span data-ttu-id="76893-123">Требование</span><span class="sxs-lookup"><span data-stu-id="76893-123">Requirement</span></span> | <span data-ttu-id="76893-124">Значение</span><span class="sxs-lookup"><span data-stu-id="76893-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76893-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76893-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76893-126">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="76893-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="76893-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76893-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76893-128">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="76893-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="76893-129">Header</span><span class="sxs-lookup"><span data-stu-id="76893-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="76893-130"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="76893-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76893-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76893-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76893-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76893-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76893-133">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="76893-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="76893-134">\_ \_ \_ Описание образца MPEG4 \_ MF</span><span class="sxs-lookup"><span data-stu-id="76893-134">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




