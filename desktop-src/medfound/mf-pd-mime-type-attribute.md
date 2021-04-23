---
description: Указывает тип MIME содержимого.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: Атрибут MF_PD_MIME_TYPE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1893253af139a73555d3a4fd483e9f59c5ae1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656635"
---
# <a name="mf_pd_mime_type-attribute"></a><span data-ttu-id="214d3-103">\_ \_ Атрибут типа MIME MF PD \_</span><span class="sxs-lookup"><span data-stu-id="214d3-103">MF\_PD\_MIME\_TYPE attribute</span></span>

<span data-ttu-id="214d3-104">Указывает тип MIME содержимого.</span><span class="sxs-lookup"><span data-stu-id="214d3-104">Specifies the MIME type of the content.</span></span>

## <a name="data-type"></a><span data-ttu-id="214d3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="214d3-105">Data type</span></span>

<span data-ttu-id="214d3-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="214d3-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="214d3-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="214d3-107">Remarks</span></span>

<span data-ttu-id="214d3-108">Этот атрибут применяется к дескрипторам представления.</span><span class="sxs-lookup"><span data-stu-id="214d3-108">This attribute applies to presentation descriptors.</span></span>

<span data-ttu-id="214d3-109">Тип MIME, предоставляемый с помощью [System. MIMEType](../properties/props-system-mimetype.md) для файлов мультимедиа, может иметь смещение для выбора типов MIME, подходящих для Digital живая Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="214d3-109">The MIME type exposed through [System.MIMEType](../properties/props-system-mimetype.md) for media files may have a bias towards choosing MIME types suitable for Digital Living Network Alliance (DLNA).</span></span>

<span data-ttu-id="214d3-110">\_ \_ Тип MIME MF PD \_ и [System. MIMEType](../properties/props-system-mimetype.md) не всегда может совпадать.</span><span class="sxs-lookup"><span data-stu-id="214d3-110">MF\_PD\_MIME\_TYPE and [System.MIMEType](../properties/props-system-mimetype.md) may not always match.</span></span>

<span data-ttu-id="214d3-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="214d3-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="214d3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="214d3-112">Requirements</span></span>



| <span data-ttu-id="214d3-113">Требование</span><span class="sxs-lookup"><span data-stu-id="214d3-113">Requirement</span></span> | <span data-ttu-id="214d3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="214d3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="214d3-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="214d3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="214d3-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="214d3-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="214d3-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="214d3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="214d3-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="214d3-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="214d3-119">Header</span><span class="sxs-lookup"><span data-stu-id="214d3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="214d3-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="214d3-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214d3-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="214d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214d3-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="214d3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="214d3-123">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="214d3-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="214d3-124">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="214d3-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="214d3-125">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="214d3-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="214d3-126">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="214d3-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
