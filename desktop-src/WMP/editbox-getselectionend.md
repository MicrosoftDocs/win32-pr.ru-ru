---
title: EDITBOX. Жетселектионенд
description: Метод Жетселектионенд извлекает конечное расположение выделенного текста в элементе управления EditBox.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- Жетселектионенд Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699272"
---
# <a name="editboxgetselectionend"></a><span data-ttu-id="7212d-104">EDITBOX. Жетселектионенд</span><span class="sxs-lookup"><span data-stu-id="7212d-104">EDITBOX.getSelectionEnd</span></span>

<span data-ttu-id="7212d-105">Метод **жетселектионенд** извлекает конечное расположение выделенного текста в элементе управления EditBox.</span><span class="sxs-lookup"><span data-stu-id="7212d-105">The **getSelectionEnd** method retrieves the ending position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a><span data-ttu-id="7212d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7212d-106">Parameters</span></span>

<span data-ttu-id="7212d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7212d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7212d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7212d-108">Return Value</span></span>

<span data-ttu-id="7212d-109">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="7212d-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7212d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7212d-110">Remarks</span></span>

<span data-ttu-id="7212d-111">Если текст не выбран, этот метод возвращает позицию точки вставки.</span><span class="sxs-lookup"><span data-stu-id="7212d-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="7212d-112">Если элемент управления является многострочным, этот метод возвращает индекс символа в элементе управления, а не индекс строки.</span><span class="sxs-lookup"><span data-stu-id="7212d-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="7212d-113">Этот метод может быть вызван только после того, как элемент управления станет видимым.</span><span class="sxs-lookup"><span data-stu-id="7212d-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="7212d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7212d-114">Requirements</span></span>



| <span data-ttu-id="7212d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7212d-115">Requirement</span></span> | <span data-ttu-id="7212d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7212d-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="7212d-117">Версия</span><span class="sxs-lookup"><span data-stu-id="7212d-117">Version</span></span><br/> | <span data-ttu-id="7212d-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7212d-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7212d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7212d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7212d-120">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="7212d-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="7212d-121">**EDITBOX. Жетселектионстарт**</span><span class="sxs-lookup"><span data-stu-id="7212d-121">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="7212d-122">**EDITBOX. Реплацеселектион**</span><span class="sxs-lookup"><span data-stu-id="7212d-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="7212d-123">**EDITBOX. Сетселектион**</span><span class="sxs-lookup"><span data-stu-id="7212d-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





