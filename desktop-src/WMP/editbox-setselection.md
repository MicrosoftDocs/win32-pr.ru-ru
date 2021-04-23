---
title: EDITBOX. Сетселектион
description: Метод Сетселектион выбирает текст в элементе управления "поле ввода" из указанного начального индекса в указанный конечный индекс.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Сетселектион Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694726"
---
# <a name="editboxsetselection"></a><span data-ttu-id="c1a59-104">EDITBOX. Сетселектион</span><span class="sxs-lookup"><span data-stu-id="c1a59-104">EDITBOX.setSelection</span></span>

<span data-ttu-id="c1a59-105">Метод **сетселектион** выбирает текст в элементе управления "поле ввода" из указанного начального индекса в указанный конечный индекс.</span><span class="sxs-lookup"><span data-stu-id="c1a59-105">The **setSelection** method selects the text in the edit box control from the specified start index to the specified end index.</span></span>

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a><span data-ttu-id="c1a59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1a59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a59-107"><span id="start"></span><span id="START"></span>*запустить*</span><span class="sxs-lookup"><span data-stu-id="c1a59-107"><span id="start"></span><span id="START"></span>*start*</span></span>
</dt> <dd>

<span data-ttu-id="c1a59-108">**Число** (**Long**), содержащее индекс символа начальной позиции выбранного текста.</span><span class="sxs-lookup"><span data-stu-id="c1a59-108">**Number** (**long**) containing the character index of the starting position of the selected text.</span></span>

</dd> <dt>

<span data-ttu-id="c1a59-109"><span id="end"></span><span id="END"></span>*конце*</span><span class="sxs-lookup"><span data-stu-id="c1a59-109"><span id="end"></span><span id="END"></span>*end*</span></span>
</dt> <dd>

<span data-ttu-id="c1a59-110">**Число** (**Long**), содержащее индекс символа конечной позиции выбранного текста.</span><span class="sxs-lookup"><span data-stu-id="c1a59-110">**Number** (**long**) containing the character index of the ending position of the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a59-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1a59-111">Return Value</span></span>

<span data-ttu-id="c1a59-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c1a59-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a59-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1a59-113">Remarks</span></span>

<span data-ttu-id="c1a59-114">Если значение Start равно 0, а конец равен 1, то выделяется весь текст в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c1a59-114">If the start is 0 and the end is  1, all of the text in the edit box control is selected.</span></span> <span data-ttu-id="c1a59-115">Если начальное значение равно 1, все выделенные элементы отменяются.</span><span class="sxs-lookup"><span data-stu-id="c1a59-115">If the start is  1, any current selection is deselected.</span></span>

<span data-ttu-id="c1a59-116">Этот метод может быть вызван только после того, как элемент управления станет видимым.</span><span class="sxs-lookup"><span data-stu-id="c1a59-116">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a59-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c1a59-117">Requirements</span></span>



| <span data-ttu-id="c1a59-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c1a59-118">Requirement</span></span> | <span data-ttu-id="c1a59-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c1a59-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="c1a59-120">Версия</span><span class="sxs-lookup"><span data-stu-id="c1a59-120">Version</span></span><br/> | <span data-ttu-id="c1a59-121">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c1a59-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1a59-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1a59-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a59-123">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="c1a59-123">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="c1a59-124">**EDITBOX. Жетселектионенд**</span><span class="sxs-lookup"><span data-stu-id="c1a59-124">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="c1a59-125">**EDITBOX. Жетселектионстарт**</span><span class="sxs-lookup"><span data-stu-id="c1a59-125">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="c1a59-126">**EDITBOX. Реплацеселектион**</span><span class="sxs-lookup"><span data-stu-id="c1a59-126">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> </dl>

 

 





