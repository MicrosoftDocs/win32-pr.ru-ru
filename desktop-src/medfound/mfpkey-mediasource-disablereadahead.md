---
description: Включает или отключает упреждающее чтение в источнике мультимедиа.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: Свойство MFPKEY_MediaSource_DisableReadAhead (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648746"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a><span data-ttu-id="061b3-103">МФПКЭЙ \_ медиасаурце \_ дисаблереадахеад, свойство</span><span class="sxs-lookup"><span data-stu-id="061b3-103">MFPKEY\_MediaSource\_DisableReadAhead property</span></span>

<span data-ttu-id="061b3-104">Включает или отключает упреждающее чтение в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="061b3-104">Enables or disables read-ahead in a media source.</span></span>



<span data-ttu-id="061b3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="061b3-105">Data type</span></span>

<span data-ttu-id="061b3-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="061b3-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="061b3-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="061b3-107">PROPVARIANT member</span></span>

<span data-ttu-id="061b3-108">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="061b3-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="061b3-109">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="061b3-109">VT\_BOOL</span></span>

<span data-ttu-id="061b3-110">**булвал**</span><span class="sxs-lookup"><span data-stu-id="061b3-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="061b3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="061b3-111">Remarks</span></span>

<span data-ttu-id="061b3-112">Приложения могут использовать это свойство для настройки некоторых источников мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="061b3-112">Applications can use this property to configure some media sources.</span></span> <span data-ttu-id="061b3-113">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="061b3-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="061b3-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="061b3-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="061b3-115">Если значение равно **\_ true**, источник мультимедиа не будет считываться в байтовом потоке вперед.</span><span class="sxs-lookup"><span data-stu-id="061b3-115">If the value is **VARIANT\_TRUE**, the media source will not read ahead in the byte stream.</span></span> <span data-ttu-id="061b3-116">Этот параметр может оптимизировать производительность, если вы планируете считывать ограниченный объем данных из источника мультимедиа, например, чтобы получить эскиз изображения из видеофайла.</span><span class="sxs-lookup"><span data-stu-id="061b3-116">This setting can optimize performance if you plan to read a limited amount of data from the media source—for example, to get a thumbnail image from a video file.</span></span>

<span data-ttu-id="061b3-117">Для типичного воспроизведения звука и видео этому свойству должно быть присвоено значение **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="061b3-117">For typical audio/video playback, this property should be set to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="061b3-118">Значение по умолчанию — **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="061b3-118">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="061b3-119">Это свойство поддерживается не каждым источником мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="061b3-119">Not every media source supports this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="061b3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="061b3-120">Requirements</span></span>



| <span data-ttu-id="061b3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="061b3-121">Requirement</span></span> | <span data-ttu-id="061b3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="061b3-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="061b3-123">Клиент</span><span class="sxs-lookup"><span data-stu-id="061b3-123">Client</span></span><br/> | <span data-ttu-id="061b3-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="061b3-124">Windows 7</span></span><br/>                                                               |
| <span data-ttu-id="061b3-125">Header</span><span class="sxs-lookup"><span data-stu-id="061b3-125">Header</span></span><br/> | <dl> <span data-ttu-id="061b3-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="061b3-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="061b3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="061b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061b3-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="061b3-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




