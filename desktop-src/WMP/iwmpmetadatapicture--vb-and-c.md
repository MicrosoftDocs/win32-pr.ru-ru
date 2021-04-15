---
title: Интерфейс Ивмпметадатапиктуре (VB и C) (WMP. h)
description: Предоставляет свойства для получения сведений об образе, содержащемуся в цифровом файле мультимедиа, представленном атрибутом WM/Пиктуреметадата.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- Ивмпметадатапиктуре (VB и C) интерфейс проигрывателя Windows Media
- Ивмпметадатапиктуре (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689192"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a><span data-ttu-id="c9084-105">Интерфейс Ивмпметадатапиктуре (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="c9084-105">IWMPMetadataPicture (VB and C#) interface</span></span>

<span data-ttu-id="c9084-106">Предоставляет свойства для получения сведений об образе, содержащемуся в цифровом файле мультимедиа, представленном атрибутом метаданных [**WM/Picture**](/windows/desktop/wmformat/wmpicture).</span><span class="sxs-lookup"><span data-stu-id="c9084-106">Provides properties for getting information about the image contained in a digital media file that is represented by a [**WM/Picture**](/windows/desktop/wmformat/wmpicture)metadata attribute.</span></span> <span data-ttu-id="c9084-107">Этот атрибут соответствует изображениям альбома, содержащимся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.</span><span class="sxs-lookup"><span data-stu-id="c9084-107">This attribute corresponds to album art images contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="c9084-108">Интерфейс **ивмпметадатапиктуре** предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c9084-108">The **IWMPMetadataPicture** interface exposes the following properties.</span></span>



| <span data-ttu-id="c9084-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="c9084-109">Property</span></span>                                                                                   | <span data-ttu-id="c9084-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c9084-110">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="c9084-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c9084-111">**Description**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | <span data-ttu-id="c9084-112">Возвращает описание изображения, представленного атрибутом метаданных.</span><span class="sxs-lookup"><span data-stu-id="c9084-112">Gets the description of the image represented by the metadata attribute.</span></span>  |
| [<span data-ttu-id="c9084-113">**Успешности**</span><span class="sxs-lookup"><span data-stu-id="c9084-113">**mimeType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | <span data-ttu-id="c9084-114">Возвращает тип MIME изображения, представленного атрибутом метаданных.</span><span class="sxs-lookup"><span data-stu-id="c9084-114">Gets the MIME type of the image represented by the metadata attribute.</span></span>    |
| [<span data-ttu-id="c9084-115">**пиктуретипе**</span><span class="sxs-lookup"><span data-stu-id="c9084-115">**pictureType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | <span data-ttu-id="c9084-116">Возвращает тип изображения, представленного атрибутом метаданных.</span><span class="sxs-lookup"><span data-stu-id="c9084-116">Gets the picture type of the image represented by the metadata attribute.</span></span> |
| [<span data-ttu-id="c9084-117">**URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="c9084-117">**URL**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | <span data-ttu-id="c9084-118">Только для внутреннего применения.</span><span class="sxs-lookup"><span data-stu-id="c9084-118">Internal use only.</span></span>                                                        |



 

<span data-ttu-id="c9084-119">Получите интерфейс **ивмпметадатапиктуре** , передав имя атрибута [**WM/Picture**](/windows/desktop/wmformat/wmpicture) следующему методу и приведя возвращаемый объект.</span><span class="sxs-lookup"><span data-stu-id="c9084-119">Get an **IWMPMetadataPicture** interface by passing in the attribute name [**WM/Picture**](/windows/desktop/wmformat/wmpicture) to the following method and casting the object that is returned.</span></span>



| <span data-ttu-id="c9084-120">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="c9084-120">Interface</span></span>                                  | <span data-ttu-id="c9084-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="c9084-121">Property</span></span>                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9084-122">**IWMPMedia3**</span><span class="sxs-lookup"><span data-stu-id="c9084-122">**IWMPMedia3**</span></span>](iwmpmedia3--vb-and-c.md) | [<span data-ttu-id="c9084-123">**жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="c9084-123">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a><span data-ttu-id="c9084-124">Элементы</span><span class="sxs-lookup"><span data-stu-id="c9084-124">Members</span></span>

<span data-ttu-id="c9084-125">Интерфейс **ивмпметадатапиктуре (VB и C#)** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="c9084-125">The **IWMPMetadataPicture (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9084-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c9084-126">Requirements</span></span>



| <span data-ttu-id="c9084-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c9084-127">Requirement</span></span> | <span data-ttu-id="c9084-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c9084-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9084-129">Header</span><span class="sxs-lookup"><span data-stu-id="c9084-129">Header</span></span><br/> | <dl> <span data-ttu-id="c9084-130"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9084-130"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9084-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9084-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9084-132">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="c9084-132">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

