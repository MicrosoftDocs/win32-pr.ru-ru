---
title: TEXT. Фонтсмусинг
description: Атрибут Фонтсмусинг указывает или получает значение, указывающее, включено ли сглаживание шрифтов.
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- Проигрыватель Windows Media TEXT. Фонтсмусинг
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694610"
---
# <a name="textfontsmoothing"></a><span data-ttu-id="a8841-104">TEXT. Фонтсмусинг</span><span class="sxs-lookup"><span data-stu-id="a8841-104">TEXT.fontSmoothing</span></span>

<span data-ttu-id="a8841-105">Атрибут **фонтсмусинг** указывает или получает значение, указывающее, включено ли сглаживание шрифтов.</span><span class="sxs-lookup"><span data-stu-id="a8841-105">The **fontSmoothing** attribute specifies or retrieves a value indicating whether font smoothing is enabled.</span></span>

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a><span data-ttu-id="a8841-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="a8841-106">Possible Values</span></span>

<span data-ttu-id="a8841-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a8841-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a8841-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a8841-108">Value</span></span> | <span data-ttu-id="a8841-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a8841-109">Description</span></span>                          |
|-------|--------------------------------------|
| <span data-ttu-id="a8841-110">true</span><span class="sxs-lookup"><span data-stu-id="a8841-110">true</span></span>  | <span data-ttu-id="a8841-111">Сглаживание шрифтов включено.</span><span class="sxs-lookup"><span data-stu-id="a8841-111">Font smoothing is enabled.</span></span>           |
| <span data-ttu-id="a8841-112">false</span><span class="sxs-lookup"><span data-stu-id="a8841-112">false</span></span> | <span data-ttu-id="a8841-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8841-113">Default.</span></span> <span data-ttu-id="a8841-114">Сглаживание шрифтов отключено.</span><span class="sxs-lookup"><span data-stu-id="a8841-114">Font smoothing is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a8841-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8841-115">Remarks</span></span>

<span data-ttu-id="a8841-116">Сглаживание шрифтов использует функцию сглаживания операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a8841-116">Font smoothing uses the anti-aliasing feature of the operating system.</span></span> <span data-ttu-id="a8841-117">Если сглаживание шрифтов включено и операционная система поддерживает сглаживание, проигрыватель Windows Media пытается сгладить текст.</span><span class="sxs-lookup"><span data-stu-id="a8841-117">If font smoothing is enabled and the operating system supports anti-aliasing, Windows Media Player attempts to smooth the text.</span></span> <span data-ttu-id="a8841-118">Не все шрифты поддерживают сглаживание.</span><span class="sxs-lookup"><span data-stu-id="a8841-118">Not all fonts support anti-aliasing.</span></span> <span data-ttu-id="a8841-119">Проигрыватель Windows Media 10 использует метод сглаживания ClearType в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8841-119">Windows Media Player 10 uses the Windows XP ClearType anti-aliasing method.</span></span>

-   <span data-ttu-id="a8841-120">**Предупреждение об ошибке** Сглаживание шрифта на прозрачном цвете может привести к тому, что прозрачный цвет будет смешиваться с символами.</span><span class="sxs-lookup"><span data-stu-id="a8841-120">**Warning** Font smoothing over a transparent color may cause the transparent color to blend into the characters.</span></span> <span data-ttu-id="a8841-121">Не рекомендуется использовать **фонтсмусинг** , если текст будет отображаться по прозрачности.</span><span class="sxs-lookup"><span data-stu-id="a8841-121">It is not recommended that you use **fontSmoothing** if the text will display over a transparency.</span></span>

<span data-ttu-id="a8841-122">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="a8841-122">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8841-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a8841-123">Requirements</span></span>



| <span data-ttu-id="a8841-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a8841-124">Requirement</span></span> | <span data-ttu-id="a8841-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a8841-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a8841-126">Версия</span><span class="sxs-lookup"><span data-stu-id="a8841-126">Version</span></span><br/> | <span data-ttu-id="a8841-127">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="a8841-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8841-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8841-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8841-129">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="a8841-129">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





