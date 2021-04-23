---
description: Задает длительность потока байтов в единицах 100-наносекундных.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: Атрибут MF_BYTESTREAM_DURATION (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344585"
---
# <a name="mf_bytestream_duration-attribute"></a><span data-ttu-id="a1e81-103">\_ \_ Атрибут длительности BYTESTREAM MF</span><span class="sxs-lookup"><span data-stu-id="a1e81-103">MF\_BYTESTREAM\_DURATION attribute</span></span>

<span data-ttu-id="a1e81-104">Задает длительность потока байтов в единицах 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="a1e81-104">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="a1e81-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a1e81-105">Data type</span></span>

<span data-ttu-id="a1e81-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a1e81-106">**UINT64**</span></span>

<span data-ttu-id="a1e81-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="a1e81-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e81-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1e81-108">Remarks</span></span>

<span data-ttu-id="a1e81-109">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a1e81-109">This attribute is optional.</span></span> <span data-ttu-id="a1e81-110">Если объект, создающий байтовый поток, может определить длительность, он может установить этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="a1e81-110">If the object that creates the byte stream can determine the duration, it can set this attribute.</span></span> <span data-ttu-id="a1e81-111">(Например, в сетевом потоке длительность может быть частью описания сеанса.)</span><span class="sxs-lookup"><span data-stu-id="a1e81-111">(For example, in a network stream, the duration might be part of the session description.)</span></span>

<span data-ttu-id="a1e81-112">Чтобы получить значение атрибута, вызовите метод **QueryInterface** в байтовом потоке, чтобы получить указатель на интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="a1e81-112">To get the attribute value, call **QueryInterface** on the byte stream to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="a1e81-113">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="a1e81-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="a1e81-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a1e81-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e81-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a1e81-115">Requirements</span></span>



| <span data-ttu-id="a1e81-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a1e81-116">Requirement</span></span> | <span data-ttu-id="a1e81-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a1e81-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e81-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1e81-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e81-119">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="a1e81-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="a1e81-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1e81-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e81-121">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="a1e81-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="a1e81-122">Header</span><span class="sxs-lookup"><span data-stu-id="a1e81-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e81-123"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1e81-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1e81-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1e81-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e81-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a1e81-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a1e81-126">Атрибуты потока байтов</span><span class="sxs-lookup"><span data-stu-id="a1e81-126">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="a1e81-127">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="a1e81-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="a1e81-128">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="a1e81-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="a1e81-129">**имфбитестреам**</span><span class="sxs-lookup"><span data-stu-id="a1e81-129">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




