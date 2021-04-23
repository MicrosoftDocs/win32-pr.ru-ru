---
title: Метод списка воспроизведения. Мовеитем
description: Метод Мовеитем изменяет расположение элемента в списке воспроизведения.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Мовеитем метод Windows Media Player
- Мовеитем метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод Мовеитем
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708556"
---
# <a name="playlistmoveitem-method"></a><span data-ttu-id="3a0a8-106">Метод списка воспроизведения. Мовеитем</span><span class="sxs-lookup"><span data-stu-id="3a0a8-106">Playlist.moveItem method</span></span>

<span data-ttu-id="3a0a8-107">Метод **мовеитем** изменяет расположение элемента в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-107">The **moveItem** method changes the location of an item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a0a8-108">Syntax</span></span>


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a><span data-ttu-id="3a0a8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a0a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a0a8-110">*олдиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a0a8-110">*oldIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0a8-111">**Число** (**Long**), содержащее старый индекс.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-111">**Number** (**long**) containing the old index.</span></span>

</dd> <dt>

<span data-ttu-id="3a0a8-112">*невиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a0a8-112">*newIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0a8-113">**Число** (**длинное**), содержащее новый индекс.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-113">**Number** (**long**) containing the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a0a8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a0a8-114">Return value</span></span>

<span data-ttu-id="3a0a8-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a0a8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a0a8-116">Remarks</span></span>

<span data-ttu-id="3a0a8-117">Списки воспроизведения, хранящиеся в библиотеке, могут изменяться вне элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-117">Playlists stored in the library can change outside your control.</span></span> <span data-ttu-id="3a0a8-118">Не забудьте отслеживать и обрабатывать все соответствующие события, связанные с списками воспроизведения, чтобы порядок элементов в списке воспроизведения неожиданно изменялся.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-118">Be sure to monitor and handle all appropriate playlist-related events so that the order of items in the playlist does not change unexpectedly.</span></span>

<span data-ttu-id="3a0a8-119">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="3a0a8-120">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3a0a8-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a0a8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3a0a8-121">Requirements</span></span>



| <span data-ttu-id="3a0a8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3a0a8-122">Requirement</span></span> | <span data-ttu-id="3a0a8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3a0a8-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0a8-124">Версия</span><span class="sxs-lookup"><span data-stu-id="3a0a8-124">Version</span></span><br/> | <span data-ttu-id="3a0a8-125">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3a0a8-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3a0a8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3a0a8-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a0a8-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a0a8-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0a8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a0a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0a8-129">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="3a0a8-130">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3a0a8-131">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="3a0a8-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





