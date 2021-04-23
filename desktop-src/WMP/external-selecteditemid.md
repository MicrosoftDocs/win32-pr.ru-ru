---
title: External. Селектедитемид
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Селектедитемид
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Внешний Селектедитемид проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694484"
---
# <a name="externalselecteditemid"></a><span data-ttu-id="2dc88-105">External. Селектедитемид</span><span class="sxs-lookup"><span data-stu-id="2dc88-105">External.selectedItemID</span></span>

> [!Note]  
> <span data-ttu-id="2dc88-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="2dc88-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2dc88-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2dc88-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2dc88-108">Свойство **селектедитемид** извлекает идентификатор элемента мультимедиа, выбранного в данный момент в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2dc88-108">The **selectedItemID** property retrieves the identifier of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc88-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dc88-109">Syntax</span></span>

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a><span data-ttu-id="2dc88-110">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="2dc88-110">Possible Values</span></span>

<span data-ttu-id="2dc88-111">Это свойство является **строкой**, доступная только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2dc88-111">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dc88-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2dc88-112">Remarks</span></span>

<span data-ttu-id="2dc88-113">Это свойство используется в сочетании со свойством [External. селектедитемтипе](external-selecteditemtype.md) .</span><span class="sxs-lookup"><span data-stu-id="2dc88-113">This property is used in combination with the [External.selectedItemType](external-selecteditemtype.md) property.</span></span> <span data-ttu-id="2dc88-114">Например, если **селектедитемтипе** равен кптраккид, то **СЕЛЕКТЕДИТЕМИД** — это идентификатор выбранной записи. Дополнительные сведения о том, как Windows Media Player характеризует представления содержимого Интернет-магазина, см. в разделе [расположение и выбранный элемент](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="2dc88-114">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="2dc88-115">Для некоторых представлений в проигрывателе Windows Media выбран определенный элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2dc88-115">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="2dc88-116">Например, предположим, что текущее представление представляет собой альбом.</span><span class="sxs-lookup"><span data-stu-id="2dc88-116">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="2dc88-117">Альбом — это контейнер дорожек, поэтому **селектедитемтипе** равен кптраккид, а **селектедитемид** — идентификатор выбранной дорожки. Другие представления не имеют выбранного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2dc88-117">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="2dc88-118">Например, если пользователь щелкнет корневой узел Интернет-магазина в элементе управления деревом, проигрыватель Windows Media отобразит страницу обнаружения, предоставленную в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="2dc88-118">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="2dc88-119">Проигрыватель не отображает ни одного контейнера элементов мультимедиа в пользовательском интерфейсе проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="2dc88-119">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="2dc88-120">В этом случае **селектедитемтипе** равно ункновнлокатион, а **селектедитемид** равен пустой строке.</span><span class="sxs-lookup"><span data-stu-id="2dc88-120">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc88-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2dc88-121">Requirements</span></span>



| <span data-ttu-id="2dc88-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2dc88-122">Requirement</span></span> | <span data-ttu-id="2dc88-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2dc88-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc88-124">Версия</span><span class="sxs-lookup"><span data-stu-id="2dc88-124">Version</span></span><br/> | <span data-ttu-id="2dc88-125">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="2dc88-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="2dc88-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2dc88-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="2dc88-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc88-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc88-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dc88-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc88-129">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="2dc88-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2dc88-130">**External. Селектедитемтипе**</span><span class="sxs-lookup"><span data-stu-id="2dc88-130">**External.selectedItemType**</span></span>](external-selecteditemtype.md)
</dt> <dt>

[<span data-ttu-id="2dc88-131">**Расположение и выбранный элемент**</span><span class="sxs-lookup"><span data-stu-id="2dc88-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





