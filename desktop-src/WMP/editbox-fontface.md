---
title: EDITBOX. Фонтфаце
description: Атрибут Фонтфаце указывает или получает шрифт для текста в элементе управления "поле ввода".
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- Фонтфаце Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698971"
---
# <a name="editboxfontface"></a><span data-ttu-id="9f625-104">EDITBOX. Фонтфаце</span><span class="sxs-lookup"><span data-stu-id="9f625-104">EDITBOX.fontFace</span></span>

<span data-ttu-id="9f625-105">Атрибут **фонтфаце** указывает или получает шрифт для текста в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="9f625-105">The **fontFace** attribute specifies or retrieves the font for text in the edit box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="9f625-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="9f625-106">Possible Values</span></span>

<span data-ttu-id="9f625-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9f625-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f625-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f625-108">Remarks</span></span>

<span data-ttu-id="9f625-109">Этот атрибут может быть именем любого допустимого шрифта, доступного в Windows.</span><span class="sxs-lookup"><span data-stu-id="9f625-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="9f625-110">Проигрыватель Windows Media не поддерживает установку шрифтов, поэтому выберите шрифт, который вы будете использовать в предполагаемой системе.</span><span class="sxs-lookup"><span data-stu-id="9f625-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="9f625-111">Если указанный **фонтфаце** недоступен в системе пользователя, элемент управления "поле ввода" по умолчанию имеет значение системный шрифт Windows.</span><span class="sxs-lookup"><span data-stu-id="9f625-111">If the **fontFace** specified is not available on the user's system, the edit box control defaults to the Windows system font.</span></span> <span data-ttu-id="9f625-112">По умолчанию для английских языковых систем используется значение Tahoma.</span><span class="sxs-lookup"><span data-stu-id="9f625-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="9f625-113">Для международных систем значение по умолчанию загружается из файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f625-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f625-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9f625-114">Requirements</span></span>



| <span data-ttu-id="9f625-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9f625-115">Requirement</span></span> | <span data-ttu-id="9f625-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9f625-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="9f625-117">Версия</span><span class="sxs-lookup"><span data-stu-id="9f625-117">Version</span></span><br/> | <span data-ttu-id="9f625-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9f625-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f625-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f625-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f625-120">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="9f625-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="9f625-121">**EDITBOX. fontSize**</span><span class="sxs-lookup"><span data-stu-id="9f625-121">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="9f625-122">**EDITBOX. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="9f625-122">**EDITBOX.fontStyle**</span></span>](editbox-fontstyle.md)
</dt> </dl>

 

 





