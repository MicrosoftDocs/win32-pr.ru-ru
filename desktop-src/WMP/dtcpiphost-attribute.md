---
title: Атрибут Дткпифост
description: Атрибут Дткпифост — это имя или IP-адрес компьютера или устройства, к которому необходимо обратиться для цифровой передачи Защита содержимого через протокол Интернета (ДТКП-IP) обмен ключами с проверкой подлинности (Аке) для элемента мультимедиа.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Дткпифост атрибут Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698895"
---
# <a name="dtcpiphost-attribute"></a><span data-ttu-id="7b07c-104">Атрибут Дткпифост</span><span class="sxs-lookup"><span data-stu-id="7b07c-104">DTCPIPHost Attribute</span></span>

<span data-ttu-id="7b07c-105">Атрибут **дткпифост** — это имя или IP-адрес компьютера или устройства, к которому необходимо обратиться для цифровой передачи защита содержимого через протокол Интернета (ДТКП-IP) обмен ключами с проверкой подлинности (Аке) для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7b07c-105">The **DTCPIPHost** attribute is the name or IP address of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7b07c-106">Применение</span><span class="sxs-lookup"><span data-stu-id="7b07c-106">Applies To</span></span>

-   [<span data-ttu-id="7b07c-107">**Звуковые элементы**</span><span class="sxs-lookup"><span data-stu-id="7b07c-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7b07c-108">**Элементы фото**</span><span class="sxs-lookup"><span data-stu-id="7b07c-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="7b07c-109">**Элементы списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="7b07c-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="7b07c-110">**Элементы видео**</span><span class="sxs-lookup"><span data-stu-id="7b07c-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7b07c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b07c-111">Remarks</span></span>

<span data-ttu-id="7b07c-112">Если этот атрибут доступен, элемент мультимедиа защищен с помощью ДТКП-IP.</span><span class="sxs-lookup"><span data-stu-id="7b07c-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="7b07c-113">Этот атрибут недоступен для элементов мультимедиа в локальной библиотеке текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b07c-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="7b07c-114">Он доступен только для элементов мультимедиа, принадлежащих удаленной библиотеке. то есть библиотека, доступная другим пользователям в домашней сети.</span><span class="sxs-lookup"><span data-stu-id="7b07c-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="7b07c-115">Чтобы определить, является ли библиотека мультимедиа удаленной, вызовите метод [**ивмплибрари:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="7b07c-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b07c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7b07c-116">Requirements</span></span>



| <span data-ttu-id="7b07c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7b07c-117">Requirement</span></span> | <span data-ttu-id="7b07c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7b07c-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="7b07c-119">Версия</span><span class="sxs-lookup"><span data-stu-id="7b07c-119">Version</span></span><br/> | <span data-ttu-id="7b07c-120">Проигрыватель Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="7b07c-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b07c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b07c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b07c-122">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="7b07c-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





