---
title: EDITBOX. wordWrap
description: Атрибут wordWrap указывает или получает значение, указывающее, включено ли перенос по словам.
ms.assetid: 027817f0-e077-4db5-8216-f9a9f41fd210
keywords:
- EDITBOX. wordWrap проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fefe92691a150571ce16b0c80d187540d58f5f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694721"
---
# <a name="editboxwordwrap"></a><span data-ttu-id="07be2-104">EDITBOX. wordWrap</span><span class="sxs-lookup"><span data-stu-id="07be2-104">EDITBOX.wordWrap</span></span>

<span data-ttu-id="07be2-105">Атрибут **WordWrap** указывает или получает значение, указывающее, включено ли перенос по словам.</span><span class="sxs-lookup"><span data-stu-id="07be2-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="07be2-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="07be2-106">Possible Values</span></span>

<span data-ttu-id="07be2-107">Этот атрибут представляет собой **логическое** значение для чтения и записи со значением по умолчанию true.</span><span class="sxs-lookup"><span data-stu-id="07be2-107">This attribute is a read/write **Boolean** with a default value of true.</span></span>

## <a name="remarks"></a><span data-ttu-id="07be2-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07be2-108">Remarks</span></span>

<span data-ttu-id="07be2-109">Этот атрибут полезен только в том случае, если для **едитстиле** задано значение Multiline.</span><span class="sxs-lookup"><span data-stu-id="07be2-109">This attribute is useful only when **editStyle** is set to "multiline".</span></span>

<span data-ttu-id="07be2-110">Если перенос по словам отключен и текст не умещается в элементе управления, текст усекается.</span><span class="sxs-lookup"><span data-stu-id="07be2-110">If word wrap is disabled, and the text does not fit in the control, the text is truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="07be2-111">Требования</span><span class="sxs-lookup"><span data-stu-id="07be2-111">Requirements</span></span>



| <span data-ttu-id="07be2-112">Требование</span><span class="sxs-lookup"><span data-stu-id="07be2-112">Requirement</span></span> | <span data-ttu-id="07be2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="07be2-113">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="07be2-114">Версия</span><span class="sxs-lookup"><span data-stu-id="07be2-114">Version</span></span><br/> | <span data-ttu-id="07be2-115">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="07be2-115">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07be2-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07be2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07be2-117">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="07be2-117">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="07be2-118">**EDITBOX. Едитстиле**</span><span class="sxs-lookup"><span data-stu-id="07be2-118">**EDITBOX.editStyle**</span></span>](editbox-editstyle.md)
</dt> </dl>

 

 





