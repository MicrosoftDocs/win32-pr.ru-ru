---
title: Событие Player. Медиаколлектионмедиаремовед
description: Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки. | Событие Player. Медиаколлектионмедиаремовед
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Проигрыватель Windows Media Event Медиаколлектионмедиаремовед
- Проигрыватель Windows Media Event Медиаколлектионмедиаремовед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионмедиаремовед
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708593"
---
# <a name="playermediacollectionmediaremoved-event"></a><span data-ttu-id="c44ec-107">Событие Player. Медиаколлектионмедиаремовед</span><span class="sxs-lookup"><span data-stu-id="c44ec-107">Player.MediaCollectionMediaRemoved event</span></span>

<span data-ttu-id="c44ec-108">Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="c44ec-108">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c44ec-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c44ec-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="c44ec-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c44ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c44ec-111">*пдиспмедиа*</span><span class="sxs-lookup"><span data-stu-id="c44ec-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="c44ec-112">Удаленный объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="c44ec-112">**Media** object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c44ec-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c44ec-113">Return value</span></span>

<span data-ttu-id="c44ec-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c44ec-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c44ec-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c44ec-115">Remarks</span></span>

<span data-ttu-id="c44ec-116">Это событие происходит только в локальной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c44ec-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="c44ec-117">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c44ec-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="c44ec-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c44ec-118">Requirements</span></span>



| <span data-ttu-id="c44ec-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c44ec-119">Requirement</span></span> | <span data-ttu-id="c44ec-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c44ec-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c44ec-121">Версия</span><span class="sxs-lookup"><span data-stu-id="c44ec-121">Version</span></span><br/> | <span data-ttu-id="c44ec-122">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="c44ec-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c44ec-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c44ec-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c44ec-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c44ec-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c44ec-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c44ec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c44ec-126">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="c44ec-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c44ec-127">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="c44ec-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="c44ec-128">**Player. Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="c44ec-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





