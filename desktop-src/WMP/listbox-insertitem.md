---
title: LISTBOX. insertItem
description: Метод insertItem Вставляет указанный текст по указанному индексу в элементе управления "список".
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- Проигрыватель Windows Media LISTBOX. insertItem
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3600b40ca164c71bd62c0a9a368516d6ad0e1edd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704435"
---
# <a name="listboxinsertitem"></a><span data-ttu-id="7d5ac-104">LISTBOX. insertItem</span><span class="sxs-lookup"><span data-stu-id="7d5ac-104">LISTBOX.insertItem</span></span>

<span data-ttu-id="7d5ac-105">Метод **insertItem** Вставляет указанный текст по указанному индексу в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="7d5ac-105">The **insertItem** method inserts the specified text at the specified index in the list box control.</span></span>

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a><span data-ttu-id="7d5ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d5ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d5ac-107"><span id="index"></span><span id="INDEX"></span>*номер*</span><span class="sxs-lookup"><span data-stu-id="7d5ac-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="7d5ac-108">**Число** (**Long**), содержащее индекс строки для извлечения.</span><span class="sxs-lookup"><span data-stu-id="7d5ac-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7d5ac-109"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="7d5ac-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="7d5ac-110">**Строка** , содержащая вставляемый текст.</span><span class="sxs-lookup"><span data-stu-id="7d5ac-110">**String** containing the text to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d5ac-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d5ac-111">Return Value</span></span>

<span data-ttu-id="7d5ac-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7d5ac-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d5ac-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d5ac-113">Remarks</span></span>

<span data-ttu-id="7d5ac-114">При вставке строки индексы строки под вставленной строкой увеличиваются на единицу.</span><span class="sxs-lookup"><span data-stu-id="7d5ac-114">When a line is inserted, the line indexes for the lines below the inserted line increase by one.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d5ac-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7d5ac-115">Requirements</span></span>



| <span data-ttu-id="7d5ac-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7d5ac-116">Requirement</span></span> | <span data-ttu-id="7d5ac-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7d5ac-117">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="7d5ac-118">Версия</span><span class="sxs-lookup"><span data-stu-id="7d5ac-118">Version</span></span><br/> | <span data-ttu-id="7d5ac-119">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7d5ac-119">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d5ac-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d5ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d5ac-121">**Элемент LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="7d5ac-121">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





