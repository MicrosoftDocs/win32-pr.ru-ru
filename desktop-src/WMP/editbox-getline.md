---
title: EDITBOX. в строке
description: Метод GetText извлекает текст для строки с указанным индексом.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- Проигрыватель Windows Media для EDITBOX.
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694627"
---
# <a name="editboxgetline"></a><span data-ttu-id="a2813-104">EDITBOX. в строке</span><span class="sxs-lookup"><span data-stu-id="a2813-104">EDITBOX.getLine</span></span>

<span data-ttu-id="a2813-105">Метод **gettext** извлекает текст для строки с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="a2813-105">The **getLine** method retrieves the text for the line with the specified index.</span></span>

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a><span data-ttu-id="a2813-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2813-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2813-107"><span id="index"></span><span id="INDEX"></span>*номер*</span><span class="sxs-lookup"><span data-stu-id="a2813-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="a2813-108">**Число** (**Long**), содержащее индекс строки для извлечения.</span><span class="sxs-lookup"><span data-stu-id="a2813-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2813-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2813-109">Return Value</span></span>

<span data-ttu-id="a2813-110">Этот метод возвращает **строку**.</span><span class="sxs-lookup"><span data-stu-id="a2813-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2813-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2813-111">Remarks</span></span>

<span data-ttu-id="a2813-112">Если индекс является недопустимым, возвращается пустая строка.</span><span class="sxs-lookup"><span data-stu-id="a2813-112">If the index is not valid, an empty string is returned.</span></span> <span data-ttu-id="a2813-113">Этот метод может быть вызван только после того, как элемент управления станет видимым.</span><span class="sxs-lookup"><span data-stu-id="a2813-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2813-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a2813-114">Requirements</span></span>



| <span data-ttu-id="a2813-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a2813-115">Requirement</span></span> | <span data-ttu-id="a2813-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2813-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="a2813-117">Версия</span><span class="sxs-lookup"><span data-stu-id="a2813-117">Version</span></span><br/> | <span data-ttu-id="a2813-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a2813-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2813-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2813-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2813-120">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="a2813-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="a2813-121">**EDITBOX. Жетлинефромчар**</span><span class="sxs-lookup"><span data-stu-id="a2813-121">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="a2813-122">**EDITBOX. Жетлинеиндекс**</span><span class="sxs-lookup"><span data-stu-id="a2813-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





