---
title: Атрибут WM/Албумковерурл
description: Атрибут WM/Албумковерурл представляет собой универсальный указатель ресурсов (URL-адрес) для обложки альбома или эскиза изображения.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Windows Media Player для атрибута WM/Албумковерурл
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704324"
---
# <a name="wmalbumcoverurl-attribute"></a><span data-ttu-id="4ae22-104">Атрибут WM/Албумковерурл</span><span class="sxs-lookup"><span data-stu-id="4ae22-104">WM/AlbumCoverURL Attribute</span></span>

<span data-ttu-id="4ae22-105">Атрибут **WM/албумковерурл** представляет собой универсальный указатель ресурсов (URL-адрес) для обложки альбома или эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="4ae22-105">The **WM/AlbumCoverURL** attribute is the uniform resource locator (URL) for album art or a thumbnail image.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4ae22-106">Применение</span><span class="sxs-lookup"><span data-stu-id="4ae22-106">Applies To</span></span>

-   [<span data-ttu-id="4ae22-107">**Звуковые элементы**</span><span class="sxs-lookup"><span data-stu-id="4ae22-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="4ae22-108">**Элементы фото**</span><span class="sxs-lookup"><span data-stu-id="4ae22-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="4ae22-109">**Элементы видео**</span><span class="sxs-lookup"><span data-stu-id="4ae22-109">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4ae22-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ae22-110">Remarks</span></span>

<span data-ttu-id="4ae22-111">Для звукового элемента этот атрибут является URL-адресом обложки альбома.</span><span class="sxs-lookup"><span data-stu-id="4ae22-111">For an audio item, this attribute is the URL of the album art.</span></span> <span data-ttu-id="4ae22-112">Для фотографии или видеозаписи этот атрибут является URL-адресом эскиза изображения.</span><span class="sxs-lookup"><span data-stu-id="4ae22-112">For a photo or video item, this attribute is the URL of a thumbnail image.</span></span>

<span data-ttu-id="4ae22-113">Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="4ae22-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="4ae22-114">Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети.</span><span class="sxs-lookup"><span data-stu-id="4ae22-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="4ae22-115">Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="4ae22-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae22-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4ae22-116">Requirements</span></span>



| <span data-ttu-id="4ae22-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4ae22-117">Requirement</span></span> | <span data-ttu-id="4ae22-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4ae22-118">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="4ae22-119">Версия</span><span class="sxs-lookup"><span data-stu-id="4ae22-119">Version</span></span><br/> | <span data-ttu-id="4ae22-120">Проигрыватель Windows Media 12 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="4ae22-120">Windows Media Player 12 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ae22-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ae22-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae22-122">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="4ae22-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





