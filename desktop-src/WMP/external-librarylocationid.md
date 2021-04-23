---
title: External. Либрарилокатионид
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Либрарилокатионид
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Внешний Либрарилокатионид проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694502"
---
# <a name="externallibrarylocationid"></a><span data-ttu-id="c3a90-105">External. Либрарилокатионид</span><span class="sxs-lookup"><span data-stu-id="c3a90-105">External.libraryLocationID</span></span>

> [!Note]  
> <span data-ttu-id="c3a90-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="c3a90-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c3a90-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c3a90-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c3a90-108">Свойство **либрарилокатионид** извлекает идентификатор конкретного элемента мультимедиа, который в настоящий момент отображается в представлении проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="c3a90-108">The **libraryLocationID** property retrieves the identifier of the specific media item that is currently displayed in the Player's view.</span></span>

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a><span data-ttu-id="c3a90-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c3a90-109">Possible Values</span></span>

<span data-ttu-id="c3a90-110">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c3a90-110">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a90-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3a90-111">Remarks</span></span>

<span data-ttu-id="c3a90-112">Это свойство работает в сочетании со свойством [External. либрарилокатионтипе](external-librarylocationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="c3a90-112">This property works in combination with the [External.libraryLocationType](external-librarylocationtype.md) property.</span></span> <span data-ttu-id="c3a90-113">Например, предположим, что **либрарилокатионтипе** равен кпалбумид, а **либрарилокатионид** равен 3.</span><span class="sxs-lookup"><span data-stu-id="c3a90-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="c3a90-114">Это означает, что в текущем представлении проигрывателя Windows Media отображается альбом с ИДЕНТИФИКАТОРом 3.</span><span class="sxs-lookup"><span data-stu-id="c3a90-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="c3a90-115">Дополнительные сведения о том, как Windows Media Player характеризует представления содержимого Интернет-магазина, см. в разделе [расположение и выбранный элемент](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="c3a90-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="c3a90-116">Некоторые представления в проигрывателе Windows Media связаны с определенным элементом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c3a90-116">Certain views in Windows Media Player are associated with a particular media item.</span></span> <span data-ttu-id="c3a90-117">Например, если текущее представление представляет отдельный альбом, **либрарилокатионтипе** равен кпалбумид, а **либрарилокатионид** — идентификатору альбома.</span><span class="sxs-lookup"><span data-stu-id="c3a90-117">For example, if the current view represents an individual album, **libraryLocationType** is equal to CPAlbumID, and **libraryLocationID** is the ID of the album.</span></span> <span data-ttu-id="c3a90-118">Другие представления не связаны с определенными элементами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c3a90-118">Other views are not associated with any particular media item.</span></span> <span data-ttu-id="c3a90-119">Например, если текущее представление представляет все альбомы, **либрарилокатионтипе** равно аллкпалбумидс, но нет осмысленного значения, которое можно было бы назначить **либрарилокатионид**.</span><span class="sxs-lookup"><span data-stu-id="c3a90-119">For example, if the current view represents all albums, **libraryLocationType** is equal to AllCPAlbumIDs, but there is no meaningful value that can be assigned to **libraryLocationID**.</span></span> <span data-ttu-id="c3a90-120">В случаях, когда свойство **либрарилокатионид** не имеет осмысленного значения, оно равно пустой строке.</span><span class="sxs-lookup"><span data-stu-id="c3a90-120">In cases where the **libraryLocationID** property has no meaningful value, it is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a90-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c3a90-121">Requirements</span></span>



| <span data-ttu-id="c3a90-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c3a90-122">Requirement</span></span> | <span data-ttu-id="c3a90-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c3a90-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a90-124">Версия</span><span class="sxs-lookup"><span data-stu-id="c3a90-124">Version</span></span><br/> | <span data-ttu-id="c3a90-125">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="c3a90-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c3a90-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a90-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3a90-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a90-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a90-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3a90-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a90-129">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="c3a90-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="c3a90-130">**External. Либрарилокатионтипе**</span><span class="sxs-lookup"><span data-stu-id="c3a90-130">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="c3a90-131">**Расположение и выбранный элемент**</span><span class="sxs-lookup"><span data-stu-id="c3a90-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





