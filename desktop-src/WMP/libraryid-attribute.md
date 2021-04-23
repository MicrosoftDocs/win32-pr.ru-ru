---
title: Атрибут Либрарид
description: Атрибут Либрарид является идентификатором библиотеки, к которой принадлежит элемент.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Либрарид атрибут Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694994"
---
# <a name="libraryid-attribute"></a><span data-ttu-id="46bf6-104">Атрибут Либрарид</span><span class="sxs-lookup"><span data-stu-id="46bf6-104">LibraryID Attribute</span></span>

<span data-ttu-id="46bf6-105">Атрибут **либрарид** является идентификатором библиотеки, к которой принадлежит элемент.</span><span class="sxs-lookup"><span data-stu-id="46bf6-105">The **LibraryID** attribute is the identifier of the library that the item belongs to.</span></span>

## <a name="applies-to"></a><span data-ttu-id="46bf6-106">Применение</span><span class="sxs-lookup"><span data-stu-id="46bf6-106">Applies To</span></span>

-   [<span data-ttu-id="46bf6-107">**Звуковые элементы**</span><span class="sxs-lookup"><span data-stu-id="46bf6-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="46bf6-108">**Элементы фото**</span><span class="sxs-lookup"><span data-stu-id="46bf6-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="46bf6-109">**Элементы списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="46bf6-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="46bf6-110">**Элементы видео**</span><span class="sxs-lookup"><span data-stu-id="46bf6-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="46bf6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46bf6-111">Remarks</span></span>

<span data-ttu-id="46bf6-112">Элемент мультимедиа может принадлежать к локальной библиотеке текущего пользователя или к библиотеке, которая стала доступна другим пользователям в домашней сети или Интернете.</span><span class="sxs-lookup"><span data-stu-id="46bf6-112">A media item might belong to the current user's local library or it might belong to a library that has been made available by another user on the home network or the Internet.</span></span>

<span data-ttu-id="46bf6-113">Значение этого атрибута совпадает со значением, возвращаемым методом [**IWMPLibrary2:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .</span><span class="sxs-lookup"><span data-stu-id="46bf6-113">The value of this attribute is the same as the value returned by the [**IWMPLibrary2::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="46bf6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="46bf6-114">Requirements</span></span>



| <span data-ttu-id="46bf6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="46bf6-115">Requirement</span></span> | <span data-ttu-id="46bf6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="46bf6-116">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="46bf6-117">Версия</span><span class="sxs-lookup"><span data-stu-id="46bf6-117">Version</span></span><br/> | <span data-ttu-id="46bf6-118">Проигрыватель Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="46bf6-118">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46bf6-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46bf6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46bf6-120">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="46bf6-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





