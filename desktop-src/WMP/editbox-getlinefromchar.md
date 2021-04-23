---
title: EDITBOX. Жетлинефромчар
description: Метод Жетлинефромчар извлекает индекс строки для указанного индекса символов.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- Жетлинефромчар Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699273"
---
# <a name="editboxgetlinefromchar"></a><span data-ttu-id="48ea1-104">EDITBOX. Жетлинефромчар</span><span class="sxs-lookup"><span data-stu-id="48ea1-104">EDITBOX.getLineFromChar</span></span>

<span data-ttu-id="48ea1-105">Метод **жетлинефромчар** извлекает индекс строки для указанного индекса символов.</span><span class="sxs-lookup"><span data-stu-id="48ea1-105">The **getLineFromChar** method retrieves the line index for the specified character index.</span></span>

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a><span data-ttu-id="48ea1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="48ea1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48ea1-107"><span id="index"></span><span id="INDEX"></span>*номер*</span><span class="sxs-lookup"><span data-stu-id="48ea1-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="48ea1-108">**Число** (**Long**), содержащее индекс символа, индекс строки которого необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="48ea1-108">**Number** (**long**) containing the index of the character whose line index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48ea1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48ea1-109">Return Value</span></span>

<span data-ttu-id="48ea1-110">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="48ea1-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="48ea1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="48ea1-111">Remarks</span></span>

<span data-ttu-id="48ea1-112">Если указанная позиция символа равно 1, этот метод извлекает индекс строки текущей строки.</span><span class="sxs-lookup"><span data-stu-id="48ea1-112">If the specified character position is  1, this method retrieves the line index of the current line.</span></span>

<span data-ttu-id="48ea1-113">Этот метод может быть вызван только после того, как элемент управления станет видимым.</span><span class="sxs-lookup"><span data-stu-id="48ea1-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="48ea1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="48ea1-114">Requirements</span></span>



| <span data-ttu-id="48ea1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="48ea1-115">Requirement</span></span> | <span data-ttu-id="48ea1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48ea1-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="48ea1-117">Версия</span><span class="sxs-lookup"><span data-stu-id="48ea1-117">Version</span></span><br/> | <span data-ttu-id="48ea1-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="48ea1-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48ea1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48ea1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ea1-120">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="48ea1-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="48ea1-121">**EDITBOX. в строке**</span><span class="sxs-lookup"><span data-stu-id="48ea1-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="48ea1-122">**EDITBOX. Жетлинеиндекс**</span><span class="sxs-lookup"><span data-stu-id="48ea1-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





