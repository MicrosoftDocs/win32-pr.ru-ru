---
title: Атрибут Длнасаурцеури
description: Атрибут Длнасаурцеури является универсальным идентификатором ресурса (URI) элемента.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Длнасаурцеури атрибут Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694916"
---
# <a name="dlnasourceuri-attribute"></a><span data-ttu-id="f8707-104">Атрибут Длнасаурцеури</span><span class="sxs-lookup"><span data-stu-id="f8707-104">DLNASourceURI Attribute</span></span>

<span data-ttu-id="f8707-105">Атрибут **длнасаурцеури** является универсальным идентификатором ресурса (URI) элемента.</span><span class="sxs-lookup"><span data-stu-id="f8707-105">The **DLNASourceURI** attribute is the universal resource identifier (URI) of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f8707-106">Применение</span><span class="sxs-lookup"><span data-stu-id="f8707-106">Applies To</span></span>

-   [<span data-ttu-id="f8707-107">**Звуковые элементы**</span><span class="sxs-lookup"><span data-stu-id="f8707-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f8707-108">**Другие элементы**</span><span class="sxs-lookup"><span data-stu-id="f8707-108">**Other Items**</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="f8707-109">**Элементы фото**</span><span class="sxs-lookup"><span data-stu-id="f8707-109">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="f8707-110">**Элементы списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="f8707-110">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="f8707-111">**Элементы видео**</span><span class="sxs-lookup"><span data-stu-id="f8707-111">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f8707-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8707-112">Remarks</span></span>

<span data-ttu-id="f8707-113">Если элемент находится в локальной библиотеке текущего пользователя, этот атрибут, атрибут [**саурцеурл**](sourceurl-attribute.md) и значение, возвращаемое [**ивмпмедиа:: Get \_ саурцеурл**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) , являются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="f8707-113">If the item is in the current user's local library, this attribute, the [**SourceURL**](sourceurl-attribute.md) attribute, and the value returned by [**IWMPMedia::get\_sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) are all the same.</span></span>

<span data-ttu-id="f8707-114">Если элемент отсутствует в локальной библиотеке текущего пользователя, но принадлежит удаленной библиотеке, этот атрибут является идентификатором формы DLNA-плайсингле://*xxx*.</span><span class="sxs-lookup"><span data-stu-id="f8707-114">If the item is not in the current user's local library, but belongs to a remote library, this attribute is an identifier of the form dlna-playsingle://*xxx*.</span></span>

<span data-ttu-id="f8707-115">Вы можете передать универсальный код ресурса (URI) DLNA-плайсингле методу [**IWMPCore3:: невмедиа**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) , чтобы получить интерфейс [**ивмпмедиа**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) , позволяющий просматривать метаданные элемента мультимедиа и, возможно, изменять рейтинг элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f8707-115">You can pass a dlna-playsingle URI to the [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) method to obtain an [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) interface that enables you to view the media item's metadata and potentially edit the media item's star rating.</span></span> <span data-ttu-id="f8707-116">Однако обратите внимание, что универсальный код ресурса (URI) DLNA-плайсингле должен быть для службы каталогов содержимого (CD), которая уже обнаружена проигрывателем Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f8707-116">Note, however, that the dlna-playsingle URI must be for a content directory service (CDS) that Windows Media Player has already discovered.</span></span> <span data-ttu-id="f8707-117">Метод **невмедиа** не будет инициировать обнаружение UPnP и поиск компакт-дисков.</span><span class="sxs-lookup"><span data-stu-id="f8707-117">The **newMedia** method will not initiate UPnP discovery and search for the CDS.</span></span>

<span data-ttu-id="f8707-118">Оценку "звезда" элемента мультимедиа в удаленной библиотеке можно изменить, только если удаленная библиотека поддерживает операцию изменения.</span><span class="sxs-lookup"><span data-stu-id="f8707-118">You can edit the star rating of a media item in a remote library only if the remote library supports the edit operation.</span></span> <span data-ttu-id="f8707-119">Удаленные библиотеки, размещенные на компьютере под управлением Windows 7, поддерживают операцию изменения.</span><span class="sxs-lookup"><span data-stu-id="f8707-119">Remote libraries hosted on a computer running Windows 7 support the edit operation.</span></span> <span data-ttu-id="f8707-120">Удаленные библиотеки, размещенные на компьютере под управлением операционной системы Windows, предшествующей Windows 7, не поддерживают операцию изменения.</span><span class="sxs-lookup"><span data-stu-id="f8707-120">Remote libraries hosted on a computer running a Windows operating system earlier than Windows 7 do not support the edit operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8707-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f8707-121">Requirements</span></span>



| <span data-ttu-id="f8707-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f8707-122">Requirement</span></span> | <span data-ttu-id="f8707-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f8707-123">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="f8707-124">Версия</span><span class="sxs-lookup"><span data-stu-id="f8707-124">Version</span></span><br/> | <span data-ttu-id="f8707-125">Проигрыватель Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="f8707-125">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8707-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8707-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8707-127">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="f8707-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





