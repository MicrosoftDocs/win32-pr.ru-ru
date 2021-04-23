---
title: LISTBOX. findItem
description: Метод findItem выполняет поиск заданной строки, начиная с элемента, следующего за указанным индексом элемента.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- Проигрыватель Windows Media LISTBOX. findItem
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694982"
---
# <a name="listboxfinditem"></a><span data-ttu-id="47979-104">LISTBOX. findItem</span><span class="sxs-lookup"><span data-stu-id="47979-104">LISTBOX.findItem</span></span>

<span data-ttu-id="47979-105">Метод **findItem** выполняет поиск заданной строки, начиная с элемента, следующего за указанным индексом элемента.</span><span class="sxs-lookup"><span data-stu-id="47979-105">The **findItem** method searches for a given string starting with the item following the specified item index.</span></span>

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a><span data-ttu-id="47979-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47979-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47979-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="47979-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="47979-108">**Число** (**Long**), содержащее индекс элемента, с которого начинается поиск.</span><span class="sxs-lookup"><span data-stu-id="47979-108">**Number** (**long**) containing the index of the item at which to start the search.</span></span>

</dd> <dt>

<span data-ttu-id="47979-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span><span class="sxs-lookup"><span data-stu-id="47979-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span></span>
</dt> <dd>

<span data-ttu-id="47979-110">**Строка** , содержащая искомый текст.</span><span class="sxs-lookup"><span data-stu-id="47979-110">**String** containing the text to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47979-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47979-111">Return Value</span></span>

<span data-ttu-id="47979-112">Этот метод возвращает **число** (**Long**), содержащее индекс элемента, содержащего строку.</span><span class="sxs-lookup"><span data-stu-id="47979-112">This method returns a **Number** (**long**) containing the index of the item that contains the string.</span></span>

## <a name="remarks"></a><span data-ttu-id="47979-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="47979-113">Remarks</span></span>

<span data-ttu-id="47979-114">Чтобы начать поиск с первой строки элемента управления "список", используйте 1 в качестве *startIndex*.</span><span class="sxs-lookup"><span data-stu-id="47979-114">To start the search at the first line of the list box control, use  1 as the *startIndex*.</span></span> <span data-ttu-id="47979-115">Чтобы продолжить поиск текста после того, как будет найдена первая строка, используйте возвращенный индекс строки в качестве *startIndex*, и поиск начнется со следующей строки.</span><span class="sxs-lookup"><span data-stu-id="47979-115">To continue to search for text after the first line is found, use the returned line index as the *startIndex*, and the search will start at the next line.</span></span> <span data-ttu-id="47979-116">Этот метод будет искать подстроки и не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="47979-116">This method will search for substrings and is not case-sensitive.</span></span>

## <a name="requirements"></a><span data-ttu-id="47979-117">Требования</span><span class="sxs-lookup"><span data-stu-id="47979-117">Requirements</span></span>



| <span data-ttu-id="47979-118">Требование</span><span class="sxs-lookup"><span data-stu-id="47979-118">Requirement</span></span> | <span data-ttu-id="47979-119">Значение</span><span class="sxs-lookup"><span data-stu-id="47979-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="47979-120">Версия</span><span class="sxs-lookup"><span data-stu-id="47979-120">Version</span></span><br/> | <span data-ttu-id="47979-121">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="47979-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47979-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47979-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47979-123">**Элемент LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="47979-123">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





