---
title: Атрибут WM/Writer
description: Атрибут WM/Writer — это имя средства записи, которое написало слова содержимого.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Проигрыватель Windows Media с атрибутом WM/Writer
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648841"
---
# <a name="wmwriter-attribute"></a><span data-ttu-id="6f23d-104">Атрибут WM/Writer</span><span class="sxs-lookup"><span data-stu-id="6f23d-104">WM/Writer Attribute</span></span>

<span data-ttu-id="6f23d-105">Атрибут **WM/Writer** — это имя средства записи, которое написало слова содержимого.</span><span class="sxs-lookup"><span data-stu-id="6f23d-105">The **WM/Writer** attribute is the name of the writer who wrote the words of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6f23d-106">Применение</span><span class="sxs-lookup"><span data-stu-id="6f23d-106">Applies To</span></span>

-   [<span data-ttu-id="6f23d-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="6f23d-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6f23d-108">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="6f23d-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="6f23d-109">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="6f23d-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6f23d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f23d-110">Remarks</span></span>

<span data-ttu-id="6f23d-111">Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6f23d-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="6f23d-112">Этот атрибут может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="6f23d-112">This attribute may have multiple values.</span></span> <span data-ttu-id="6f23d-113">Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="6f23d-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="6f23d-114">**Модуль записи** является псевдонимом для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="6f23d-114">**Writer** is an alias for this attribute.</span></span>

<span data-ttu-id="6f23d-115">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмвритер.</span><span class="sxs-lookup"><span data-stu-id="6f23d-115">The Windows Media Format SDK constant for this attribute is g\_wszWMWriter.</span></span>

<span data-ttu-id="6f23d-116">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6f23d-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f23d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6f23d-117">Requirements</span></span>



| <span data-ttu-id="6f23d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6f23d-118">Requirement</span></span> | <span data-ttu-id="6f23d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6f23d-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6f23d-120">Версия</span><span class="sxs-lookup"><span data-stu-id="6f23d-120">Version</span></span><br/> | <span data-ttu-id="6f23d-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6f23d-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f23d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f23d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f23d-123">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="6f23d-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="6f23d-124">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="6f23d-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





