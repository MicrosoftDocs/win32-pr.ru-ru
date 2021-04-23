---
description: Задает исходный URL-адрес для потока байтов.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Атрибут MF_BYTESTREAM_ORIGIN_NAME (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682878"
---
# <a name="mf_bytestream_origin_name-attribute"></a><span data-ttu-id="3fc41-103">\_ \_ Атрибут имени источника MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="3fc41-103">MF\_BYTESTREAM\_ORIGIN\_NAME attribute</span></span>

<span data-ttu-id="3fc41-104">Задает исходный URL-адрес для потока байтов.</span><span class="sxs-lookup"><span data-stu-id="3fc41-104">Specifies the original URL for a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="3fc41-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3fc41-105">Data type</span></span>

<span data-ttu-id="3fc41-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="3fc41-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="3fc41-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fc41-107">Remarks</span></span>

<span data-ttu-id="3fc41-108">Файловые потоки байтов могут поддерживать этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="3fc41-108">File-based byte streams can support this attribute.</span></span> <span data-ttu-id="3fc41-109">Значение атрибута задается при создании потока байтов.</span><span class="sxs-lookup"><span data-stu-id="3fc41-109">The attribute value is set when the byte stream is created.</span></span> <span data-ttu-id="3fc41-110">Чтобы получить значение атрибута, запросите объект потока байтов для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="3fc41-110">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="3fc41-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="3fc41-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc41-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3fc41-112">Requirements</span></span>



| <span data-ttu-id="3fc41-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3fc41-113">Requirement</span></span> | <span data-ttu-id="3fc41-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3fc41-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc41-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fc41-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc41-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="3fc41-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3fc41-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fc41-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc41-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="3fc41-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3fc41-119">Header</span><span class="sxs-lookup"><span data-stu-id="3fc41-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc41-120"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fc41-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc41-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fc41-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc41-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3fc41-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3fc41-123">Атрибуты потока байтов</span><span class="sxs-lookup"><span data-stu-id="3fc41-123">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="3fc41-124">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="3fc41-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="3fc41-125">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="3fc41-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="3fc41-126">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="3fc41-126">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




