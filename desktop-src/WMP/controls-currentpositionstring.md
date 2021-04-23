---
title: Controls. Куррентпоситионстринг
description: Свойство Куррентпоситионстринг извлекает текущую позицию в элементе мультимедиа в виде строки в формате чч мм СС (часы, минуты и секунды).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Проигрыватель Windows Media Controls. Куррентпоситионстринг
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698991"
---
# <a name="controlscurrentpositionstring"></a><span data-ttu-id="b5b6f-104">Controls. Куррентпоситионстринг</span><span class="sxs-lookup"><span data-stu-id="b5b6f-104">Controls.currentPositionString</span></span>

<span data-ttu-id="b5b6f-105">Свойство **куррентпоситионстринг** извлекает текущую позицию в элементе мультимедиа в виде **строки** , отформатированной как чч: мм: СС (часы, минуты и секунды).</span><span class="sxs-lookup"><span data-stu-id="b5b6f-105">The **currentPositionString** property retrieves the current position in the media item as a **String** formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a><span data-ttu-id="b5b6f-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b5b6f-106">Possible Values</span></span>

<span data-ttu-id="b5b6f-107">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5b6f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5b6f-108">Remarks</span></span>

<span data-ttu-id="b5b6f-109">Если размер элемента мультимедиа меньше часа, часть чч: не включается.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-109">If the media item is less than an hour long, the HH: portion is not included.</span></span>

> [!Note]  
> <span data-ttu-id="b5b6f-110">Необходимо включить код для остановки таймера при остановке или приостановке элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-110">You should include code to stop the timer when the media item is stopped or paused.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b5b6f-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="b5b6f-111">Examples</span></span>

<span data-ttu-id="b5b6f-112">В следующем примере JScript запускается таймер HTML, который отображает текущее расположение файла мультимедиа с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-112">The following JScript example starts an HTML timer that displays the current position of the media file at one-second intervals.</span></span> <span data-ttu-id="b5b6f-113">Для вывода текущей позицией был создан HTML-элемент с именем MyText.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-113">An HTML TEXT element named MyText was created to display the current position.</span></span> <span data-ttu-id="b5b6f-114">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="b5b6f-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a><span data-ttu-id="b5b6f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b5b6f-115">Requirements</span></span>



| <span data-ttu-id="b5b6f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b5b6f-116">Requirement</span></span> | <span data-ttu-id="b5b6f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b5b6f-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b6f-118">Версия</span><span class="sxs-lookup"><span data-stu-id="b5b6f-118">Version</span></span><br/> | <span data-ttu-id="b5b6f-119">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="b5b6f-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b5b6f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b5b6f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5b6f-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5b6f-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b6f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5b6f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b6f-123">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="b5b6f-123">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





