---
title: External. Селектедитемтипе
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Селектедитемтипе
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- Внешний Селектедитемтипе проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694483"
---
# <a name="externalselecteditemtype"></a><span data-ttu-id="2ab06-105">External. Селектедитемтипе</span><span class="sxs-lookup"><span data-stu-id="2ab06-105">External.selectedItemType</span></span>

> [!Note]  
> <span data-ttu-id="2ab06-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="2ab06-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2ab06-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2ab06-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2ab06-108">Свойство **селектедитемтипе** Извлекает тип элемента мультимедиа, выбранного в данный момент в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2ab06-108">The **selectedItemType** property retrieves the type of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab06-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ab06-109">Syntax</span></span>

<span data-ttu-id="2ab06-110">Window. external. Селектедитемтипе ()</span><span class="sxs-lookup"><span data-stu-id="2ab06-110">window.external.selectedItemType()</span></span>

## <a name="possible-values"></a><span data-ttu-id="2ab06-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="2ab06-111">Possible Values</span></span>

<span data-ttu-id="2ab06-112">Это свойство является **строкой** только для чтения, содержащей одну из [констант расположения библиотеки](library-location-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2ab06-112">This property is a read-only **String** that contains one of the [library location constants](library-location-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab06-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ab06-113">Remarks</span></span>

<span data-ttu-id="2ab06-114">Это свойство используется в сочетании со свойством **External. селектедитемид** .</span><span class="sxs-lookup"><span data-stu-id="2ab06-114">This property is used in combination with the **External.selectedItemID** property.</span></span> <span data-ttu-id="2ab06-115">Например, если **селектедитемтипе** равен кптраккид, то **СЕЛЕКТЕДИТЕМИД** — это идентификатор выбранной записи. Дополнительные сведения о том, как Windows Media Player характеризует представления содержимого Интернет-магазина, см. в разделе [расположение и выбранный элемент](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="2ab06-115">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="2ab06-116">Для некоторых представлений в проигрывателе Windows Media выбран определенный элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2ab06-116">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="2ab06-117">Например, предположим, что текущее представление представляет собой альбом.</span><span class="sxs-lookup"><span data-stu-id="2ab06-117">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="2ab06-118">Альбом — это контейнер дорожек, поэтому **селектедитемтипе** равен кптраккид, а **селектедитемид** — идентификатор выбранной дорожки. Другие представления не имеют выбранного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2ab06-118">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="2ab06-119">Например, если пользователь щелкнет корневой узел Интернет-магазина в элементе управления деревом, проигрыватель Windows Media отобразит страницу обнаружения, предоставленную в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="2ab06-119">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="2ab06-120">Проигрыватель не отображает ни одного контейнера элементов мультимедиа в пользовательском интерфейсе проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="2ab06-120">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="2ab06-121">В этом случае **селектедитемтипе** равно ункновнлокатион, а **селектедитемид** равен пустой строке.</span><span class="sxs-lookup"><span data-stu-id="2ab06-121">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab06-122">Требования</span><span class="sxs-lookup"><span data-stu-id="2ab06-122">Requirements</span></span>



| <span data-ttu-id="2ab06-123">Требование</span><span class="sxs-lookup"><span data-stu-id="2ab06-123">Requirement</span></span> | <span data-ttu-id="2ab06-124">Значение</span><span class="sxs-lookup"><span data-stu-id="2ab06-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab06-125">Версия</span><span class="sxs-lookup"><span data-stu-id="2ab06-125">Version</span></span><br/> | <span data-ttu-id="2ab06-126">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="2ab06-126">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="2ab06-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2ab06-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="2ab06-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ab06-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab06-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ab06-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab06-130">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="2ab06-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2ab06-131">**External. Селектедитемид**</span><span class="sxs-lookup"><span data-stu-id="2ab06-131">**External.selectedItemID**</span></span>](external-selecteditemid.md)
</dt> <dt>

[<span data-ttu-id="2ab06-132">**Расположение и выбранный элемент**</span><span class="sxs-lookup"><span data-stu-id="2ab06-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





