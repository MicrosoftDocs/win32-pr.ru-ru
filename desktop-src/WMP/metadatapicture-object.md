---
title: Объект Метадатапиктуре
description: Объект Метадатапиктуре предоставляет способ получения значений атрибута метаданных WM/Picture. Этот атрибут соответствует обложке альбома, содержащейся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- Проигрыватель Windows Media Object Метадатапиктуре
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 892b162ba05ab43740565c849b00bc4e3c52aad6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488129"
---
# <a name="metadatapicture-object"></a><span data-ttu-id="53e3d-105">Объект Метадатапиктуре</span><span class="sxs-lookup"><span data-stu-id="53e3d-105">MetadataPicture Object</span></span>

<span data-ttu-id="53e3d-106">Объект **метадатапиктуре** предоставляет способ получения значений атрибута метаданных [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) .</span><span class="sxs-lookup"><span data-stu-id="53e3d-106">The **MetadataPicture** object provides a way to retrieve the values of the [**WM/Picture**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) metadata attribute.</span></span> <span data-ttu-id="53e3d-107">Этот атрибут соответствует обложке альбома, содержащейся в цифровом файле мультимедиа, а не к обложкам альбома, загруженным через Интернет.</span><span class="sxs-lookup"><span data-stu-id="53e3d-107">This attribute corresponds to album art contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="53e3d-108">Объект **метадатапиктуре** поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="53e3d-108">The **MetadataPicture** object supports the following properties.</span></span>



| <span data-ttu-id="53e3d-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="53e3d-109">Property</span></span>                                           | <span data-ttu-id="53e3d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="53e3d-110">Description</span></span>                                       |
|----------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="53e3d-111">**nописание**</span><span class="sxs-lookup"><span data-stu-id="53e3d-111">**description**</span></span>](metadatapicture-description.md) | <span data-ttu-id="53e3d-112">Извлекает описание образа метаданных.</span><span class="sxs-lookup"><span data-stu-id="53e3d-112">Retrieves a description of the metadata image.</span></span>    |
| [<span data-ttu-id="53e3d-113">**Успешности**</span><span class="sxs-lookup"><span data-stu-id="53e3d-113">**mimeType**</span></span>](metadatapicture-mimetype.md)       | <span data-ttu-id="53e3d-114">Возвращает тип MIME изображения метаданных.</span><span class="sxs-lookup"><span data-stu-id="53e3d-114">Retrieves the MIME type of the metadata image.</span></span>    |
| [<span data-ttu-id="53e3d-115">**пиктуретипе**</span><span class="sxs-lookup"><span data-stu-id="53e3d-115">**pictureType**</span></span>](metadatapicture-picturetype.md) | <span data-ttu-id="53e3d-116">Возвращает тип изображения для метаданных.</span><span class="sxs-lookup"><span data-stu-id="53e3d-116">Retrieves the picture type of the metadata image.</span></span> |
| [<span data-ttu-id="53e3d-117">**URL-адрес**</span><span class="sxs-lookup"><span data-stu-id="53e3d-117">**URL**</span></span>](metadatapicture-url.md)                 | <span data-ttu-id="53e3d-118">Только для внутреннего применения.</span><span class="sxs-lookup"><span data-stu-id="53e3d-118">Internal use only.</span></span>                                |



 

<span data-ttu-id="53e3d-119">Доступ к объекту **метадатапиктуре** осуществляется с помощью следующего метода.</span><span class="sxs-lookup"><span data-stu-id="53e3d-119">The **MetadataPicture** object is accessed through the following method.</span></span>



| <span data-ttu-id="53e3d-120">Объект</span><span class="sxs-lookup"><span data-stu-id="53e3d-120">Object</span></span>                        | <span data-ttu-id="53e3d-121">Метод</span><span class="sxs-lookup"><span data-stu-id="53e3d-121">Method</span></span>                                               |
|-------------------------------|------------------------------------------------------|
| [<span data-ttu-id="53e3d-122">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="53e3d-122">**Media**</span></span>](media-object.md) | [<span data-ttu-id="53e3d-123">**жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="53e3d-123">**getItemInfoByType**</span></span>](media-getiteminfobytype.md) |



 

<span data-ttu-id="53e3d-124">В целях иллюстрации `player.currentMedia.getItemInfoByType(name, language, index)` используется в разделах синтаксиса Reference.</span><span class="sxs-lookup"><span data-stu-id="53e3d-124">For purposes of illustration, `player.currentMedia.getItemInfoByType(name, language, index)` is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="53e3d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53e3d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e3d-126">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="53e3d-126">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 