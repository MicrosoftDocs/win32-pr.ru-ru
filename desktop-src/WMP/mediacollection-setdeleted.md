---
title: Медиаколлектион. Сетделетед, метод
description: Метод Сетделетед перемещает указанный элемент мультимедиа в папку Удаленные элементы. | Медиаколлектион. Сетделетед, метод
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- Сетделетед метод Windows Media Player
- Сетделетед метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Сетделетед
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685408"
---
# <a name="mediacollectionsetdeleted-method"></a><span data-ttu-id="95f33-107">Медиаколлектион. Сетделетед, метод</span><span class="sxs-lookup"><span data-stu-id="95f33-107">MediaCollection.setDeleted method</span></span>

<span data-ttu-id="95f33-108">Метод **сетделетед** перемещает указанный элемент мультимедиа в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="95f33-108">The **setDeleted** method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f33-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95f33-109">Syntax</span></span>


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a><span data-ttu-id="95f33-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="95f33-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f33-111">*элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95f33-111">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f33-112">Перемещаемый объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="95f33-112">**Media** object being moved.</span></span>

</dd> <dt>

<span data-ttu-id="95f33-113">*значение true* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95f33-113">*true* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95f33-114">Всегда указывайте это значение.</span><span class="sxs-lookup"><span data-stu-id="95f33-114">Always specify this value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f33-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95f33-115">Return value</span></span>

<span data-ttu-id="95f33-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="95f33-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95f33-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95f33-117">Remarks</span></span>

<span data-ttu-id="95f33-118">Этот метод не удаляет файлы с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="95f33-118">This method does not remove files from the user's computer.</span></span>

<span data-ttu-id="95f33-119">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="95f33-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="95f33-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="95f33-120">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="95f33-121">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95f33-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="95f33-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="95f33-122">Examples</span></span>

<span data-ttu-id="95f33-123">В следующем примере JScript используется *медиаколлектион*. **сетделетед** переместить определенный элемент мультимедиа, хранящийся в переменной с именем медиаобжект, в папку Удаленные элементы.</span><span class="sxs-lookup"><span data-stu-id="95f33-123">The following JScript example uses *MediaCollection*.**setDeleted** to move a particular media item, stored in the variable named mediaObject, to the deleted items folder.</span></span> <span data-ttu-id="95f33-124">*Медиаколлектион*. метод **IsDeleted** сначала проверяет, был ли уже удален элемент.</span><span class="sxs-lookup"><span data-stu-id="95f33-124">The *MediaCollection*.**isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="95f33-125">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="95f33-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="95f33-126">Требования</span><span class="sxs-lookup"><span data-stu-id="95f33-126">Requirements</span></span>



| <span data-ttu-id="95f33-127">Требование</span><span class="sxs-lookup"><span data-stu-id="95f33-127">Requirement</span></span> | <span data-ttu-id="95f33-128">Значение</span><span class="sxs-lookup"><span data-stu-id="95f33-128">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f33-129">Версия</span><span class="sxs-lookup"><span data-stu-id="95f33-129">Version</span></span><br/> | <span data-ttu-id="95f33-130">Проигрыватель Windows Media версии 7,0, Windows Media Player версии 7,1 или Windows Media Player для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="95f33-130">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="95f33-131">Этот метод не поддерживается для серии проигрывателя Windows Media 9 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="95f33-131">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="95f33-132">DLL</span><span class="sxs-lookup"><span data-stu-id="95f33-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="95f33-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95f33-133"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="95f33-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95f33-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f33-135">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="95f33-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="95f33-136">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="95f33-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="95f33-137">**Медиаколлектион. isDeleted**</span><span class="sxs-lookup"><span data-stu-id="95f33-137">**MediaCollection.isDeleted**</span></span>](mediacollection-isdeleted.md)
</dt> <dt>

[<span data-ttu-id="95f33-138">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="95f33-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="95f33-139">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="95f33-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





