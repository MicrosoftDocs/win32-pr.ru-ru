---
description: Эти константы определяют значения, указывающие тип объектов Иконтекстноде.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Типы узлов контекста (Иагуид. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143000"
---
# <a name="context-node-types"></a><span data-ttu-id="42e49-103">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="42e49-103">Context Node Types</span></span>

<span data-ttu-id="42e49-104">Эти константы определяют значения, указывающие тип объектов [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="42e49-104">These constants define values that specify the type of [**IContextNode**](icontextnode.md) objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="42e49-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="42e49-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="42e49-106">Описание</span><span class="sxs-lookup"><span data-stu-id="42e49-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <span data-ttu-id="42e49-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(аналисишинт)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-108">Представляет узел, содержащий дополнительные сведения о контексте для региона, который <a href="iinkanalyzer.md"><strong>иинканализер</strong></a> использует для улучшения его анализа.</span><span class="sxs-lookup"><span data-stu-id="42e49-108">Represents a node that contains additional context information for a region that the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> uses to improve its analysis.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <span data-ttu-id="42e49-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(кустомрекогнизер)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CustomRecognizer)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-110">Представляет узел, используемый для одной операции распознавания.</span><span class="sxs-lookup"><span data-stu-id="42e49-110">Represents a node used for a single recognition operation.</span></span><br/> <span data-ttu-id="42e49-111">Все штрихи и узлы, входящие в пользовательский узел распознавателя, распознаются независимой операцией распознавания и не анализируются <a href="iinkanalyzer.md"><strong>иинканализер</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="42e49-111">All strokes and nodes that are within a custom recognizer node are recognized by an independent recognition operation and are not analyzed by the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span></span><br/> <span data-ttu-id="42e49-112">Пользовательский узел распознавателя должен быть прямым дочерним элементом корневого узла анализатора красок.</span><span class="sxs-lookup"><span data-stu-id="42e49-112">A custom recognizer node must be the direct child of ink analyzer's root node.</span></span><br/> <span data-ttu-id="42e49-113">Пользовательский узел распознавателя может содержать следующие типы дочерних элементов:</span><span class="sxs-lookup"><span data-stu-id="42e49-113">A custom recognizer node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="42e49-114">Любое количество узлов Унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="42e49-114">Any number of UnclassifiedInk nodes.</span></span></li>
<li><span data-ttu-id="42e49-115">Любое количество узлов объектов.</span><span class="sxs-lookup"><span data-stu-id="42e49-115">Any number of Object nodes.</span></span></li>
<li><span data-ttu-id="42e49-116">Любое число узлов линий.</span><span class="sxs-lookup"><span data-stu-id="42e49-116">Any number of Line nodes.</span></span></li>
<li><span data-ttu-id="42e49-117">Любое количество узлов Инкворд.</span><span class="sxs-lookup"><span data-stu-id="42e49-117">Any number of InkWord nodes.</span></span></li>
<li><span data-ttu-id="42e49-118">Любое количество узлов с неизвестным значением идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="42e49-118">Any number of nodes with an unknown Guid value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <span data-ttu-id="42e49-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(изображение)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Image)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-120">Представляет узел для двумерного региона, в котором в документе могут существовать любые изображения, отличные от рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="42e49-120">Represents a node for a two-dimensional region where any non-ink images can exist in the document.</span></span><br/> <span data-ttu-id="42e49-121"><a href="iinkanalyzer.md"><strong>Иинканализер</strong></a> не создает узлы образа.</span><span class="sxs-lookup"><span data-stu-id="42e49-121">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce image nodes.</span></span> <span data-ttu-id="42e49-122">Используйте <a href="icontextnode-createsubnode.md"><strong>иконтекстноде:: креатесубноде</strong></a> , чтобы добавить узел изображения в дерево узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="42e49-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add an image node to the context node tree.</span></span> <span data-ttu-id="42e49-123">Затем <strong>иинканализер</strong> использует регионы, определенные узлом изображения, чтобы определить, какие заметки рукописного ввода заметок не являются изображениями рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="42e49-123">The <strong>IInkAnalyzer</strong> then uses the regions defined by the image node to determine if any ink annotates the non-ink image.</span></span><br/> <span data-ttu-id="42e49-124">Узел изображения не может содержать дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="42e49-124">An image node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <span data-ttu-id="42e49-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(инкбуллет)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-126">Инкбуллет Контекстнодетипе представляет коллекцию штрихов, образующих маркер в маркированном списке.</span><span class="sxs-lookup"><span data-stu-id="42e49-126">The InkBullet ContextNodeType represents a collection of strokes that make up a bullet in a bulleted list.</span></span><br/> <span data-ttu-id="42e49-127">Контекстноде типа Инкбуллет не может иметь дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="42e49-127">A ContextNode of type InkBullet cannot have any children.</span></span> <span data-ttu-id="42e49-128">Он может быть только дочерним по отношению к Контекстноде абзаца.</span><span class="sxs-lookup"><span data-stu-id="42e49-128">It can only be a child of a Paragraph ContextNode.</span></span> <span data-ttu-id="42e49-129">Только один Инкбуллет может находиться в одном абзаце Контекстноде.</span><span class="sxs-lookup"><span data-stu-id="42e49-129">Only one InkBullet can appear in a single Paragraph ContextNode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <span data-ttu-id="42e49-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(инкдравинг)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-131">Представляет узел для коллекции штрихов, образующих рисование.</span><span class="sxs-lookup"><span data-stu-id="42e49-131">Represents a node for a collection of strokes that constitutes a drawing.</span></span><br/> <span data-ttu-id="42e49-132">Рисунки — это штрихи, которые определяются как фигуры или абстрактные эскизы.</span><span class="sxs-lookup"><span data-stu-id="42e49-132">Drawings are strokes that are determined to be shapes or abstract sketches.</span></span> <span data-ttu-id="42e49-133">Обычно это любые штрихи, не классифицированные как написание штрихов.</span><span class="sxs-lookup"><span data-stu-id="42e49-133">They are generally any strokes that are not classified as writing strokes.</span></span><br/> <span data-ttu-id="42e49-134">Узел рисования рукописного ввода не может содержать дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="42e49-134">An ink drawing node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <span data-ttu-id="42e49-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(инкворд)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-136">Представляет узел для коллекции штрихов, образующих логическую группу для формирования распознаваемого слова.</span><span class="sxs-lookup"><span data-stu-id="42e49-136">Represents a node for a collection of strokes that constitutes a logical grouping to form a recognizable word.</span></span><br/> <span data-ttu-id="42e49-137">Узел рукописного слова не может содержать дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="42e49-137">An ink word node cannot contain any child elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <span data-ttu-id="42e49-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(строка)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Line)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-139">Представляет узел для строки слов.</span><span class="sxs-lookup"><span data-stu-id="42e49-139">Represents a node for a line of words.</span></span><br/> <span data-ttu-id="42e49-140">Узел линии может содержать следующие типы дочерних элементов:</span><span class="sxs-lookup"><span data-stu-id="42e49-140">A line node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="42e49-141">Любое количество узлов рукописных слов.</span><span class="sxs-lookup"><span data-stu-id="42e49-141">Any number of ink word nodes.</span></span></li>
<li><span data-ttu-id="42e49-142">Любое количество узлов текстовых слов.</span><span class="sxs-lookup"><span data-stu-id="42e49-142">Any number of text word nodes.</span></span></li>
<li><span data-ttu-id="42e49-143">Любое количество узлов с неизвестным значением <strong>идентификатора GUID</strong> .</span><span class="sxs-lookup"><span data-stu-id="42e49-143">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <span data-ttu-id="42e49-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(объект)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Object)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-145">Представляет узел для объекта, возвращаемого &quot; &quot; пользовательским распознавателем объекта.</span><span class="sxs-lookup"><span data-stu-id="42e49-145">Represents a node for an object that is returned from an &quot;object&quot; custom recognizer.</span></span><br/> <span data-ttu-id="42e49-146">Узел объекта не может содержать дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="42e49-146">An object node cannot contain any child elements.</span></span><br/> <span data-ttu-id="42e49-147">Узлы объектов могут содержать только пользовательские узлы распознавателя.</span><span class="sxs-lookup"><span data-stu-id="42e49-147">Only custom recognizer nodes can contain object nodes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <span data-ttu-id="42e49-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(абзац)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Paragraph)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-149">Представляет узел для коллекции узлов, образующих логическую группу строк.</span><span class="sxs-lookup"><span data-stu-id="42e49-149">Represents a node for a collection of nodes that constitutes a logical grouping of lines.</span></span><br/> <span data-ttu-id="42e49-150">Точное определение абзаца определяется механизмами анализа.</span><span class="sxs-lookup"><span data-stu-id="42e49-150">The exact definition of a paragraph is determined by the analyzing engines.</span></span> <span data-ttu-id="42e49-151">Как правило, абзац содержит группы строк, которые можно переформатировать вместе, если размер поля, содержащего строки, было изменено.</span><span class="sxs-lookup"><span data-stu-id="42e49-151">In general, a paragraph contains groups of lines that would reflow together if the box that contains the lines were resized.</span></span><br/> <span data-ttu-id="42e49-152">Узел абзаца может содержать следующие типы дочерних элементов:</span><span class="sxs-lookup"><span data-stu-id="42e49-152">A paragraph node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="42e49-153">Любое количество узлов с маркерами ввода.</span><span class="sxs-lookup"><span data-stu-id="42e49-153">Any number of ink bullet nodes.</span></span></li>
<li><span data-ttu-id="42e49-154">Любое число узлов линий.</span><span class="sxs-lookup"><span data-stu-id="42e49-154">Any number of line nodes.</span></span></li>
<li><span data-ttu-id="42e49-155">Любое количество узлов с неизвестным значением <strong>идентификатора GUID</strong> .</span><span class="sxs-lookup"><span data-stu-id="42e49-155">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <span data-ttu-id="42e49-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(корневой)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(Root)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-157">Представляет узел для верхнего узла дерева узлов, описывающих результаты анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="42e49-157">Represents a node for the top node of a tree of nodes that describe the results of ink analysis.</span></span><br/> <span data-ttu-id="42e49-158">Корневые узлы обычно получаются из метода <a href="iinkanalyzer-getrootnode.md"><strong>метода иинканализер:: жетрутноде</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="42e49-158">Root nodes are generally obtained from the <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode Method</strong></a> method.</span></span><br/> <span data-ttu-id="42e49-159">Корневой узел может содержать следующие типы дочерних элементов:</span><span class="sxs-lookup"><span data-stu-id="42e49-159">A root node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="42e49-160">Любое количество узлов подсказок анализа.</span><span class="sxs-lookup"><span data-stu-id="42e49-160">Any number of analysis hint nodes.</span></span></li>
<li><span data-ttu-id="42e49-161">Любое число настраиваемых узлов распознавателя.</span><span class="sxs-lookup"><span data-stu-id="42e49-161">Any number of custom recognizer nodes.</span></span></li>
<li><span data-ttu-id="42e49-162">Любое количество узлов образа.</span><span class="sxs-lookup"><span data-stu-id="42e49-162">Any number of image nodes.</span></span></li>
<li><span data-ttu-id="42e49-163">Любое количество узлов рисования рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="42e49-163">Any number of ink drawing nodes.</span></span></li>
<li><span data-ttu-id="42e49-164">Любое количество узлов области записи.</span><span class="sxs-lookup"><span data-stu-id="42e49-164">Any number of writing region nodes.</span></span></li>
<li><span data-ttu-id="42e49-165">Любое количество неклассифицированных узлов рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="42e49-165">Any number of unclassified ink nodes.</span></span></li>
<li><span data-ttu-id="42e49-166">Любое количество узлов с неизвестным значением <strong>идентификатора GUID</strong> .</span><span class="sxs-lookup"><span data-stu-id="42e49-166">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <span data-ttu-id="42e49-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(текстворд)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TextWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-168">Представляет узел для двумерного региона, в котором в документе может находиться любой нерукописный текст.</span><span class="sxs-lookup"><span data-stu-id="42e49-168">Represents a node for the two-dimensional region where any non-ink text can exist in the document.</span></span><br/> <span data-ttu-id="42e49-169"><a href="iinkanalyzer.md"><strong>Иинканализер</strong></a> не создает узлы текстовых слов.</span><span class="sxs-lookup"><span data-stu-id="42e49-169">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce text word nodes.</span></span> <span data-ttu-id="42e49-170">Используйте <a href="icontextnode-createsubnode.md"><strong>иконтекстноде:: креатесубноде</strong></a> , чтобы добавить текстовый узел Word в дерево узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="42e49-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add a text word node to the context node tree.</span></span> <span data-ttu-id="42e49-171">Затем <strong>иинканализер</strong> использует регионы, определенные узлом текстового слова, чтобы определить, закомментировать ли рукописный ввод нерукописный текст.</span><span class="sxs-lookup"><span data-stu-id="42e49-171">The <strong>IInkAnalyzer</strong> then uses the regions defined by the text word node to determine if any ink annotates the non-ink text.</span></span><br/> <span data-ttu-id="42e49-172">Будущие распознаватели могут использовать область, определенную узлом текстового слова, чтобы определить, какие примечания рукописного ввода не являются текстовыми.</span><span class="sxs-lookup"><span data-stu-id="42e49-172">Future recognizers may use the region defined by a text word node to determine if any ink annotates the non-ink word.</span></span><br/> <span data-ttu-id="42e49-173">Узел текстового слова не может содержать дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="42e49-173">A text word node cannot have any child elements</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <span data-ttu-id="42e49-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(унклассифиединк)</dt> </span><span class="sxs-lookup"><span data-stu-id="42e49-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="42e49-175">Представляет узел для всех штрихов, которые еще не классифицированы или не распознаны.</span><span class="sxs-lookup"><span data-stu-id="42e49-175">Represents a node for any strokes that have not yet been classified or recognized.</span></span><br/> <span data-ttu-id="42e49-176">Неклассифицированный узел рукописного ввода не может иметь дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="42e49-176">An unclassified ink node cannot have any child elements.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="42e49-177">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42e49-177">Remarks</span></span>

<span data-ttu-id="42e49-178">Дополнительные сведения о различных типах узлов контекста см. в разделе [Общие сведения об анализе рукописного текста](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="42e49-178">For more information about the different context node types, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42e49-179">Требования</span><span class="sxs-lookup"><span data-stu-id="42e49-179">Requirements</span></span>



| <span data-ttu-id="42e49-180">Требование</span><span class="sxs-lookup"><span data-stu-id="42e49-180">Requirement</span></span> | <span data-ttu-id="42e49-181">Значение</span><span class="sxs-lookup"><span data-stu-id="42e49-181">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42e49-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42e49-182">Minimum supported client</span></span><br/> | <span data-ttu-id="42e49-183">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="42e49-183">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="42e49-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42e49-184">Minimum supported server</span></span><br/> | <span data-ttu-id="42e49-185">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="42e49-185">None supported</span></span><br/>                                                           |
| <span data-ttu-id="42e49-186">Header</span><span class="sxs-lookup"><span data-stu-id="42e49-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="42e49-187"><dt>Иагуид. h</dt></span><span class="sxs-lookup"><span data-stu-id="42e49-187"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e49-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42e49-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e49-189">**Иконтекстноде:: Креатепартиаллипопулатедсубноде**</span><span class="sxs-lookup"><span data-stu-id="42e49-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="42e49-190">**Иконтекстноде:: Креатесубноде**</span><span class="sxs-lookup"><span data-stu-id="42e49-190">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="42e49-191">**Иконтекстноде:: GetType**</span><span class="sxs-lookup"><span data-stu-id="42e49-191">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="42e49-192">**Метод Иинканализер:: Креатеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="42e49-192">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="42e49-193">**Метод Иинканализер:: Креатекустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="42e49-193">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="42e49-194">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="42e49-194">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="42e49-195">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="42e49-195">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="42e49-196">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="42e49-196">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="42e49-197">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="42e49-197">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




