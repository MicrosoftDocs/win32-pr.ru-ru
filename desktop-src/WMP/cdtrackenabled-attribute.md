---
title: Атрибут Кдтраккенаблед
description: Атрибут Кдтраккенаблед указывает, включена ли запись для воспроизведения.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Кдтраккенаблед атрибут Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699170"
---
# <a name="cdtrackenabled-attribute"></a><span data-ttu-id="1db12-104">Атрибут Кдтраккенаблед</span><span class="sxs-lookup"><span data-stu-id="1db12-104">CDTrackEnabled Attribute</span></span>

<span data-ttu-id="1db12-105">Атрибут **кдтраккенаблед** указывает, включена ли запись для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="1db12-105">The **CDTrackEnabled** attribute indicates whether the track is enabled for playback.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1db12-106">Применение</span><span class="sxs-lookup"><span data-stu-id="1db12-106">Applies To</span></span>

-   [<span data-ttu-id="1db12-107">Дорожки компакт-диска</span><span class="sxs-lookup"><span data-stu-id="1db12-107">CD Tracks</span></span>](cd-track-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1db12-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1db12-108">Remarks</span></span>

<span data-ttu-id="1db12-109">Этот атрибут хранится только в кэше библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1db12-109">This attribute is stored only in the library cache.</span></span>

<span data-ttu-id="1db12-110">При воспроизведении компакт-диска в проигрывателе Windows Media пользователь может выбрать запись и указать, что ее не следует воспроизводить.</span><span class="sxs-lookup"><span data-stu-id="1db12-110">When playing a CD in Windows Media Player, the user may select a track and specify that it should not be played.</span></span> <span data-ttu-id="1db12-111">Это значение атрибута равно true, если запись может быть воспроизведена, или false, если пользователь указал, что трассировка не должна воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="1db12-111">This value of this attribute is True if the track can be played, or False if the user specified that the track should not be played.</span></span>

<span data-ttu-id="1db12-112">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1db12-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1db12-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1db12-113">Requirements</span></span>



| <span data-ttu-id="1db12-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1db12-114">Requirement</span></span> | <span data-ttu-id="1db12-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1db12-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1db12-116">Версия</span><span class="sxs-lookup"><span data-stu-id="1db12-116">Version</span></span><br/> | <span data-ttu-id="1db12-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1db12-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1db12-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1db12-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db12-119">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="1db12-119">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





