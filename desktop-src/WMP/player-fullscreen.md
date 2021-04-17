---
title: Player. полноэкранный режим
description: Свойство "полноэкранное" указывает или получает значение, указывающее, воспроизводится ли видео в полноэкранном режиме.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Player. полноэкранный проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694577"
---
# <a name="playerfullscreen"></a><span data-ttu-id="ef147-104">Player. полноэкранный режим</span><span class="sxs-lookup"><span data-stu-id="ef147-104">Player.fullScreen</span></span>

<span data-ttu-id="ef147-105">Свойство " **полноэкранное** " указывает или получает значение, указывающее, воспроизводится ли видео в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="ef147-105">The **fullScreen** property specifies or retrieves a value indicating whether video content is played back in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef147-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef147-106">Syntax</span></span>

<span data-ttu-id="ef147-107">*проигрыватель* . во **весь экран**</span><span class="sxs-lookup"><span data-stu-id="ef147-107">*player* .**fullScreen**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ef147-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ef147-108">Possible Values</span></span>

<span data-ttu-id="ef147-109">Это свойство является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ef147-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="ef147-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ef147-110">Value</span></span> | <span data-ttu-id="ef147-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ef147-111">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="ef147-112">true</span><span class="sxs-lookup"><span data-stu-id="ef147-112">true</span></span>  | <span data-ttu-id="ef147-113">Видеоматериал воспроизводится в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="ef147-113">Video content is played back in full-screen mode.</span></span>              |
| <span data-ttu-id="ef147-114">false</span><span class="sxs-lookup"><span data-stu-id="ef147-114">false</span></span> | <span data-ttu-id="ef147-115">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef147-115">Default.</span></span> <span data-ttu-id="ef147-116">Видеоматериалы не воспроизводятся в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="ef147-116">Video content is not played back in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ef147-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef147-117">Remarks</span></span>

<span data-ttu-id="ef147-118">Чтобы полноэкранный режим работал правильно при внедрении элемента управления проигрывателя Windows Media, область отображения видео должна иметь высоту и ширину по крайней мере на один пиксель.</span><span class="sxs-lookup"><span data-stu-id="ef147-118">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="ef147-119">Если для **uiMode** задано значение "Mini" или "Full", то высота самого элемента управления должна быть 65 или больше для размещения видеообласти в дополнение к пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="ef147-119">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="ef147-120">Если для **uiMode** задано значение "Невидимый", то установка этого свойства в значение true вызовет ошибку и не влияет на поведение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ef147-120">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="ef147-121">Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно «None».</span><span class="sxs-lookup"><span data-stu-id="ef147-121">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="ef147-122">Если для **uiMode** задано значение Full или Mini, проигрыватель Windows Media отображает элементы управления движением в полноэкранном режиме при перемещении курсора мыши.</span><span class="sxs-lookup"><span data-stu-id="ef147-122">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="ef147-123">По истечении короткого интервала перемещения мыши элементы управления транспорта скрываются.</span><span class="sxs-lookup"><span data-stu-id="ef147-123">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="ef147-124">Если для **uiMode** задано значение "нет", никакие элементы управления не отображаются в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="ef147-124">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="ef147-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ef147-125">**Note**</span></span>

<span data-ttu-id="ef147-126">Для отображения элементов управления транспорта в полноэкранном режиме требуется операционная система Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ef147-126">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

<span data-ttu-id="ef147-127">Если элементы управления передачей не отображаются в полноэкранном режиме, проигрыватель Windows Media автоматически выходит из полноэкранного режима при остановке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ef147-127">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

<span data-ttu-id="ef147-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ef147-128">**Note**</span></span>

<span data-ttu-id="ef147-129">Всегда проинформируйте пользователя о том, как вернуться из полноэкранного режима.</span><span class="sxs-lookup"><span data-stu-id="ef147-129">Always be sure to inform the user how to return from full-screen mode.</span></span>

## <a name="examples"></a><span data-ttu-id="ef147-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="ef147-130">Examples</span></span>

<span data-ttu-id="ef147-131">В следующем примере создается HTML-кнопка ввода, которая использует *проигрыватель*. **полноэкранный** режим для переключения внедренного объекта Player на полноэкранный.</span><span class="sxs-lookup"><span data-stu-id="ef147-131">The following example creates an HTML input button that uses *Player*.**fullScreen** to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="ef147-132">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="ef147-132">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a><span data-ttu-id="ef147-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ef147-133">Requirements</span></span>



| <span data-ttu-id="ef147-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ef147-134">Requirement</span></span> | <span data-ttu-id="ef147-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ef147-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef147-136">Версия</span><span class="sxs-lookup"><span data-stu-id="ef147-136">Version</span></span><br/> | <span data-ttu-id="ef147-137">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ef147-137">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ef147-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ef147-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="ef147-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef147-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef147-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef147-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef147-141">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="ef147-141">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





