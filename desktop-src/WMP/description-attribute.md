---
title: Атрибут Description (пакет SDK для проигрывателя)
description: Атрибут Description является описанием содержимого.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Описание атрибут Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694761"
---
# <a name="description-attribute"></a><span data-ttu-id="e5d76-104">Атрибут Description</span><span class="sxs-lookup"><span data-stu-id="e5d76-104">Description Attribute</span></span>

<span data-ttu-id="e5d76-105">Атрибут **Description** является описанием содержимого.</span><span class="sxs-lookup"><span data-stu-id="e5d76-105">The **Description** attribute is a description of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e5d76-106">Применение</span><span class="sxs-lookup"><span data-stu-id="e5d76-106">Applies To</span></span>

-   [<span data-ttu-id="e5d76-107">Музыкальные файлы</span><span class="sxs-lookup"><span data-stu-id="e5d76-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e5d76-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5d76-108">Remarks</span></span>

<span data-ttu-id="e5d76-109">Этот атрибут хранится в музыкальных файлах, а не в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="e5d76-109">This attribute is stored in music files, not in the library.</span></span>

<span data-ttu-id="e5d76-110">Этот атрибут может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="e5d76-110">This attribute may have multiple values.</span></span> <span data-ttu-id="e5d76-111">Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать *носитель*. метод **жетитеминфобитипе** , а не метод *Media*. getItemInfo.</span><span class="sxs-lookup"><span data-stu-id="e5d76-111">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.getItemInfo method.</span></span>

<span data-ttu-id="e5d76-112">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмдескриптион.</span><span class="sxs-lookup"><span data-stu-id="e5d76-112">The Windows Media Format SDK constant for this attribute is g\_wszWMDescription.</span></span>

<span data-ttu-id="e5d76-113">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e5d76-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d76-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e5d76-114">Requirements</span></span>



| <span data-ttu-id="e5d76-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e5d76-115">Requirement</span></span> | <span data-ttu-id="e5d76-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d76-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e5d76-117">Версия</span><span class="sxs-lookup"><span data-stu-id="e5d76-117">Version</span></span><br/> | <span data-ttu-id="e5d76-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e5d76-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5d76-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5d76-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d76-120">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="e5d76-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





