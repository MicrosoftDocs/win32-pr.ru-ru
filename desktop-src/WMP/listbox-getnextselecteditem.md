---
title: LISTBOX. Жетнекстселектедитем
description: Метод Жетнекстселектедитем извлекает следующий выбранный элемент в элементе управления "список", начиная с элемента с указанным индексом.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- Проигрыватель Windows Media LISTBOX. Жетнекстселектедитем
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694968"
---
# <a name="listboxgetnextselecteditem"></a><span data-ttu-id="e8494-104">LISTBOX. Жетнекстселектедитем</span><span class="sxs-lookup"><span data-stu-id="e8494-104">LISTBOX.getNextSelectedItem</span></span>

<span data-ttu-id="e8494-105">Метод **жетнекстселектедитем** извлекает следующий выбранный элемент в элементе управления "список", начиная с элемента с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="e8494-105">The **getNextSelectedItem** method retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a><span data-ttu-id="e8494-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8494-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="e8494-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="e8494-108">**Число** (**Long**), содержащее индекс элемента, предшествующего получаемому элементу.</span><span class="sxs-lookup"><span data-stu-id="e8494-108">**Number** (**long**) containing the index of the item that precedes the item being retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8494-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8494-109">Return Value</span></span>

<span data-ttu-id="e8494-110">Этот метод возвращает **число** (**Long**), содержащее индекс следующего выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="e8494-110">This method returns a **Number** (**long**) containing the index of the next selected item.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8494-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8494-111">Remarks</span></span>

<span data-ttu-id="e8494-112">Чтобы начать поиск с начала, используйте значение 1 для начального индекса.</span><span class="sxs-lookup"><span data-stu-id="e8494-112">To start search from the beginning, use  1 for the start index.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8494-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e8494-113">Requirements</span></span>



| <span data-ttu-id="e8494-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e8494-114">Requirement</span></span> | <span data-ttu-id="e8494-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e8494-115">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="e8494-116">Версия</span><span class="sxs-lookup"><span data-stu-id="e8494-116">Version</span></span><br/> | <span data-ttu-id="e8494-117">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e8494-117">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8494-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8494-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8494-119">**Элемент LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="e8494-119">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





