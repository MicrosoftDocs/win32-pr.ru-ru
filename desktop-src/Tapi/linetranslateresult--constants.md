---
description: '\_Константы побитового флага линетранслатересулт описывают различные результаты преобразования адресов.'
ms.assetid: 7b834c57-d862-4fe6-828c-9e8fa20f3ec7
title: Константы LINETRANSLATERESULT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad10c3da2b4250ded5706e4aaa10b9b61f8739b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680030"
---
# <a name="linetranslateresult_-constants"></a><span data-ttu-id="e7b22-103">\_Константы линетранслатересулт</span><span class="sxs-lookup"><span data-stu-id="e7b22-103">LINETRANSLATERESULT\_ Constants</span></span>

<span data-ttu-id="e7b22-104">Константы побитового флага **линетранслатересулт \_** описывают различные результаты преобразования адресов.</span><span class="sxs-lookup"><span data-stu-id="e7b22-104">The **LINETRANSLATERESULT\_** bit-flag constants describe various results of an address translation.</span></span>

<dl> <dt>

<span data-ttu-id="e7b22-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ каноническая**</span><span class="sxs-lookup"><span data-stu-id="e7b22-105"><span id="LINETRANSLATERESULT_CANONICAL"></span><span id="linetranslateresult_canonical"></span>**LINETRANSLATERESULT\_CANONICAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-106">Указывает, что входная строка находилась в допустимом каноническом формате.</span><span class="sxs-lookup"><span data-stu-id="e7b22-106">Indicates that the input string was in valid canonical format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ диалбиллинг**</span><span class="sxs-lookup"><span data-stu-id="e7b22-107"><span id="LINETRANSLATERESULT_DIALBILLING"></span><span id="linetranslateresult_dialbilling"></span>**LINETRANSLATERESULT\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-108">Указывает, что возвращаемый адрес содержит "$".</span><span class="sxs-lookup"><span data-stu-id="e7b22-108">Indicates that the returned address contains a "$".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ диалдиалтоне**</span><span class="sxs-lookup"><span data-stu-id="e7b22-109"><span id="LINETRANSLATERESULT_DIALDIALTONE"></span><span id="linetranslateresult_dialdialtone"></span>**LINETRANSLATERESULT\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-110">Указывает, что возвращаемый адрес содержит "W".</span><span class="sxs-lookup"><span data-stu-id="e7b22-110">Indicates that the returned address contains a "W".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ диалпромпт**</span><span class="sxs-lookup"><span data-stu-id="e7b22-111"><span id="LINETRANSLATERESULT_DIALPROMPT"></span><span id="linetranslateresult_dialprompt"></span>**LINETRANSLATERESULT\_DIALPROMPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-112">Указывает, что возвращаемый адрес содержит знак "?".</span><span class="sxs-lookup"><span data-stu-id="e7b22-112">Indicates that the returned address contains a "?".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ диалкуиет**</span><span class="sxs-lookup"><span data-stu-id="e7b22-113"><span id="LINETRANSLATERESULT_DIALQUIET"></span><span id="linetranslateresult_dialquiet"></span>**LINETRANSLATERESULT\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-114">Указывает, что возвращаемый адрес содержит символ "@".</span><span class="sxs-lookup"><span data-stu-id="e7b22-114">Indicates that the returned address contain a "@".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ Международная**</span><span class="sxs-lookup"><span data-stu-id="e7b22-115"><span id="LINETRANSLATERESULT_INTERNATIONAL"></span><span id="linetranslateresult_international"></span>**LINETRANSLATERESULT\_INTERNATIONAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-116">Указывает, что вызов обрабатывается как Международный вызов (код страны или региона, указанный в адресе назначения, отличается от кода страны или региона, указанного для **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="e7b22-116">Indicates that the call is being treated as an international call (country or region code specified in the destination address is different from the country or region code specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ интолллист**</span><span class="sxs-lookup"><span data-stu-id="e7b22-117"><span id="LINETRANSLATERESULT_INTOLLLIST"></span><span id="linetranslateresult_intolllist"></span>**LINETRANSLATERESULT\_INTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-118">Указывает, что локальный вызов набирается как длинное расстояние, так как страна или регион имеют платный звонок, а префикс отображается в **Толлпрефикслист** **CurrentLocation**.</span><span class="sxs-lookup"><span data-stu-id="e7b22-118">Indicates that the local call is being dialed as long distance because the country or region has toll calling and the prefix appears in the **TollPrefixList** of the **CurrentLocation**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ локальный**</span><span class="sxs-lookup"><span data-stu-id="e7b22-119"><span id="LINETRANSLATERESULT_LOCAL"></span><span id="linetranslateresult_local"></span>**LINETRANSLATERESULT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-120">Указывает, что вызов обрабатывается как локальный вызов (код страны или региона, а код города, указанный в адресе назначения, совпадает с указанными для **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="e7b22-120">Indicates that the call is being treated as a local call (country or region code and area code specified in the destination address are the same as those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ лонгдистанце**</span><span class="sxs-lookup"><span data-stu-id="e7b22-121"><span id="LINETRANSLATERESULT_LONGDISTANCE"></span><span id="linetranslateresult_longdistance"></span>**LINETRANSLATERESULT\_LONGDISTANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-122">Указывает, что вызов обрабатывается как Междугородний вызов (код страны или региона, указанный в адресе назначения, совпадает с кодом города, который отличается от указанного для **CurrentLocation**).</span><span class="sxs-lookup"><span data-stu-id="e7b22-122">Indicates that the call is being treated as a long distance call (country or region code specified in the destination address is the same but area code is different from those specified for the **CurrentLocation**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ нотинтолллист**</span><span class="sxs-lookup"><span data-stu-id="e7b22-123"><span id="LINETRANSLATERESULT_NOTINTOLLLIST"></span><span id="linetranslateresult_notintolllist"></span>**LINETRANSLATERESULT\_NOTINTOLLLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-124">Указывает, что страна или регион поддерживает платный звонок, но префикс не отображается в **толлпрефикслист**, поэтому вызов набирается как локальный вызов.</span><span class="sxs-lookup"><span data-stu-id="e7b22-124">Indicates that the country or region supports toll calling but the prefix does not appear in the **TollPrefixList**, so the call is dialed as a local call.</span></span> <span data-ttu-id="e7b22-125">Обратите внимание, что при отключении обоих плат и НОТИНТОЛЛИСТ текущая страна или регион не поддерживает платные префиксы, а элементы пользовательского интерфейса, связанные с платными префиксами, не должны быть представлены пользователю. Если один из этих бит включен, страна или регион поддерживают платные списки, а соответствующие элементы пользовательского интерфейса должны быть включены.</span><span class="sxs-lookup"><span data-stu-id="e7b22-125">Note that if both INTOLLIST and NOTINTOLLIST are off, the current country or region does not support toll prefixes, and user-interface elements related to toll prefixes should not be presented to the user; if either such bit is on, the country or region does support toll lists, and the related user-interface elements should be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТный \_ перевод**</span><span class="sxs-lookup"><span data-stu-id="e7b22-126"><span id="LINETRANSLATERESULT_NOTRANSLATION"></span><span id="linetranslateresult_notranslation"></span>**LINETRANSLATERESULT\_NOTRANSLATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-127">Указывает, что преобразование адресов недоступно.</span><span class="sxs-lookup"><span data-stu-id="e7b22-127">Indicates that address translation is not available.</span></span> <span data-ttu-id="e7b22-128">Этот элемент предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="e7b22-128">This element is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b22-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**ЛИНЕТРАНСЛАТЕРЕСУЛТ \_ воицедетект**</span><span class="sxs-lookup"><span data-stu-id="e7b22-129"><span id="LINETRANSLATERESULT_VOICEDETECT"></span><span id="linetranslateresult_voicedetect"></span>**LINETRANSLATERESULT\_VOICEDETECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e7b22-130">Указывает, что возвращаемый адрес с набором номера содержит ":".</span><span class="sxs-lookup"><span data-stu-id="e7b22-130">Indicates that the returned dialable address contains a ":".</span></span> <span data-ttu-id="e7b22-131">Этот элемент предоставляется только приложениям, которые согласовывают версию TAPI 2,0 или более позднюю.</span><span class="sxs-lookup"><span data-stu-id="e7b22-131">This element is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>

> [!Note]  
> <span data-ttu-id="e7b22-132">Символ ":" (двоеточие) будет добавлен в список символов, которые могут быть внедрены в строку с набором номера и переданы в адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="e7b22-132">The ":" (colon) character will be added to the list of characters that can be embedded in a dialable string and passed into destination addresses.</span></span> <span data-ttu-id="e7b22-133">Попытка передать его из приложения на линейное устройство, которое поддерживает более раннюю версию API, чем 2,0, скорее всего \_ , приведет к линирр инваладдресс или, возможно, в том, что он полностью пропускается.</span><span class="sxs-lookup"><span data-stu-id="e7b22-133">Attempting to pass it from an application to a line device that supports an API version earlier than 2.0 will most likely result in LINEERR\_INVALADDRESS, or possibly in the character being ignored entirely.</span></span> <span data-ttu-id="e7b22-134">Значение этого символа — «Pause, пока не будет обнаружено голосовое приглашение, затем продолжить набор»; Он предназначен для использования при автоматическом подключении к системам, которые предоставляют голосовые запросы, такие как междугородные звонки.</span><span class="sxs-lookup"><span data-stu-id="e7b22-134">The meaning of this character is "Pause until a voice prompt is detected, then continue dialing"; it is intended for use when automatically dialing into systems that give voice prompts, such as long distance calling card processors.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7b22-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7b22-135">Remarks</span></span>

<span data-ttu-id="e7b22-136">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="e7b22-136">No extensibility.</span></span> <span data-ttu-id="e7b22-137">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="e7b22-137">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b22-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e7b22-138">Requirements</span></span>



| <span data-ttu-id="e7b22-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e7b22-139">Requirement</span></span> | <span data-ttu-id="e7b22-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e7b22-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e7b22-141">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e7b22-141">TAPI version</span></span><br/> | <span data-ttu-id="e7b22-142">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e7b22-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e7b22-143">Header</span><span class="sxs-lookup"><span data-stu-id="e7b22-143">Header</span></span><br/>       | <dl> <span data-ttu-id="e7b22-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b22-144"><dt>Tapi.h</dt></span></span> </dl> |



 

 




