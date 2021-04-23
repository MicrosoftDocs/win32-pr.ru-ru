---
title: Метод списка воспроизведения. insertItem
description: Метод insertItem вставляет элемент мультимедиа в список воспроизведения в указанном расположении.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- insertItem метод Windows Media Player
- insertItem метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704130"
---
# <a name="playlistinsertitem-method"></a><span data-ttu-id="dbf69-106">Метод списка воспроизведения. insertItem</span><span class="sxs-lookup"><span data-stu-id="dbf69-106">Playlist.insertItem method</span></span>

<span data-ttu-id="dbf69-107">Метод **insertItem** вставляет элемент мультимедиа в список воспроизведения в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="dbf69-107">The **insertItem** method inserts a media item into the playlist at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf69-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbf69-108">Syntax</span></span>


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a><span data-ttu-id="dbf69-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbf69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf69-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf69-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf69-111">**Число** (**Long**), содержащее индекс, по которому нужно добавить элемент.</span><span class="sxs-lookup"><span data-stu-id="dbf69-111">**Number** (**long**) containing the index at which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="dbf69-112">*элемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf69-112">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf69-113">Вставляемый объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="dbf69-113">**Media** object to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf69-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbf69-114">Return value</span></span>

<span data-ttu-id="dbf69-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dbf69-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf69-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbf69-116">Remarks</span></span>

<span data-ttu-id="dbf69-117">Номера индексов всех элементов после вставленного элемента будут увеличены на единицу.</span><span class="sxs-lookup"><span data-stu-id="dbf69-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="dbf69-118">Чтобы использовать этот метод, требуется полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="dbf69-118">To use this method, full access to the library is required.</span></span> <span data-ttu-id="dbf69-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dbf69-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf69-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dbf69-120">Requirements</span></span>



| <span data-ttu-id="dbf69-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dbf69-121">Requirement</span></span> | <span data-ttu-id="dbf69-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dbf69-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf69-123">Версия</span><span class="sxs-lookup"><span data-stu-id="dbf69-123">Version</span></span><br/> | <span data-ttu-id="dbf69-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="dbf69-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dbf69-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf69-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="dbf69-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf69-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf69-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbf69-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf69-128">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="dbf69-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="dbf69-129">**Список воспроизведения. элемент**</span><span class="sxs-lookup"><span data-stu-id="dbf69-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="dbf69-130">**Список воспроизведения. removeItem**</span><span class="sxs-lookup"><span data-stu-id="dbf69-130">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="dbf69-131">**Settings. Медиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="dbf69-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="dbf69-132">**Settings. Рекуестмедиаакцессригхтс**</span><span class="sxs-lookup"><span data-stu-id="dbf69-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





