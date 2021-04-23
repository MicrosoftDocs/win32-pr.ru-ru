---
title: Справочник по MIDI
description: Справочник по MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Мультимедиа Windows, цифровой интерфейс музыкальных инструментов (MIDI)
- мультимедиа, цифровой интерфейс музыкальных инструментов (MIDI)
- мультимедийный звук, цифровой интерфейс музыкальных инструментов (MIDI)
- аудио, цифровой интерфейс музыкальных инструментов (MIDI)
- Windows мультимедиа, Справочник MIDI
- мультимедиа, Справочник MIDI
- мультимедиа аудио, Справочник MIDI
- аудио, Справочник MIDI
- Цифровой интерфейс MIDI, справочные материалы
- MIDI (цифровой интерфейс музыкального инструмента), Справочник
- Справочник по MIDI, сведения
- Справочник по MIDI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412908"
---
# <a name="midi-reference"></a><span data-ttu-id="041a7-115">Справочник по MIDI</span><span class="sxs-lookup"><span data-stu-id="041a7-115">MIDI Reference</span></span>

<span data-ttu-id="041a7-116">В этом разделе описываются функции, макросы, сообщения и структуры, связанные с цифровым интерфейсом MIDI.</span><span class="sxs-lookup"><span data-stu-id="041a7-116">This section describes the functions, macros, messages, and structures associated with the Musical Instrument Digital Interface (MIDI).</span></span> <span data-ttu-id="041a7-117">Эти элементы группируются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="041a7-117">These elements are grouped as follows.</span></span>

## <a name="allocating-and-managing-buffers"></a><span data-ttu-id="041a7-118">Выделение буферов и управление ими</span><span class="sxs-lookup"><span data-stu-id="041a7-118">Allocating and Managing Buffers</span></span>

-   [<span data-ttu-id="041a7-119">**мидихдр**</span><span class="sxs-lookup"><span data-stu-id="041a7-119">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [<span data-ttu-id="041a7-120">**мидиинаддбуффер**</span><span class="sxs-lookup"><span data-stu-id="041a7-120">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [<span data-ttu-id="041a7-121">**мидиинпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="041a7-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [<span data-ttu-id="041a7-122">**мидиинунпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="041a7-122">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [<span data-ttu-id="041a7-123">**мидиаутпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="041a7-123">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [<span data-ttu-id="041a7-124">**мидиаутунпрепарехеадер**</span><span class="sxs-lookup"><span data-stu-id="041a7-124">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a><span data-ttu-id="041a7-125">Функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="041a7-125">Callback Functions</span></span>

-   <span data-ttu-id="041a7-126">[**мидиинпрок**](/previous-versions//dd798460(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="041a7-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span></span>
-   <span data-ttu-id="041a7-127">[**мидиаутпрок**](/previous-versions//dd798478(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="041a7-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="041a7-128">Возможности устройства</span><span class="sxs-lookup"><span data-stu-id="041a7-128">Device Capabilities</span></span>

-   [<span data-ttu-id="041a7-129">**мидиинкапс**</span><span class="sxs-lookup"><span data-stu-id="041a7-129">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [<span data-ttu-id="041a7-130">**мидиинжетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="041a7-130">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [<span data-ttu-id="041a7-131">**мидиинжетид**</span><span class="sxs-lookup"><span data-stu-id="041a7-131">**midiInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [<span data-ttu-id="041a7-132">**мидиинжетнумдевс**</span><span class="sxs-lookup"><span data-stu-id="041a7-132">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [<span data-ttu-id="041a7-133">**мидиауткапс**</span><span class="sxs-lookup"><span data-stu-id="041a7-133">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [<span data-ttu-id="041a7-134">**мидиаутжетдевкапс**</span><span class="sxs-lookup"><span data-stu-id="041a7-134">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [<span data-ttu-id="041a7-135">**мидиаутжетид**</span><span class="sxs-lookup"><span data-stu-id="041a7-135">**midiOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [<span data-ttu-id="041a7-136">**мидиаутжетнумдевс**</span><span class="sxs-lookup"><span data-stu-id="041a7-136">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [<span data-ttu-id="041a7-137">**мидистрмбуффвер**</span><span class="sxs-lookup"><span data-stu-id="041a7-137">**MIDISTRMBUFFVER**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a><span data-ttu-id="041a7-138">Обработка ошибок</span><span class="sxs-lookup"><span data-stu-id="041a7-138">Error Processing</span></span>

-   [<span data-ttu-id="041a7-139">**мидиинжетеррортекст**</span><span class="sxs-lookup"><span data-stu-id="041a7-139">**midiInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [<span data-ttu-id="041a7-140">**мидиаутжетеррортекст**</span><span class="sxs-lookup"><span data-stu-id="041a7-140">**midiOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [<span data-ttu-id="041a7-141">**\_Ошибка MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-141">**MIM\_ERROR**</span></span>](mim-error.md)
-   [<span data-ttu-id="041a7-142">**\_ЛОНЖЕРРОР MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-142">**MIM\_LONGERROR**</span></span>](mim-longerror.md)
-   [<span data-ttu-id="041a7-143">**MM \_ , \_ Ошибка MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-143">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)
-   [<span data-ttu-id="041a7-144">**MM \_ MIM \_ лонжеррор**</span><span class="sxs-lookup"><span data-stu-id="041a7-144">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a><span data-ttu-id="041a7-145">Управление потоками MIDI</span><span class="sxs-lookup"><span data-stu-id="041a7-145">Managing MIDI Streams</span></span>

-   [<span data-ttu-id="041a7-146">**мидистреамклосе**</span><span class="sxs-lookup"><span data-stu-id="041a7-146">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [<span data-ttu-id="041a7-147">**мидистреамопен**</span><span class="sxs-lookup"><span data-stu-id="041a7-147">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [<span data-ttu-id="041a7-148">**мидистреамаут**</span><span class="sxs-lookup"><span data-stu-id="041a7-148">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="041a7-149">**мидистреампаусе**</span><span class="sxs-lookup"><span data-stu-id="041a7-149">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="041a7-150">**мидистреампоситион**</span><span class="sxs-lookup"><span data-stu-id="041a7-150">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [<span data-ttu-id="041a7-151">**мидистреампроперти**</span><span class="sxs-lookup"><span data-stu-id="041a7-151">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [<span data-ttu-id="041a7-152">**мидистреамрестарт**</span><span class="sxs-lookup"><span data-stu-id="041a7-152">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="041a7-153">**мидистреамстоп**</span><span class="sxs-lookup"><span data-stu-id="041a7-153">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a><span data-ttu-id="041a7-154">Открытие и закрытие устройств</span><span class="sxs-lookup"><span data-stu-id="041a7-154">Opening and Closing Devices</span></span>

-   [<span data-ttu-id="041a7-155">**мидиинклосе**</span><span class="sxs-lookup"><span data-stu-id="041a7-155">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [<span data-ttu-id="041a7-156">**мидиинопен**</span><span class="sxs-lookup"><span data-stu-id="041a7-156">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [<span data-ttu-id="041a7-157">**мидиаутклосе**</span><span class="sxs-lookup"><span data-stu-id="041a7-157">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [<span data-ttu-id="041a7-158">**мидиаутопен**</span><span class="sxs-lookup"><span data-stu-id="041a7-158">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [<span data-ttu-id="041a7-159">**\_закрытие MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-159">**MIM\_CLOSE**</span></span>](mim-close.md)
-   [<span data-ttu-id="041a7-160">**\_Запуск MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-160">**MIM\_OPEN**</span></span>](mim-open.md)
-   [<span data-ttu-id="041a7-161">**MM \_ MIM, \_ закрытие**</span><span class="sxs-lookup"><span data-stu-id="041a7-161">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)
-   [<span data-ttu-id="041a7-162">**MM \_ MIM \_ Open**</span><span class="sxs-lookup"><span data-stu-id="041a7-162">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)
-   [<span data-ttu-id="041a7-163">**\_закрытие mm MOM \_**</span><span class="sxs-lookup"><span data-stu-id="041a7-163">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md)
-   [<span data-ttu-id="041a7-164">**\_ \_ открытая MOM mm**</span><span class="sxs-lookup"><span data-stu-id="041a7-164">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)
-   [<span data-ttu-id="041a7-165">**\_закрытие MOM**</span><span class="sxs-lookup"><span data-stu-id="041a7-165">**MOM\_CLOSE**</span></span>](mom-close.md)
-   [<span data-ttu-id="041a7-166">**диспетчер MOM \_ открыт**</span><span class="sxs-lookup"><span data-stu-id="041a7-166">**MOM\_OPEN**</span></span>](mom-open.md)

## <a name="output-devices"></a><span data-ttu-id="041a7-167">Устройства вывода</span><span class="sxs-lookup"><span data-stu-id="041a7-167">Output Devices</span></span>

-   [<span data-ttu-id="041a7-168">кэйаррай</span><span class="sxs-lookup"><span data-stu-id="041a7-168">KEYARRAY</span></span>](keyarray.md)
-   [<span data-ttu-id="041a7-169">**мидиауткачедрумпатчес**</span><span class="sxs-lookup"><span data-stu-id="041a7-169">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [<span data-ttu-id="041a7-170">**мидиауткачепатчес**</span><span class="sxs-lookup"><span data-stu-id="041a7-170">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [<span data-ttu-id="041a7-171">**мидиаутжетволуме**</span><span class="sxs-lookup"><span data-stu-id="041a7-171">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [<span data-ttu-id="041a7-172">**мидиаутсетволуме**</span><span class="sxs-lookup"><span data-stu-id="041a7-172">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [<span data-ttu-id="041a7-173">патчаррай</span><span class="sxs-lookup"><span data-stu-id="041a7-173">PATCHARRAY</span></span>](patcharray.md)

## <a name="playing-a-message-or-messages"></a><span data-ttu-id="041a7-174">Воспроизведение сообщения или сообщений</span><span class="sxs-lookup"><span data-stu-id="041a7-174">Playing a Message or Messages</span></span>

-   [<span data-ttu-id="041a7-175">**МЕВТ \_ евентпарм**</span><span class="sxs-lookup"><span data-stu-id="041a7-175">**MEVT\_EVENTPARM**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [<span data-ttu-id="041a7-176">**МЕВТ \_ EVENTTYPE**</span><span class="sxs-lookup"><span data-stu-id="041a7-176">**MEVT\_EVENTTYPE**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [<span data-ttu-id="041a7-177">**мидиевент**</span><span class="sxs-lookup"><span data-stu-id="041a7-177">**MIDIEVENT**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [<span data-ttu-id="041a7-178">**мидиаутлонгмсг**</span><span class="sxs-lookup"><span data-stu-id="041a7-178">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [<span data-ttu-id="041a7-179">**мидиаутресет**</span><span class="sxs-lookup"><span data-stu-id="041a7-179">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [<span data-ttu-id="041a7-180">**мидиаутшортмсг**</span><span class="sxs-lookup"><span data-stu-id="041a7-180">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [<span data-ttu-id="041a7-181">**мидистреамаут**</span><span class="sxs-lookup"><span data-stu-id="041a7-181">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="041a7-182">**мидистреампаусе**</span><span class="sxs-lookup"><span data-stu-id="041a7-182">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="041a7-183">**мидистреамрестарт**</span><span class="sxs-lookup"><span data-stu-id="041a7-183">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="041a7-184">**мидистреамстоп**</span><span class="sxs-lookup"><span data-stu-id="041a7-184">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [<span data-ttu-id="041a7-185">**MM, \_ MOM \_**</span><span class="sxs-lookup"><span data-stu-id="041a7-185">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)
-   [<span data-ttu-id="041a7-186">**MM \_ MOM \_ поситионкб**</span><span class="sxs-lookup"><span data-stu-id="041a7-186">**MM\_MOM\_POSITIONCB**</span></span>](mm-mom-positioncb.md)
-   [<span data-ttu-id="041a7-187">**MOM \_**</span><span class="sxs-lookup"><span data-stu-id="041a7-187">**MOM\_DONE**</span></span>](mom-done.md)
-   [<span data-ttu-id="041a7-188">**MOM \_ поситионкб**</span><span class="sxs-lookup"><span data-stu-id="041a7-188">**MOM\_POSITIONCB**</span></span>](mom-positioncb.md)

## <a name="recording"></a><span data-ttu-id="041a7-189">Запись</span><span class="sxs-lookup"><span data-stu-id="041a7-189">Recording</span></span>

-   [<span data-ttu-id="041a7-190">**мидиконнект**</span><span class="sxs-lookup"><span data-stu-id="041a7-190">**midiConnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [<span data-ttu-id="041a7-191">**мидидисконнект**</span><span class="sxs-lookup"><span data-stu-id="041a7-191">**midiDisconnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [<span data-ttu-id="041a7-192">**мидиинресет**</span><span class="sxs-lookup"><span data-stu-id="041a7-192">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [<span data-ttu-id="041a7-193">**мидиинстарт**</span><span class="sxs-lookup"><span data-stu-id="041a7-193">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [<span data-ttu-id="041a7-194">**мидиинстоп**</span><span class="sxs-lookup"><span data-stu-id="041a7-194">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [<span data-ttu-id="041a7-195">**мидипроптемпо**</span><span class="sxs-lookup"><span data-stu-id="041a7-195">**MIDIPROPTEMPO**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [<span data-ttu-id="041a7-196">**мидипроптимедив**</span><span class="sxs-lookup"><span data-stu-id="041a7-196">**MIDIPROPTIMEDIV**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [<span data-ttu-id="041a7-197">**\_данные MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-197">**MIM\_DATA**</span></span>](mim-data.md)
-   [<span data-ttu-id="041a7-198">**\_ЛОНГДАТА MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-198">**MIM\_LONGDATA**</span></span>](mim-longdata.md)
-   [<span data-ttu-id="041a7-199">**\_MOREDATA MIM**</span><span class="sxs-lookup"><span data-stu-id="041a7-199">**MIM\_MOREDATA**</span></span>](mim-moredata.md)
-   [<span data-ttu-id="041a7-200">**MM \_ MIM \_ Data**</span><span class="sxs-lookup"><span data-stu-id="041a7-200">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)
-   [<span data-ttu-id="041a7-201">**MM \_ MIM \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="041a7-201">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)
-   [<span data-ttu-id="041a7-202">**MM \_ MIM \_ лонгдата**</span><span class="sxs-lookup"><span data-stu-id="041a7-202">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a><span data-ttu-id="041a7-203">Отправка сообщений на устройства</span><span class="sxs-lookup"><span data-stu-id="041a7-203">Sending Messages to Devices</span></span>

-   [<span data-ttu-id="041a7-204">**мидиинмессаже**</span><span class="sxs-lookup"><span data-stu-id="041a7-204">**midiInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [<span data-ttu-id="041a7-205">**мидиаутмессаже**</span><span class="sxs-lookup"><span data-stu-id="041a7-205">**midiOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a><span data-ttu-id="041a7-206">См. также</span><span class="sxs-lookup"><span data-stu-id="041a7-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="041a7-207">Цифровой интерфейс музыкальных инструментов (MIDI)</span><span class="sxs-lookup"><span data-stu-id="041a7-207">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 