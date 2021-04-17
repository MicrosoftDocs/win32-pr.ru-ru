---
title: Событие Player. Медиачанже
description: Событие Медиачанже возникает при изменении элемента мультимедиа. | Событие Player. Медиачанже
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Проигрыватель Windows Media Event Медиачанже
- Проигрыватель Windows Media Event Медиачанже, класс Player
- Класс проигрывателя Windows Media Player, событие Медиачанже
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708487"
---
# <a name="playermediachange-event"></a><span data-ttu-id="da1e6-107">Событие Player. Медиачанже</span><span class="sxs-lookup"><span data-stu-id="da1e6-107">Player.MediaChange event</span></span>

<span data-ttu-id="da1e6-108">Событие **медиачанже** возникает при изменении элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="da1e6-108">The **MediaChange** event occurs when a media item changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1e6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da1e6-109">Syntax</span></span>


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a><span data-ttu-id="da1e6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="da1e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1e6-111">*Элемент*</span><span class="sxs-lookup"><span data-stu-id="da1e6-111">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="da1e6-112">Объект **мультимедиа** , представляющий измененный элемент.</span><span class="sxs-lookup"><span data-stu-id="da1e6-112">**Media** object representing the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1e6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da1e6-113">Return value</span></span>

<span data-ttu-id="da1e6-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="da1e6-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1e6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da1e6-115">Remarks</span></span>

<span data-ttu-id="da1e6-116">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="da1e6-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="da1e6-117">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="da1e6-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="da1e6-118">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="da1e6-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="da1e6-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="da1e6-119">Examples</span></span>

<span data-ttu-id="da1e6-120">В следующем примере JScript для вывода имени текущего элемента мультимедиа используется элемент HTML DIV с именем MediaName.</span><span class="sxs-lookup"><span data-stu-id="da1e6-120">The following JScript example uses an HTML DIV element, named MediaName, to display the name of the current media item.</span></span> <span data-ttu-id="da1e6-121">Код обновляет текст в DIV при каждом возникновении события **медиачанже** .</span><span class="sxs-lookup"><span data-stu-id="da1e6-121">The code updates the text in the DIV with each occurrence of the **mediaChange** event.</span></span> <span data-ttu-id="da1e6-122">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="da1e6-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="da1e6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="da1e6-123">Requirements</span></span>



| <span data-ttu-id="da1e6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="da1e6-124">Requirement</span></span> | <span data-ttu-id="da1e6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="da1e6-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da1e6-126">Версия</span><span class="sxs-lookup"><span data-stu-id="da1e6-126">Version</span></span><br/> | <span data-ttu-id="da1e6-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="da1e6-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="da1e6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="da1e6-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="da1e6-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1e6-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1e6-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da1e6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da1e6-131">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="da1e6-131">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





