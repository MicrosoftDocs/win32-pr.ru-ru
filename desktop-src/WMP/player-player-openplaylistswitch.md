---
title: Событие Player. Опенплайлистсвитч
description: Событие Опенплайлистсвитч возникает, когда начинается воспроизведение заголовка на DVD-диске. | Событие Player. Опенплайлистсвитч
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Проигрыватель Windows Media Event Опенплайлистсвитч
- Проигрыватель Windows Media Event Опенплайлистсвитч, класс Player
- Класс проигрывателя Windows Media Player, событие Опенплайлистсвитч
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704243"
---
# <a name="playeropenplaylistswitch-event"></a><span data-ttu-id="dfe84-107">Событие Player. Опенплайлистсвитч</span><span class="sxs-lookup"><span data-stu-id="dfe84-107">Player.OpenPlaylistSwitch event</span></span>

<span data-ttu-id="dfe84-108">Событие **опенплайлистсвитч** возникает, когда начинается воспроизведение заголовка на DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="dfe84-108">The **OpenPlaylistSwitch** event occurs when a title on a DVD begins playing.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe84-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfe84-109">Syntax</span></span>


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a><span data-ttu-id="dfe84-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfe84-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfe84-111">*питем*</span><span class="sxs-lookup"><span data-stu-id="dfe84-111">*pItem*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe84-112">Объект **списка воспроизведения** , представляющий заголовок.</span><span class="sxs-lookup"><span data-stu-id="dfe84-112">**Playlist** object representing the title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfe84-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfe84-113">Return value</span></span>

<span data-ttu-id="dfe84-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dfe84-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfe84-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfe84-115">Remarks</span></span>

<span data-ttu-id="dfe84-116">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="dfe84-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="dfe84-117">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="dfe84-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe84-118">Требования</span><span class="sxs-lookup"><span data-stu-id="dfe84-118">Requirements</span></span>



| <span data-ttu-id="dfe84-119">Требование</span><span class="sxs-lookup"><span data-stu-id="dfe84-119">Requirement</span></span> | <span data-ttu-id="dfe84-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dfe84-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe84-121">Версия</span><span class="sxs-lookup"><span data-stu-id="dfe84-121">Version</span></span><br/> | <span data-ttu-id="dfe84-122">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="dfe84-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="dfe84-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dfe84-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="dfe84-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfe84-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe84-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfe84-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe84-126">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="dfe84-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





