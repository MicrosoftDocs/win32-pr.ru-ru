---
description: Возвращает действующий URL-адрес потока байтов.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: Атрибут MF_BYTESTREAM_EFFECTIVE_URL (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682879"
---
# <a name="mf_bytestream_effective_url-attribute"></a><span data-ttu-id="2bc89-103">\_Атрибут BYTESTREAM для \_ действующего \_ URL-адреса MF</span><span class="sxs-lookup"><span data-stu-id="2bc89-103">MF\_BYTESTREAM\_EFFECTIVE\_URL attribute</span></span>

<span data-ttu-id="2bc89-104">Возвращает действующий URL-адрес потока байтов.</span><span class="sxs-lookup"><span data-stu-id="2bc89-104">Gets the effective URL of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="2bc89-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2bc89-105">Data type</span></span>

## <a name="getset"></a><span data-ttu-id="2bc89-106">Get/Set</span><span class="sxs-lookup"><span data-stu-id="2bc89-106">Get/set</span></span>

<span data-ttu-id="2bc89-107">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="2bc89-107">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="2bc89-108">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="2bc89-108">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2bc89-109">Применяется к</span><span class="sxs-lookup"><span data-stu-id="2bc89-109">Applies to</span></span>

[<span data-ttu-id="2bc89-110">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="2bc89-110">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="2bc89-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bc89-111">Remarks</span></span>

<span data-ttu-id="2bc89-112">Действующий URL-адрес может отличаться от исходного URL-адреса, если исходный URL-адрес содержит дополнительные сведения, например строки поиска или привязки, или если запрос был перенаправлен.</span><span class="sxs-lookup"><span data-stu-id="2bc89-112">The effective URL can differ from the original URL if the original URL contains any extra information, such as search strings or anchors, or if the request was redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc89-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2bc89-113">Requirements</span></span>



| <span data-ttu-id="2bc89-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2bc89-114">Requirement</span></span> | <span data-ttu-id="2bc89-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2bc89-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc89-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bc89-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc89-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="2bc89-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="2bc89-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bc89-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc89-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="2bc89-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="2bc89-120">Header</span><span class="sxs-lookup"><span data-stu-id="2bc89-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc89-121"><dt>Мфобжектс. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc89-121"><dt>Mfobjects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc89-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bc89-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc89-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bc89-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2bc89-124">Атрибуты потока байтов</span><span class="sxs-lookup"><span data-stu-id="2bc89-124">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="2bc89-125">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="2bc89-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




