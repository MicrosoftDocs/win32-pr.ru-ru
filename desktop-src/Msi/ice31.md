---
description: ICE31 проверяет все стандартные стили шрифтов, используемые в элементах управления, отображающих текст. Также проверяется, что свойство Дефаултуифонт ссылается на допустимый стиль шрифта.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265221"
---
# <a name="ice31"></a><span data-ttu-id="ff0da-104">ICE31</span><span class="sxs-lookup"><span data-stu-id="ff0da-104">ICE31</span></span>

<span data-ttu-id="ff0da-105">ICE31 проверяет все стандартные стили шрифтов, используемые в [элементах управления](controls.md) , отображающих текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-105">ICE31 validates any predefined font styles used in [controls](controls.md) that display text.</span></span> <span data-ttu-id="ff0da-106">Также проверяется, что свойство [**дефаултуифонт**](defaultuifont.md) ссылается на допустимый стиль шрифта.</span><span class="sxs-lookup"><span data-stu-id="ff0da-106">It also validates that the [**DefaultUIFont**](defaultuifont.md) property refers to a valid font style.</span></span>

<span data-ttu-id="ff0da-107">Элементы управления могут иметь стандартный стиль шрифта, как описано в разделе [Добавление элементов управления и текста](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="ff0da-107">Controls can have a predefined font style as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="ff0da-108">Чтобы задать шрифт и начертание текстовой строки, перед строкой отображаемых символов укажите { \\ Style} или {&*Style*}.</span><span class="sxs-lookup"><span data-stu-id="ff0da-108">To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&*style*}.</span></span> <span data-ttu-id="ff0da-109">Где Style — это идентификатор, указанный в столбце система создала шрифт [таблицы система создала шрифт](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff0da-109">Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="ff0da-110">Если ни один из этих элементов отсутствует, но свойство [**дефаултуифонт**](defaultuifont.md) определено как допустимый стиль текста, будет использоваться этот шрифт.</span><span class="sxs-lookup"><span data-stu-id="ff0da-110">If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.</span></span>

<span data-ttu-id="ff0da-111">ICE31 проверяет текстовый столбец для каждого элемента управления в [таблице управления](control-table.md) , чтобы проверить наличие допустимой записи в [таблице система создала шрифт](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff0da-111">ICE31 checks the Text column for each control in the [Control Table](control-table.md) to verifies that a valid entry exist in the [TextStyle table](textstyle-table.md).</span></span>

<span data-ttu-id="ff0da-112">ICE31 игнорирует [элемент управления скроллаблетекст](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="ff0da-112">ICE31 ignores the [ScrollableText Control](scrollabletext-control.md).</span></span>

## <a name="results"></a><span data-ttu-id="ff0da-113">Результаты</span><span class="sxs-lookup"><span data-stu-id="ff0da-113">Results</span></span>

<span data-ttu-id="ff0da-114">ICE31 отправляет сообщение об ошибке для неопределенных стилей, слишком длинных имен стилей, отсутствующих таблиц система создала шрифт и тегов Style без закрывающих скобок.</span><span class="sxs-lookup"><span data-stu-id="ff0da-114">ICE31 posts an error message for undefined styles, style names that are too long, a missing TextStyle table, and style tags with no closing brace.</span></span>

<span data-ttu-id="ff0da-115">ICE31 отправляет предупреждение, если тег Style находится не в начале строки, или если элемент управления имеет несколько тегов Style.</span><span class="sxs-lookup"><span data-stu-id="ff0da-115">ICE31 posts a warning if the style tag is not at the beginning of the line, or if a control has multiple style tags.</span></span>

## <a name="example"></a><span data-ttu-id="ff0da-116">Пример</span><span class="sxs-lookup"><span data-stu-id="ff0da-116">Example</span></span>

<span data-ttu-id="ff0da-117">ICE31 отправляет следующие ошибки для приведенного примера:</span><span class="sxs-lookup"><span data-stu-id="ff0da-117">ICE31 posts the following errors for the example shown:</span></span>

-   <span data-ttu-id="ff0da-118">Элемент управления Диалогб. Control1 использует неопределенный система создала шрифт Бадстиле.</span><span class="sxs-lookup"><span data-stu-id="ff0da-118">Control DialogB.Control1 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="ff0da-119">Элемент управления Диалогб. Control2 использует неопределенный система создала шрифт Бадстиле.</span><span class="sxs-lookup"><span data-stu-id="ff0da-119">Control DialogB.Control2 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="ff0da-120">Для элемента управления Диалогб. Control6 в текстовом стиле отсутствует закрывающая фигурная скобка.</span><span class="sxs-lookup"><span data-stu-id="ff0da-120">Control DialogB.Control6 is missing closing brace in text style.</span></span>
-   <span data-ttu-id="ff0da-121">Control Диалогб. Control3 указывает текстовый стиль, который является слишком длинным, чтобы быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="ff0da-121">Control DialogB.Control3 specifies a text style that is too long to be valid.</span></span>

<span data-ttu-id="ff0da-122">ICE31 отправляет следующее предупреждение для приведенного примера:</span><span class="sxs-lookup"><span data-stu-id="ff0da-122">ICE31 posts the following warning for the example shown:</span></span>

-   <span data-ttu-id="ff0da-123">Тег стиля текста в Диалогб. Control4 не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="ff0da-123">Text Style tag in DialogB.Control4 has no effect.</span></span> <span data-ttu-id="ff0da-124">Вы действительно хотите, чтобы он отображался как текст?</span><span class="sxs-lookup"><span data-stu-id="ff0da-124">Do you really want it to appear as text?</span></span>

<span data-ttu-id="ff0da-125">[Таблица управления](control-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="ff0da-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="ff0da-126">Диалог</span><span class="sxs-lookup"><span data-stu-id="ff0da-126">Dialog</span></span>  | <span data-ttu-id="ff0da-127">Control</span><span class="sxs-lookup"><span data-stu-id="ff0da-127">Control</span></span>  | <span data-ttu-id="ff0da-128">Текст</span><span class="sxs-lookup"><span data-stu-id="ff0da-128">Text</span></span>                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0da-129">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="ff0da-129">DialogA</span></span> | <span data-ttu-id="ff0da-130">Control0</span><span class="sxs-lookup"><span data-stu-id="ff0da-130">Control0</span></span> | <span data-ttu-id="ff0da-131">{ \\ Окстиле} это отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-131">{\\OKStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="ff0da-132">Диалоговое окно</span><span class="sxs-lookup"><span data-stu-id="ff0da-132">DialogA</span></span> | <span data-ttu-id="ff0da-133">Control1</span><span class="sxs-lookup"><span data-stu-id="ff0da-133">Control1</span></span> | <span data-ttu-id="ff0da-134">{&Окстиле} Это отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-134">{&OKStyle}This is the text to display.</span></span>                                                                                                                              |
| <span data-ttu-id="ff0da-135">диалогб</span><span class="sxs-lookup"><span data-stu-id="ff0da-135">DialogB</span></span> | <span data-ttu-id="ff0da-136">Control1</span><span class="sxs-lookup"><span data-stu-id="ff0da-136">Control1</span></span> | <span data-ttu-id="ff0da-137">{&Бадстиле} Это отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-137">{&BadStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="ff0da-138">диалогб</span><span class="sxs-lookup"><span data-stu-id="ff0da-138">DialogB</span></span> | <span data-ttu-id="ff0da-139">Control2</span><span class="sxs-lookup"><span data-stu-id="ff0da-139">Control2</span></span> | <span data-ttu-id="ff0da-140">{ \\ Бадстиле} это отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-140">{\\BadStyle}This is the text to display.</span></span>                                                                                                                            |
| <span data-ttu-id="ff0da-141">диалогб</span><span class="sxs-lookup"><span data-stu-id="ff0da-141">DialogB</span></span> | <span data-ttu-id="ff0da-142">Control3</span><span class="sxs-lookup"><span data-stu-id="ff0da-142">Control3</span></span> | <span data-ttu-id="ff0da-143">{&ный стиль, который имеет более 72 символов и, следовательно, не может быть стилем, даже если вы каким-то образом управляли его в таблице система создала шрифт} Это отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-143">{&Style that is over 72 chars and therefore cannot possibly be a style even if somehow you did manage to get it in the TextStyle table}This is the text to display.</span></span> |
| <span data-ttu-id="ff0da-144">диалогб</span><span class="sxs-lookup"><span data-stu-id="ff0da-144">DialogB</span></span> | <span data-ttu-id="ff0da-145">Control4</span><span class="sxs-lookup"><span data-stu-id="ff0da-145">Control4</span></span> | <span data-ttu-id="ff0da-146">Предупреждение { \\ окстиле} это отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-146">Warning {\\OKStyle}This is the text to display.</span></span>                                                                                                                     |
| <span data-ttu-id="ff0da-147">диалогб</span><span class="sxs-lookup"><span data-stu-id="ff0da-147">DialogB</span></span> | <span data-ttu-id="ff0da-148">Control5</span><span class="sxs-lookup"><span data-stu-id="ff0da-148">Control5</span></span> | <span data-ttu-id="ff0da-149">{ \\ Окстиле} {&окстиле} это отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="ff0da-149">{\\OKStyle}{&OKStyle}This is the text to display.</span></span>                                                                                                                   |
| <span data-ttu-id="ff0da-150">диалогб</span><span class="sxs-lookup"><span data-stu-id="ff0da-150">DialogB</span></span> | <span data-ttu-id="ff0da-151">Control6</span><span class="sxs-lookup"><span data-stu-id="ff0da-151">Control6</span></span> | <span data-ttu-id="ff0da-152">{ \\ Окстиле — это текст для вывода.</span><span class="sxs-lookup"><span data-stu-id="ff0da-152">{\\OKStyle This is the text to display.</span></span>                                                                                                                             |



 

<span data-ttu-id="ff0da-153">[Таблица система создала шрифт](textstyle-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="ff0da-153">[TextStyle table](textstyle-table.md) (partial)</span></span>



| <span data-ttu-id="ff0da-154">Система создала шрифт</span><span class="sxs-lookup"><span data-stu-id="ff0da-154">TextStyle</span></span> |
|-----------|
| <span data-ttu-id="ff0da-155">окстиле</span><span class="sxs-lookup"><span data-stu-id="ff0da-155">OkStyle</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="ff0da-156">См. также</span><span class="sxs-lookup"><span data-stu-id="ff0da-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff0da-157">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="ff0da-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



