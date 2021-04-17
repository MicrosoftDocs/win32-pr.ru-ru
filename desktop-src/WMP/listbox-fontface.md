---
title: LISTBOX. Фонтфаце
description: Атрибут Фонтфаце указывает или получает шрифт для элемента управления "список".
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- Проигрыватель Windows Media LISTBOX. Фонтфаце
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694973"
---
# <a name="listboxfontface"></a><span data-ttu-id="b3626-104">LISTBOX. Фонтфаце</span><span class="sxs-lookup"><span data-stu-id="b3626-104">LISTBOX.fontFace</span></span>

<span data-ttu-id="b3626-105">Атрибут **фонтфаце** указывает или получает шрифт для элемента управления "список".</span><span class="sxs-lookup"><span data-stu-id="b3626-105">The **fontFace** attribute specifies or retrieves the font for the list box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="b3626-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b3626-106">Possible Values</span></span>

<span data-ttu-id="b3626-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b3626-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3626-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3626-108">Remarks</span></span>

<span data-ttu-id="b3626-109">Этот атрибут может быть именем любого допустимого шрифта, доступного в Windows.</span><span class="sxs-lookup"><span data-stu-id="b3626-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="b3626-110">Проигрыватель Windows Media не поддерживает установку шрифтов, поэтому выберите шрифт, который вы будете использовать в предполагаемой системе.</span><span class="sxs-lookup"><span data-stu-id="b3626-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="b3626-111">Если указанный **фонтфаце** недоступен в системе пользователя, элемент управления "список" по умолчанию имеет значение системный шрифт Windows.</span><span class="sxs-lookup"><span data-stu-id="b3626-111">If the **fontFace** specified is not available on the user's system, the list box control defaults to the Windows system font.</span></span> <span data-ttu-id="b3626-112">По умолчанию для английских языковых систем используется значение Tahoma.</span><span class="sxs-lookup"><span data-stu-id="b3626-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="b3626-113">Для международных систем значение по умолчанию загружается из файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3626-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3626-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b3626-114">Requirements</span></span>



| <span data-ttu-id="b3626-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b3626-115">Requirement</span></span> | <span data-ttu-id="b3626-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b3626-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="b3626-117">Версия</span><span class="sxs-lookup"><span data-stu-id="b3626-117">Version</span></span><br/> | <span data-ttu-id="b3626-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b3626-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3626-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3626-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3626-120">**Элемент LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="b3626-120">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="b3626-121">**Список LISTBOX. fontSize**</span><span class="sxs-lookup"><span data-stu-id="b3626-121">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="b3626-122">**LISTBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="b3626-122">**LISTBOX.fontStyle**</span></span>](listbox-fontstyle.md)
</dt> </dl>

 

 





