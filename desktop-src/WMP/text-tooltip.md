---
title: TEXT. toolTip
description: Атрибут toolTip указывает или получает текст подсказки для элемента управления Text.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675411"
---
# <a name="texttooltip"></a><span data-ttu-id="aee62-104">TEXT. toolTip</span><span class="sxs-lookup"><span data-stu-id="aee62-104">TEXT.toolTip</span></span>

<span data-ttu-id="aee62-105">Атрибут **ToolTip** указывает или получает текст подсказки для элемента управления Text.</span><span class="sxs-lookup"><span data-stu-id="aee62-105">The **toolTip** attribute specifies or retrieves the ToolTip text for the text control.</span></span>

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a><span data-ttu-id="aee62-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="aee62-106">Possible Values</span></span>

<span data-ttu-id="aee62-107">Этот атрибут является **строкой** для чтения и записи и имеет максимальную длину 1024 символов.</span><span class="sxs-lookup"><span data-stu-id="aee62-107">This attribute is a read/write **String** with a maximum length of 1024 characters.</span></span> <span data-ttu-id="aee62-108">У него нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aee62-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aee62-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aee62-109">Remarks</span></span>

<span data-ttu-id="aee62-110">Если этот атрибут не указан и текст в атрибуте **value** усекается в элементе управления Text, или для свойства **WordWrap** задано значение true, подсказка будет отображать полный текст атрибута **value** .</span><span class="sxs-lookup"><span data-stu-id="aee62-110">If this attribute is not specified, and the text in the **value** attribute is truncated in the Text control, or **wordWrap** is set to true, the ToolTip will display the full text of the **value** attribute.</span></span>

<span data-ttu-id="aee62-111">Если для этого атрибута задано значение "" (пустая строка), подсказка не отображается.</span><span class="sxs-lookup"><span data-stu-id="aee62-111">When this attribute is set to "" (empty string), no ToolTip is displayed.</span></span>

<span data-ttu-id="aee62-112">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="aee62-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee62-113">Требования</span><span class="sxs-lookup"><span data-stu-id="aee62-113">Requirements</span></span>



| <span data-ttu-id="aee62-114">Требование</span><span class="sxs-lookup"><span data-stu-id="aee62-114">Requirement</span></span> | <span data-ttu-id="aee62-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aee62-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="aee62-116">Версия</span><span class="sxs-lookup"><span data-stu-id="aee62-116">Version</span></span><br/> | <span data-ttu-id="aee62-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="aee62-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aee62-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aee62-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee62-119">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="aee62-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="aee62-120">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="aee62-120">**TEXT.value**</span></span>](text-value.md)
</dt> <dt>

[<span data-ttu-id="aee62-121">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="aee62-121">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





