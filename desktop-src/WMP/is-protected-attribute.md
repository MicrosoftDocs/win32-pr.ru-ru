---
title: Атрибут Is_Protected
description: '\_Атрибут protected указывает, защищено ли содержимое с помощью управления цифровыми правами (DRM).'
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protectedный атрибут проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689510"
---
# <a name="is_protected-attribute"></a><span data-ttu-id="26cdf-104">\_Защищенный атрибут</span><span class="sxs-lookup"><span data-stu-id="26cdf-104">Is\_Protected Attribute</span></span>

<span data-ttu-id="26cdf-105">Атрибут **\_ protected** указывает, защищено ли содержимое с помощью управления цифровыми правами (DRM).</span><span class="sxs-lookup"><span data-stu-id="26cdf-105">The **Is\_Protected** attribute indicates whether the content is protected using digital rights management (DRM).</span></span>

## <a name="applies-to"></a><span data-ttu-id="26cdf-106">Применение</span><span class="sxs-lookup"><span data-stu-id="26cdf-106">Applies To</span></span>

-   [<span data-ttu-id="26cdf-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="26cdf-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="26cdf-108">Часто используемые файлы Windows Media</span><span class="sxs-lookup"><span data-stu-id="26cdf-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="26cdf-109">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="26cdf-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="26cdf-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26cdf-110">Remarks</span></span>

<span data-ttu-id="26cdf-111">Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="26cdf-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="26cdf-112">**Дигиталлисекуре** является псевдонимом для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="26cdf-112">**DigitallySecure** is an alias for this attribute.</span></span>

<span data-ttu-id="26cdf-113">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмпротектед.</span><span class="sxs-lookup"><span data-stu-id="26cdf-113">The Windows Media Format SDK constant for this attribute is g\_wszWMProtected.</span></span>

<span data-ttu-id="26cdf-114">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="26cdf-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="26cdf-115">Требования</span><span class="sxs-lookup"><span data-stu-id="26cdf-115">Requirements</span></span>



| <span data-ttu-id="26cdf-116">Требование</span><span class="sxs-lookup"><span data-stu-id="26cdf-116">Requirement</span></span> | <span data-ttu-id="26cdf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="26cdf-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="26cdf-118">Версия</span><span class="sxs-lookup"><span data-stu-id="26cdf-118">Version</span></span><br/> | <span data-ttu-id="26cdf-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="26cdf-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26cdf-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26cdf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26cdf-121">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="26cdf-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





