---
title: External. Аддтобаскет, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Аддтобаскет, метод
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Аддтобаскет метод Windows Media Player
- Аддтобаскет метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Аддтобаскет
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695209"
---
# <a name="externaladdtobasket-method"></a><span data-ttu-id="e097a-107">External. Аддтобаскет, метод</span><span class="sxs-lookup"><span data-stu-id="e097a-107">External.addToBasket method</span></span>

> [!Note]  
> <span data-ttu-id="e097a-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="e097a-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e097a-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e097a-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e097a-110">Метод **аддтобаскет** добавляет элементы мультимедиа на панель списка (также называемую корзиной) в проигрывателе Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e097a-110">The **addToBasket** method adds media items to the list pane (also called the basket) in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="e097a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e097a-111">Syntax</span></span>


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="e097a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e097a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e097a-113">*ViewType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e097a-113">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e097a-114">**Строка** , указывающая тип элемента, добавляемого на панель списка.</span><span class="sxs-lookup"><span data-stu-id="e097a-114">**String** that specifies the type of item being added to the list pane.</span></span> <span data-ttu-id="e097a-115">Вызывающий объект должен присвоить этому параметру одну из следующих [констант расположения библиотеки](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="e097a-115">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="e097a-116">кплистид</span><span class="sxs-lookup"><span data-stu-id="e097a-116">CPListID</span></span>

<span data-ttu-id="e097a-117">кптраккид</span><span class="sxs-lookup"><span data-stu-id="e097a-117">CPTrackID</span></span>

<span data-ttu-id="e097a-118">кпалбумид</span><span class="sxs-lookup"><span data-stu-id="e097a-118">CPAlbumID</span></span>

<span data-ttu-id="e097a-119">кпартист</span><span class="sxs-lookup"><span data-stu-id="e097a-119">CPArtist</span></span>

<span data-ttu-id="e097a-120">кпженреид</span><span class="sxs-lookup"><span data-stu-id="e097a-120">CPGenreID</span></span>

<span data-ttu-id="e097a-121">кпалбумсубженреид</span><span class="sxs-lookup"><span data-stu-id="e097a-121">CPAlbumSubGenreID</span></span>

<span data-ttu-id="e097a-122">кпрадиоид</span><span class="sxs-lookup"><span data-stu-id="e097a-122">CPRadioID</span></span>

</dd> <dt>

<span data-ttu-id="e097a-123">*Виевидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e097a-123">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e097a-124">**Строка** , содержащая идентификаторы, разделенные точками с запятой, для элементов, добавляемых на панель списка.</span><span class="sxs-lookup"><span data-stu-id="e097a-124">**String** containing the IDs, delimited by semicolons, of the items to be added to the list pane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e097a-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e097a-125">Return value</span></span>

<span data-ttu-id="e097a-126">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e097a-126">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e097a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e097a-127">Requirements</span></span>



| <span data-ttu-id="e097a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e097a-128">Requirement</span></span> | <span data-ttu-id="e097a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e097a-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e097a-130">Версия</span><span class="sxs-lookup"><span data-stu-id="e097a-130">Version</span></span><br/> | <span data-ttu-id="e097a-131">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="e097a-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="e097a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e097a-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="e097a-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e097a-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e097a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e097a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e097a-135">**Екстерналобжект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="e097a-135">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e097a-136">**External. Баскеттитле**</span><span class="sxs-lookup"><span data-stu-id="e097a-136">**External.basketTitle**</span></span>](external-baskettitle.md)
</dt> </dl>

 

 





