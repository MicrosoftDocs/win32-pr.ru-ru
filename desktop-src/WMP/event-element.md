---
title: Элемент EVENT (пакет SDK для WMP)
description: Элемент EVENT определяет поведение или действие, предпринимаемое проигрывателем Windows Media при получении команды сценария, помеченной как событие.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Проигрыватель Windows Media, элемент события
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694584"
---
# <a name="event-element"></a><span data-ttu-id="7f78d-104">Элемент EVENT</span><span class="sxs-lookup"><span data-stu-id="7f78d-104">EVENT Element</span></span>

<span data-ttu-id="7f78d-105">Элемент **event** определяет поведение или действие, предпринимаемое проигрывателем Windows Media при получении команды сценария, помеченной как событие.</span><span class="sxs-lookup"><span data-stu-id="7f78d-105">The **EVENT** element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a><span data-ttu-id="7f78d-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7f78d-106">Attributes</span></span>

<span data-ttu-id="7f78d-107">**Имя** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7f78d-107">**NAME** (required)</span></span>

<span data-ttu-id="7f78d-108">Имя события.</span><span class="sxs-lookup"><span data-stu-id="7f78d-108">The name of the event.</span></span>

<span data-ttu-id="7f78d-109">**Вхендоне** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7f78d-109">**WHENDONE** (required)</span></span>

<span data-ttu-id="7f78d-110">Значение, определяющее проигрыватель Windows Media после воспроизведения упоминаемого содержимого.</span><span class="sxs-lookup"><span data-stu-id="7f78d-110">A value that defines what Windows Media Player does after playing the referenced content.</span></span>

<span data-ttu-id="7f78d-111">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="7f78d-111">The following values are possible.</span></span>



| <span data-ttu-id="7f78d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7f78d-112">Value</span></span>  | <span data-ttu-id="7f78d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7f78d-113">Description</span></span>                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f78d-114">RESUME</span><span class="sxs-lookup"><span data-stu-id="7f78d-114">RESUME</span></span> | <span data-ttu-id="7f78d-115">Текущая запись (клип, прерванный событием) возобновляет воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="7f78d-115">The current entry (the clip interrupted by the event) resumes playing.</span></span> <span data-ttu-id="7f78d-116">Если содержимое хранится, оно возобновляется в том же месте, где оно было остановлено. Если содержимое является широковещательным, оно возобновляется в текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="7f78d-116">If the content is stored content, it resumes at the same point where it stopped; if the content is broadcast, it resumes at the current position.</span></span>        |
| <span data-ttu-id="7f78d-117">NEXT</span><span class="sxs-lookup"><span data-stu-id="7f78d-117">NEXT</span></span>   | <span data-ttu-id="7f78d-118">Следующий элемент **entry** играет роль, если событие не произошло и проигрыватель Windows Media достиг конца текущего клипа.</span><span class="sxs-lookup"><span data-stu-id="7f78d-118">The next **ENTRY** element plays as if the event had not occurred and Windows Media Player had reached the end of the current clip.</span></span>                                                                                             |
| <span data-ttu-id="7f78d-119">BREAK</span><span class="sxs-lookup"><span data-stu-id="7f78d-119">BREAK</span></span>  | <span data-ttu-id="7f78d-120">Если текущая запись находится в цикле **повтора** , цикл завершается, как если бы число повторов было завершено.</span><span class="sxs-lookup"><span data-stu-id="7f78d-120">If the current entry is within a **REPEAT** loop, the loop terminates as if the repeat count had been completed.</span></span> <span data-ttu-id="7f78d-121">В противном случае проигрыватель Windows Media переходит к концу списка воспроизведения, как будто последняя запись была выполнена как обычно.</span><span class="sxs-lookup"><span data-stu-id="7f78d-121">Otherwise, Windows Media Player jumps to the end of the playlist as if the final entry had completed as usual.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="7f78d-122">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7f78d-122">Parent/Child Elements</span></span>



| <span data-ttu-id="7f78d-123">Иерархия</span><span class="sxs-lookup"><span data-stu-id="7f78d-123">Hierarchy</span></span>       | <span data-ttu-id="7f78d-124">Элементы</span><span class="sxs-lookup"><span data-stu-id="7f78d-124">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="7f78d-125">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7f78d-125">Parent elements</span></span> | <span data-ttu-id="7f78d-126">**ASX**</span><span class="sxs-lookup"><span data-stu-id="7f78d-126">**ASX**</span></span>                 |
| <span data-ttu-id="7f78d-127">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7f78d-127">Child elements</span></span>  | <span data-ttu-id="7f78d-128">**запись**, **ентриреф**</span><span class="sxs-lookup"><span data-stu-id="7f78d-128">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f78d-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f78d-129">Remarks</span></span>

<span data-ttu-id="7f78d-130">Этот элемент определяет поведение или действие, предпринимаемое проигрывателем Windows Media при получении команды сценария, помеченной как событие.</span><span class="sxs-lookup"><span data-stu-id="7f78d-130">This element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span> <span data-ttu-id="7f78d-131">Событие — это конкретный тип команды сценария, внедренной в поток, отправленный проигрывателю Windows Media, который состоит из двойной строки.</span><span class="sxs-lookup"><span data-stu-id="7f78d-131">An event is a particular type of script command embedded in a stream sent to Windows Media Player that consists of a double string.</span></span> <span data-ttu-id="7f78d-132">Первая строка является словом Event, а вторая — именем события.</span><span class="sxs-lookup"><span data-stu-id="7f78d-132">The first string is the word "event", and the second string is the event name.</span></span> <span data-ttu-id="7f78d-133">Имя события во второй строке должно совпадать с именем события, определенным в метафайле.</span><span class="sxs-lookup"><span data-stu-id="7f78d-133">The event name in the second string must match the event name defined in the metafile.</span></span> <span data-ttu-id="7f78d-134">(В совпадении регистр не учитывается.) События могут отправляться проигрывателю Windows Media, получающему поток в режиме реального времени, или могут быть сохранены в формате ASF, WMA или WMV, который доставляется в виде одноадресного потока по требованию.</span><span class="sxs-lookup"><span data-stu-id="7f78d-134">(The match is not case-sensitive.) Events can be sent to Windows Media Player receiving a real-time stream, or can be saved in an .asf, .wma, or .wmv file that gets delivered as an on-demand unicast stream.</span></span> <span data-ttu-id="7f78d-135">Когда проигрыватель Windows Media получает команду сценария, он обрабатывает событие в соответствии с определением в элементе **event** .</span><span class="sxs-lookup"><span data-stu-id="7f78d-135">When Windows Media Player receives the script command, it processes the event as defined by the **EVENT** element.</span></span>

<span data-ttu-id="7f78d-136">Этот элемент определяет область элементов **entry** или **ентриреф** , которые обрабатываются каждый раз, когда проигрыватель Windows Media получает команду сценария с именованным событием.</span><span class="sxs-lookup"><span data-stu-id="7f78d-136">This element defines a scope of **ENTRY** or **ENTRYREF** elements that are processed whenever Windows Media Player receives the script command with the named event.</span></span> <span data-ttu-id="7f78d-137">**Ентриреф** может быть URL-адресом, который указывает на страницу ASP.</span><span class="sxs-lookup"><span data-stu-id="7f78d-137">The **ENTRYREF** can be a URL that points to an ASP page.</span></span> <span data-ttu-id="7f78d-138">С помощью этого элемента можно указать поведение переключения потоков практически в реальном времени, в отличие от предварительно созданных изменений потока с помощью ссылок на другие фрагменты содержимого или метафайлы Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f78d-138">With this element, you can specify a behavior for stream switching in near real time, as opposed to pre-authored stream changes using references to other pieces of content or Windows Media metafiles.</span></span>

<span data-ttu-id="7f78d-139">При использовании страниц ASP для создания списков воспроизведения необходимо указать значение для *ответа*. Свойство **ContentType** и *ответ*. Свойство **Expires** на странице ASP из-за проблем с задержкой проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f78d-139">When you use ASP pages to generate playlists, you must specify a value for the *Response*.**ContentType** property and the *Response*.**expires** property in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="7f78d-140">*Ответ*. **ContentType** должен быть допустимым расширением имени файла для метафайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f78d-140">The *Response*.**ContentType** must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="7f78d-141">Допустимые типы: ASF, ASX, WMA, мастика, WMV и ввкс.</span><span class="sxs-lookup"><span data-stu-id="7f78d-141">Valid types include .asf, .asx, .wma, .wax, .wmv, and .wvx.</span></span>

<span data-ttu-id="7f78d-142">Дополнительные сведения об использовании объекта **Response** в ASP см. в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="7f78d-142">See the Platform SDK for details about using the **Response** object in ASP.</span></span>

<span data-ttu-id="7f78d-143">Этот элемент может находиться в любом месте элемента **ASX** .</span><span class="sxs-lookup"><span data-stu-id="7f78d-143">This element can appear anywhere within the **ASX** element.</span></span> <span data-ttu-id="7f78d-144">Если несколько элементов **событий** в элементе **ASX** имеют одинаковые значения для атрибутов **имени** , проигрыватель Windows Media использует первое вхождение в элементе **ASX** и игнорирует все остальные.</span><span class="sxs-lookup"><span data-stu-id="7f78d-144">If multiple **EVENT** elements within an **ASX** element have identical values for their **NAME** attributes, Windows Media Player uses the first occurrence within the **ASX** element, and ignores all others.</span></span> <span data-ttu-id="7f78d-145">Если у элементов **события** есть разные атрибуты **имени** , их порядок в элементе **ASX** не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="7f78d-145">When **EVENT** elements have distinct **NAME** attributes, their order within the **ASX** element does not matter.</span></span>

<span data-ttu-id="7f78d-146">Проигрыватель Windows Media отклоняет события, получаемые им при обработке другого события.</span><span class="sxs-lookup"><span data-stu-id="7f78d-146">Windows Media Player discards events it receives while processing another event.</span></span> <span data-ttu-id="7f78d-147">Вложение событий не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7f78d-147">Nesting of events is not supported.</span></span> <span data-ttu-id="7f78d-148">Когда проигрыватель Windows Media находится в режиме предварительного просмотра, содержимое события не ограничивается элементом **превиевдуратион** ; Полная длина содержимого события может воспроизводиться, даже если срок действия предварительной версии элемента активной **записи** истекает до окончания события.</span><span class="sxs-lookup"><span data-stu-id="7f78d-148">When Windows Media Player is in preview mode, event content is not constrained by the **PREVIEWDURATION** element; the full length of event content can play even if the preview duration for the active **ENTRY** element expires prior to the end of the event.</span></span>

## <a name="examples"></a><span data-ttu-id="7f78d-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="7f78d-149">Examples</span></span>

<span data-ttu-id="7f78d-150">В этом примере, когда проигрыватель Windows Media получает событие команды сценария и строку команды "Адлинк" в потоковой передаче, он выполняет поиск в списке воспроизведения с **EVENTNAME** "адлинк".</span><span class="sxs-lookup"><span data-stu-id="7f78d-150">In this example, when Windows Media Player receives the script command EVENT and command string "Adlink" in the streaming media it is rendering, it searches the playlist for an **EVENTNAME** "Adlink".</span></span> <span data-ttu-id="7f78d-151">Проигрыватель Windows Media переключается из потока, который подготовится к просмотру, и воспроизводит содержимое, указанное в **событии**" https://example.microsoft.com/adlink.htm ".</span><span class="sxs-lookup"><span data-stu-id="7f78d-151">Windows Media Player switches from the stream it is rendering and plays the content referenced in the **EVENT**, "https://example.microsoft.com/adlink.htm".</span></span>

<span data-ttu-id="7f78d-152">Атрибуту **записи** **клиентскип** присваивается значение No, чтобы предотвратить пропуск клипа **события** .</span><span class="sxs-lookup"><span data-stu-id="7f78d-152">**ENTRY** attribute **CLIENTSKIP** is set to NO to prevent the **EVENT** clip from being skipped.</span></span> <span data-ttu-id="7f78d-153">Его необходимо воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="7f78d-153">It must be played.</span></span>

<span data-ttu-id="7f78d-154">Сценарий `WHENDONE="RESUME"` указывает проигрывателю Windows Media возобновить воспроизведение предыдущего носителя, с которого он переключился, как только адлинк. ASF завершит работу.</span><span class="sxs-lookup"><span data-stu-id="7f78d-154">The script `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous media it switched from as soon as Adlink.asf is finished.</span></span>


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="7f78d-155">Требования</span><span class="sxs-lookup"><span data-stu-id="7f78d-155">Requirements</span></span>



| <span data-ttu-id="7f78d-156">Требование</span><span class="sxs-lookup"><span data-stu-id="7f78d-156">Requirement</span></span> | <span data-ttu-id="7f78d-157">Значение</span><span class="sxs-lookup"><span data-stu-id="7f78d-157">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7f78d-158">Версия</span><span class="sxs-lookup"><span data-stu-id="7f78d-158">Version</span></span><br/> | <span data-ttu-id="7f78d-159">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="7f78d-159">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f78d-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f78d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f78d-161">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7f78d-161">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7f78d-162">**Справочник по метафайлу Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7f78d-162">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="7f78d-163">**Объектная модель проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7f78d-163">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





