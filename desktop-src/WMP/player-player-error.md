---
title: Событие Player. Error
description: Событие ошибки возникает при возникновении состояния ошибки.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Проигрыватель Windows Media, событие ошибки
- Событие ошибки Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, событие ошибки
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708316"
---
# <a name="playererror-event"></a><span data-ttu-id="e1f49-106">Событие Player. Error</span><span class="sxs-lookup"><span data-stu-id="e1f49-106">Player.Error event</span></span>

<span data-ttu-id="e1f49-107">Событие **ошибки** возникает при возникновении состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="e1f49-107">The **Error** event occurs when there is an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f49-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1f49-108">Syntax</span></span>


```JScript
Player.Error()
```



## <a name="parameters"></a><span data-ttu-id="e1f49-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1f49-109">Parameters</span></span>

<span data-ttu-id="e1f49-110">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="e1f49-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1f49-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1f49-111">Return value</span></span>

<span data-ttu-id="e1f49-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e1f49-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e1f49-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="e1f49-113">Examples</span></span>

<span data-ttu-id="e1f49-114">В следующем примере JScript создается обработчик событий для вывода текста описания первой ошибки в очереди ошибок.</span><span class="sxs-lookup"><span data-stu-id="e1f49-114">The following JScript example creates an event handler to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="e1f49-115">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="e1f49-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="e1f49-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e1f49-116">Requirements</span></span>



| <span data-ttu-id="e1f49-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e1f49-117">Requirement</span></span> | <span data-ttu-id="e1f49-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e1f49-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f49-119">Версия</span><span class="sxs-lookup"><span data-stu-id="e1f49-119">Version</span></span><br/> | <span data-ttu-id="e1f49-120">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="e1f49-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e1f49-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e1f49-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1f49-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1f49-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f49-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1f49-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f49-124">**Ерроритем. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="e1f49-124">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> <dt>

[<span data-ttu-id="e1f49-125">**Ошибка. элемент**</span><span class="sxs-lookup"><span data-stu-id="e1f49-125">**Error.item**</span></span>](error-item.md)
</dt> <dt>

[<span data-ttu-id="e1f49-126">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="e1f49-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





