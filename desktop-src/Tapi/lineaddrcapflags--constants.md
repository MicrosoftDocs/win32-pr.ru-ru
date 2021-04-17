---
description: '\_Константы битового флага линеаддркапфлагс используются в элементе дваддркапфлагс структуры данных линеаддресскапс для описания различных возможностей логического адреса.'
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Константы LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685340"
---
# <a name="lineaddrcapflags_-constants"></a><span data-ttu-id="a35c1-103">\_Константы линеаддркапфлагс</span><span class="sxs-lookup"><span data-stu-id="a35c1-103">LINEADDRCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="a35c1-104"> \_ Константы битового флага линеаддркапфлагс используются в элементе **дваддркапфлагс** структуры данных [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) для описания различных возможностей логического адреса.</span><span class="sxs-lookup"><span data-stu-id="a35c1-104">The **LINEADDRCAPFLAGS**\_ bit-flag constants are used in the **dwAddrCapFlags** member of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure to describe various Boolean address capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="a35c1-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**ЛИНЕАДДРКАПФЛАГС \_ акцепттоалерт**</span><span class="sxs-lookup"><span data-stu-id="a35c1-105"><span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS\_ACCEPTTOALERT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-106">**Значение true** , если вызов предложения должен быть принят с помощью [**линеакцепт**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) , чтобы начать предупреждать пользователей на обоих концах вызова; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a35c1-106">**TRUE** if an offering call must be accepted using [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) to start alerting the users at both ends of the call; otherwise, **FALSE**.</span></span> <span data-ttu-id="a35c1-107">Обычно это используется только с ISDN.</span><span class="sxs-lookup"><span data-stu-id="a35c1-107">This is typically only used with ISDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**ЛИНЕАДДРКАПФЛАГС \_ акдграуп**</span><span class="sxs-lookup"><span data-stu-id="a35c1-108"><span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS\_ACDGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-109">Адрес поддерживает [ACD Groups](about-call-center-controls.md#acd-group-object) в связи с операциями центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="a35c1-109">The address supports [ACD Groups](about-call-center-controls.md#acd-group-object) in connection with call center operations.</span></span> <span data-ttu-id="a35c1-110">Дополнительные сведения о ACDных группах см. в разделе [об элементах управления центра обработки вызовов](./about-call-center-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="a35c1-110">See [About Call Center Controls](./about-call-center-controls.md) for additional information on ACD groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**ЛИНЕАДДРКАПФЛАГС \_ аутореконнект**</span><span class="sxs-lookup"><span data-stu-id="a35c1-111"><span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS\_AUTORECONNECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-112">Указывает, будет ли автоматически повторно подключаться к вызову на удержании консультации.</span><span class="sxs-lookup"><span data-stu-id="a35c1-112">Specifies whether dropping a consultation call automatically reconnects to the call on consultation hold.</span></span> <span data-ttu-id="a35c1-113">**Значение true** , если повторное соединение происходит автоматически; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a35c1-113">**TRUE** if reconnect happens automatically; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**ЛИНЕАДДРКАПФЛАГС \_ блоккиддефаулт**</span><span class="sxs-lookup"><span data-stu-id="a35c1-114"><span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS\_BLOCKIDDEFAULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-115">Указывает, отправляет ли сеть по умолчанию или блокирует сведения об ИДЕНТИФИКАТОРе вызывающего объекта при выполнении вызова по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="a35c1-115">Specifies whether the network by default sends or blocks caller ID information when making a call on this address.</span></span> <span data-ttu-id="a35c1-116">Если **значение — true**, сведения об идентификаторе блокируются по умолчанию; Если **значение равно false**, сведения об идентификаторе передаются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a35c1-116">If **TRUE**, identifier information is blocked by default; if **FALSE**, identifier information is transmitted by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**ЛИНЕАДДРКАПФЛАГС \_ блоккидоверриде**</span><span class="sxs-lookup"><span data-stu-id="a35c1-117"><span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS\_BLOCKIDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-118">Указывает, можно ли переопределить параметр по умолчанию для отправки или блокировки сведений об ИДЕНТИФИКАТОРе вызывающего объекта по вызову.</span><span class="sxs-lookup"><span data-stu-id="a35c1-118">Specifies whether the default setting for sending or blocking of caller ID information can be overridden per call.</span></span> <span data-ttu-id="a35c1-119">При **значении true** переопределение возможно; Если **значение равно false**, переопределение невозможно.</span><span class="sxs-lookup"><span data-stu-id="a35c1-119">If **TRUE**, override is possible; if **FALSE**, override is not possible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**ЛИНЕАДДРКАПФЛАГС \_ комплетионид**</span><span class="sxs-lookup"><span data-stu-id="a35c1-120"><span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**LINEADDRCAPFLAGS\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-121">Указывает, являются ли идентификаторы завершения, возвращаемые [**линекомплетекалл**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) , полезными и уникальными.</span><span class="sxs-lookup"><span data-stu-id="a35c1-121">Specifies whether the completion identifiers returned by [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) are useful and unique.</span></span> <span data-ttu-id="a35c1-122">**Значение true** , если полезно; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a35c1-122">**TRUE** if useful; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**ЛИНЕАДДРКАПФЛАГС \_ конфдроп**</span><span class="sxs-lookup"><span data-stu-id="a35c1-123"><span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS\_CONFDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-124">**Значение true** , если [**линедроп**](/windows/desktop/api/Tapi/nf-tapi-linedrop) на родительском вызове Конференции также имеет побочный результат удаления (то есть отсоединения) с другими сторонами, участвующими в вызове конференции; **Значение false** , если вызов конференции по-прежнему позволяет другим сторонам общаться друг с другом.</span><span class="sxs-lookup"><span data-stu-id="a35c1-124">**TRUE** if [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on a conference call parent also has the side effect of dropping (that is, disconnecting) the other parties involved in the conference call; **FALSE** if dropping a conference call still allows the other parties to talk among themselves.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**ЛИНЕАДДРКАПФЛАГС \_ конференцехелд**</span><span class="sxs-lookup"><span data-stu-id="a35c1-125"><span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS\_CONFERENCEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-126">Указывает, можно ли выполнить принудительное обращение к нежестко удерживаемому вызову.</span><span class="sxs-lookup"><span data-stu-id="a35c1-126">Specifies whether a hard-held call can be conferenced to.</span></span> <span data-ttu-id="a35c1-127">Часто в качестве вызова конференции можно добавить только вызовы с удержанием на консультации.</span><span class="sxs-lookup"><span data-stu-id="a35c1-127">Often, only calls on consultation hold can be added to as a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**ЛИНЕАДДРКАПФЛАГС \_ конференцемаке**</span><span class="sxs-lookup"><span data-stu-id="a35c1-128"><span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS\_CONFERENCEMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-129">Указывает, можно ли установить полностью новый вызов для использования в качестве вызова консультации (для добавления) на Конференции.</span><span class="sxs-lookup"><span data-stu-id="a35c1-129">Specifies whether an entirely new call can be established for use as a consultation call (to add) on conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**ЛИНЕАДДРКАПФЛАГС \_ дестоффхук**</span><span class="sxs-lookup"><span data-stu-id="a35c1-130"><span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS\_DESTOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-131">Указывает, может ли телефон вызываемой стороны автоматически принудительно оффхук при совершении вызовов.</span><span class="sxs-lookup"><span data-stu-id="a35c1-131">Specifies whether the called party's phone can automatically be forced offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**ЛИНЕАДДРКАПФЛАГС \_ набор**</span><span class="sxs-lookup"><span data-stu-id="a35c1-132"><span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS\_DIALED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-133">Указывает, можно ли набрать адрес назначения по этому адресу для выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="a35c1-133">Specifies whether a destination address can be dialed on this address for making a call.</span></span> <span data-ttu-id="a35c1-134">**Значение true** , если адрес назначения должен быть набран; **Значение false** , если адрес назначения фиксирован (как и "горячий телефон").</span><span class="sxs-lookup"><span data-stu-id="a35c1-134">**TRUE** if a destination address must be dialed; **FALSE** if the destination address is fixed (as with a "hot phone").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдбусинааддр**</span><span class="sxs-lookup"><span data-stu-id="a35c1-135"><span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS\_FWDBUSYNAADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-136">Указывает, могут ли пересылать вызовы для занятости и без ответов использовать разные адреса перенаправления.</span><span class="sxs-lookup"><span data-stu-id="a35c1-136">Specifies whether call forwarding for busy and for no answer can use different forwarding addresses.</span></span> <span data-ttu-id="a35c1-137">Этот флаг имеет смысл только в том случае, если перенаправление в состояние «занято» и «без ответа» можно контролировать отдельно.</span><span class="sxs-lookup"><span data-stu-id="a35c1-137">This flag is meaningful only if forwarding for busy and for no answer can be controlled separately.</span></span> <span data-ttu-id="a35c1-138">Этот флаг имеет **значение true** , если пересылка в занятом состоянии и без ответа может использовать другие адреса назначения. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="a35c1-138">This flag is **TRUE** if forwarding for busy and for no answer can use different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдконсулт**</span><span class="sxs-lookup"><span data-stu-id="a35c1-139"><span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS\_FWDCONSULT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-140">Указывает, включает ли переадресация вызовов установку вызова консультации.</span><span class="sxs-lookup"><span data-stu-id="a35c1-140">Specifies whether call forwarding involves the establishment of a consultation call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдинтекстаддр**</span><span class="sxs-lookup"><span data-stu-id="a35c1-141"><span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS\_FWDINTEXTADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-142">Указывает, могут ли внутренние и внешние вызовы перенаправляться на разные адреса пересылки.</span><span class="sxs-lookup"><span data-stu-id="a35c1-142">Specifies whether internal and external calls can be forwarded to different forwarding addresses.</span></span> <span data-ttu-id="a35c1-143">Этот флаг имеет смысл только в том случае, если переадресация внутренних и внешних вызовов может осуществляться отдельно.</span><span class="sxs-lookup"><span data-stu-id="a35c1-143">This flag is meaningful only if forwarding of internal and external calls can be controlled separately.</span></span> <span data-ttu-id="a35c1-144">Этот флаг имеет **значение true** , если внутренние и внешние вызовы могут перенаправляться на разные адреса назначения. в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="a35c1-144">This flag is **TRUE** if internal and external calls can be forwarded to different destination addresses; otherwise, it is **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвднумрингс**</span><span class="sxs-lookup"><span data-stu-id="a35c1-145"><span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS\_FWDNUMRINGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-146">Указывает, можно ли указать число колец для ответного вызова без ответа при пересылке вызовов без ответа.</span><span class="sxs-lookup"><span data-stu-id="a35c1-146">Specifies whether the number of rings for a no-answer can be specified when forwarding calls on no answer.</span></span> <span data-ttu-id="a35c1-147">Если **значение — true**, допустимый диапазон указывается в элементах **двминфвднумрингс** и **двмаксфвднумрингс** структуры [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .</span><span class="sxs-lookup"><span data-stu-id="a35c1-147">If **TRUE**, the valid range is provided in the **dwMinFwdNumRings** and **dwMaxFwdNumRings** members of the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**ЛИНЕАДДРКАПФЛАГС \_ фвдстатусвалид**</span><span class="sxs-lookup"><span data-stu-id="a35c1-148"><span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS\_FWDSTATUSVALID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-149">Указывает, является ли состояние перенаправления в структуре [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) для этого адреса допустимым или не является наиболее подходящей оценкой, указанным отсутствием точного подтверждения коммутатором или сетью.</span><span class="sxs-lookup"><span data-stu-id="a35c1-149">Specifies whether the forwarding status in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure for this address is valid or is at most a "best estimate," given absence of accurate confirmation by the switch or network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**ЛИНЕАДДРКАПФЛАГС \_ холдмакеснев**</span><span class="sxs-lookup"><span data-stu-id="a35c1-150"><span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS\_HOLDMAKESNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-151">Когда вызов по этому адресу помещается в удержание (с помощью [**линехолд**](/windows/desktop/api/Tapi/nf-tapi-linehold) или внешнего действия), автоматически создается новый вызов (скорее всего, в линекаллстате \_ диалтоне).</span><span class="sxs-lookup"><span data-stu-id="a35c1-151">When a call on this address is placed on hold (using [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) or external action), a new call is automatically created (most likely in LINECALLSTATE\_DIALTONE).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**ЛИНЕАДДРКАПФЛАГС \_ ноекстерналкаллс**</span><span class="sxs-lookup"><span data-stu-id="a35c1-152"><span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS\_NOEXTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-153">Адрес связан с внутренней линией УАТС, которая ограничена таким образом, что она не может использоваться для размещения вызовов к адресу за пределами коммутатора (например, это внутренней).</span><span class="sxs-lookup"><span data-stu-id="a35c1-153">The address is associated with an internal line on a PBX that is restricted in such a way that it cannot be used to place calls to an address outside the switch (for example, it is an intercom).</span></span> <span data-ttu-id="a35c1-154">Приложение может использовать эту индикацию, чтобы помочь пользователю выбрать правильный внешний вид вызова, который будет использоваться для выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="a35c1-154">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="a35c1-155">Если этот бит отключен, он не обязательно указывает, что адрес можно использовать для выполнения внешних вызовов, так как поставщик услуг может не компания cognizant тип строки.</span><span class="sxs-lookup"><span data-stu-id="a35c1-155">When this bit is off, it does not necessarily indicate that the address can be used to make external calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**ЛИНЕАДДРКАПФЛАГС \_ ноинтерналкаллс**</span><span class="sxs-lookup"><span data-stu-id="a35c1-156"><span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS\_NOINTERNALCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-157">Адрес связан с прямой СОВМЕСТНОй линией (магистральным каналом) и не может использоваться для выполнения внутренних вызовов УАТС.</span><span class="sxs-lookup"><span data-stu-id="a35c1-157">The address is associated with a direct CO line (trunk), and cannot be used to make internal calls on a PBX.</span></span> <span data-ttu-id="a35c1-158">Приложение может использовать эту индикацию, чтобы помочь пользователю выбрать правильный внешний вид вызова, который будет использоваться для выполнения вызова.</span><span class="sxs-lookup"><span data-stu-id="a35c1-158">The application can use this indication to assist the user in selecting the correct call appearance to use for making a call.</span></span> <span data-ttu-id="a35c1-159">Если этот бит отключен, он не обязательно указывает, что адрес можно использовать для выполнения внутренних вызовов, так как поставщик услуг может не компания cognizant тип строки.</span><span class="sxs-lookup"><span data-stu-id="a35c1-159">When this bit is off, it does not necessarily indicate that the address can be used to make internal calls, because the service provider may not be cognizant of the line type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**ЛИНЕАДДРКАПФЛАГС \_ нопстнаддресстранслатион**</span><span class="sxs-lookup"><span data-stu-id="a35c1-160"><span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS\_NOPSTNADDRESSTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-161">Этот адрес не поддерживает преобразование адресов телефонной сети с открытым коммутируемым адресом.</span><span class="sxs-lookup"><span data-stu-id="a35c1-161">This address does not support public switched telephone network address translation.</span></span> <span data-ttu-id="a35c1-162">Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="a35c1-162">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**ЛИНЕАДДРКАПФЛАГС \_ оригоффхук**</span><span class="sxs-lookup"><span data-stu-id="a35c1-163"><span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS\_ORIGOFFHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-164">Указывает, может ли телефон исходной стороны автоматически принимать оффхук при выполнении вызовов.</span><span class="sxs-lookup"><span data-stu-id="a35c1-164">Specifies whether the originating party's phone can automatically be taken offhook when making calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**ЛИНЕАДДРКАПФЛАГС \_ партиалдиал**</span><span class="sxs-lookup"><span data-stu-id="a35c1-165"><span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS\_PARTIALDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-166">Указывает, доступен ли частичный набор.</span><span class="sxs-lookup"><span data-stu-id="a35c1-166">Specifies whether partial dialing is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**ЛИНЕАДДРКАПФЛАГС \_ пиккупкаллваит**</span><span class="sxs-lookup"><span data-stu-id="a35c1-167"><span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS\_PICKUPCALLWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-168">**Значение true** , если [**линепиккуп**](/windows/desktop/api/Tapi/nf-tapi-linepickup) можно использовать для получения вызова, обнаруженного пользователем как вызов с ожиданием вызова; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a35c1-168">**TRUE** if [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can be used to pick up a call detected by the user as a call-waiting call; otherwise, **FALSE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**ЛИНЕАДДРКАПФЛАГС \_ пиккупграупид**</span><span class="sxs-lookup"><span data-stu-id="a35c1-169"><span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS\_PICKUPGROUPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-170">Указывает, требуется ли идентификатор группы для отправки вызова.</span><span class="sxs-lookup"><span data-stu-id="a35c1-170">Specifies whether a group identifier is required for call pickup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**ЛИНЕАДДРКАПФЛАГС \_ предиктиведиалер**</span><span class="sxs-lookup"><span data-stu-id="a35c1-171"><span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS\_PREDICTIVEDIALER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-172">Этот адрес содержит расширенные возможности мониторинга хода вызова, которые можно применять к исходящим вызовам для определения состояний вызова, таких как *звонка*, *Busy*, *спеЦиалинфо* и *Connected*, или типа носителя устройства, отвечающего на вызов.</span><span class="sxs-lookup"><span data-stu-id="a35c1-172">This address has enhanced call progress monitoring capabilities which can be applied to outgoing calls to determine call states such as *ringback*, *busy*, *specialinfo*, and *connected*, or the media type of the device answering the call.</span></span> <span data-ttu-id="a35c1-173">Она также может иметь возможность автоматически передавать исходящие вызовы на другой адрес, когда вызов достигает какого-либо предопределенного набора состояний.</span><span class="sxs-lookup"><span data-stu-id="a35c1-173">It may also have the ability to automatically transfer outgoing calls to another address when a call reaches any of a predefined set of states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**\_очередь линеаддркапфлагс**</span><span class="sxs-lookup"><span data-stu-id="a35c1-174"><span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-175">Этот адрес не связан с конкретной станцией или физическим устройством, но является местом хранения, где вызовы ожидают дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="a35c1-175">This address is not associated with a particular station or physical device, but is a holding place where calls wait for further processing.</span></span> <span data-ttu-id="a35c1-176">Вызовы, помещаемые в очередь, могут получить определенную обработку.</span><span class="sxs-lookup"><span data-stu-id="a35c1-176">The calls placed in the queue may receive a particular treatment.</span></span> <span data-ttu-id="a35c1-177">Они также могут автоматически передаваться при доступности определенного ресурса (например, если очередь является ACD-очередью, а вызовы ожидают доступного агента).</span><span class="sxs-lookup"><span data-stu-id="a35c1-177">They may also be automatically transferred when a particular resource becomes available (for example, if the queue is an ACD queue and calls are waiting for an available agent).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**ЛИНЕАДДРКАПФЛАГС \_ раутепоинт**</span><span class="sxs-lookup"><span data-stu-id="a35c1-178"><span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS\_ROUTEPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-179">Этот адрес не связан с конкретной станцией или физическим устройством, но является местом хранения, где вызовы ожидают маршрутизации приложением (приложение проверяет вызываемый адрес и может перенаправить вызов на другой адрес).</span><span class="sxs-lookup"><span data-stu-id="a35c1-179">This address is not associated with a particular station or physical device, but is a holding place where calls wait for routing by the application (the application examines the called address, and can redirect the call to another address).</span></span> <span data-ttu-id="a35c1-180">Вызов также может быть автоматически передан в случае истечения времени ожидания маршрутизации (обычно параметр предполагает маршрутизацию по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="a35c1-180">The call can also be automatically transferred if a routing timeout expires (the switch usually assumes a default routing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**ЛИНЕАДДРКАПФЛАГС \_ безопасность**</span><span class="sxs-lookup"><span data-stu-id="a35c1-181"><span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS\_SECURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-182">Указывает, можно ли обеспечить безопасность вызовов в этом адресе во время настройки вызова.</span><span class="sxs-lookup"><span data-stu-id="a35c1-182">Specifies whether calls on this address can be made secure at call-setup time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**ЛИНЕАДДРКАПФЛАГС \_ сеткаллингид**</span><span class="sxs-lookup"><span data-stu-id="a35c1-183"><span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS\_SETCALLINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-184">Приложение может выбрать установку элемента **каллингпартид** в [**линекаллпарамс**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) при вызове [**линемакекалл**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) и других функций, которые принимают структуру **линекаллпарамс** .</span><span class="sxs-lookup"><span data-stu-id="a35c1-184">The application can choose to set the **CallingPartyID** member in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) when calling [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) and other functions that accept a **LINECALLPARAMS** structure.</span></span> <span data-ttu-id="a35c1-185">Поставщик услуг, если содержимое идентификатора приемлемо и доступен путь, передайте идентификатор вызываемой стороне, чтобы указать удостоверение вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="a35c1-185">The service provider will, if the content of the identifier is acceptable and a path is available, pass the identifier along to the called party to indicate the identity of the calling party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**ЛИНЕАДДРКАПФЛАГС \_ сетупконфнулл**</span><span class="sxs-lookup"><span data-stu-id="a35c1-186"><span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS\_SETUPCONFNULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-187">Указывает, начинается ли настройка вызова конференции с начальным вызовом (**false**) или без начального вызова (**true**).</span><span class="sxs-lookup"><span data-stu-id="a35c1-187">Specifies whether setting up a conference call starts out with an initial call (**FALSE**) or with no initial call (**TRUE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**ЛИНЕАДДРКАПФЛАГС \_ трансферхелд**</span><span class="sxs-lookup"><span data-stu-id="a35c1-188"><span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS\_TRANSFERHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-189">Указывает, можно ли передать жестко Удерживаемый вызов.</span><span class="sxs-lookup"><span data-stu-id="a35c1-189">Specifies whether a hard-held call can be transferred.</span></span> <span data-ttu-id="a35c1-190">Часто могут быть переданы только вызовы с удержанием на консультации.</span><span class="sxs-lookup"><span data-stu-id="a35c1-190">Often, only calls on consultation hold can be transferred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a35c1-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**ЛИНЕАДДРКАПФЛАГС \_ трансфермаке**</span><span class="sxs-lookup"><span data-stu-id="a35c1-191"><span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS\_TRANSFERMAKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a35c1-192">Указывает, можно ли установить полностью новый вызов для использования в качестве вызова консультации при перемещении.</span><span class="sxs-lookup"><span data-stu-id="a35c1-192">Specifies whether an entirely new call can be established for use as a consultation call on transfer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a35c1-193">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a35c1-193">Remarks</span></span>

<span data-ttu-id="a35c1-194">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="a35c1-194">No extensibility.</span></span> <span data-ttu-id="a35c1-195">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="a35c1-195">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="a35c1-196">Требования</span><span class="sxs-lookup"><span data-stu-id="a35c1-196">Requirements</span></span>



| <span data-ttu-id="a35c1-197">Требование</span><span class="sxs-lookup"><span data-stu-id="a35c1-197">Requirement</span></span> | <span data-ttu-id="a35c1-198">Значение</span><span class="sxs-lookup"><span data-stu-id="a35c1-198">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a35c1-199">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a35c1-199">TAPI version</span></span><br/> | <span data-ttu-id="a35c1-200">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a35c1-200">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a35c1-201">Header</span><span class="sxs-lookup"><span data-stu-id="a35c1-201">Header</span></span><br/>       | <dl> <span data-ttu-id="a35c1-202"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a35c1-202"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35c1-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a35c1-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35c1-204">**линеакцепт**</span><span class="sxs-lookup"><span data-stu-id="a35c1-204">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[<span data-ttu-id="a35c1-205">**линеаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="a35c1-205">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="a35c1-206">**линеаддрессстатус**</span><span class="sxs-lookup"><span data-stu-id="a35c1-206">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="a35c1-207">**линекаллпарамс**</span><span class="sxs-lookup"><span data-stu-id="a35c1-207">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="a35c1-208">**линекомплетекалл**</span><span class="sxs-lookup"><span data-stu-id="a35c1-208">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="a35c1-209">**линедроп**</span><span class="sxs-lookup"><span data-stu-id="a35c1-209">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="a35c1-210">**линехолд**</span><span class="sxs-lookup"><span data-stu-id="a35c1-210">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[<span data-ttu-id="a35c1-211">**линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="a35c1-211">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="a35c1-212">**линепиккуп**</span><span class="sxs-lookup"><span data-stu-id="a35c1-212">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

