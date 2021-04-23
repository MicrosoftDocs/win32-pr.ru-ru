---
title: Метод Query. Бегиннекстграуп
description: Метод Бегиннекстграуп начинает новую группу условий. | Метод Query. Бегиннекстграуп
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- Бегиннекстграуп метод Windows Media Player
- метод Бегиннекстграуп Windows Media Player, класс запроса
- Класс запроса проигрыватель Windows Media Player, метод Бегиннекстграуп
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708422"
---
# <a name="querybeginnextgroup-method"></a><span data-ttu-id="2f70d-107">Метод Query. Бегиннекстграуп</span><span class="sxs-lookup"><span data-stu-id="2f70d-107">Query.beginNextGroup method</span></span>

<span data-ttu-id="2f70d-108">Метод **бегиннекстграуп** начинает новую группу условий.</span><span class="sxs-lookup"><span data-stu-id="2f70d-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f70d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f70d-109">Syntax</span></span>


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a><span data-ttu-id="2f70d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f70d-110">Parameters</span></span>

<span data-ttu-id="2f70d-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2f70d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f70d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f70d-112">Return value</span></span>

<span data-ttu-id="2f70d-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2f70d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f70d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f70d-114">Remarks</span></span>

<span data-ttu-id="2f70d-115">Начало новой группы условий означает, что вы завершили текущую группу условий.</span><span class="sxs-lookup"><span data-stu-id="2f70d-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="2f70d-116">Новая группа условий всегда объединяется с предыдущей группой условий с помощью логики или.</span><span class="sxs-lookup"><span data-stu-id="2f70d-116">The new condition group is always concatenated to the previous condition group using OR logic.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f70d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2f70d-117">Requirements</span></span>



| <span data-ttu-id="2f70d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2f70d-118">Requirement</span></span> | <span data-ttu-id="2f70d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2f70d-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f70d-120">Версия</span><span class="sxs-lookup"><span data-stu-id="2f70d-120">Version</span></span><br/> | <span data-ttu-id="2f70d-121">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="2f70d-121">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="2f70d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2f70d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2f70d-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f70d-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f70d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f70d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f70d-125">**Медиаколлектион. createQuery**</span><span class="sxs-lookup"><span data-stu-id="2f70d-125">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="2f70d-126">**Медиаколлектион. Жетплайлистбикуери**</span><span class="sxs-lookup"><span data-stu-id="2f70d-126">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="2f70d-127">**Медиаколлектион. Жетстрингколлектионбикуери**</span><span class="sxs-lookup"><span data-stu-id="2f70d-127">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="2f70d-128">**Объект запроса**</span><span class="sxs-lookup"><span data-stu-id="2f70d-128">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="2f70d-129">**Query. Аддкондитион**</span><span class="sxs-lookup"><span data-stu-id="2f70d-129">**Query.addCondition**</span></span>](query-addcondition.md)
</dt> </dl>

 

 





