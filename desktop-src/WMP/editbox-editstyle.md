---
title: EDITBOX. Едитстиле
description: Атрибут Едитстиле указывает или получает стиль элемента управления "поле ввода".
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- Едитстиле Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695213"
---
# <a name="editboxeditstyle"></a><span data-ttu-id="1661e-104">EDITBOX. Едитстиле</span><span class="sxs-lookup"><span data-stu-id="1661e-104">EDITBOX.editStyle</span></span>

<span data-ttu-id="1661e-105">Атрибут **едитстиле** указывает или получает стиль элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="1661e-105">The **editStyle** attribute specifies or retrieves the style of the edit box control.</span></span>

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a><span data-ttu-id="1661e-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1661e-106">Possible Values</span></span>

<span data-ttu-id="1661e-107">Этот атрибут является **строкой** для чтения и записи, содержащей одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1661e-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="1661e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1661e-108">Value</span></span>     | <span data-ttu-id="1661e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1661e-109">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="1661e-110">нормальный</span><span class="sxs-lookup"><span data-stu-id="1661e-110">normal</span></span>    | <span data-ttu-id="1661e-111">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1661e-111">Default.</span></span> <span data-ttu-id="1661e-112">Отображает нормальный текст в одной строке.</span><span class="sxs-lookup"><span data-stu-id="1661e-112">Displays normal text on a single line.</span></span>                                 |
| <span data-ttu-id="1661e-113">password</span><span class="sxs-lookup"><span data-stu-id="1661e-113">password</span></span>  | <span data-ttu-id="1661e-114">Отображает звездочки ( \* ) вместо текста.</span><span class="sxs-lookup"><span data-stu-id="1661e-114">Displays asterisks (\*) in place of text.</span></span> <span data-ttu-id="1661e-115">Может указываться только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="1661e-115">Can only be specified at design time.</span></span> |
| <span data-ttu-id="1661e-116">верхний регистр</span><span class="sxs-lookup"><span data-stu-id="1661e-116">uppercase</span></span> | <span data-ttu-id="1661e-117">Отображает текст в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="1661e-117">Displays text as all uppercase.</span></span>                                                 |
| <span data-ttu-id="1661e-118">Нижний регистр</span><span class="sxs-lookup"><span data-stu-id="1661e-118">lowercase</span></span> | <span data-ttu-id="1661e-119">Отображает текст в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="1661e-119">Displays text as all lowercase.</span></span>                                                 |
| <span data-ttu-id="1661e-120">number</span><span class="sxs-lookup"><span data-stu-id="1661e-120">number</span></span>    | <span data-ttu-id="1661e-121">Отображаются только числа.</span><span class="sxs-lookup"><span data-stu-id="1661e-121">Only displays numbers.</span></span>                                                          |
| <span data-ttu-id="1661e-122">нескольких</span><span class="sxs-lookup"><span data-stu-id="1661e-122">multiline</span></span> | <span data-ttu-id="1661e-123">Отображает несколько строк текста.</span><span class="sxs-lookup"><span data-stu-id="1661e-123">Displays multiple lines of text.</span></span> <span data-ttu-id="1661e-124">Может указываться только во время разработки.</span><span class="sxs-lookup"><span data-stu-id="1661e-124">Can only be specified at design time.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="1661e-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1661e-125">Remarks</span></span>

<span data-ttu-id="1661e-126">Для этого атрибута можно задать только значение "пароль" или "Многострочный" во время разработки.</span><span class="sxs-lookup"><span data-stu-id="1661e-126">This attribute can only be set to "password" or "multiline" at design time.</span></span> <span data-ttu-id="1661e-127">Если для него задано значение "Многострочный", то во время выполнения его нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="1661e-127">If it is set to "multiline", the value cannot be changed at run time.</span></span>

## <a name="requirements"></a><span data-ttu-id="1661e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1661e-128">Requirements</span></span>



| <span data-ttu-id="1661e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1661e-129">Requirement</span></span> | <span data-ttu-id="1661e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1661e-130">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="1661e-131">Версия</span><span class="sxs-lookup"><span data-stu-id="1661e-131">Version</span></span><br/> | <span data-ttu-id="1661e-132">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1661e-132">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1661e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1661e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1661e-134">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="1661e-134">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> </dl>

 

 





