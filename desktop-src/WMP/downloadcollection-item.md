---
title: Довнлоадколлектион. Item, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод Item извлекает объект, ожидающий загрузки.
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс Довнлоадколлектион
- Класс Довнлоадколлектион Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698948"
---
# <a name="downloadcollectionitem-method"></a><span data-ttu-id="fc23b-108">Довнлоадколлектион. Item, метод</span><span class="sxs-lookup"><span data-stu-id="fc23b-108">DownloadCollection.item method</span></span>

> [!Note]  
> <span data-ttu-id="fc23b-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="fc23b-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fc23b-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc23b-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fc23b-111">Метод **Item** извлекает объект, ожидающий загрузки.</span><span class="sxs-lookup"><span data-stu-id="fc23b-111">The **item** method retrieves a pending download object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc23b-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc23b-112">Syntax</span></span>


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a><span data-ttu-id="fc23b-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc23b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc23b-114">Идентификатор *ItemId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc23b-114">*itemId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc23b-115">**Число** (**длинное**), указывающее индекс извлекаемого **довнлоадитем** .</span><span class="sxs-lookup"><span data-stu-id="fc23b-115">**Number** (**long**) specifying the index of the **DownloadItem** to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc23b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc23b-116">Return value</span></span>

<span data-ttu-id="fc23b-117">Этот метод возвращает объект **довнлоадитем** .</span><span class="sxs-lookup"><span data-stu-id="fc23b-117">This method returns a **DownloadItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc23b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc23b-118">Remarks</span></span>

<span data-ttu-id="fc23b-119">Значение *ItemId* отсчитывается от нуля.</span><span class="sxs-lookup"><span data-stu-id="fc23b-119">The *itemID* value is zero-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc23b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="fc23b-120">Requirements</span></span>



| <span data-ttu-id="fc23b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="fc23b-121">Requirement</span></span> | <span data-ttu-id="fc23b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="fc23b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc23b-123">Версия</span><span class="sxs-lookup"><span data-stu-id="fc23b-123">Version</span></span><br/> | <span data-ttu-id="fc23b-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fc23b-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="fc23b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fc23b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fc23b-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc23b-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc23b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc23b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc23b-128">**Объект Довнлоадколлектион**</span><span class="sxs-lookup"><span data-stu-id="fc23b-128">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> <dt>

[<span data-ttu-id="fc23b-129">**Объект Довнлоадитем**</span><span class="sxs-lookup"><span data-stu-id="fc23b-129">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





