---
description: '\_Константы линемедиамоде описывают типы носителей (или режимы) сеанса связи или вызова.'
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Константы LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679586"
---
# <a name="linemediamode_-constants"></a><span data-ttu-id="f62ce-103">\_Константы линемедиамоде</span><span class="sxs-lookup"><span data-stu-id="f62ce-103">LINEMEDIAMODE\_ Constants</span></span>

<span data-ttu-id="f62ce-104">Константы **линемедиамоде \_** описывают типы носителей (или режимы) сеанса связи или вызова.</span><span class="sxs-lookup"><span data-stu-id="f62ce-104">The **LINEMEDIAMODE\_** constants describe media types (or modes)of a communications session or call.</span></span>

<dl> <dt>

<span data-ttu-id="f62ce-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**ЛИНЕМЕДИАМОДЕ \_ аутоматедвоице**</span><span class="sxs-lookup"><span data-stu-id="f62ce-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE\_AUTOMATEDVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-106">В вызове обнаружена радиоэнергия, а речь локально обрабатывается автоматическим приложением, например, с помощью отвечающего приложения.</span><span class="sxs-lookup"><span data-stu-id="f62ce-106">Voice energy was detected on the call, and the voice is locally handled by an automated application such as with an answering machine application.</span></span> <span data-ttu-id="f62ce-107">Если поставщик услуг не может различить интерактивные и автоматические голоса при входящем вызове, он сообщит о вызове в качестве интерактивного голоса.</span><span class="sxs-lookup"><span data-stu-id="f62ce-107">When a service provider cannot distinguish between interactive and automated voice on an incoming call, it will report the call as interactive voice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**\_модем линемедиамоде**</span><span class="sxs-lookup"><span data-stu-id="f62ce-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE\_DATAMODEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-109">Сеанс модема данных в вызове.</span><span class="sxs-lookup"><span data-stu-id="f62ce-109">A data modem session on the call.</span></span> <span data-ttu-id="f62ce-110">Для использования текущих модемных протоколов требуется вызванная станция для запуска подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f62ce-110">Current modem protocols require the called station to initiate the handshake.</span></span> <span data-ttu-id="f62ce-111">Для вызова входящего модема, как правило, приложение может не выполнять никаких срабатываний.</span><span class="sxs-lookup"><span data-stu-id="f62ce-111">For an incoming data modem call, the application can typically make no positive detection.</span></span> <span data-ttu-id="f62ce-112">То, как поставщик услуг делает это определение, является его выбором.</span><span class="sxs-lookup"><span data-stu-id="f62ce-112">How the service provider makes this determination is its choice.</span></span> <span data-ttu-id="f62ce-113">Например, период бездействия сразу после ответа на входящий вызов можно использовать в качестве эвристики для принятия решения о том, что это может быть вызов модема данных.</span><span class="sxs-lookup"><span data-stu-id="f62ce-113">For example, a period of silence just after answering an incoming call can be used as a heuristic to decide that this might be a data modem call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**ЛИНЕМЕДИАМОДЕ \_ ADSI**</span><span class="sxs-lookup"><span data-stu-id="f62ce-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE\_ADSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-115">Сеанс интерфейса ADSI (аналоговый интерфейс служб дисплея) при вызове.</span><span class="sxs-lookup"><span data-stu-id="f62ce-115">An ADSI (Analog Display Services Interface) session on the call.</span></span> <span data-ttu-id="f62ce-116">Интерфейсы ADSI улучшают голосовые вызовы с помощью буквенно-цифровых данных, загружаемых на телефон, и использования мягких кнопок на телефоне.</span><span class="sxs-lookup"><span data-stu-id="f62ce-116">ADSI enhances voice calls with alphanumeric information downloaded to the phone and the use of soft buttons on the phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**ЛИНЕМЕДИАМОДЕ \_ дигиталдата**</span><span class="sxs-lookup"><span data-stu-id="f62ce-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE\_DIGITALDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-118">Поток цифровых данных неопределенного формата.</span><span class="sxs-lookup"><span data-stu-id="f62ce-118">A digital data stream of unspecified format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**ЛИНЕМЕДИАМОДЕ \_ G3FAX**</span><span class="sxs-lookup"><span data-stu-id="f62ce-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE\_G3FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-120">Факс группы 3 отправляется или получается через вызов.</span><span class="sxs-lookup"><span data-stu-id="f62ce-120">A group 3 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**ЛИНЕМЕДИАМОДЕ \_ G4FAX**</span><span class="sxs-lookup"><span data-stu-id="f62ce-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE\_G4FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-122">Факс группы 4 отправляется или получается через вызов.</span><span class="sxs-lookup"><span data-stu-id="f62ce-122">A group 4 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**ЛИНЕМЕДИАМОДЕ \_ интерактивевоице**</span><span class="sxs-lookup"><span data-stu-id="f62ce-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE\_INTERACTIVEVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-124">В вызове обнаружена радиоэнергия, и вызов обрабатывается как интерактивный голосовой звонок с человеком на обоих концах.</span><span class="sxs-lookup"><span data-stu-id="f62ce-124">Voice energy was detected on the call, and the call is handled as an interactive voice call with humans on both ends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**\_смешанный линемедиамоде**</span><span class="sxs-lookup"><span data-stu-id="f62ce-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE\_MIXED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-126">Смешанный сеанс в вызове.</span><span class="sxs-lookup"><span data-stu-id="f62ce-126">A mixed session on the call.</span></span> <span data-ttu-id="f62ce-127">Mixed является одной из телематикных служб ISDN.</span><span class="sxs-lookup"><span data-stu-id="f62ce-127">Mixed is one of the ISDN telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**ЛИНЕМЕДИАМОДЕ \_ TDD**</span><span class="sxs-lookup"><span data-stu-id="f62ce-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE\_TDD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-129">Тест TDD (телефонные устройства для подключения с потерей слуха) при вызове.</span><span class="sxs-lookup"><span data-stu-id="f62ce-129">A TDD (Telephony Devices for the Deaf) session on the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**ЛИНЕМЕДИАМОДЕ \_ TELETEX**</span><span class="sxs-lookup"><span data-stu-id="f62ce-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE\_TELETEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-131">Сеанс Teletex в вызове.</span><span class="sxs-lookup"><span data-stu-id="f62ce-131">A teletex session on the call.</span></span> <span data-ttu-id="f62ce-132">Teletex — одна из телематик служб.</span><span class="sxs-lookup"><span data-stu-id="f62ce-132">Teletex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**ЛИНЕМЕДИАМОДЕный \_ номер телекса**</span><span class="sxs-lookup"><span data-stu-id="f62ce-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE\_TELEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-134">Сеанс телекса в вызове.</span><span class="sxs-lookup"><span data-stu-id="f62ce-134">A telex session on the call.</span></span> <span data-ttu-id="f62ce-135">Номер телекса является одной из телематик Services.</span><span class="sxs-lookup"><span data-stu-id="f62ce-135">Telex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**\_видео линемедиамоде**</span><span class="sxs-lookup"><span data-stu-id="f62ce-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE\_VIDEO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-137">Тип носителя вызова — Video.</span><span class="sxs-lookup"><span data-stu-id="f62ce-137">The media type of the call is video.</span></span> <span data-ttu-id="f62ce-138">(TAPI версии 2,1 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="f62ce-138">(TAPI versions 2.1 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**ЛИНЕМЕДИАМОДЕ \_ видеотекс**</span><span class="sxs-lookup"><span data-stu-id="f62ce-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE\_VIDEOTEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-140">Сеанс видеотекс в вызове.</span><span class="sxs-lookup"><span data-stu-id="f62ce-140">A videotex session on the call.</span></span> <span data-ttu-id="f62ce-141">Видеотекс — это одна из телематик служб.</span><span class="sxs-lookup"><span data-stu-id="f62ce-141">Videotex is one the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**ЛИНЕМЕДИАМОДЕ \_ воицевиев**</span><span class="sxs-lookup"><span data-stu-id="f62ce-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE\_VOICEVIEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-143">Тип носителя вызова — Воицевиев.</span><span class="sxs-lookup"><span data-stu-id="f62ce-143">The media type of the call is VoiceView.</span></span> <span data-ttu-id="f62ce-144">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="f62ce-144">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f62ce-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**ЛИНЕМЕДИАМОДЕ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="f62ce-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f62ce-146">Поток мультимедиа существует, но его режим в настоящее время неизвестен и может быть известен позже.</span><span class="sxs-lookup"><span data-stu-id="f62ce-146">A media stream exists but its mode is not currently known and may become known later.</span></span> <span data-ttu-id="f62ce-147">Это соответствует вызову с неклассифицированным типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f62ce-147">This would correspond to a call with an unclassified media type.</span></span> <span data-ttu-id="f62ce-148">В типичных средах аналоговой телефонии тип носителя входящего звонка может быть неизвестным до тех пор, пока не будет получен ответ на вызов, и поток мультимедиа отфильтрован для выполнения определения.</span><span class="sxs-lookup"><span data-stu-id="f62ce-148">In typical analog telephony environments, an incoming call's media type may be unknown until after the call has been answered and the media stream has been filtered to make a determination.</span></span>

<span data-ttu-id="f62ce-149">Если задан неизвестный флаг режима мультимедиа, также можно задать другие флаги мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f62ce-149">If the unknown media-mode flag is set, other media flags can also be set.</span></span> <span data-ttu-id="f62ce-150">Это означает, что носитель неизвестен, но, скорее всего, является одним из других выбранных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="f62ce-150">This is used to signify that the media is unknown but that it is likely to be one of the other selected media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f62ce-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f62ce-151">Remarks</span></span>

<span data-ttu-id="f62ce-152">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="f62ce-152">All 32 bits are reserved.</span></span>

<span data-ttu-id="f62ce-153">Обратите внимание, что режим носителя и тип мультимедиа являются разными понятиями.</span><span class="sxs-lookup"><span data-stu-id="f62ce-153">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="f62ce-154">Режим носителя вызова указывает на качество телефонного подключения, которое предоставляется в основном в сети.</span><span class="sxs-lookup"><span data-stu-id="f62ce-154">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="f62ce-155">Тип носителя вызова указывает на тип информационного потока, который передается через этот вызов.</span><span class="sxs-lookup"><span data-stu-id="f62ce-155">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="f62ce-156">Факсы группы 3 или модемы данных — это типы мультимедиа, использующие вызов с режимом носителя 3,1 кГц.</span><span class="sxs-lookup"><span data-stu-id="f62ce-156">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

<span data-ttu-id="f62ce-157">Для обеспечения обратной совместимости поставщик услуг должен проверить согласованную версию API в строке и не использовать это значение ЛИНЕМЕДИАМОДЕ, \_ если оно не поддерживается в согласованной версии.</span><span class="sxs-lookup"><span data-stu-id="f62ce-157">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEMEDIAMODE\_ value if not supported on the negotiated version.</span></span>

## <a name="requirements"></a><span data-ttu-id="f62ce-158">Требования</span><span class="sxs-lookup"><span data-stu-id="f62ce-158">Requirements</span></span>



| <span data-ttu-id="f62ce-159">Требование</span><span class="sxs-lookup"><span data-stu-id="f62ce-159">Requirement</span></span> | <span data-ttu-id="f62ce-160">Значение</span><span class="sxs-lookup"><span data-stu-id="f62ce-160">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f62ce-161">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f62ce-161">TAPI version</span></span><br/> | <span data-ttu-id="f62ce-162">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f62ce-162">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f62ce-163">Header</span><span class="sxs-lookup"><span data-stu-id="f62ce-163">Header</span></span><br/>       | <dl> <span data-ttu-id="f62ce-164"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f62ce-164"><dt>Tapi.h</dt></span></span> </dl> |



 

 




