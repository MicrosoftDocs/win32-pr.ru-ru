---
title: Атрибут WM/проводника
description: Атрибут WM/проводника — это имя проводника музыки.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- Проигрыватель Windows Media с атрибутом WM/проводника
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704315"
---
# <a name="wmconductor-attribute"></a><span data-ttu-id="8b675-104">Атрибут WM/проводника</span><span class="sxs-lookup"><span data-stu-id="8b675-104">WM/Conductor Attribute</span></span>

<span data-ttu-id="8b675-105">Атрибут **WM/проводника** — это имя проводника музыки.</span><span class="sxs-lookup"><span data-stu-id="8b675-105">The **WM/Conductor** attribute is the name of the conductor of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8b675-106">Применение</span><span class="sxs-lookup"><span data-stu-id="8b675-106">Applies To</span></span>

-   [<span data-ttu-id="8b675-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="8b675-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="8b675-108">Дорожки компакт-диска</span><span class="sxs-lookup"><span data-stu-id="8b675-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="8b675-109">Часто используемые атрибуты файлов Windows Media</span><span class="sxs-lookup"><span data-stu-id="8b675-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="8b675-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b675-110">Remarks</span></span>

<span data-ttu-id="8b675-111">Этот атрибут хранится как в библиотеке (или в кэше), так и в файле цифрового носителя.</span><span class="sxs-lookup"><span data-stu-id="8b675-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="8b675-112">Этот атрибут может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="8b675-112">This attribute may have multiple values.</span></span> <span data-ttu-id="8b675-113">Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="8b675-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="8b675-114">**Проводник** является псевдонимом для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="8b675-114">**Conductor** is an alias for this attribute.</span></span>

<span data-ttu-id="8b675-115">Константа Windows Media Format SDK для этого атрибута — g \_ всзвмкондуктор.</span><span class="sxs-lookup"><span data-stu-id="8b675-115">The Windows Media Format SDK constant for this attribute is g\_wszWMConductor.</span></span>

<span data-ttu-id="8b675-116">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8b675-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b675-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8b675-117">Requirements</span></span>



| <span data-ttu-id="8b675-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8b675-118">Requirement</span></span> | <span data-ttu-id="8b675-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8b675-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8b675-120">Версия</span><span class="sxs-lookup"><span data-stu-id="8b675-120">Version</span></span><br/> | <span data-ttu-id="8b675-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8b675-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b675-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b675-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b675-123">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="8b675-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="8b675-124">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="8b675-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





