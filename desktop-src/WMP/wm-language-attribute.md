---
title: Атрибут WM/Language
description: Атрибут WM/Language является языком элемента.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Атрибут WM/Language проигрывателя Windows Media
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704297"
---
# <a name="wmlanguage-attribute"></a><span data-ttu-id="6332e-104">Атрибут WM/Language</span><span class="sxs-lookup"><span data-stu-id="6332e-104">WM/Language Attribute</span></span>

<span data-ttu-id="6332e-105">Атрибут **WM/Language** является языком элемента.</span><span class="sxs-lookup"><span data-stu-id="6332e-105">The **WM/Language** attribute is the language of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6332e-106">Применение</span><span class="sxs-lookup"><span data-stu-id="6332e-106">Applies To</span></span>

-   [<span data-ttu-id="6332e-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="6332e-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6332e-108">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="6332e-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="6332e-109">Элементы Радио</span><span class="sxs-lookup"><span data-stu-id="6332e-109">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="6332e-110">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="6332e-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6332e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6332e-111">Remarks</span></span>

<span data-ttu-id="6332e-112">Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6332e-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="6332e-113">Этот атрибут может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="6332e-113">This attribute may have multiple values.</span></span> <span data-ttu-id="6332e-114">Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="6332e-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="6332e-115">**Язык** является псевдонимом для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="6332e-115">**Language** is an alias for this attribute.</span></span>

<span data-ttu-id="6332e-116">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмлангуаже.</span><span class="sxs-lookup"><span data-stu-id="6332e-116">The Windows Media Format SDK constant for this attribute is g\_wszWMLanguage.</span></span>

<span data-ttu-id="6332e-117">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6332e-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6332e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6332e-118">Requirements</span></span>



| <span data-ttu-id="6332e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6332e-119">Requirement</span></span> | <span data-ttu-id="6332e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6332e-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6332e-121">Версия</span><span class="sxs-lookup"><span data-stu-id="6332e-121">Version</span></span><br/> | <span data-ttu-id="6332e-122">Проигрыватель Windows Media 9 Series или более поздней версии (элемент Radio поддерживается только в проигрывателе Windows Media 9 Series)</span><span class="sxs-lookup"><span data-stu-id="6332e-122">Windows Media Player 9 Series or later (The radio item is supported only in Windows Media Player 9 Series)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6332e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6332e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6332e-124">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="6332e-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="6332e-125">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="6332e-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





