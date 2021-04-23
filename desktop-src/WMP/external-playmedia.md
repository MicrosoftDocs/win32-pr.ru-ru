---
title: External. Плаймедиа, метод
description: На этой странице документируется компонент пакета SDK для проигрывателя Windows Media 9 и пакета SDK для проигрывателя Windows Media 10. В последующих версиях он может быть недоступен.
ms.assetid: 48071318-e853-4139-8fe4-17d1cdbef8f5
keywords:
- Плаймедиа метод Windows Media Player
- Плаймедиа метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод Плаймедиа
topic_type:
- apiref
api_name:
- External.playMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0330e7e68d8b4e3747c019e0841f872d279c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694491"
---
# <a name="externalplaymedia-method"></a><span data-ttu-id="69811-107">External. Плаймедиа, метод</span><span class="sxs-lookup"><span data-stu-id="69811-107">External.playMedia method</span></span>

<span data-ttu-id="69811-108">На этой странице документируется компонент пакета SDK для проигрывателя Windows Media 9 и пакета SDK для проигрывателя Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="69811-108">This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK.</span></span> <span data-ttu-id="69811-109">В последующих версиях он может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="69811-109">It may be unavailable in subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="69811-110">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="69811-110">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="69811-111">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="69811-111">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="69811-112">Метод **плаймедиа** указывает URL-адрес цифрового мультимедийного элемента для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="69811-112">The **playMedia** method specifies the URL of a digital media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="69811-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69811-113">Syntax</span></span>


```JScript
External.playMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="69811-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="69811-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69811-115">*URL-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69811-115">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69811-116">**Строка** , указывающая URL-адрес мультимедийного элемента для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="69811-116">**String** specifying the URL of the digital media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69811-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69811-117">Return value</span></span>

<span data-ttu-id="69811-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="69811-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69811-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69811-119">Remarks</span></span>

<span data-ttu-id="69811-120">Этот метод доступен только для веб-страниц, размещенных в компоненте **Guide** .</span><span class="sxs-lookup"><span data-stu-id="69811-120">This method is only available to webpages hosted in the **Guide** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="69811-121">Требования</span><span class="sxs-lookup"><span data-stu-id="69811-121">Requirements</span></span>



| <span data-ttu-id="69811-122">Требование</span><span class="sxs-lookup"><span data-stu-id="69811-122">Requirement</span></span> | <span data-ttu-id="69811-123">Значение</span><span class="sxs-lookup"><span data-stu-id="69811-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69811-124">Версия</span><span class="sxs-lookup"><span data-stu-id="69811-124">Version</span></span><br/> | <span data-ttu-id="69811-125">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="69811-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="69811-126">DLL</span><span class="sxs-lookup"><span data-stu-id="69811-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="69811-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69811-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69811-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69811-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69811-129">**Внешний объект для Интернет-магазинов типа 2**</span><span class="sxs-lookup"><span data-stu-id="69811-129">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





