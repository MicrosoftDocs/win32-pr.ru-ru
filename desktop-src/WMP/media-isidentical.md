---
title: Метод Media. одинаковы
description: Метод «идентичен» получает значение, указывающее, совпадает ли указанный объект с текущим. | Метод Media. одинаковы
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- метод, аналогичный проигрывателю Windows Media
- тождественный метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод тождественности
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695152"
---
# <a name="mediaisidentical-method"></a><span data-ttu-id="7e64b-107">Метод Media. одинаковы</span><span class="sxs-lookup"><span data-stu-id="7e64b-107">Media.isIdentical method</span></span>

<span data-ttu-id="7e64b-108">Метод « **идентичен** » получает значение, указывающее, совпадает ли указанный объект с текущим.</span><span class="sxs-lookup"><span data-stu-id="7e64b-108">The **isIdentical** method retrieves a value indicating whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e64b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e64b-109">Syntax</span></span>


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a><span data-ttu-id="7e64b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e64b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e64b-111">*носитель* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e64b-111">*media* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e64b-112">Объект **мультимедиа** для сравнения с текущим объектом **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="7e64b-112">**Media** object to compare with the current **Media** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e64b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e64b-113">Return value</span></span>

<span data-ttu-id="7e64b-114">Этот метод возвращает **логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="7e64b-114">This method returns a **Boolean**.</span></span>

## <a name="examples"></a><span data-ttu-id="7e64b-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="7e64b-115">Examples</span></span>

<span data-ttu-id="7e64b-116">В следующем примере JScript используется *носитель*. **идентично** , чтобы проверить, совпадает ли элемент мультимедиа с именем невмедиа с текущим элементом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7e64b-116">The following JScript example uses *Media*.**isIdentical** to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="7e64b-117">Если они не совпадают, будет воспроизведен новый элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7e64b-117">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="7e64b-118">В противном случае текущий носитель продолжит воспроизводиться без прерывания.</span><span class="sxs-lookup"><span data-stu-id="7e64b-118">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="7e64b-119">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="7e64b-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a><span data-ttu-id="7e64b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7e64b-120">Requirements</span></span>



| <span data-ttu-id="7e64b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7e64b-121">Requirement</span></span> | <span data-ttu-id="7e64b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7e64b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e64b-123">Версия</span><span class="sxs-lookup"><span data-stu-id="7e64b-123">Version</span></span><br/> | <span data-ttu-id="7e64b-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="7e64b-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7e64b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7e64b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e64b-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e64b-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e64b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e64b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e64b-128">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="7e64b-128">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





