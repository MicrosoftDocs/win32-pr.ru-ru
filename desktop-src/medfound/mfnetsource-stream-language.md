---
description: Хранит строку, отправленную в заголовке Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: Свойство MFNETSOURCE_STREAM_LANGUAGE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423522"
---
# <a name="mfnetsource_stream_language-property"></a><span data-ttu-id="e4925-103">\_ \_ Свойство языка потока мфнетсаурце</span><span class="sxs-lookup"><span data-stu-id="e4925-103">MFNETSOURCE\_STREAM\_LANGUAGE property</span></span>

<span data-ttu-id="e4925-104">Хранит строку, отправленную в заголовке Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="e4925-104">Stores the string sent in the Accept-Language header.</span></span>



<span data-ttu-id="e4925-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e4925-105">Data type</span></span>

<span data-ttu-id="e4925-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="e4925-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e4925-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="e4925-107">PROPVARIANT member</span></span>

<span data-ttu-id="e4925-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="e4925-108">\**WCHAR\** _</span></span>

<span data-ttu-id="e4925-109">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="e4925-109">VT\_LPWSTR</span></span>

<span data-ttu-id="e4925-110">_ *пвсзвал*\*</span><span class="sxs-lookup"><span data-stu-id="e4925-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="e4925-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4925-111">Remarks</span></span>

<span data-ttu-id="e4925-112">\_ \_ Константа языка потока мфнетсаурце определяет идентификатор GUID для ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="e4925-112">The MFNETSOURCE\_STREAM\_LANGUAGE constant defines the GUID for the property key.</span></span> <span data-ttu-id="e4925-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="e4925-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="e4925-114">Чтобы задать это свойство в сетевом источнике, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="e4925-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="e4925-115">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e4925-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4925-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e4925-116">Requirements</span></span>



| <span data-ttu-id="e4925-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e4925-117">Requirement</span></span> | <span data-ttu-id="e4925-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e4925-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e4925-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4925-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4925-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e4925-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e4925-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4925-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4925-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4925-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e4925-123">Header</span><span class="sxs-lookup"><span data-stu-id="e4925-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4925-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4925-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4925-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4925-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4925-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4925-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e4925-127">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4925-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




