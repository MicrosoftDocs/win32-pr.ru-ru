---
title: Медиаколлектион. isDeleted, метод
description: Метод IsDeleted извлекает значение, указывающее, находится ли указанный элемент мультимедиа в папке удаленных элементов.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- метод IsDeleted Windows Media Player
- метод IsDeleted Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод isDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685410"
---
# <a name="mediacollectionisdeleted-method"></a><span data-ttu-id="de115-106">Медиаколлектион. isDeleted, метод</span><span class="sxs-lookup"><span data-stu-id="de115-106">MediaCollection.isDeleted method</span></span>

<span data-ttu-id="de115-107">Метод **IsDeleted** извлекает значение, указывающее, находится ли указанный элемент мультимедиа в папке удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="de115-107">The **isDeleted** method retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="de115-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de115-108">Syntax</span></span>


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="de115-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="de115-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de115-110">*элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de115-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de115-111">Объект **мультимедиа** , который может быть удален.</span><span class="sxs-lookup"><span data-stu-id="de115-111">**Media** object that might be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de115-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de115-112">Return value</span></span>

<span data-ttu-id="de115-113">Этот метод возвращает **логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="de115-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="de115-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de115-114">Remarks</span></span>

<span data-ttu-id="de115-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="de115-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="de115-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="de115-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="de115-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="de115-117">**Windows Media Player 10 Mobile:** This method always returns **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="de115-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="de115-118">Examples</span></span>

<span data-ttu-id="de115-119">В следующем примере JScript используется *медиаколлектион*. **удаляется, чтобы проверить** , находится ли конкретный элемент мультимедиа, хранящийся в переменной с именем медиаобжект, в папке удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="de115-119">The following JScript example uses *MediaCollection*.**isDeleted** to test whether a particular media item, stored in the variable named mediaObject, is in the deleted items folder.</span></span> <span data-ttu-id="de115-120">Если элемент мультимедиа еще не был удален, он перемещается в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="de115-120">If the media item has not been deleted already, it is moved to the deleted items folder.</span></span> <span data-ttu-id="de115-121">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="de115-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="de115-122">Требования</span><span class="sxs-lookup"><span data-stu-id="de115-122">Requirements</span></span>



| <span data-ttu-id="de115-123">Требование</span><span class="sxs-lookup"><span data-stu-id="de115-123">Requirement</span></span> | <span data-ttu-id="de115-124">Значение</span><span class="sxs-lookup"><span data-stu-id="de115-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de115-125">Версия</span><span class="sxs-lookup"><span data-stu-id="de115-125">Version</span></span><br/> | <span data-ttu-id="de115-126">Проигрыватель Windows Media версии 7,0, Windows Media Player версии 7,1 или Windows Media Player для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="de115-126">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="de115-127">Этот метод не поддерживается для серии проигрывателя Windows Media 9 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="de115-127">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="de115-128">DLL</span><span class="sxs-lookup"><span data-stu-id="de115-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="de115-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de115-129"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="de115-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de115-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de115-131">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="de115-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="de115-132">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="de115-132">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="de115-133">**Медиаколлектион. Сетделетед**</span><span class="sxs-lookup"><span data-stu-id="de115-133">**MediaCollection.setDeleted**</span></span>](mediacollection-setdeleted.md)
</dt> <dt>

[<span data-ttu-id="de115-134">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="de115-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="de115-135">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="de115-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





