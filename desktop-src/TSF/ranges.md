---
title: Диапазоны
description: Диапазоны
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Платформа текстовых служб (TSF), диапазоны
- TSF (платформа текстовых служб), диапазоны
- текстовые службы, диапазоны
- Приложения с поддержкой TSF, диапазоны
- ranges
- Платформа текстовых служб (TSF), привязки
- TSF (платформа текстовых служб), привязки
- текстовые службы, привязки
- Приложения с поддержкой TSF, привязки
- Привязки
- Платформа текстовых служб (TSF), клоны
- TSF (платформа текстовых служб), клоны
- текстовые службы, клоны
- Приложения с поддержкой TSF, клоны
- клонов
- Платформа текстовых служб (TSF), резервные копии
- TSF (платформа текстовых служб), резервные копии
- службы текстового ввода, резервные копии
- Приложения с поддержкой TSF, резервные копии
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986816"
---
# <a name="ranges"></a><span data-ttu-id="61337-123">Диапазоны</span><span class="sxs-lookup"><span data-stu-id="61337-123">Ranges</span></span>

## <a name="anchors"></a><span data-ttu-id="61337-124">Привязки</span><span class="sxs-lookup"><span data-stu-id="61337-124">Anchors</span></span>

<span data-ttu-id="61337-125">Диапазон отделяется двумя *привязками*, начальной привязкой и конечной привязкой.</span><span class="sxs-lookup"><span data-stu-id="61337-125">A range is delimited by two *anchors*, a start anchor and an end anchor.</span></span> <span data-ttu-id="61337-126">В мнимой области существует привязка между двумя символами.</span><span class="sxs-lookup"><span data-stu-id="61337-126">An anchor exists in an imaginary slot between two characters.</span></span> <span data-ttu-id="61337-127">Начальная привязка относится к тексту, расположенному после привязки, а конечная привязка относится к тексту, предшествующему привязке.</span><span class="sxs-lookup"><span data-stu-id="61337-127">The start anchor relates to text that follows the anchor and the end anchor relates to text that precedes the anchor.</span></span> <span data-ttu-id="61337-128">Начальная и конечная привязки могут находиться в одном и том же месте.</span><span class="sxs-lookup"><span data-stu-id="61337-128">Both the start and end anchors can exist in the same location.</span></span> <span data-ttu-id="61337-129">В этом случае диапазон имеет нулевую длину.</span><span class="sxs-lookup"><span data-stu-id="61337-129">In this case, the range has zero length.</span></span>

<span data-ttu-id="61337-130">Например, начните со следующего текста:</span><span class="sxs-lookup"><span data-stu-id="61337-130">For example, start with the following text:</span></span>


```C++
This is text.
```



<span data-ttu-id="61337-131">Теперь примените к этому тексту диапазон, содержащий как начальную, так и конечную привязки в позиции 0.</span><span class="sxs-lookup"><span data-stu-id="61337-131">Now apply a range to this text with both the start and end anchors at position 0.</span></span> <span data-ttu-id="61337-132">Он визуально представляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61337-132">It is visually represented as:</span></span>


```C++
<anchor></anchor>This is text.
```



<span data-ttu-id="61337-133">Привязки не занимают пробелов внутри самого текста.</span><span class="sxs-lookup"><span data-stu-id="61337-133">The anchors do not take up any space within the text itself.</span></span> <span data-ttu-id="61337-134">Это диапазон нулевой длины, и его текст пуст.</span><span class="sxs-lookup"><span data-stu-id="61337-134">This is a zero-length range and its text is empty.</span></span>

<span data-ttu-id="61337-135">Теперь сдвигаются конечную точку привязки + 3 позиции.</span><span class="sxs-lookup"><span data-stu-id="61337-135">Now shift the end anchor +3 positions.</span></span> <span data-ttu-id="61337-136">Он визуально представляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61337-136">It is visually represented as:</span></span>


```C++
<anchor>Thi</anchor>s is text.
```



<span data-ttu-id="61337-137">Начальная привязка располагается непосредственно перед символом в позиции 0, а конечная привязка размещается сразу после символа в позиции 3, так как конечная привязка перемещена в правый 3 места.</span><span class="sxs-lookup"><span data-stu-id="61337-137">The start anchor is positioned just before the character in position 0 and the end anchor is positioned just after the character in position 3 because the end anchor moved to the right 3 places.</span></span> <span data-ttu-id="61337-138">Теперь диапазон текста — «эт».</span><span class="sxs-lookup"><span data-stu-id="61337-138">The range of text is now "Thi".</span></span>

<span data-ttu-id="61337-139">Кроме того, нельзя выполнить начальную привязку, чтобы следовать конечной точке, а конечная привязка не может предшествовать начальной точке привязки.</span><span class="sxs-lookup"><span data-stu-id="61337-139">Additionally, the start anchor cannot be made to follow the end anchor and the end anchor cannot be made to precede the start anchor.</span></span>

## <a name="anchor-gravity"></a><span data-ttu-id="61337-140">Сила притяжения привязки</span><span class="sxs-lookup"><span data-stu-id="61337-140">Anchor Gravity</span></span>

<span data-ttu-id="61337-141">Каждая привязка имеет параметр " *сила притяжения* ", который определяет, как привязка реагирует при вставке текста в текстовый поток в позиции привязки.</span><span class="sxs-lookup"><span data-stu-id="61337-141">Each anchor has a *gravity* setting that determines how the anchor responds when text is inserted into the text stream at the anchor position.</span></span> <span data-ttu-id="61337-142">При вставке в позицию привязки в позиции привязки необходимо выполнить корректировку.</span><span class="sxs-lookup"><span data-stu-id="61337-142">When an insertion is made at the position of an anchor, an adjustment must be made in the position of the anchor.</span></span> <span data-ttu-id="61337-143">Сила притяжения определяет, как выполняется корректировка положения привязки.</span><span class="sxs-lookup"><span data-stu-id="61337-143">The gravity determines how this anchor position adjustment is made.</span></span>

<span data-ttu-id="61337-144">Пример:</span><span class="sxs-lookup"><span data-stu-id="61337-144">For example:</span></span>


```C++
It is <anchor></anchor>cold today.
```



<span data-ttu-id="61337-145">Если слово «очень» вставляется в позиции диапазона, начальная привязка может располагаться до или после вставленного слова:</span><span class="sxs-lookup"><span data-stu-id="61337-145">If the word "very " is inserted at the range position, the start anchor can be positioned either before or after the inserted word:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="61337-146">\- - или -</span><span class="sxs-lookup"><span data-stu-id="61337-146">\- Or -</span></span>


```C++
It is very <anchor></anchor>cold today.
```



<span data-ttu-id="61337-147">Сила притяжения привязок определяет способ изменения положения привязки при вставке в позицию.</span><span class="sxs-lookup"><span data-stu-id="61337-147">The anchor gravity specifies how the anchor is repositioned when an insertion is made at its position.</span></span> <span data-ttu-id="61337-148">Сила притяжения может быть либо *обратно* , либо *вперед*.</span><span class="sxs-lookup"><span data-stu-id="61337-148">The gravity can be either *backward* or *forward*.</span></span>

<span data-ttu-id="61337-149">Если у привязки есть обратная сила притяжения, то при вставке привязка перемещается в обратном направлении относительно точки вставки, чтобы вставленный текст находился после привязки:</span><span class="sxs-lookup"><span data-stu-id="61337-149">If the anchor has backward gravity, the anchor moves backward, relative to the insertion point, on insertion so that the inserted text follows the anchor:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="61337-150">Если у привязки есть прямая сила притяжения, привязка перемещается вперед (относительно точки вставки) к вставке, чтобы вставленный текст предшествовал привязке:</span><span class="sxs-lookup"><span data-stu-id="61337-150">If the anchor has forward gravity, the anchor moves forward (relative to the insertion point) on insertion so that the inserted text precedes the anchor:</span></span>


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a><span data-ttu-id="61337-151">Клоны и резервные копии</span><span class="sxs-lookup"><span data-stu-id="61337-151">Clones and Backups</span></span>

<span data-ttu-id="61337-152">Существует два способа создания "копии" объекта диапазона.</span><span class="sxs-lookup"><span data-stu-id="61337-152">There are two ways to make a "copy" of a range object.</span></span> <span data-ttu-id="61337-153">Первый — создать *клон* диапазона с помощью [Итфранже:: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span><span class="sxs-lookup"><span data-stu-id="61337-153">The first is to make a *clone* of the range using [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span></span> <span data-ttu-id="61337-154">Второй — создать *резервную копию* диапазона с помощью [ITfContext:: креатеранжебаккуп](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span><span class="sxs-lookup"><span data-stu-id="61337-154">The second is to make a *backup* of the range using [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span></span>

<span data-ttu-id="61337-155">Клон — это копия диапазона, в который не входят статические данные.</span><span class="sxs-lookup"><span data-stu-id="61337-155">A clone is a copy of a range that does not include static data.</span></span> <span data-ttu-id="61337-156">Привязки диапазона копируются, но клон по-прежнему охватывает диапазон текста внутри контекста.</span><span class="sxs-lookup"><span data-stu-id="61337-156">The anchors of the range are copied, but the clone still covers a range of text within the context.</span></span> <span data-ttu-id="61337-157">Клон — это объект Range во всех отношениях.</span><span class="sxs-lookup"><span data-stu-id="61337-157">A clone is a range object in all respects.</span></span> <span data-ttu-id="61337-158">Это означает, что текст и свойства клонированного диапазона являются динамическими и будут изменяться при изменении текста и/или свойств диапазона, охватываемого клоном.</span><span class="sxs-lookup"><span data-stu-id="61337-158">This means that the text and properties for a cloned range are dynamic and will change if the text and/or properties of the range covered by the clone changes.</span></span>

<span data-ttu-id="61337-159">В резервной копии хранится текст и свойства диапазона во время создания резервной копии в виде статических данных.</span><span class="sxs-lookup"><span data-stu-id="61337-159">A backup stores the text and properties of a range at the time the backup is made as static data.</span></span> <span data-ttu-id="61337-160">Резервная копия также создает точную копию исходного диапазона, чтобы можно было контролировать изменения размера и расположения исходного диапазона.</span><span class="sxs-lookup"><span data-stu-id="61337-160">A backup also clones the original range so that changes to the size and position of the original range can be tracked.</span></span> <span data-ttu-id="61337-161">Это означает, что текст и свойства для диапазона резервного копирования являются статическими и не изменяются при изменении текста и/или свойств диапазона, охватываемого резервной копией.</span><span class="sxs-lookup"><span data-stu-id="61337-161">This means that the text and properties for a backed up range are static and do not change if the text and/or properties of the range covered by the backup changes.</span></span>

<span data-ttu-id="61337-162">Например, следующий диапазон (Пранже) в контексте:</span><span class="sxs-lookup"><span data-stu-id="61337-162">For example, the following range (pRange) within the context:</span></span>


```C++
"This is some <pRange>text</pRange>."
```



<span data-ttu-id="61337-163">Теперь создайте клон и резервную копию этого диапазона:</span><span class="sxs-lookup"><span data-stu-id="61337-163">Now make a clone and a backup of this range:</span></span>


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



<span data-ttu-id="61337-164">Теперь объекты содержат следующее:</span><span class="sxs-lookup"><span data-stu-id="61337-164">Now, the objects contain the following:</span></span>


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="61337-165">Теперь измените текст Пранже:</span><span class="sxs-lookup"><span data-stu-id="61337-165">Now change the text of pRange:</span></span>


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



<span data-ttu-id="61337-166">Теперь объекты содержат следующее:</span><span class="sxs-lookup"><span data-stu-id="61337-166">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="61337-167">Установка текста привела к изменению текста в контексте.</span><span class="sxs-lookup"><span data-stu-id="61337-167">Setting the text caused the text within the context to change.</span></span> <span data-ttu-id="61337-168">Это также привело к изменению конечной привязки Пранже и Пклоне.</span><span class="sxs-lookup"><span data-stu-id="61337-168">It also caused the end anchor of pRange and pClone to change.</span></span> <span data-ttu-id="61337-169">Пклоне теперь содержит "другие слова", так как текст изменился в диапазоне, и эти изменения будут записаны по всем диапазонам.</span><span class="sxs-lookup"><span data-stu-id="61337-169">pClone now contains "other words" because the text changed within the range and these changes are tracked by all ranges.</span></span> <span data-ttu-id="61337-170">При изменении текста, охваченного Пранже и Пклоне, текст Пклоне также изменился.</span><span class="sxs-lookup"><span data-stu-id="61337-170">When the text covered by both pRange and pClone changed, the text of pClone changed as well.</span></span>

<span data-ttu-id="61337-171">Текст в Пбаккуп не изменился с исходного Пранже, поскольку данные (текст и свойства) в резервной копии не связаны с контекстом и хранятся отдельно.</span><span class="sxs-lookup"><span data-stu-id="61337-171">The text in pBackup has not changed from the original pRange because the data (text and properties) in the backup is unrelated to the context and is stored separately.</span></span> <span data-ttu-id="61337-172">Клон, содержащийся в резервной копии, фактически изменяется, но данные являются статическими.</span><span class="sxs-lookup"><span data-stu-id="61337-172">The clone contained within the backup does actually change, but the data is static.</span></span>

<span data-ttu-id="61337-173">При восстановлении резервной копии можно полностью применить резервную копию к клону в резервной копии или к другому диапазону.</span><span class="sxs-lookup"><span data-stu-id="61337-173">When restoring a backup, the backup can be applied to the clone within the backup or to a different range entirely.</span></span> <span data-ttu-id="61337-174">Чтобы применить резервную копию к клону в резервной копии, передайте **значение NULL** в [итфранжебаккуп:: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="61337-174">To apply the backup to the clone within the backup, pass **NULL** to [ITfRangeBackup::Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) as shown in the following code example:</span></span>


```C++
pBackup->Restore(ec, NULL);
```



<span data-ttu-id="61337-175">Теперь объекты содержат следующее:</span><span class="sxs-lookup"><span data-stu-id="61337-175">Now, the objects contain the following:</span></span>


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="61337-176">Чтобы восстановить резервную копию в другой диапазон, передайте указатель на объект Range при вызове **итфранжебаккуп:: Restore**.</span><span class="sxs-lookup"><span data-stu-id="61337-176">To restore the backup to a different range, pass a pointer to the range object when calling **ITfRangeBackup::Restore**.</span></span> <span data-ttu-id="61337-177">Заархивированный текст и свойства будут применены к новому диапазону.</span><span class="sxs-lookup"><span data-stu-id="61337-177">The backed up text and properties will be applied to the new range.</span></span> <span data-ttu-id="61337-178">Например, при использовании приведенного выше примера для вызова **RESTORE** пранже будет изменен, чтобы продемонстрировать это:</span><span class="sxs-lookup"><span data-stu-id="61337-178">For example, using the example above prior to the **Restore** call, pRange will be modified to demonstrate this:</span></span>


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



<span data-ttu-id="61337-179">Теперь объекты содержат следующее:</span><span class="sxs-lookup"><span data-stu-id="61337-179">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="61337-180">Когда конечная привязка Пранже была смещена влево на две позиции, конечная привязка Пклоне не изменилась.</span><span class="sxs-lookup"><span data-stu-id="61337-180">When the end anchor of pRange was shifted to the left two places, the end anchor of pClone did not change.</span></span>

<span data-ttu-id="61337-181">Теперь восстановите резервную копию с помощью Пранже, как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="61337-181">Now restore the backup using pRange with the following code example:</span></span>


```C++
pBackup->Restore(ec, pRange);
```



<span data-ttu-id="61337-182">Теперь объекты содержат следующее:</span><span class="sxs-lookup"><span data-stu-id="61337-182">Now, the objects contain the following:</span></span>


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



<span data-ttu-id="61337-183">Текст, покрываемый Пранже, был заменен на "Text", часть текста, покрываемая Пклоне, изменилась, а Пбаккуп изменяется в соответствии с Пранже.</span><span class="sxs-lookup"><span data-stu-id="61337-183">The text covered by pRange has been replaced with "text", a portion of the text covered by pClone has changed, and pBackup changes to match pRange.</span></span>

 

 




