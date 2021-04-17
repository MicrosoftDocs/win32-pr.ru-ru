---
description: '\_Константы побитового флага линекаллинфостате описывают различные элементы сведений о вызовах, о которых приложение может получать уведомления в строке \_ каллинфо сообщения.'
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: Константы LINECALLINFOSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674897"
---
# <a name="linecallinfostate_-constants"></a><span data-ttu-id="20f14-103">\_Константы линекаллинфостате</span><span class="sxs-lookup"><span data-stu-id="20f14-103">LINECALLINFOSTATE\_ Constants</span></span>

<span data-ttu-id="20f14-104">Константы побитового флага **линекаллинфостате \_** описывают различные элементы сведений о вызовах, о которых приложение может получать уведомления в [**строке \_ каллинфо**](line-callinfo.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="20f14-104">The **LINECALLINFOSTATE\_** bit-flag constants describe various call information items about which an application can be notified in the [**LINE\_CALLINFO**](line-callinfo.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="20f14-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="20f14-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE\_APPSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-106">Зависящее от приложения поле записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-106">The application-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ беарермоде**</span><span class="sxs-lookup"><span data-stu-id="20f14-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE\_BEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-108">Поле режима носителя в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-108">The bearer mode field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ каллдата**</span><span class="sxs-lookup"><span data-stu-id="20f14-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE\_CALLDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-110">Элемент **каллдата** в [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) был обновлен.</span><span class="sxs-lookup"><span data-stu-id="20f14-110">The **CallData** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ калледид**</span><span class="sxs-lookup"><span data-stu-id="20f14-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE\_CALLEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-112">Одно из полей, связанных с Калледид, в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-112">One of the calledID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ каллерид**</span><span class="sxs-lookup"><span data-stu-id="20f14-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE\_CALLERID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-114">Одно из полей, связанных с Каллерид, в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-114">One of the callerID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ каллид**</span><span class="sxs-lookup"><span data-stu-id="20f14-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-116">Поле "идентификатор вызова" записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-116">The call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ чаргингинфо**</span><span class="sxs-lookup"><span data-stu-id="20f14-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE\_CHARGINGINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-118">Сведения о расходах записи о вызовах.</span><span class="sxs-lookup"><span data-stu-id="20f14-118">The charging information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ комплетионид**</span><span class="sxs-lookup"><span data-stu-id="20f14-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-120">Поле идентификатора завершения записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-120">The completion identifier field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ коннектедид**</span><span class="sxs-lookup"><span data-stu-id="20f14-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE\_CONNECTEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-122">Одно из полей, связанных с Коннектедид, в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-122">One of the connectedID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ девспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="20f14-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-124">Зависящее от устройства поле записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-124">The device-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ диалпарамс**</span><span class="sxs-lookup"><span data-stu-id="20f14-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE\_DIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-126">Параметры набора для записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-126">The dial parameters of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ дисплей**</span><span class="sxs-lookup"><span data-stu-id="20f14-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**LINECALLINFOSTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-128">Отображаемое поле записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-128">The display field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ хигхлевелкомп**</span><span class="sxs-lookup"><span data-stu-id="20f14-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE\_HIGHLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-130">Поле высокого уровня совместимости в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-130">The high level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ ловлевелкомп**</span><span class="sxs-lookup"><span data-stu-id="20f14-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE\_LOWLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-132">Поле низкого уровня совместимости в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-132">The low level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ медиамоде**</span><span class="sxs-lookup"><span data-stu-id="20f14-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE\_MEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-134">Поле типа носителя для записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-134">The media type field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ монитормодес**</span><span class="sxs-lookup"><span data-stu-id="20f14-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE\_MONITORMODES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-136">Один или несколько полей с цифрами, тоновыми или мультимедийными данными в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-136">One or more of the digit, tone, or media monitoring fields in the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ нуммониторс**</span><span class="sxs-lookup"><span data-stu-id="20f14-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE\_NUMMONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-138">Изменилось поле "число мониторов" в записи сведений о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-138">The number of monitors field in the call-information record has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ нумовнердекр**</span><span class="sxs-lookup"><span data-stu-id="20f14-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE\_NUMOWNERDECR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-140">Число полей Owner в записи о вызове было уменьшено.</span><span class="sxs-lookup"><span data-stu-id="20f14-140">The number of owner field in the call-information record was decreased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ нумовнеринкр**</span><span class="sxs-lookup"><span data-stu-id="20f14-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE\_NUMOWNERINCR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-142">Число полей Owner в записи о вызове было увеличено.</span><span class="sxs-lookup"><span data-stu-id="20f14-142">The number of owner field in the call-information record was increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**\_источник линекаллинфостате**</span><span class="sxs-lookup"><span data-stu-id="20f14-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE\_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-144">Поле источника записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-144">The origin field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_**</span><span class="sxs-lookup"><span data-stu-id="20f14-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-146">Были изменены элементы сведений о вызовах, кроме перечисленных ниже.</span><span class="sxs-lookup"><span data-stu-id="20f14-146">Call information items other than those listed below have changed.</span></span> <span data-ttu-id="20f14-147">Приложение должно проверить сведения о текущем вызове, чтобы определить, какие элементы были изменены.</span><span class="sxs-lookup"><span data-stu-id="20f14-147">The application should check the current call information to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ QoS**</span><span class="sxs-lookup"><span data-stu-id="20f14-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE\_QOS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-149">Один или несколько элементов **QoS** в [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) были обновлены.</span><span class="sxs-lookup"><span data-stu-id="20f14-149">One or more of the **QOS** members in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**\_ставка линекаллинфостате**</span><span class="sxs-lookup"><span data-stu-id="20f14-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**LINECALLINFOSTATE\_RATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-151">Поле Rate записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-151">The rate field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**\_Причина линекаллинфостате**</span><span class="sxs-lookup"><span data-stu-id="20f14-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**LINECALLINFOSTATE\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-153">Поле Reason (причина) записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-153">The reason field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ редиректингид**</span><span class="sxs-lookup"><span data-stu-id="20f14-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE\_REDIRECTINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-155">Идентификатор адреса расположения, которое перенаправляет вызов.</span><span class="sxs-lookup"><span data-stu-id="20f14-155">The address identifier of the location that redirected a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ редиректионид**</span><span class="sxs-lookup"><span data-stu-id="20f14-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE\_REDIRECTIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-157">Идентификатор адреса расположения, в которое был перенаправлен вызов.</span><span class="sxs-lookup"><span data-stu-id="20f14-157">The address identifier of the location to which a call has been redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ релатедкаллид**</span><span class="sxs-lookup"><span data-stu-id="20f14-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE\_RELATEDCALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-159">Поле связанного идентификатора вызова записи сведений о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-159">The related call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**\_терминал линекаллинфостате**</span><span class="sxs-lookup"><span data-stu-id="20f14-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**LINECALLINFOSTATE\_TERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-161">Сведения о режиме терминала в записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-161">The terminal mode information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**\_Обработка линекаллинфостате**</span><span class="sxs-lookup"><span data-stu-id="20f14-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**LINECALLINFOSTATE\_TREATMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-163">Элемент **каллтреатмент** в [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) был обновлен.</span><span class="sxs-lookup"><span data-stu-id="20f14-163">The **CallTreatment** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span> <span data-ttu-id="20f14-164">Это может произойти в ответ на функцию [**линесеткаллтреатмент**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) , изменение состояния вызова, вызов "Vector" или другого скрипта, управляющего вызовом, или после завершения воспроизведения записанного сообщения (обычно это означает изменение в "тишине" или "Музыка").</span><span class="sxs-lookup"><span data-stu-id="20f14-164">This can occur in response to a [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) function, a call state change, a call "vector" or other script controlling the call, or upon completion of playback of a recorded message (ordinarily, indicating a change to "silence" or "music").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**\_магистраль линекаллинфостате**</span><span class="sxs-lookup"><span data-stu-id="20f14-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-166">Поле магистрали записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-166">The trunk field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="20f14-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**ЛИНЕКАЛЛИНФОСТАТЕ \_ усерусеринфо**</span><span class="sxs-lookup"><span data-stu-id="20f14-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE\_USERUSERINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="20f14-168">Сведения о пользователе для записи о вызове.</span><span class="sxs-lookup"><span data-stu-id="20f14-168">The user-user information of the call-information record.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20f14-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20f14-169">Remarks</span></span>

<span data-ttu-id="20f14-170">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="20f14-170">No extensibility.</span></span> <span data-ttu-id="20f14-171">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="20f14-171">All 32 bits are reserved.</span></span>

<span data-ttu-id="20f14-172">Когда в этой структуре данных происходят изменения, в приложение отправляется сообщение [**Line \_ каллинфо**](line-callinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="20f14-172">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="20f14-173">Параметры этого сообщения являются маркером вызова и указанием измененного информационного элемента.</span><span class="sxs-lookup"><span data-stu-id="20f14-173">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="20f14-174">Структура данных [**линеаддресскапс**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) также указывает, какие из этих элементов сведений о вызовах являются допустимыми для каждого вызова в адресе.</span><span class="sxs-lookup"><span data-stu-id="20f14-174">The [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure also indicates which of these call information elements are valid for every call on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f14-175">Требования</span><span class="sxs-lookup"><span data-stu-id="20f14-175">Requirements</span></span>



| <span data-ttu-id="20f14-176">Требование</span><span class="sxs-lookup"><span data-stu-id="20f14-176">Requirement</span></span> | <span data-ttu-id="20f14-177">Значение</span><span class="sxs-lookup"><span data-stu-id="20f14-177">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="20f14-178">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="20f14-178">TAPI version</span></span><br/> | <span data-ttu-id="20f14-179">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="20f14-179">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="20f14-180">Header</span><span class="sxs-lookup"><span data-stu-id="20f14-180">Header</span></span><br/>       | <dl> <span data-ttu-id="20f14-181"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f14-181"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f14-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20f14-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f14-183">**Строка \_ каллинфо**</span><span class="sxs-lookup"><span data-stu-id="20f14-183">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="20f14-184">**линеаддресскапс**</span><span class="sxs-lookup"><span data-stu-id="20f14-184">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="20f14-185">**линекаллинфо**</span><span class="sxs-lookup"><span data-stu-id="20f14-185">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="20f14-186">**линесеткаллтреатмент**</span><span class="sxs-lookup"><span data-stu-id="20f14-186">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




