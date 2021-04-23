---
description: Количество секунд, в течение которых данные сетевых источников при запуске заменяются.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: Свойство MFNETSOURCE_BUFFERINGTIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21c165e58ebd5f2aec0f1ca7ce38281f8c94896d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154966"
---
# <a name="mfnetsource_bufferingtime-property"></a><span data-ttu-id="fffda-103">МФНЕТСАУРЦЕ \_ буфферингтиме, свойство</span><span class="sxs-lookup"><span data-stu-id="fffda-103">MFNETSOURCE\_BUFFERINGTIME property</span></span>

<span data-ttu-id="fffda-104">Количество секунд, в течение которых данные сетевых источников при запуске заменяются.</span><span class="sxs-lookup"><span data-stu-id="fffda-104">Number of seconds of data that the network source buffers at startup.</span></span>



<span data-ttu-id="fffda-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fffda-105">Data type</span></span>

<span data-ttu-id="fffda-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="fffda-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="fffda-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="fffda-107">PROPVARIANT member</span></span>

<span data-ttu-id="fffda-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="fffda-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="fffda-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fffda-109">VT\_I4</span></span>

<span data-ttu-id="fffda-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="fffda-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="fffda-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fffda-111">Remarks</span></span>

<span data-ttu-id="fffda-112">Константа **мфнетсаурце \_ буфферингтиме** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="fffda-112">The constant **MFNETSOURCE\_BUFFERINGTIME** defines the GUID for this property key.</span></span> <span data-ttu-id="fffda-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="fffda-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="fffda-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="fffda-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="fffda-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="fffda-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="fffda-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="fffda-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="fffda-117">Значение этого свойства по умолчанию равно 5 секундам.</span><span class="sxs-lookup"><span data-stu-id="fffda-117">The default value of this property is 5 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="fffda-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fffda-118">Requirements</span></span>



| <span data-ttu-id="fffda-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fffda-119">Requirement</span></span> | <span data-ttu-id="fffda-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fffda-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fffda-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fffda-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fffda-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fffda-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fffda-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fffda-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fffda-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fffda-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fffda-125">Header</span><span class="sxs-lookup"><span data-stu-id="fffda-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fffda-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fffda-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fffda-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fffda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffda-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fffda-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="fffda-129">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="fffda-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="fffda-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fffda-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




