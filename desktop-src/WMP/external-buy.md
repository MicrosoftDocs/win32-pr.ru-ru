---
title: Метод external. reкупает
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Purchase инициирует покупку набора элементов мультимедиа.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- Купить метод проигрыватель Windows Media Player
- Купить метод проигрыватель Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод "Купить"
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695099"
---
# <a name="externalbuy-method"></a><span data-ttu-id="71ad8-108">Метод external. reкупает</span><span class="sxs-lookup"><span data-stu-id="71ad8-108">External.buy method</span></span>

> [!Note]  
> <span data-ttu-id="71ad8-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="71ad8-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="71ad8-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71ad8-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="71ad8-111">Метод **Purchase** инициирует покупку набора элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="71ad8-111">The **buy** method initiates the purchase of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ad8-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71ad8-112">Syntax</span></span>


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="71ad8-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="71ad8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ad8-114">*ViewType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71ad8-114">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71ad8-115">**Строка** , указывающая тип покупаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="71ad8-115">**String** that specifies the type of item to be purchased.</span></span> <span data-ttu-id="71ad8-116">Вызывающий объект должен присвоить этому параметру одну из следующих [констант расположения библиотеки](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="71ad8-116">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="71ad8-117">кплистид</span><span class="sxs-lookup"><span data-stu-id="71ad8-117">CPListID</span></span>

<span data-ttu-id="71ad8-118">кптраккид</span><span class="sxs-lookup"><span data-stu-id="71ad8-118">CPTrackID</span></span>

<span data-ttu-id="71ad8-119">кпалбумид</span><span class="sxs-lookup"><span data-stu-id="71ad8-119">CPAlbumID</span></span>

</dd> <dt>

<span data-ttu-id="71ad8-120">*Виевидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71ad8-120">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71ad8-121">**Строка** , содержащая идентификаторы (разделенные точками с запятой) для покупаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="71ad8-121">**String** containing the IDs, delimited by semicolons, of the items to be purchased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ad8-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71ad8-122">Return value</span></span>

<span data-ttu-id="71ad8-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="71ad8-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ad8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="71ad8-124">Requirements</span></span>



| <span data-ttu-id="71ad8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="71ad8-125">Requirement</span></span> | <span data-ttu-id="71ad8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="71ad8-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71ad8-127">Версия</span><span class="sxs-lookup"><span data-stu-id="71ad8-127">Version</span></span><br/> | <span data-ttu-id="71ad8-128">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="71ad8-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="71ad8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="71ad8-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="71ad8-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ad8-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ad8-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71ad8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ad8-132">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="71ad8-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="71ad8-133">**Внешняя. download**</span><span class="sxs-lookup"><span data-stu-id="71ad8-133">**External.download**</span></span>](external-download.md)
</dt> <dt>

[<span data-ttu-id="71ad8-134">**Ивмпконтентпартнер:: Купить**</span><span class="sxs-lookup"><span data-stu-id="71ad8-134">**IWMPContentPartner::Buy**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[<span data-ttu-id="71ad8-135">**Приобретение мультимедийного содержимого**</span><span class="sxs-lookup"><span data-stu-id="71ad8-135">**Purchasing Media Content**</span></span>](purchasing-media-content.md)
</dt> </dl>

 

 





