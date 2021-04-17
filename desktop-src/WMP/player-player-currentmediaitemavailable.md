---
title: Событие Player. Куррентмедиаитемаваилабле
description: Событие Куррентмедиаитемаваилабле возникает при доступности элемента метаданных изображения в текущем элементе мультимедиа. | Событие Player. Куррентмедиаитемаваилабле
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Проигрыватель Windows Media Event Куррентмедиаитемаваилабле
- Проигрыватель Windows Media Event Куррентмедиаитемаваилабле, класс Player
- Класс проигрывателя Windows Media Player, событие Куррентмедиаитемаваилабле
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704258"
---
# <a name="playercurrentmediaitemavailable-event"></a><span data-ttu-id="bbfb1-107">Событие Player. Куррентмедиаитемаваилабле</span><span class="sxs-lookup"><span data-stu-id="bbfb1-107">Player.CurrentMediaItemAvailable event</span></span>

<span data-ttu-id="bbfb1-108">Событие **куррентмедиаитемаваилабле** возникает при доступности элемента метаданных изображения в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-108">The **CurrentMediaItemAvailable** event occurs when a graphic metadata item in the current media item becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbfb1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbfb1-109">Syntax</span></span>


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="bbfb1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbfb1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbfb1-111">*бстритемнаме*</span><span class="sxs-lookup"><span data-stu-id="bbfb1-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="bbfb1-112">**Строка** , содержащая имя текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-112">**String** containing the name of the current media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbfb1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbfb1-113">Return value</span></span>

<span data-ttu-id="bbfb1-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbfb1-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbfb1-115">Remarks</span></span>

<span data-ttu-id="bbfb1-116">Так как воспроизведение может начаться до полной загрузки элемента мультимедиа, все метаданные, содержащиеся в элементе мультимедиа (например, обложку альбома), могут быть недоступны при начале воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-116">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="bbfb1-117">Это событие предупреждает о завершении загрузки графического элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-117">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="bbfb1-118">Затем можно получить объект **мультимедиа** , передав значение *бстритемнаме* в *медиаколлектион*. метод **жетбинаме** , после которого можно получить доступ к графическому элементу метаданных с помощью *носителя*. **жетитеминфобитипе** и укажите **WM/Picture** в качестве имени атрибута.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-118">You can then retrieve the **Media** object by passing the value of *bstrItemName* to the *MediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *Media*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

<span data-ttu-id="bbfb1-119">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="bbfb1-120">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="bbfb1-121">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbfb1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bbfb1-122">Requirements</span></span>



| <span data-ttu-id="bbfb1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bbfb1-123">Requirement</span></span> | <span data-ttu-id="bbfb1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bbfb1-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfb1-125">Версия</span><span class="sxs-lookup"><span data-stu-id="bbfb1-125">Version</span></span><br/> | <span data-ttu-id="bbfb1-126">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="bbfb1-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bbfb1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bbfb1-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="bbfb1-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbfb1-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbfb1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbfb1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbfb1-130">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="bbfb1-130">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="bbfb1-131">**Media. Жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="bbfb1-131">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="bbfb1-132">**Медиаколлектион. Жетбинаме**</span><span class="sxs-lookup"><span data-stu-id="bbfb1-132">**MediaCollection.getByName**</span></span>](mediacollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="bbfb1-133">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="bbfb1-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





