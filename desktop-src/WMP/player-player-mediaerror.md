---
title: Событие Player. Медиаеррор
description: Событие Медиаеррор возникает, когда объект мультимедиа имеет условие ошибки.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Проигрыватель Windows Media Event Медиаеррор
- Проигрыватель Windows Media Event Медиаеррор, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаеррор
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708359"
---
# <a name="playermediaerror-event"></a><span data-ttu-id="6de1e-106">Событие Player. Медиаеррор</span><span class="sxs-lookup"><span data-stu-id="6de1e-106">Player.MediaError event</span></span>

<span data-ttu-id="6de1e-107">Событие **медиаеррор** возникает, когда объект **мультимедиа** имеет условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="6de1e-107">The **MediaError** event occurs when the **Media** object has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de1e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6de1e-108">Syntax</span></span>


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a><span data-ttu-id="6de1e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6de1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de1e-110">*пмедиаобжект*</span><span class="sxs-lookup"><span data-stu-id="6de1e-110">*pMediaObject*</span></span> 
</dt> <dd>

<span data-ttu-id="6de1e-111">Объект **мультимедиа** с условием ошибки.</span><span class="sxs-lookup"><span data-stu-id="6de1e-111">**Media** object that has an error condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de1e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6de1e-112">Return value</span></span>

<span data-ttu-id="6de1e-113">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6de1e-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6de1e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6de1e-114">Remarks</span></span>

<span data-ttu-id="6de1e-115">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6de1e-115">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="6de1e-116">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="6de1e-116">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de1e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6de1e-117">Requirements</span></span>



| <span data-ttu-id="6de1e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6de1e-118">Requirement</span></span> | <span data-ttu-id="6de1e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6de1e-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6de1e-120">Версия</span><span class="sxs-lookup"><span data-stu-id="6de1e-120">Version</span></span><br/> | <span data-ttu-id="6de1e-121">Проигрыватель Windows Media для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="6de1e-121">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="6de1e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6de1e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6de1e-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6de1e-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de1e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6de1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de1e-125">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="6de1e-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





