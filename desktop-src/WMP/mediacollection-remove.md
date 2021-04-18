---
title: Медиаколлектион. Remove, метод
description: Метод Remove удаляет элемент из коллекции носителей.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- метод Remove Windows Media Player
- метод Remove Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион проигрыватель Windows Media Player, метод Remove
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685409"
---
# <a name="mediacollectionremove-method"></a><span data-ttu-id="08fb1-106">Медиаколлектион. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="08fb1-106">MediaCollection.remove method</span></span>

<span data-ttu-id="08fb1-107">Метод **Remove** удаляет элемент из коллекции носителей.</span><span class="sxs-lookup"><span data-stu-id="08fb1-107">The **remove** method removes an item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="08fb1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08fb1-108">Syntax</span></span>


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a><span data-ttu-id="08fb1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="08fb1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08fb1-110">*элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08fb1-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08fb1-111">Объект **мультимедиа** для удаления.</span><span class="sxs-lookup"><span data-stu-id="08fb1-111">**Media** object to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="08fb1-112">*Удаление* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08fb1-112">*delete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08fb1-113">**Логическое значение** , указывающее, следует ли удалить элемент.</span><span class="sxs-lookup"><span data-stu-id="08fb1-113">**Boolean** indicating whether to remove the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08fb1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08fb1-114">Return value</span></span>

<span data-ttu-id="08fb1-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="08fb1-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08fb1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08fb1-116">Remarks</span></span>

<span data-ttu-id="08fb1-117">Этот метод удаляет элемент из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="08fb1-117">This method deletes an item from the library.</span></span> <span data-ttu-id="08fb1-118">Этот метод не удаляет файлы с компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="08fb1-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="08fb1-119">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="08fb1-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="08fb1-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="08fb1-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08fb1-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="08fb1-121">Examples</span></span>

<span data-ttu-id="08fb1-122">В следующем примере JScript, после запроса пользователя, окончательно удаляется первый элемент мультимедиа из коллекции мультимедиа с помощью *медиаколлектион*. **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="08fb1-122">The following JScript example, after prompting the user, permanently deletes the first media item in the media collection by using *MediaCollection*.**remove**.</span></span> <span data-ttu-id="08fb1-123">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="08fb1-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a><span data-ttu-id="08fb1-124">Требования</span><span class="sxs-lookup"><span data-stu-id="08fb1-124">Requirements</span></span>



| <span data-ttu-id="08fb1-125">Требование</span><span class="sxs-lookup"><span data-stu-id="08fb1-125">Requirement</span></span> | <span data-ttu-id="08fb1-126">Значение</span><span class="sxs-lookup"><span data-stu-id="08fb1-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08fb1-127">Версия</span><span class="sxs-lookup"><span data-stu-id="08fb1-127">Version</span></span><br/> | <span data-ttu-id="08fb1-128">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="08fb1-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="08fb1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="08fb1-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="08fb1-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08fb1-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08fb1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08fb1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08fb1-132">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="08fb1-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="08fb1-133">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="08fb1-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="08fb1-134">**Медиаколлектион. Add**</span><span class="sxs-lookup"><span data-stu-id="08fb1-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="08fb1-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="08fb1-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="08fb1-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="08fb1-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





