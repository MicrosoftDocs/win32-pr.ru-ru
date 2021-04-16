---
title: Кдромколлектион. Item, метод
description: Метод Item извлекает объект CDROM по указанному индексу.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс Кдромколлектион
- Класс Кдромколлектион Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699172"
---
# <a name="cdromcollectionitem-method"></a><span data-ttu-id="e1224-106">Кдромколлектион. Item, метод</span><span class="sxs-lookup"><span data-stu-id="e1224-106">CdromCollection.item method</span></span>

<span data-ttu-id="e1224-107">Метод **Item** извлекает объект **CDROM** по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="e1224-107">The **item** method retrieves the **Cdrom** object at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1224-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1224-108">Syntax</span></span>


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e1224-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1224-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1224-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1224-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1224-111">**Число** (**Long**), содержащее индекс.</span><span class="sxs-lookup"><span data-stu-id="e1224-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1224-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1224-112">Return value</span></span>

<span data-ttu-id="e1224-113">Этот метод возвращает объект **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="e1224-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1224-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1224-114">Remarks</span></span>

<span data-ttu-id="e1224-115">Чтобы использовать этот метод, требуется доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="e1224-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e1224-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e1224-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e1224-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e1224-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="e1224-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="e1224-118">Examples</span></span>

<span data-ttu-id="e1224-119">В следующем примере JScript используется *кдромколлектион*. **элемент** для печати имени списка воспроизведения с каждого компакт-диска, доступного на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e1224-119">The following JScript example uses *CdromCollection*.**item** to print the playlist name from each CD available on the computer.</span></span> <span data-ttu-id="e1224-120">Если на самом деле диск содержит содержимое DVD, требуется ОС Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e1224-120">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="e1224-121">Создан HTML-элемент TextArea с ИДЕНТИФИКАТОРом "списки воспроизведения".</span><span class="sxs-lookup"><span data-stu-id="e1224-121">An HTML TextArea element was created with ID = "playlists".</span></span> <span data-ttu-id="e1224-122">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="e1224-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="e1224-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e1224-123">Requirements</span></span>



| <span data-ttu-id="e1224-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e1224-124">Requirement</span></span> | <span data-ttu-id="e1224-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e1224-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1224-126">Версия</span><span class="sxs-lookup"><span data-stu-id="e1224-126">Version</span></span><br/> | <span data-ttu-id="e1224-127">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="e1224-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e1224-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e1224-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1224-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1224-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1224-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1224-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1224-131">**CDROM. ДривеспеЦифиер**</span><span class="sxs-lookup"><span data-stu-id="e1224-131">**Cdrom.driveSpecifier**</span></span>](cdrom-drivespecifier.md)
</dt> <dt>

[<span data-ttu-id="e1224-132">**Объект Кдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="e1224-132">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="e1224-133">**Кдромколлектион. Count**</span><span class="sxs-lookup"><span data-stu-id="e1224-133">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="e1224-134">**Playlist.name**</span><span class="sxs-lookup"><span data-stu-id="e1224-134">**Playlist.name**</span></span>](playlist-name.md)
</dt> <dt>

[<span data-ttu-id="e1224-135">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="e1224-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e1224-136">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="e1224-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





