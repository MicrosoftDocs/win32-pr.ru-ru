---
title: Атрибут Длнасерверудн
description: Атрибут Длнасерверудн — это уникальное имя устройства сервера, на котором размещен элемент мультимедиа.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- Длнасерверудн атрибут Windows Media Player
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698749"
---
# <a name="dlnaserverudn-attribute"></a><span data-ttu-id="813a7-104">Атрибут Длнасерверудн</span><span class="sxs-lookup"><span data-stu-id="813a7-104">DLNAServerUDN Attribute</span></span>

<span data-ttu-id="813a7-105">Атрибут **длнасерверудн** — это уникальное имя устройства сервера, на котором размещен элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="813a7-105">The **DLNAServerUDN** attribute is the unique device name of the server that hosts the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="813a7-106">Применение</span><span class="sxs-lookup"><span data-stu-id="813a7-106">Applies To</span></span>

-   [<span data-ttu-id="813a7-107">**Звуковые элементы**</span><span class="sxs-lookup"><span data-stu-id="813a7-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="813a7-108">**Элементы фото**</span><span class="sxs-lookup"><span data-stu-id="813a7-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="813a7-109">**Элементы списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="813a7-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="813a7-110">**Элементы видео**</span><span class="sxs-lookup"><span data-stu-id="813a7-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="813a7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="813a7-111">Remarks</span></span>

<span data-ttu-id="813a7-112">Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="813a7-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="813a7-113">Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети.</span><span class="sxs-lookup"><span data-stu-id="813a7-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="813a7-114">Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="813a7-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="813a7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="813a7-115">Requirements</span></span>



| <span data-ttu-id="813a7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="813a7-116">Requirement</span></span> | <span data-ttu-id="813a7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="813a7-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="813a7-118">Версия</span><span class="sxs-lookup"><span data-stu-id="813a7-118">Version</span></span><br/> | <span data-ttu-id="813a7-119">Проигрыватель Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="813a7-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="813a7-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="813a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="813a7-121">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="813a7-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





