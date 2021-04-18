---
title: Довнлоадколлектион. removeItem, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Метод removeItem удаляет скачанный элемент из коллекции загрузки.
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- removeItem метод Windows Media Player
- removeItem метод Windows Media Player, класс Довнлоадколлектион
- Класс Довнлоадколлектион Windows Media Player, метод removeItem
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699210"
---
# <a name="downloadcollectionremoveitem-method"></a><span data-ttu-id="be632-108">Довнлоадколлектион. removeItem, метод</span><span class="sxs-lookup"><span data-stu-id="be632-108">DownloadCollection.removeItem method</span></span>

> [!Note]  
> <span data-ttu-id="be632-109">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="be632-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="be632-110">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="be632-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="be632-111">Метод **RemoveItem** удаляет скачанный элемент из коллекции загрузки.</span><span class="sxs-lookup"><span data-stu-id="be632-111">The **removeItem** method removes a download item from a download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="be632-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be632-112">Syntax</span></span>


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a><span data-ttu-id="be632-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="be632-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be632-114">Идентификатор *ItemId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be632-114">*itemID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be632-115">**Число** (**длинное**), определяющее индекс удаляемого **довнлоадитем** .</span><span class="sxs-lookup"><span data-stu-id="be632-115">**Number** (**long**) specifying the index of the **DownloadItem** to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be632-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be632-116">Return value</span></span>

<span data-ttu-id="be632-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="be632-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be632-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be632-118">Remarks</span></span>

<span data-ttu-id="be632-119">Если выполняется загрузка, представленная идентификатором *ItemId* , этот метод отменяет скачивание.</span><span class="sxs-lookup"><span data-stu-id="be632-119">If the download represented by *itemID* is in progress, this method cancels the download.</span></span>

## <a name="requirements"></a><span data-ttu-id="be632-120">Требования</span><span class="sxs-lookup"><span data-stu-id="be632-120">Requirements</span></span>



| <span data-ttu-id="be632-121">Требование</span><span class="sxs-lookup"><span data-stu-id="be632-121">Requirement</span></span> | <span data-ttu-id="be632-122">Значение</span><span class="sxs-lookup"><span data-stu-id="be632-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be632-123">Версия</span><span class="sxs-lookup"><span data-stu-id="be632-123">Version</span></span><br/> | <span data-ttu-id="be632-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="be632-124">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="be632-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be632-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="be632-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be632-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be632-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be632-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be632-128">**Довнлоадколлектион. Item**</span><span class="sxs-lookup"><span data-stu-id="be632-128">**DownloadCollection.item**</span></span>](downloadcollection-item.md)
</dt> <dt>

[<span data-ttu-id="be632-129">**Объект Довнлоадколлектион**</span><span class="sxs-lookup"><span data-stu-id="be632-129">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





