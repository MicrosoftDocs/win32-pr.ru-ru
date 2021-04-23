---
title: Событие проигрывателя. буферизация
description: Событие буферизации возникает, когда элемент управления проигрывателя Windows Media начинает или заканчивается буферизацией или загружается. | Событие проигрывателя. буферизация
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Буферизация проигрывателя Windows Media Player
- Буферизация проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, событие буферизации
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704345"
---
# <a name="playerbuffering-event"></a><span data-ttu-id="6a165-107">Событие проигрывателя. буферизация</span><span class="sxs-lookup"><span data-stu-id="6a165-107">Player.Buffering event</span></span>

<span data-ttu-id="6a165-108">Событие **буферизации** возникает, когда элемент управления проигрывателя Windows Media начинает или заканчивается буферизацией или загружается.</span><span class="sxs-lookup"><span data-stu-id="6a165-108">The **Buffering** event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a165-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a165-109">Syntax</span></span>


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a><span data-ttu-id="6a165-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a165-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a165-111">*Запуск*</span><span class="sxs-lookup"><span data-stu-id="6a165-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="6a165-112">**Логическое значение** , содержащее одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6a165-112">**Boolean** containing one of the following values.</span></span>



| <span data-ttu-id="6a165-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6a165-113">Value</span></span> | <span data-ttu-id="6a165-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6a165-114">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="6a165-115">true</span><span class="sxs-lookup"><span data-stu-id="6a165-115">true</span></span>  | <span data-ttu-id="6a165-116">Буферизация начата.</span><span class="sxs-lookup"><span data-stu-id="6a165-116">Buffering has started.</span></span> |
| <span data-ttu-id="6a165-117">false</span><span class="sxs-lookup"><span data-stu-id="6a165-117">false</span></span> | <span data-ttu-id="6a165-118">Буферизация завершена.</span><span class="sxs-lookup"><span data-stu-id="6a165-118">Buffering has ended.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a165-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a165-119">Return value</span></span>

<span data-ttu-id="6a165-120">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6a165-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a165-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a165-121">Remarks</span></span>

<span data-ttu-id="6a165-122">Это событие используется для определения времени, в течение которого буферизация или загрузка начинается или останавливается.</span><span class="sxs-lookup"><span data-stu-id="6a165-122">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="6a165-123">Один и тот же блок событий можно использовать в обоих случаях и в тестовой *сети*. **буфферингпрогресс** и *Network*. **довнлоадпрогресс** , чтобы определить, является ли проигрыватель Windows Media в данный момент буферизацией или загрузкой содержимого.</span><span class="sxs-lookup"><span data-stu-id="6a165-123">You can use the same event block for both cases and test *Network*.**bufferingProgress** and *Network*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

<span data-ttu-id="6a165-124">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с помощью имени параметра.</span><span class="sxs-lookup"><span data-stu-id="6a165-124">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file by using the parameter name given.</span></span> <span data-ttu-id="6a165-125">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="6a165-125">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a165-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6a165-126">Requirements</span></span>



| <span data-ttu-id="6a165-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6a165-127">Requirement</span></span> | <span data-ttu-id="6a165-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6a165-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a165-129">Версия</span><span class="sxs-lookup"><span data-stu-id="6a165-129">Version</span></span><br/> | <span data-ttu-id="6a165-130">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6a165-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6a165-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6a165-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="6a165-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a165-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a165-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a165-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a165-134">**Network. Буфферингпрогресс**</span><span class="sxs-lookup"><span data-stu-id="6a165-134">**Network.bufferingProgress**</span></span>](network-bufferingprogress.md)
</dt> <dt>

[<span data-ttu-id="6a165-135">**Network. Довнлоадпрогресс**</span><span class="sxs-lookup"><span data-stu-id="6a165-135">**Network.downloadProgress**</span></span>](network-downloadprogress.md)
</dt> <dt>

[<span data-ttu-id="6a165-136">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="6a165-136">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





