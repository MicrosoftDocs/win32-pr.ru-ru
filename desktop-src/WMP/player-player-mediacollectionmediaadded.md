---
title: Событие Player. Медиаколлектионмедиааддед
description: Событие Медиаколлектионмедиааддед возникает при добавлении элемента мультимедиа в локальную библиотеку. | Событие Player. Медиаколлектионмедиааддед
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- Проигрыватель Windows Media Event Медиаколлектионмедиааддед
- Проигрыватель Windows Media Event Медиаколлектионмедиааддед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионмедиааддед
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18dd0536f508090c46f9fc5a9059c809f50091d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708484"
---
# <a name="playermediacollectionmediaadded-event"></a><span data-ttu-id="733e4-107">Событие Player. Медиаколлектионмедиааддед</span><span class="sxs-lookup"><span data-stu-id="733e4-107">Player.MediaCollectionMediaAdded event</span></span>

<span data-ttu-id="733e4-108">Событие Медиаколлектионмедиааддед возникает при добавлении элемента мультимедиа в локальную библиотеку.</span><span class="sxs-lookup"><span data-stu-id="733e4-108">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="733e4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="733e4-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="733e4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="733e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733e4-111">*пдиспмедиа*</span><span class="sxs-lookup"><span data-stu-id="733e4-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="733e4-112">Добавленный объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="733e4-112">**Media** object that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733e4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="733e4-113">Return value</span></span>

<span data-ttu-id="733e4-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="733e4-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="733e4-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="733e4-115">Remarks</span></span>

<span data-ttu-id="733e4-116">Это событие происходит только в локальной библиотеке.</span><span class="sxs-lookup"><span data-stu-id="733e4-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="733e4-117">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="733e4-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="733e4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="733e4-118">Requirements</span></span>



| <span data-ttu-id="733e4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="733e4-119">Requirement</span></span> | <span data-ttu-id="733e4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="733e4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="733e4-121">Версия</span><span class="sxs-lookup"><span data-stu-id="733e4-121">Version</span></span><br/> | <span data-ttu-id="733e4-122">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="733e4-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="733e4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="733e4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="733e4-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="733e4-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733e4-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="733e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733e4-126">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="733e4-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="733e4-127">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="733e4-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="733e4-128">**Player. Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="733e4-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





