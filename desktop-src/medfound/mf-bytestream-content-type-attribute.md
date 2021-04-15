---
description: Указывает тип MIME потока байтов.
ms.assetid: bcf86ece-2673-4ed8-98fd-cd0e2154b4a8
title: Атрибут MF_BYTESTREAM_CONTENT_TYPE (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7413fa6fd2ce74530432d60976e3c7ebf702af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682880"
---
# <a name="mf_bytestream_content_type-attribute"></a><span data-ttu-id="5b7d1-103">\_ \_ Атрибут типа содержимого MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="5b7d1-103">MF\_BYTESTREAM\_CONTENT\_TYPE attribute</span></span>

<span data-ttu-id="5b7d1-104">Указывает тип MIME потока байтов.</span><span class="sxs-lookup"><span data-stu-id="5b7d1-104">Specifies the MIME type of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5b7d1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5b7d1-105">Data type</span></span>

<span data-ttu-id="5b7d1-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="5b7d1-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="5b7d1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b7d1-107">Remarks</span></span>

<span data-ttu-id="5b7d1-108">Чтобы получить значение атрибута, запросите объект потока байтов для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="5b7d1-108">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="5b7d1-109">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="5b7d1-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b7d1-110">Требования</span><span class="sxs-lookup"><span data-stu-id="5b7d1-110">Requirements</span></span>



| <span data-ttu-id="5b7d1-111">Требование</span><span class="sxs-lookup"><span data-stu-id="5b7d1-111">Requirement</span></span> | <span data-ttu-id="5b7d1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7d1-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b7d1-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b7d1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5b7d1-114">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="5b7d1-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="5b7d1-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b7d1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5b7d1-116">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="5b7d1-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="5b7d1-117">Header</span><span class="sxs-lookup"><span data-stu-id="5b7d1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b7d1-118"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b7d1-118"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b7d1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b7d1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b7d1-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b7d1-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b7d1-121">Атрибуты потока байтов</span><span class="sxs-lookup"><span data-stu-id="5b7d1-121">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="5b7d1-122">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="5b7d1-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="5b7d1-123">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="5b7d1-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="5b7d1-124">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="5b7d1-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




