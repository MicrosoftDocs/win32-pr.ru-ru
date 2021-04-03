---
title: Шрифт состояния
description: Шрифт состояния
ms.assetid: eba697e8-8be5-4692-b7b2-a52c5642022a
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, отображение состояния
- обложки, отображение состояния
- Справочник по обложкам, отображению состояния
- Отображение состояния в обложках, шрифты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a773f3baaeda0eaa90dfe0702957b5b7888271
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986751"
---
# <a name="status-font"></a><span data-ttu-id="e6ea0-107">Шрифт состояния</span><span class="sxs-lookup"><span data-stu-id="e6ea0-107">Status Font</span></span>

<span data-ttu-id="e6ea0-108">Необходимо определить шрифт, используемый для представления состояния, которое вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-108">You must define the font used by the status display you wish to use.</span></span> <span data-ttu-id="e6ea0-109">Шрифт определяется тремя значениями, разделенными запятыми, представляющими начертание, размер и плотность шрифта.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-109">The font is defined by three values, separated by commas, representing the face, size, and weight of the font.</span></span>

<span data-ttu-id="e6ea0-110">**Значения гарнитуры**</span><span class="sxs-lookup"><span data-stu-id="e6ea0-110">**Typeface Values**</span></span>

<span data-ttu-id="e6ea0-111">Любое имя гарнитуры можно использовать, если оно может быть установлено на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-111">Any typeface name can be used if it is likely to be installed on the user's machine.</span></span> <span data-ttu-id="e6ea0-112">Если гарнитура не найдена на компьютере, операционная система выберет альтернативный вариант.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-112">If a typeface is not found on the machine, an alternate will be selected by the operating system.</span></span> <span data-ttu-id="e6ea0-113">В следующей таблице показаны гарнитуры, которые обычно находятся на устройствах под управлением Windows Mobile 2003.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-113">The following table shows the typefaces that are usually found on Windows Mobile 2003-based devices.</span></span>



| <span data-ttu-id="e6ea0-114">Шрифт</span><span class="sxs-lookup"><span data-stu-id="e6ea0-114">Typeface</span></span>       | <span data-ttu-id="e6ea0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="e6ea0-115">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="e6ea0-116">Tahoma</span><span class="sxs-lookup"><span data-stu-id="e6ea0-116">Tahoma</span></span>         | <span data-ttu-id="e6ea0-117">Гарнитура без засечек.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-117">A sans-serif typeface.</span></span>   |
| <span data-ttu-id="e6ea0-118">Консоль луЦида</span><span class="sxs-lookup"><span data-stu-id="e6ea0-118">Lucida Console</span></span> | <span data-ttu-id="e6ea0-119">Гарнитура с засечками.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-119">A square-serif typeface.</span></span> |



 

<span data-ttu-id="e6ea0-120">**Значения размера**</span><span class="sxs-lookup"><span data-stu-id="e6ea0-120">**Size Values**</span></span>

<span data-ttu-id="e6ea0-121">Это размер шрифта в точках.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-121">This is the size of the typeface in points.</span></span> <span data-ttu-id="e6ea0-122">Допустимо любое положительное целочисленное значение, однако рекомендуется использовать числа от 10 до 18.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-122">Any positive integer value is valid, though numbers between 10 and 18 are recommended.</span></span> <span data-ttu-id="e6ea0-123">Размер меньше 10 может быть трудным для чтения, а размеры свыше 18 могут не оставлять достаточно места для показа нескольких букв за раз.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-123">Sizes smaller than 10 may be difficult to read, and sizes above 18 may not leave enough space to display more than a few letters at a time.</span></span>

<span data-ttu-id="e6ea0-124">**Весовые значения**</span><span class="sxs-lookup"><span data-stu-id="e6ea0-124">**Weight Values**</span></span>

<span data-ttu-id="e6ea0-125">В следующей таблице показаны только допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-125">The only values allowed are shown in the following table.</span></span>



| <span data-ttu-id="e6ea0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e6ea0-126">Value</span></span> | <span data-ttu-id="e6ea0-127">Описание</span><span class="sxs-lookup"><span data-stu-id="e6ea0-127">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="e6ea0-128">B</span><span class="sxs-lookup"><span data-stu-id="e6ea0-128">B</span></span>     | <span data-ttu-id="e6ea0-129">Жирный</span><span class="sxs-lookup"><span data-stu-id="e6ea0-129">Bold</span></span>        |
| <span data-ttu-id="e6ea0-130">Нет</span><span class="sxs-lookup"><span data-stu-id="e6ea0-130">N</span></span>     | <span data-ttu-id="e6ea0-131">Норм.</span><span class="sxs-lookup"><span data-stu-id="e6ea0-131">Normal</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="e6ea0-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e6ea0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6ea0-133">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e6ea0-133">**Status**</span></span>](status.md)
</dt> </dl>

 

 




