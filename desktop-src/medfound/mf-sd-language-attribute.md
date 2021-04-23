---
description: Указывает язык для потока.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: Атрибут MF_SD_LANGUAGE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266019"
---
# <a name="mf_sd_language-attribute"></a><span data-ttu-id="927e6-103">\_ \_ Атрибут языка MF SD</span><span class="sxs-lookup"><span data-stu-id="927e6-103">MF\_SD\_LANGUAGE attribute</span></span>

<span data-ttu-id="927e6-104">Указывает язык для потока.</span><span class="sxs-lookup"><span data-stu-id="927e6-104">Specifies the language for a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="927e6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="927e6-105">Data type</span></span>

<span data-ttu-id="927e6-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="927e6-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="927e6-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="927e6-107">Remarks</span></span>

<span data-ttu-id="927e6-108">Значением этого атрибута является тег языка, соответствующий RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="927e6-108">The value of this attribute is an RFC 1766-compliant language tag.</span></span> <span data-ttu-id="927e6-109">Этот атрибут применяется к дескрипторам потоков.</span><span class="sxs-lookup"><span data-stu-id="927e6-109">This attribute applies to stream descriptors.</span></span>

<span data-ttu-id="927e6-110">Источник мультимедиа (или любой объект, создающий дескриптор потока) может установить этот атрибут, если поток имеет указанный язык.</span><span class="sxs-lookup"><span data-stu-id="927e6-110">A media source (or any object that creates a stream descriptor) can set this attribute if the stream has a specified language.</span></span> <span data-ttu-id="927e6-111">Приложения могут запрашивать этот атрибут для получения языка.</span><span class="sxs-lookup"><span data-stu-id="927e6-111">Applications can query this attribute to get the language.</span></span> <span data-ttu-id="927e6-112">Если атрибут не задан, поток не имеет указанного языка.</span><span class="sxs-lookup"><span data-stu-id="927e6-112">If the attribute is not set, the stream does not have a specified language.</span></span>

<span data-ttu-id="927e6-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="927e6-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="927e6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="927e6-114">Requirements</span></span>



| <span data-ttu-id="927e6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="927e6-115">Requirement</span></span> | <span data-ttu-id="927e6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="927e6-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="927e6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="927e6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="927e6-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="927e6-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="927e6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="927e6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="927e6-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="927e6-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="927e6-121">Header</span><span class="sxs-lookup"><span data-stu-id="927e6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="927e6-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="927e6-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="927e6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="927e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927e6-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="927e6-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="927e6-125">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="927e6-125">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="927e6-126">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="927e6-126">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="927e6-127">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="927e6-127">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="927e6-128">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="927e6-128">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




