---
title: TEXT. Фонтфаце
description: Атрибут Фонтфаце указывает или получает гарнитуру для элемента управления "текст".
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Проигрыватель Windows Media TEXT. Фонтфаце
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717964"
---
# <a name="textfontface"></a><span data-ttu-id="b4581-104">TEXT. Фонтфаце</span><span class="sxs-lookup"><span data-stu-id="b4581-104">TEXT.fontFace</span></span>

<span data-ttu-id="b4581-105">Атрибут **фонтфаце** указывает или получает гарнитуру для элемента управления "текст".</span><span class="sxs-lookup"><span data-stu-id="b4581-105">The **fontFace** attribute specifies or retrieves the typeface for the Text control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="b4581-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b4581-106">Possible Values</span></span>

<span data-ttu-id="b4581-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b4581-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4581-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4581-108">Remarks</span></span>

<span data-ttu-id="b4581-109">Этот атрибут может быть именем любого допустимого шрифта, доступного в Windows.</span><span class="sxs-lookup"><span data-stu-id="b4581-109">This attribute can be the name of any valid font available on Windows.</span></span> <span data-ttu-id="b4581-110">Проигрыватель Windows Media не поддерживает установку шрифтов, поэтому выберите шрифт, который вы будете использовать в предполагаемой системе.</span><span class="sxs-lookup"><span data-stu-id="b4581-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="b4581-111">Если указанный **фонтфаце** недоступен в системе пользователя, то элемент управления "текст" по умолчанию имеет системный шрифт Windows.</span><span class="sxs-lookup"><span data-stu-id="b4581-111">If the **fontFace** specified is not available on the user's system, the Text control defaults to the Windows system font.</span></span>

<span data-ttu-id="b4581-112">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="b4581-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4581-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b4581-113">Requirements</span></span>



| <span data-ttu-id="b4581-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b4581-114">Requirement</span></span> | <span data-ttu-id="b4581-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b4581-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b4581-116">Версия</span><span class="sxs-lookup"><span data-stu-id="b4581-116">Version</span></span><br/> | <span data-ttu-id="b4581-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="b4581-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4581-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4581-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4581-119">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="b4581-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="b4581-120">**TEXT. fontSize**</span><span class="sxs-lookup"><span data-stu-id="b4581-120">**TEXT.fontSize**</span></span>](text-fontsize.md)
</dt> </dl>

 

 





