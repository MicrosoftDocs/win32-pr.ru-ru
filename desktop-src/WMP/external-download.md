---
title: Метод external. download
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод download инициирует загрузку набора элементов мультимедиа.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Загрузка метода Windows Media Player
- метод загрузки Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод download
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694503"
---
# <a name="externaldownload-method"></a><span data-ttu-id="a5919-108">Метод external. download</span><span class="sxs-lookup"><span data-stu-id="a5919-108">External.download method</span></span>

> [!Note]  
> <span data-ttu-id="a5919-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="a5919-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a5919-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a5919-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a5919-111">Метод **download** инициирует загрузку набора элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a5919-111">The **download** method initiates the download of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5919-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5919-112">Syntax</span></span>


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a><span data-ttu-id="a5919-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5919-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5919-114">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5919-114">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5919-115">[Константа расположения библиотеки](library-location-constants.md) , указывающая тип загружаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="a5919-115">A [library location constant](library-location-constants.md) that specifies the type of item to be downloaded.</span></span> <span data-ttu-id="a5919-116">Например, Кптраккид указывает, что необходимо загрузить одну или несколько дорожек.</span><span class="sxs-lookup"><span data-stu-id="a5919-116">For example, CPTrackID specifies that one or more tracks are to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="a5919-117">*Идентификаторы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5919-117">*IDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5919-118">**Строка** , содержащая идентификаторы (разделенные точками с запятой) загружаемых элементов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a5919-118">**String** containing the IDs, delimited by semicolons, of the media items to be downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5919-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5919-119">Return value</span></span>

<span data-ttu-id="a5919-120">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a5919-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5919-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a5919-121">Requirements</span></span>



| <span data-ttu-id="a5919-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a5919-122">Requirement</span></span> | <span data-ttu-id="a5919-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a5919-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5919-124">Версия</span><span class="sxs-lookup"><span data-stu-id="a5919-124">Version</span></span><br/> | <span data-ttu-id="a5919-125">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="a5919-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="a5919-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a5919-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a5919-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5919-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5919-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5919-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5919-129">**Загрузка мультимедийного содержимого**</span><span class="sxs-lookup"><span data-stu-id="a5919-129">**Downloading Media Content**</span></span>](downloading-media-content.md)
</dt> <dt>

[<span data-ttu-id="a5919-130">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="a5919-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a5919-131">**External. Купить**</span><span class="sxs-lookup"><span data-stu-id="a5919-131">**External.buy**</span></span>](external-buy.md)
</dt> <dt>

[<span data-ttu-id="a5919-132">**Ивмпконтентпартнер::D гружать**</span><span class="sxs-lookup"><span data-stu-id="a5919-132">**IWMPContentPartner::Download**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





