---
title: EDITBOX. Жетселектионстарт
description: Метод Жетселектионстарт извлекает начальную точку выделенного текста в элементе управления EditBox.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- Жетселектионстарт Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699271"
---
# <a name="editboxgetselectionstart"></a><span data-ttu-id="0dbd4-104">EDITBOX. Жетселектионстарт</span><span class="sxs-lookup"><span data-stu-id="0dbd4-104">EDITBOX.getSelectionStart</span></span>

<span data-ttu-id="0dbd4-105">Метод **жетселектионстарт** извлекает начальную точку выделенного текста в элементе управления EditBox.</span><span class="sxs-lookup"><span data-stu-id="0dbd4-105">The **getSelectionStart** method retrieves the starting position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a><span data-ttu-id="0dbd4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dbd4-106">Parameters</span></span>

<span data-ttu-id="0dbd4-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0dbd4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dbd4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dbd4-108">Return Value</span></span>

<span data-ttu-id="0dbd4-109">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="0dbd4-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="0dbd4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0dbd4-110">Remarks</span></span>

<span data-ttu-id="0dbd4-111">Если текст не выбран, этот метод возвращает позицию точки вставки.</span><span class="sxs-lookup"><span data-stu-id="0dbd4-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="0dbd4-112">Если элемент управления является многострочным, этот метод возвращает индекс символа в элементе управления, а не индекс строки.</span><span class="sxs-lookup"><span data-stu-id="0dbd4-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="0dbd4-113">Этот метод может быть вызван только после того, как элемент управления станет видимым.</span><span class="sxs-lookup"><span data-stu-id="0dbd4-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dbd4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0dbd4-114">Requirements</span></span>



| <span data-ttu-id="0dbd4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0dbd4-115">Requirement</span></span> | <span data-ttu-id="0dbd4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0dbd4-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="0dbd4-117">Версия</span><span class="sxs-lookup"><span data-stu-id="0dbd4-117">Version</span></span><br/> | <span data-ttu-id="0dbd4-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0dbd4-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0dbd4-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0dbd4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dbd4-120">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="0dbd4-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="0dbd4-121">**EDITBOX. Жетселектионенд**</span><span class="sxs-lookup"><span data-stu-id="0dbd4-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="0dbd4-122">**EDITBOX. Реплацеселектион**</span><span class="sxs-lookup"><span data-stu-id="0dbd4-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="0dbd4-123">**EDITBOX. Сетселектион**</span><span class="sxs-lookup"><span data-stu-id="0dbd4-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





