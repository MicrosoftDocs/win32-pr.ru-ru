---
title: Метод Player. Опенплайер
description: Метод Опенплайер открывает проигрыватель Windows Media с использованием указанного URL-адреса. | Метод Player. Опенплайер
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Опенплайер метод Windows Media Player
- метод Опенплайер проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Опенплайер
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704347"
---
# <a name="playeropenplayer-method"></a><span data-ttu-id="cd155-107">Метод Player. Опенплайер</span><span class="sxs-lookup"><span data-stu-id="cd155-107">Player.openPlayer method</span></span>

<span data-ttu-id="cd155-108">Метод **опенплайер** открывает проигрыватель Windows Media с использованием указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="cd155-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd155-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd155-109">Syntax</span></span>


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="cd155-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd155-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd155-111">*URL-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd155-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd155-112">**Строка** , представляющая URL-адрес элемента мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cd155-112">**String** representing the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd155-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd155-113">Return value</span></span>

<span data-ttu-id="cd155-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cd155-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd155-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd155-115">Remarks</span></span>

<span data-ttu-id="cd155-116">Этот метод запускает проигрыватель Windows Media с указанным URL-адресом в качестве текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd155-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="cd155-117">Если проигрыватель был ранее закрыт в режиме обложки, он будет открыт с использованием обложки, последней выбранной пользователем.</span><span class="sxs-lookup"><span data-stu-id="cd155-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="cd155-118">В противном случае проигрыватель откроется в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="cd155-118">Otherwise, the Player opens in full mode.</span></span>

<span data-ttu-id="cd155-119">Если этот метод вызывается из элемента управления Плайерактивекс Windows Media, внедренного в удаленный режим, его поведение идентично *плайераппликатион*. метод **свитчтоплайераппликатион** .</span><span class="sxs-lookup"><span data-stu-id="cd155-119">If this method is called from a Windows Media PlayerActiveX control embedded in remote mode, its behavior is identical to the *PlayerApplication*.**switchToPlayerApplication** method.</span></span>

<span data-ttu-id="cd155-120">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cd155-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd155-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cd155-121">Requirements</span></span>



| <span data-ttu-id="cd155-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cd155-122">Requirement</span></span> | <span data-ttu-id="cd155-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cd155-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd155-124">Версия</span><span class="sxs-lookup"><span data-stu-id="cd155-124">Version</span></span><br/> | <span data-ttu-id="cd155-125">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cd155-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="cd155-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cd155-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="cd155-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd155-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd155-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd155-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd155-129">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="cd155-129">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="cd155-130">**Плайераппликатион. Свитчтоплайераппликатион**</span><span class="sxs-lookup"><span data-stu-id="cd155-130">**PlayerApplication.switchToPlayerApplication**</span></span>](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





