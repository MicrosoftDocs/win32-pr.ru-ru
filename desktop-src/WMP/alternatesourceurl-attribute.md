---
title: Атрибут Алтернатесаурцеурл
description: Атрибут Алтернатесаурцеурл — это универсальный указатель ресурсов для элемента мультимедиа, который служит альтернативой атрибутам Длнасаурцеури и Саурцеурл.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Алтернатесаурцеурл атрибут Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695027"
---
# <a name="alternatesourceurl-attribute"></a><span data-ttu-id="d9cf4-104">Атрибут Алтернатесаурцеурл</span><span class="sxs-lookup"><span data-stu-id="d9cf4-104">AlternateSourceURL Attribute</span></span>

<span data-ttu-id="d9cf4-105">Атрибут **алтернатесаурцеурл** — это универсальный указатель ресурсов для элемента мультимедиа, который служит альтернативой атрибутам [**длнасаурцеури**](dlnasourceuri-attribute.md) и [**саурцеурл**](sourceurl-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d9cf4-105">The **AlternateSourceURL** attribute is a uniform resource locator for the media item that serves as an alternative to the [**DLNASourceURI**](dlnasourceuri-attribute.md) and [**SourceURL**](sourceurl-attribute.md) attributes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d9cf4-106">Применение</span><span class="sxs-lookup"><span data-stu-id="d9cf4-106">Applies To</span></span>

-   [<span data-ttu-id="d9cf4-107">**Звуковые элементы**</span><span class="sxs-lookup"><span data-stu-id="d9cf4-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="d9cf4-108">**Элементы фото**</span><span class="sxs-lookup"><span data-stu-id="d9cf4-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="d9cf4-109">**Элементы списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="d9cf4-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="d9cf4-110">**Элементы видео**</span><span class="sxs-lookup"><span data-stu-id="d9cf4-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="d9cf4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9cf4-111">Remarks</span></span>

<span data-ttu-id="d9cf4-112">Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d9cf4-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="d9cf4-113">Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети.</span><span class="sxs-lookup"><span data-stu-id="d9cf4-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="d9cf4-114">Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="d9cf4-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9cf4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d9cf4-115">Requirements</span></span>



| <span data-ttu-id="d9cf4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d9cf4-116">Requirement</span></span> | <span data-ttu-id="d9cf4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d9cf4-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="d9cf4-118">Версия</span><span class="sxs-lookup"><span data-stu-id="d9cf4-118">Version</span></span><br/> | <span data-ttu-id="d9cf4-119">Проигрыватель Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="d9cf4-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9cf4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9cf4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9cf4-121">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="d9cf4-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





