---
title: Player. Енаблеконтекстмену
description: Свойство Енаблеконтекстмену указывает или получает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Проигрыватель проигрывателя Windows Media Player. Енаблеконтекстмену
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694580"
---
# <a name="playerenablecontextmenu"></a><span data-ttu-id="b2359-104">Player. Енаблеконтекстмену</span><span class="sxs-lookup"><span data-stu-id="b2359-104">Player.enableContextMenu</span></span>

<span data-ttu-id="b2359-105">Свойство **енаблеконтекстмену** указывает или получает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="b2359-105">The **enableContextMenu** property specifies or retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2359-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2359-106">Syntax</span></span>

<span data-ttu-id="b2359-107">*проигрыватель*. **енаблеконтекстмену**</span><span class="sxs-lookup"><span data-stu-id="b2359-107">*player*.**enableContextMenu**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b2359-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b2359-108">Possible Values</span></span>

<span data-ttu-id="b2359-109">Это свойство является логическим значением для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b2359-109">This property is a read/write Boolean.</span></span>



| <span data-ttu-id="b2359-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b2359-110">Value</span></span> | <span data-ttu-id="b2359-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b2359-111">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="b2359-112">true</span><span class="sxs-lookup"><span data-stu-id="b2359-112">true</span></span>  | <span data-ttu-id="b2359-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2359-113">Default.</span></span> <span data-ttu-id="b2359-114">Включите контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="b2359-114">Enable the context menu.</span></span> |
| <span data-ttu-id="b2359-115">false</span><span class="sxs-lookup"><span data-stu-id="b2359-115">false</span></span> | <span data-ttu-id="b2359-116">Не включайте контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="b2359-116">Do not enable the context menu.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="b2359-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2359-117">Remarks</span></span>

<span data-ttu-id="b2359-118">Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно «None».</span><span class="sxs-lookup"><span data-stu-id="b2359-118">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="b2359-119">**Проигрыватель Windows Media 10 Mobile:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b2359-119">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2359-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b2359-120">Requirements</span></span>



| <span data-ttu-id="b2359-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b2359-121">Requirement</span></span> | <span data-ttu-id="b2359-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b2359-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2359-123">Версия</span><span class="sxs-lookup"><span data-stu-id="b2359-123">Version</span></span><br/> | <span data-ttu-id="b2359-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b2359-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b2359-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b2359-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b2359-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2359-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2359-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2359-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2359-128">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="b2359-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





