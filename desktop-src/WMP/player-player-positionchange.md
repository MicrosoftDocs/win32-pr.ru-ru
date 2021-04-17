---
title: Событие Player. Поситиончанже
description: Событие Поситиончанже возникает при изменении текущей позиции элемента мультимедиа.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Проигрыватель Windows Media Event Поситиончанже
- Проигрыватель Windows Media Event Поситиончанже, класс Player
- Класс проигрывателя Windows Media Player, событие Поситиончанже
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704411"
---
# <a name="playerpositionchange-event"></a><span data-ttu-id="65815-106">Событие Player. Поситиончанже</span><span class="sxs-lookup"><span data-stu-id="65815-106">Player.PositionChange event</span></span>

<span data-ttu-id="65815-107">Событие **поситиончанже** возникает при изменении текущей позиции элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="65815-107">The **PositionChange** event occurs when the current position of the media item has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="65815-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65815-108">Syntax</span></span>


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a><span data-ttu-id="65815-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="65815-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65815-110">*олдпоситион*</span><span class="sxs-lookup"><span data-stu-id="65815-110">*oldPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="65815-111">Число (**Double**), указывающее старую точку.</span><span class="sxs-lookup"><span data-stu-id="65815-111">Number (**double**) specifying the old position.</span></span>

</dd> <dt>

<span data-ttu-id="65815-112">*невпоситион*</span><span class="sxs-lookup"><span data-stu-id="65815-112">*newPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="65815-113">**Число** (**Double**), задающее новую точку.</span><span class="sxs-lookup"><span data-stu-id="65815-113">**Number** (**double**) specifying the new position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65815-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65815-114">Return value</span></span>

<span data-ttu-id="65815-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="65815-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65815-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65815-116">Remarks</span></span>

<span data-ttu-id="65815-117">Это событие не вызывается во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="65815-117">This event is not raised routinely during playback.</span></span> <span data-ttu-id="65815-118">Это происходит только тогда, когда что-то активно изменяет текущее положение воспроизводимого мультимедийного элемента, например перемещение маркера поиска или кода, указывающего значение для *элементов управления*. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="65815-118">It only occurs when something actively changes the current position of the playing media item, such as the user moving the seek handle or code specifying a value for *Controls*.**currentPosition**.</span></span>

<span data-ttu-id="65815-119">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="65815-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="65815-120">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="65815-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="65815-121">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="65815-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="65815-122">Требования</span><span class="sxs-lookup"><span data-stu-id="65815-122">Requirements</span></span>



| <span data-ttu-id="65815-123">Требование</span><span class="sxs-lookup"><span data-stu-id="65815-123">Requirement</span></span> | <span data-ttu-id="65815-124">Значение</span><span class="sxs-lookup"><span data-stu-id="65815-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65815-125">Версия</span><span class="sxs-lookup"><span data-stu-id="65815-125">Version</span></span><br/> | <span data-ttu-id="65815-126">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="65815-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="65815-127">DLL</span><span class="sxs-lookup"><span data-stu-id="65815-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="65815-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65815-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65815-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65815-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65815-130">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="65815-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





